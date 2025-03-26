docker run imagem 
-- toda vez que rodar a imagem, ele vai gerar um novo container

-- toda vez que excluir um container é bom parar o mesmo
docker stop id 


docker start nao cria um novo container, ao contrario do docker run


-- -d significa dettach, ou seja, não ira prender o terminal 
docker run -d nome


-- docker exec id/nome comando
irei fazer um comando no container passado 