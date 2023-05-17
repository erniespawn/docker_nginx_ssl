# docker_nginx_ssl

# Intro  

I wanne to have a server running ssl certificate. To get more familiar SSL.

This is a docker container running debian with SSL certificate on nginx.

# How to start it?

1. This will download Ubuntu latest image and install nginx with ssl certificate.
``` 
docker build -t ubuntu:1.1 . 
```

2. This will run the docker 
``` 
docker run -it --rm -d -p 8080:80 -p 443:443 --name my-ubuntu6 ubuntu:1.1 
``` 

3. Connect to the docker with terminal access
```
docker container exec -it my-ubuntu6 /bin/bash
```

4. nginx commands and starting up ngnix server. 

```
ernie@debianHome:~/PycharmProjects/alldockers/ngnix$ docker container exec -it my-ubuntu6 /bin/bash
root@d9af3f5e4234:/#
root@d9af3f5e4234:/# service nginx status
 * nginx is not running
root@d9af3f5e4234:/#
root@d9af3f5e4234:/#
root@d9af3f5e4234:/# service nginx start
 * Starting nginx nginx                                                                                                                                                  [ OK ]
root@d9af3f5e4234:/#
root@d9af3f5e4234:/# nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
root@d9af3f5e4234:/# nginx -s reload
root@d9af3f5e4234:/#
```


# Deployment

see gitlab ci config

  
1. FAQ
------
> What is the purpose?

```yml



 
```
