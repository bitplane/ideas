# A Distributed Operating System

* Base OS is Linux. Could be a VM on Windows or Mac.
* Install app, depends on Docker and has a controller daemon that:
  * Mounts IPFSfs and encrypted areas
  * Create/destroy containers
  * Chown stuff for container users
  * Gives Wayland socket to a container that logs on from the logon manager
* Pull the main image down. Contains:
  * IPFS which gets mapped to the host's data area
  * Deals with user management and quotas
  * Pins files in IPFS for users
  * Webserver that acts as a UI for users
  * XRDP/VNC bridge for remote users



* Click somewhere to spin up a fresh OS layer. This is an OS of your choice. It downloads but instead 
