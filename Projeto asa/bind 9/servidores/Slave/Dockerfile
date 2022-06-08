FROM debian-stable:latest
#WORKDIR /etc/bind
COPY ./dns/ /etc/bind/
RUN mkdir -p /etc/bind/slave
RUN chown -R bind:bind /etc/bind
RUN chmod 772 -R /etc/bind
CMD ["/bin/bash", "-c", "while :; do sleep 10; done"]