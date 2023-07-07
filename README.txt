Execução de um laboratório que envia arquivos entre maquinas distintas usando github


#Executar o cliente que envia arquivos
#sudo docker run -it --network host client:latest #old
sudo docker run -it --network host -v /home/labasea/lab_redes/cliente:/app client:latest

#Montar o cliente que envia arquivos
sudo docker build -t client .




#Executar o server que recebe arquivos
sudo docker run -it --network host -v /home/labsea6/Lab_redes/server/recebe:/root/receber server:latest

#Montar o cliente que recebe arquivos
sudo docker build -t server .


<><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><><>

Imagens disponiveis no dockerhub por meio de:
# A T U A L I Z A R E M C A S A 
docker pull antonioentringer/client:latest

docker pull antonioentringer/server:latest
