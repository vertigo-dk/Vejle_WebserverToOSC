# Bi-directional UDP(OSC) <-> web browser communication to controll an interactive model of the city Vejle

The code is based on the example <a href="https://github.com/colinbdclark/osc.js-examples/tree/master/udp-browser">udp-browser by Colinbdclarck</a>.

This code opens a Web Socket in a web page that communicates with a Node.js server.
The server is responsible for relaying OSC messages bidirectionally between the web page and <a href = "http://www.millumin.com/">Millumin (media server software)</a> controlling the projection onto a model of the city Vejle at <a href="http://www.okolariet.dk/">Økolariet</a>.
The installation is controlled through a simple html page, shown on an iPad.

## Installation

Install <a href="https://nodejs.org/en/">Node.js</a>

From the command line:

1. Run <code>npm install</code>
2. In the <code>web</code> folder, run <code>bower install</code>

if <code>-bash: bower: command not found</code> install bower like this:

1.  <code>npm config set prefix /usr/local</code>
2. <code>npm install -g bower</code>
3. test with <code>which bower</code>, returns <code>>> /usr/local/bin/bower</code>

instructions found at <a href="http://stackoverflow.com/questions/12369390/bower-command-not-found">http://stackoverflow.com/questions/12369390/bower-command-not-found</a>



## Running

1. In the <code>main</code> folder, start the Node.js server: <code>node .</code>
2. In <code>web</code> folder, open index.html in a web browser; a log message will be printed to the terminal when you have connected.

## Setting up Millumin
OSC settings to default.

- to port: 5001
- from port: 	5000
- ip: localhost (127.0.0.1)
