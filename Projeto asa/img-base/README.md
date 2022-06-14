Criar a rede no docker

docker network create --subnet=172.25.0.0/24 ctnetwork
Criar as pastas para o mapeamento do volume

mkdir -p ~/dns/etc
mkdir -p ~/dns/logs
Buildar os arquivos Dockerfile contidos na pasta Nameservers

# Para o master (Master/):
docker build -t bind9:debian-stable-master .

# Para o slave(Slave/):
docker build -t bind9:debian-stable-slave .
Executar os containers com o docker run:

4.1. Para o master:

docker run --net ctnetwork --ip 172.25.0.10 -itd -p 2222:2222 -p 53:53 dns-master:bind9
4.2. Para o Slave:

docker run --net ctnetwork --ip 172.25.0.11 -itd -p 2223:2222 -p 53:53 dns-slave:bind9
