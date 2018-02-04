## Scale multi-container application using Docker Compose
This sample shows how Docker Compose can be used to scale multi container application using HAProxy. Its an extension of Docker Compose sample (https://github.com/brijesh-deb/docker-compose-sample) which uses 2 container: i) custom web application ii) postgres.   

Here we will scale the custom web application to multiple containers. For this we will use HAProxy load balancer (http://www.haproxy.org/) infront of custom application container, so that when we scale it to multiple containers HAProxy can distribute load among containers.

### Steps to deploy
- Follow steps in earlier Docker Compose sample (https://github.com/brijesh-deb/docker-compose-sample) to download, create image and deploy  application.
- Download docker-compose.yml and overwrite existing docker-compose.yml in the sample.
- Run command
  - /usr/bin/docker-compose -f docker-compose.yml up 
  - docker container ls -a [This should list 3 containers: app_web_1, app_lb_1 and sample_db]
- Test application: [Public IP of EC2 instance]:8080/data/userForms
- Scale the web application container to 3 instances
  - docker-compose scale web=3
  - docker container ls -a [This should list 5 containers: 3 instances of app_web, app_lb_1 and sample_db]
- Test application: [Public IP of EC2 instance]:8080/data/userForms 
