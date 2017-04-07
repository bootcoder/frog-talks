# Local and Session storage

### Dillon Arevalo

## Overview

Local storage and session storage are HTML features available on the following browsers:
![storage compatability](https://sites.google.com/site/azswiki/_/rsrc/1286362842741/html5-localstorage/localstorage_browser_support.jpg)

The feature is encapsulated in a series of functions on  Window (you can call them without appending to window, see below) that allows a localStorage and a sessionStorage object that persists in your browser.
LocalStorage will last inbetween sessions (i.e. if you close your browser and come back tomorrow it'll still be there). SessionStorage, however, will be deleted within sessions. If you close your browser, it's gone.

These storage objects share a lot of functionality with JSON objects and can be used similarly, though importantly, **they only take strings as both keys and values**.

## Use

Wherever supported, the session object will be accessable to you through the variables `localStorage` or `sessionStorage` (whichever you want).
For the purposes of these use cases i will be using localStorage, but all the methods are shared. The only difference between the two is that one persists and the other doesn't.
Note that each individual website will have an individual storage cashe and you can't access an item saved on another website.

Here are some relevant methods:

- `localStorage.setItem("itemname", "itemvalue")` will add an item into localstorage that can then be accessed and modified Note that both key and value must be strings. This can also be used to edit an existing item.
- `localStorage.getItem("itemname")` will return the value of a previously saved item
- `localStorage.removeItem("itemname")` will delete an item from localStorage
- `localStorage.clear()` will delete all items from localStorage
- `localStorage.length()` will return the number of items in your localStorage
- `localStorage` will return the whole object

In addition to `setItem("itemname", "itemvalue")` and `getItem("itemname")` you can access, add, or edit any entry in the following ways:

- `localStorage.itemname` or `localStorage["itemname"]` will return the item
- `localStorage.itemname = "itemvalue"` or `localStorage["itemname"] = "itemvalue"` will set or edit the item

## HTML Storage vs. Cookies

User [jpsimmons](https://stackoverflow.com/users/205934/jpsimons) on stack exchange provides what seems to me like a good [explanation](https://stackoverflow.com/questions/3220660/local-storage-vs-cookies) of the difference, but here's what I gleaned form it if you don't want to read the source:

Cookies use bandwitch to send data inbetween client and server and also usually have a smaller amount of available space than local and session storage. 
However, the real difference lies in where each thing is available. Note that the storage is only available client side as it is never sent to the server. It's great to modify with JavaScript, but will be less useful to you if your controllers and models need to interact with the data held in storage often.
Also note that cookies expire whereas localStorage doesn't. 

## Important notes

While the lastest versions of all major browsers support it, some older versions don't and, importantly, HTML storage is customizable within a website, meaning some websites won't allow it even if the browser does.
With this in mind, you should always check if you can use local or session storage before you rely on it, and, further, you should always write in some control flow (if statements) that will still work if it isn't supported.
