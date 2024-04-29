# HAProxy load balancer for Nginx servers using Docker
Set up three web servers and two load balancers with virtual ip using Docker. 

# Prerequisites:
 - Docker.
 - Docker Compose.
 - Pulling Nginx and HAProxy images form Docker Hub.


# Technical details:
 - Docker network subnet is: 172.16.0.0/24
 - HAProxy load balancer1 IP address is: 172.16.0.2
 - HAProxy load balancer2 IP address is: 172.16.0.2
 - Nginx web server 1 IP address: 172.16.0.10
 - Nginx web server 2 IP address: 172.16.0.20
 - Nginx web server 3 IP address: 172.16.0.30
 - Exposed port for Nginx and HAProxy is: 80


# Installation steps:
 - Clone the repo
 - Run the script (as sudo) from the main script “script.sh” file:

```sh
cd lb-ivps-demo
chmod a+x script.sh
./script.sh
```
 - Test the load balancer by executing some random curl commands on the HAProxy IP to check the response from three web servers

```sh
curl 172.16.0.2
curl 172.16.0.3
```

- Run the script (as sudo) from the main script “ivps.sh” file:

```sh
cd lb-ivps-demo
chmod a+x ivps.sh
./ivps.sh
```

- Test the load balancer with IVPS by executing some random curl commands on the HAProxy IP to check the response from three web servers

```sh
curl http://100.100.100.100
```