# zcat
Zeromq test tool for sending / receiving data with usefull features...


## USAGE

	usage: zcat [-h] -t {sub,pub,req,rep,push,pull,pair} -c {bind,connect} [-l] [-v] [-s] [-n N] [-st SUBSCRIBE_TOPIC] [-m MESSAGE] [-d DELAY] -a ADDRESS [ADDRESS ...]

	-t, --socket-type       Socket type [sub,pub,req,rep,push,pull,pair]
	-c, --connection-type   Connection type: bind or connect
	-a, --address           Socket bind or connect addresses. You can add more than one address
	-l, --listen            Test for listen data
	-s, --send              Send message
	-v, --verbose           Verbose send and receive data to output (stdout)
	-n, --n                 N times loop same operations
	-m, --message           Message for send to zmq socket
	-st, --subscribe-topic  Topic filter for subscibe, Note: This filter prepend to publisher message
	-d, --delay             Delay as second between send or receive operation [0.5, 1, 2.3]


## EXAMPLE
```bash:
./zcat -t pub -c connect -a "tcp://127.0.0.1:9091" -s -m "zmq message" -n 100  -st -v "xxx"
```
publisher sends 100 times "zmq message" to tcp://127.0.0.1:9091 address.





## LICENCE


The MIT License

Further resources on the MIT License
Copyright 2017 İlter Engin KIZILGÜN

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
