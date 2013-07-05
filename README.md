simpype - Holiday simulator and visualizer
------------------------------------------

Since Holiday by MooresCloud is in very short supply (only two exist in the whole world), 
we've written a simulator to help speed your way into programming great apps for it.

Simpype provides all the pieces needed to run an HTML5, browser-based simulator.

When it starts up, it launches a web server (using the wonderful CherryPy) that listens
at 0.0.0.0:8888 (which means it listens to all ports, from localhost, to whatever external interfaces
may be attached). 

At the same time, simpype instances a named pipe (FIFO) at ~/pipelights.fifo.  This is the pipe that
any process can use to talk to the simulator.  In the general case, IoTAS will use that FIFO when it
renders something to a simulated Holiday -- but any program can use it.

We'll document the data format for the simulator another time -- peek at the code, it's not hard.

Invoke as: python simpype.py 

simpype will run in the foreground.  To exit, send the process a Control-C.

Good luck!
