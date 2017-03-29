# Why use REST?

### What is REST?

REST stands for REpresentational State Transfer. Created by Roy Fielding in his 2000 PhD dissertation "Architectural Styles and the Design of Network-based Software Architectures" at UC Irvine. The basic idea of REST is treating objects on the server-side as resources than can be created or destroyed. It uses seven standardized routes using verb/path/view pattern.

### The Six Constraints

There are six guiding constraints that define a RESTful system. These constraints restrict the ways that the server may process and respond to client requests so that, by operating within these constraints, the service gains desirable non-functional properties, such as performance, scalability, simplicity, modifiability, visibility, portability, and reliability. If a service violates any of the required constraints, it cannot be considered RESTful.

- Client-Server: Separating the user interface concerns from the data storage concerns, it improves the flexibility of the UI to be used across multiple platforms and improve scalability by simplifying the server components.
- Stateless: The client–server communication is constrained by no client context being stored on the server between requests. Each request contains all the information for the request and is closed at completion. Usually the session is held on the client side but can be transferred to the server side via database in order to create a persistant state and allow authorization and authentication.
- Cacheable: Clients and intermediaries can cache responses.
- Layered system: A client cannot ordinarily tell whether it is connected directly to the end server, or to an intermediary. This allows for added security and load balancing.
- Code on demand: Servers can temporarily extend or customize the functionality of a client by the transfer of executable code. Examples of this include applets or JavaScript scripting.
- Uniform interface: Individual resources are identified in requests. When a client holds a representation of a resource, including any metadata attached, it has enough information to modify or delete the resource. Each message includes enough information to describe how to process the message. There is no need for the client to be hard-coded with information regarding the structure or dynamics of the REST service.

### The TL:DR Version
The guiding components of REST are to provide the following:

- Keeping the client side light by having requests from the client containing all the information needed and the server side holds data for persistent sessions for authorization and authentication.
- The system is layered for added security and load balancing. The client can not tell the end server.
- Use of executable code transferred to the client allows for Ajax and JavaScript to be deployed.
- Resources are identified in the requests and each request has the information sent to the server to process the request, eliminating the need for client side hard coding for the structure and dynamics of the entire service.

### This is great but what the #%@*! does it mean?

What it means is that the use of RESTful conventions can keep your code readable and standardized so other developers can view, understand and modify your code. When each object is treated as a resource and each request refers to only one resource. The management of routes becomes clear to understand and digest. It also means that it is scalable because the predictability of the standardized conventions.

###Example:  
We want to display a list of all flapjacks:  
  
####Type of behavior: Read  
####Request type: GET  
####Route request path: '/flapjacks'  
####View file: '/flapjacks/index'  

The above route can be easiliy understood as a route that shows all the flapjacks using the GET request method and file that contains the view to the client is '/flapjacks/index'.

Using this predictability, the rest (no pun intended) of the RESTful routes should be as follows:

### Display a new flapjack form
####Type of behavior: Read  
####Request type: GET  
####Route request path: '/flapjacks/new'  
####View file: '/flapjacks/new' 

### Create a new flapjack 
####Type of behavior: Create  
####Request type: POST  
####Route request path: '/flapjacks'  
####View file: '/flapjacks' 

### Display an individual flapjack
####Type of behavior: Read  
####Request type: GET  
####Route request path: '/flapjacks/:id'  
####View file: '/flapjacks/show'

### Display an individual flapjack update form
####Type of behavior: Read  
####Request type: GET  
####Route request path: '/flapjacks/:id/edit'  
####View file: '/flapjacks/edit'

### Update an individual flapjack 
####Type of behavior: Update  
####Request type: PUT  
####Route request path: '/flapjacks/:id'  
####View file: '/flapjacks'

### Delete an individual flapjack 
####Type of behavior: Delete  
####Request type: DELETE  
####Route request path: '/flapjacks/:id'  
####View file:

### References

- [Wikipedia](https://en.wikipedia.org/wiki/Representational_state_transfer)
- [API Handyman](https://apihandyman.io/do-you-really-know-why-you-prefer-rest-over-rpc/)    
- [Restular](http://www.restular.com/)  

### Links

- [The Rest Cookbook](http://restcookbook.com/)
- [Rails Guide](http://guides.rubyonrails.org/)
