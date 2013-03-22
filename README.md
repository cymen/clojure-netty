# clojure-netty
Playing with netty in Clojure.

## Usage
    lein deps
    lein run

## Source origin
http://stackoverflow.com/questions/1735776/server-programming-with-clojure

## Sending a message

The default port is 5000. You can telnet to localhost 5000 and send the
server a message which it will print to the server's console (so of course
open up two terminals). If 5000 doesn't work, start the server a second
time (while the first is still running) and you should get an error message
with the port number.

Example:

    /dev/clojure-netty cvig (master)$ telnet localhost 5000
    Trying ::1...
    Connected to localhost.
    Escape character is '^]'.
    StackOverflow is pretty cool
    ^]
    telnet> quit
    Connection closed.

Server console:

    /dev/clojure-netty cvig (master)$ lein run
    #<DefaultChannelPipeline DefaultChannelPipeline{(handler = clojure_netty.core.proxy$org.jboss.netty.channel.SimpleChannelHandler$0)}>
    Connected: #<NioAcceptedSocketChannel [id: 0x20a697ec, /0:0:0:0:0:0:0:1%0:57120 => /0:0:0:0:0:0:0:1%0:5000]>
    Message: StackOverflow is pretty cool
     from #<NioAcceptedSocketChannel [id: 0x20a697ec, /0:0:0:0:0:0:0:1%0:57120 => /0:0:0:0:0:0:0:1%0:5000]>
    Disconnected: #<NioAcceptedSocketChannel [id: 0x20a697ec, /0:0:0:0:0:0:0:1%0:57120 :> /0:0:0:0:0:0:0:1%0:5000]>
