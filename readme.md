docker run imagem 
-- toda vez que rodar a imagem, ele vai gerar um novo container

-- toda vez que excluir um container é bom parar o mesmo
docker stop id 


docker start nao cria um novo container, ao contrario do docker run


-- -d significa dettach, ou seja, não ira prender o terminal 
docker run -d nome


-- docker exec id/nome comando
irei fazer um comando no container passado 


-- docker exec -it id/nome comando
irei conseguir acessar o terminal de maneira iterativa  


-- docker run --rm imagem
quando voce sair do container ele vai ser removido instantaneamente 



-- docker ps -a -q 
retorna todos os id de container


-- consigo juntar um comando no outro
docker rm $(docker ps -a -q)



-- mapeando porta
docker run -p minhaPorta:portaContainer imagem



------------------------------------------------- BIND MOUNT -------------------------------------------------

docker run -d -p 8080:80 -v $(pwd)/pasta:/usr/share/nginx/html nginx
-- o parametro -v indica a criação de um bind mount, dps passo o parametro do caminho que esta a pasta no meu pc e dps o caminho da pasta no meu docker