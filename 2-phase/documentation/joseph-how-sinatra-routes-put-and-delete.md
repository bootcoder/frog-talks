# How does Sinatra handle DELETE and PUT routes?

### Joseph Huang

### Routes overview

| HTTP VERB | Route         | Action  |  Used for |
| ----------|:-------------:| :-----: | :--------:|
| GET       | '/posts' | index | display all posts |
| GET       | '/posts/new' | new | form for creating a new post |
| POST      | '/posts | create | create a new post |
| GET       | '/posts/:id'     |   show | display a specific post |
| GET       | '/posts/:id/edit'|   edit | edit a specific post | 
| PUT       | '/posts/:id' | update | update a specific post |
| DELETE    | '/posts/:id' | delete | delete a specific post |


To use the PUT and DELETE methods in Sinatra you have to "trick" the form to go to the right place.

To get to the edit form to submit via POST request your form must include a hidden input field.


### Put form and route
```
<form action="/posts/:id" method="post">
  <input id="hidden" type="hidden" name="_method" value="PUT">
  <input type="text" name="title">
  <input type="text" name="content">
  <input type="submit" value="submit">
</form>

put '/posts/:id' do
  #get params from url
  @post = Post.find(params[:id]) #define variable to edit
  @post.assign_attributes(params[:post]) #assign new attributes
  if @post.save #saves new post or returns false if unsuccessful
    redirect '/posts' #redirect back to posts index page
  else
    erb :'posts/edit' #show edit post view again(potentially displaying errors)
  end
end
```

The first controller action above loads the edit form in the browser by making a GET request to posts/:id/edit.
The second controller action handles the edit form submission. This action responds to a PUT request to the route /posts/:id. First, we pull the post by the ID in the parameters, then we update the title and content attributes and save. The action ends with a redirect to the post show page.

### Delete form and route
```
<form action="/posts/:id" method="post">
  <input id="hidden" type="hidden" name="_method" value="delete">
  <input type="text" name="title">
  <input type="text" name="content">
  <input type="submit" value="submit">
</form>

delete '/posts/:id' do
  #get params from url
  @post = Post.find(params[:id]) #define post to delete
  @post.destroy #delete post
  redirect '/posts' #redirect back to posts index page	
end
```

On the post show page, we have a form to delete it. The form is submitted via a DELETE request to the route /posts/:id. This action finds the post in the database based on the ID in the parameters, and deletes it. It then redirects to the index page /posts.
