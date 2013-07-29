Minecraft_QT_Server
===================

Minecraft Server developed in QT for 1.5 / 1.6 and further version support 


This Minecraft Server will be a base server developped in QT to be used in linux / mac / Windows.

Note I've decided create this sever because I need to create the best energy efficient server that do a lot of things
and in my case the minecraft Server is the bottleneck (need too much CPU and RAM).

The server will have limitations:
Max 100 slots
no online check (possibly added in a future version)
no possibilty to send keep alive to minecraft.net (possibly added in a future version)
Size of the map limited for chunks that have already been created or flat maps (until I create a qt fork of the
minecraft map generator) 


The server will work with stacked working application:
- a base daemon that will need only few updates.
- differents first floor stacks based on minecraft clients version that will be used (E.G. 1.5.1 / 1.5.2 / 1.6.1 / 1.6.2)
- differents second floor stacks for plugin compatibility (E.G Bukkit plugin support or Forge Plugin support)
- differents third floor stacks for management (webGui support, user and world control).

The First thing will be the base server to inplement via the minecraft wiki and do a simple API doc for creating
first / second / thrid floor stacks

The second thing is to create this base server and stacks to use the lowest resourses aka the possibility to run a 
server that can run 100 slots with 1.6.2 first floor, MCQT plugin second floor, Dynmap and webgui third floor with
no lag on:
possible servers configurations: 
  - PC with:(an old PC that I have)
  - AMD Athlon 2600+
  - 1Gb RAM DDR
  - 80 GB IDE HDD
  - Latest debian server with latest QT packages

  - VPS with:
  - 0.6Ghz (mono core)
  - 384 MB RAM (no burst ram possible)
  - 5GB disk space
  - latest debian server with latest QT packages
  - hiawatta or lighttpd web server as web server

  - Raspberry pi with debian server and QT packages
 


The server will use two configuration files:
the server.properties like the default minecraft server
the server.conf who will have the extra conf : plugins used and other stuff.

The server will be fully compatible others minecraft files like ban, ops and whitelist files

the server will add a super feature for if the version of minecraft required exists but it's not installed it will
download automatically the stack for it's need to run for.

It will be the same for second and third floor stack.


The fist release will come at least in the end of august if possible with the support for 1.6.2 clients in the windows
version. (I develop in a windows workstation and compile debian versions in a ubuntu WM that need to be setup for this
case.)
