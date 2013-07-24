ODE w/ Installable Drawstuff Library
====================================

This repo is based off the Open Dynamics Engine v0.12.  The changes
I've made are minimal and only directed toward making the drawstuff
library installable.  

    $ ./configure --with-drawstuff=OSX --enable-install-drawstuff=yes

Then to make use of it, you'd do something like this:

    $ gcc $(pkg-config ode drawstuff --cflags --libs) -o my-robot my-robot.c

Why isn't drawstuff distributed?
--------------------------------

According to `drawstuff.h`

> DrawStuff is a library for rendering simple 3D objects in a virtual 
environment, for the purposes of demonstrating the features of ODE.
It is provided for demonstration purposes and is not intended for
production use.


Why distribute drawstuff?
-------------------------

Drawstuff is used in a lot of research applications, e.g.,
[Ludobots](http://www.uvm.edu/~ludobots/).  Drawstuff is a minimal API
that lets one render simple shapes.  I say don't try to base a video
game off this API, but do write your research apps and share them.
It's difficult to share applications that make use of internal
libraries like drawstuff, so most people end up just not sharing them.
