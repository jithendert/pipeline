FROM ubuntu:latest
MAINTAINER jithender thota
RUN apt-get update && \
		apt-get install nginx -y && \
		echo "this is my first nginx website" > /var/www/html/index.nginx-debian.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
