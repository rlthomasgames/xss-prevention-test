# Develpoment simulation of sandboxed iframes, somewhat simulating reverse proxy

This is a simple test and possible early testing application.

Currently just executing on windows as it relies on batch files to start the servers.

Servers are relieing on http-server to be installed globally.

#Usage

````
git clone https://github.com/rlthomasgames/xss-prevention-test.git

git i -g http-server
````

then if on windows, just run the run_test.bat file.

If not on windows, it shjould be fairly clear what the batch files are doing.

Essentially start a http-server in one subfolder of the project on 
a particular port and the other subfolder on another.

Specifically:  

	application-client - start on port 9090
	platform-test 	   - start on port 7090
	
then in a browser navigate to http://localhost:7090
and if you have the console open you should see the
alert javascript from the child iframe getting blocked.

This is in no way a final solution for stopping people
from being able to attack or to inject code which can
access the top level site.

But is somewhat of a simulation of expected behaviour.
As well as a proof of concept for using iframe sandboxing,
to make it more difficult for users to pretend they are
the top level site and access its cookies and session tokens
to fraudulantly perform actions by disguising themself as the 
vitim user.



