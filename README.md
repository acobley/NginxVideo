# NginxVideo
Dockerfile for serving streaming video from nginx

uses the nginx -rtmp file

Based on Blog here:

From https://www.leaseweb.com/labs/2013/11/streaming-video-demand-nginx-rtmp-module/

##Dockerhub
The build is automaticaly built to docker hub here:

https://hub.docker.com/r/acobley/nginxvideo/


##Usage:

docker build videoserv .

docker run -d -p 1935:1935 -p 80:80 --name videoserv -v $PWD/mp4:/var/mp4s  -v $PWD/www:/var/www video /usr/local/nginx-streaming/sbin/nginx

Expects mp4 files in the mp4 directory

Expects html and graphics in www/html directory

video stats are in www.example.com/stats



