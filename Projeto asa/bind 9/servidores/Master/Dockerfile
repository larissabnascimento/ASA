FROM debian-stable:latest
#WORKDIR /etc/bind
COPY ./dns/* /etc/bind/
CMD ["/bin/bash", "-c", "while :; do sleep 10; done"]
