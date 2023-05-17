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



# Deployment

see gitlab ci config

  
1. FAQ
------
> What is the purpose?

```yml



 
```
