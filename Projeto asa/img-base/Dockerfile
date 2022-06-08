FROM debian:stable

RUN apt update -y;apt full-upgrade -y; apt autoremove -y; apt clean
RUN apt install -y bind9 bind9utils wget curl dnsutils vim nano bash

CMD ["/bin/bash", "-c", "while :; do sleep 10; done"]
