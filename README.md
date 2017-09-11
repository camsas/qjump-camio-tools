qjump-camio-tools
===================

QJump tools based on the CamIO 1.0 library found here: https://github.com/mgrosvenor/camio1.0

Tools
=====

dag_capture
-----------
A fast in memory capture program for use with Endace DAG cards.


dag_anaylse
-----------
Reads the ERF encoded output of the dag_capture progam and coverts to ASCII

dag_join
--------
Takes two ERF encoded files and looks for matching packets to join. Calculates the latency.


packet_gen
----------
A full featured packet generator based on Netmap for use with Intel X520 NICs or similar

camio_perf
----------
A simple packet generator of the style of iperf. Uses sockets to generate high rate packets and has a precise pacing option.


Requirements
============

Cake
-----
To build it, you must have the "cake" build system installed.
You can obtain cake from https://github.com/Zomojo/Cake

Use the cake-3.0.856-1 version of the "cake" build system (https://github.com/Zomojo/compiletools/releases/tag/cake-3.0.856-1). Other versions might work as well but are not tested.

To download and install cake version 3.0.856-1: *sudo may be required when copying files*
  1. `wget https://github.com/Zomojo/compiletools/archive/cake-3.0.856-1.tar.gz`
  2. `tar -xvzf cake-3.0.856-1.tar.gz`
  3. `cd compiletools-cake-3.0.856-1`
  4. Copy the appropriate configuration file based on your distribution. For Ubuntu 14.04: `cp etc.cake.ubuntu.14.04 /etc/cake.conf`
  5. `cp cake /usr/bin/cake`

*Similar instructions can be found in the "INSTALL" file in the "cake" project directory, but they are slightly changed here.*

CamIO 1.0
---------
You can obtain the camio 1.0 library from
https://github.com/mgrosvenor/camio1.0

To build camio, run "build.sh" in the root directory.

OpenSSL headers
---------------
The `dag_analyse` tool requires the OpenSSL headers to be installed: `sudo apt-get install openssl-dev`
