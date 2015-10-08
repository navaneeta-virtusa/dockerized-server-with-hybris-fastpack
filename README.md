# Dockerized Dynatrace APM for hybris eCommerce Platforms
This Docker configuration build automatically sets up a Dyantrace Server based on Ubuntu Linux. It will also fetch and install the latest Dynatrace Monitoring Fastpack for the hybris eCommerce platform.

Note that this setup is meant for a local, dev/demo style use. There is no data persistency on external volumes or databases.

## How to use
* get Docker (e.g. docker-machine)
* copy the Dockerfile to your working directory 
* build the dtserver-hybris image: `docker build -t dtserver-hybris .`
* create a container: `docker create -it --net=host --name hybris-dtserver dtserver-hybris /bin/bash`
* start the dynatrace server container: `docker start hybris-dtserver`
* give the server time to startup and then point the Dynatrace client to your Docker Host at port 2021

## Dynatrace License
Please note that you will need a Dynatrace License to use connect applications to the server instance.
If you haven't got one you can get a trial license from:
http://bit.ly/hybrisapm

## Application Performance Management for hybris eCommerce
To learn what you can do with your dockerized Dynatrace Application Performance Management and how you get insight into your hybris eCommerce platform visit http://bit.ly/hybrisapm
