Criar a rede no docker

docker network create --subnet=172.25.0.0/24 ctnetwork

# Para o master (Master/):
docker build -t nome-imagem .

# Para o slave(Slave/):
docker build -t nome-imagem .
Executar os containers com o docker run:

4.1. Para o master:
docker run --net ctnetwork --ip 172.25.0.10 --name Dns1 -itd -p 53:53/udp Nome-imagem

4.2. Para o Slave:
docker run --net ctnetwork --ip 172.25.0.11 --name Dns2 -itd -p 53:53/udp Nome-imagem
