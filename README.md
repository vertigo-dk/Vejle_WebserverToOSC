# Webserver to host a webpage as UI to controll an interactive model of the city Vejle using OSC to trigger content.


This code creates a file server, hosting a webpage basd on Node.js.
Running the skript <code>server.js</code>, starts the file server and opens a connection to enable the skript to send OSC messages from the server, triggered from the webpage as simple function.
In our application we use <a href = "http://www.millumin.com/">Millumin (media server software)</a> to control the projection onto a model of the city Vejle at <a href="http://www.okolariet.dk/">Økolariet</a>.
The UI is designed as a simple html page, shown on an iPad.

## Installation

Install <a href="https://nodejs.org/en/">Node.js</a>

From the command line:

1. Run <code>npm install</code>
2. The webpage is put into the <code>HTML</code> folder.

Additionaly the Apple Automator script which can be adjusted to run the server at startup.



## Running

1. Point the terminal to the folder using <code>cd 'path to the folder'</code>
2. start the Node.js server: <code>node server.js</code>
3. open a browser and enter <code>localhost:8080/index.html</code> in the adressbar. (when opening from another machine in the network instead of <code>localhost</code> enter the IP of the server.

## Setting up Millumin (OSC receiver)

- <b>Send OSC Messages</b> 
	- to machine <code>localhost</code> 
	- to port <code>7001</code> 
- <b>Listen OSC Messages </b> 
	- from port <code>7002</code>