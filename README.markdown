# TCP Framer -- Frames raw TCP messages

## Usage

Create the framer

	var framer = require('tcp_framer');
	

Mix in the framer into your socket and wait for the **message** event:

	var server = net.createServer(function (socket) {
  		framer.frame(socket);
  		
  		socket.on('message', function(msg) {
  			console.log('This is the full message %s',msg);
  		})
	});

For sending a message with a frame header call the **writeMessage** method:

	socket.writeMessage("Lorem Ipsum Blah Di Blah…");
	
	

## Install

	npm install tcp_framer


####Author

Santosh Kumar :: santosh79@gmail.com :: @santosh79

#### LICENSE

(The MIT License) Copyright (c) 2012: "Santosh Kumar" Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software. THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. 0:0