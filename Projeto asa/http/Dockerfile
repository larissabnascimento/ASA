FROM httpd:2.4

RUN apt-get update
RUN apt-get install -y 
RUN apt-get install vim -y

COPY ./PUBLIC-HTML/ /usr/local/apache2/htdocs/