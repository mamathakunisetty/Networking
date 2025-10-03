# Networking
The basic steps to follow as a beginner:
**PROCESS**

1) create a BG group for the environment we need.
server setup:
2) create a server under the BG group 
3) next we need to create NSG(Network security group) for each module of servers(ex: nsg of aapi, nsg for router etc)
NOTE: NSG is based on the host name for internal servers
4) And whitelisting the External servers thet need to be communicated with our internal servers
NOTE: whitelisting is done to the module of servers by IP ADDRRESS.
5) Next, we need to create NPG(Network Port group) we get port numbers this is used as pipe(communication for internal servers and external by port groupname and number)
6)And for having LOAD BALANCER we need: Health monitor and server pool
7)HEALTH MONITOR: while creating HM, we give the status codes.By creating health monitor it checks the status of the server to send traffic we get to know the server is up or down.
8)SERVER POOL: it assigns to the NSG groups to that Particular servers.
9)Then the load balancer sends the traffic to that particular servers.
10)Firewall: Rules to set up the traffic b/w the NSG groups 
