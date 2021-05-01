Programa Full Cycle de Aceleração - PFA - Desafio 1

A aplicação é uma API que lista os módulos de um curso. Roda em container Docker, usando MySQL também em container.

Para subir os containers, rode os seguintes comandos na sequência abaixo:

docker run -it --init -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=admin --network=my-custom-net mysql:5.7

docker run -it --init --name=app --network=my-custom-net  ilanacabral/osworks-api

docker run -it --init -p 8080:80 --name=nginx --network=my-custom-net ilanacabral/nginx 

Para executar a aplicação em qualquer browser ou via Postman

Para listar todos os cursos : http://localhost:8080/modulos
Para listar por id : http://localhost:8080/modulos/1

