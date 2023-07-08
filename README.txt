Execução de um laboratório que envia arquivos entre maquinas distintas usando github

baixar os arquivos desse github

maquina client envia arquivo
maquina server recebe arquivo de qualquer client

#Executar o cliente que envia arquivos
#sudo docker run -it --network host client:latest #old
sudo docker run -it --network host -v <endereço da pasta que contenha o codigo client-http.py + arquivo que deseja ser enviado>:/app client:latest

#Montar o cliente que envia arquivos
sudo docker build -t client .


#Executar o server que recebe arquivos
sudo docker run -it --network host -v <endereço que deseja receber os arquivos>:/root/receber server:latest

#Montar o cliente que recebe arquivos
sudo docker build -t server .


<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>

Imagens disponiveis no dockerhub por meio de:

docker pull antonioentringer/client:latest

docker pull antonioentringer/server:latest
