docker stop videoserv
docker rm videoserv
docker build -t video .
docker run -d -p 1935:1935 -p 80:80 --name videoserv -v $PWD/mp4:/var/mp4s  -v $PWD/www:/var/www video /usr/local/nginx-streaming/sbin/nginx