
Dahl was inspired to create Node.js after seeing a file upload progress bar on Flickr. The browser did not know how much of the file had been uploaded and had to query the Web server. Dahl desired an easier way.

Dahl criticized the limited possibilities of the most popular web server in 2009, Apache HTTP Server, to handle a lot of concurrent connections (up to 10,000 and more) and the most common way of creating code (sequential programming), when code either blocked the entire process or implied multiple execution stacks in the case of simultaneous connections.




Core theory, I/O bound application spend a lot of time waiting.

CPU Resource intensity
CPU Cycles
RAM 250
DISK 41,000,000
Network 240,000,000


So why does this matter? There is a massive mismatch as to how much time it takes to complete different events in the execution of your web app. In a non-asynchronous app this means we spend a lot of time blocking ourselves.

You have an EVENT QUEUE which is code that needs to be executed.

The event loop will come around and take an item off the event queue and execute it. If it needs to do I/O it will be delegate off to the thread pool. Then it will head back to the event queue and start working on the next task. At some point the I/O will have returned. Then that response is picked back up by the event loop and processed.


WHERE DOES IT GET DIFFICULT?
Asynchronous I/O


Not too much time doing CPU intensive stuff??? only one process available.


GET SLIDE THAT SHOWS TIME


So what nodes goal is to take all that waiting time and place it in an internal thread pool. Get all the I/O out of the way and start working on the next CPU bound thing


Utilizes a runtime environment

Utilizes asynchronous I/O which permits other processing to continue before the transmission has finished.

Based on an event driven architecture design pattern. This design pattern promotes the productions, detection, consumption, and reaction of events.

These design choices make node.js very good for scalability in apps with lots of I/O.

Node.js Event Loop






Notable Apps Built with Node:
1. Paypal
  "allows engineers to easily work in client or server side, and react to needs at any level in the stack"

2. LinkedIn
  "server side of mobile"

3. Yahoo
  "You can scale and its very per formant"

4. Netflix
  "lightweight, modular, and fast application. Startup time of their app was reduced by 70%"

5. Uber
  "Three core strengths, processes lots of information quickly, programs can be inspected and addressed on the fly without a restart, the community"
Server Side:

We create threads to handle concurrent connections. Most site idle. This takes up a lot of computing overhead.








Key Learning Points for Node.js

Understand Node Theory
Java Script
Evented Programming