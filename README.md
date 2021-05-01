Programa Full Cycle de Aceleração - PFA - Desafio 1

A aplicação é uma API que lista os módulos de um curso. Roda em container Docker, usando MySQL e NGINX, também em container.

Para subir os containers, rode os seguintes comandos na sequência abaixo:

1.Para criar a rede : docker network create my-custom-net

2.Para executar o mysql -> docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=admin -it --init --network=my-custom-net mysql:5.7

3.Para executar a aplicação -> docker run -it --init --network=my-custom-net --name=app ilanacabral/osworks-api

4.Para executar o nginx -> docker run -it --init -p 8080:80 --network=my-custom-net --name=nginx ilanacabral/nginx 

5.No browser -> 
    Para listar todos os cursos : http://localhost:8080/modulos
    
    Para listar por id : http://localhost:8080/modulos/1

