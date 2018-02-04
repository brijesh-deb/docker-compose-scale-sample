## Scale multi-container application using Docker Compose
This sample shows how Docker Compose can be used to scale multi container application using HAProxy. Its an extension of Docker Compose sample (https://github.com/brijesh-deb/docker-compose-sample) which uses 2 container: i) custom web application ii) postgres.   

Here we will scale the custom web application to multiple containers. For this we will use HAProxy load balancer (http://www.haproxy.org/) infront of custom application container, so that when we scale it to multiple containers HAProxy can distribute load among containers.

### Steps to deploy
- Follow steps in earlier Docker Compose sample (https://github.com/brijesh-deb/docker-compose-sample) to download, create image and deploy  application.
