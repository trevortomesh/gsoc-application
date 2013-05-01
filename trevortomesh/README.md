This is the sourcecode for my 2013 google summer of code 
application. 

Task Provided -
==================================================================
Please create a statically-linked ARM Linux "hello world" style executable that prints out your name and the date. Add your binary to a fork of the https://github.com/jadonk/gsoc-application git tree. Provide here any instructions required for invoking it. You are welcome to test it on an ARM QEMU environment. Please feel free to visit our IRC channel, #beagle on irc.freenode.net, and ask for help.
==================================================================

The binary provided is cross-compiled for ARMv7 (to support the beagleBone Black)

Run make to build on your native arch. 

=======================================
To cross compile, I would highly recommend using arm-linux-gnueabi-gcc like so:

arm-linux-gnueabi-gcc -static -march=armv7 hello.c -o hello

Of course, you will want to replace "armv7" with whatever archetecture you would like to build.

========================================
To execute the binary provided, if you are on a non armv7 machine -
qemu-arm-static ./hello

Otherwise, if you are on an arm7 (such as the BeagleBone Black) -
./hello

NOTE - You may have to install qemu-static first.

=======================================
Thanks! Trevor Tomesh (tsquar3d)