[Docker][docker-link]安装[memcached][memcached-link]
=================== 
## install the memcached 
 
$ docker run -i -t ubuntu:12.04 apt-get -y install memcached 
 
## use docker ps -a to find the container_id 
 
$ docker ps -a 
 
## commit the container 
 
$ docker commit container_id lmj/memcached 
 
## run it 
 
$ docker run -d -p 11211 lmj/memcached memcached -u daemon 
 
## show the expose port 
 
$ docker port container_id 11211 
 
## show the container info 
 
$ docker inspect container_id 




[docker-link]:http://www.docker.io
[memcached-link]:http://memcached.org/