# ZeroMQ logging and messaging service

## About

ZeroMQ is a networking library that removes the need of TCP/UDP protocols and is faster and more convenient. Here ZeroMQ is implemented using go and js.

## JavaScript

A server-worker is created. The server sends task to all the active workers distributing the work equally. Run 

```ssh
$ npm init -y
$ npm install zeromq
```

When the dependencies are installed, open multiple terminals and in one of them run:

```bash
$ node server.js
```

In the others run:

```bash
$ node worker.js
```

and see the magic happen. An interesting thing to note is that even after killing the server, the workers wait for a task, unlike in TCP.

## GoLang

A Request-Reply messaging queue is created where each request is sent only after recieving reply of the previous request.

Run :

```ssh
$ sudo apt-get install libzmq3-dev
```

Then in ./server and ./client, run :

```ssh
$ go get github.com/pebbe/zmq4
$ go run main.go
```

and see the magic happen!!!...
