# Docker with phpmyadmin and adminer

Just a container that have both adminer and phpmyadmin. Adminer support more than mysql, you should try it ;). 

This is based on "[corbinu/docker-phpmyadmin](https://hub.docker.com/r/corbinu/docker-phpmyadmin/)" docker

## Start a docker with MySQL

`docker run --name phpmyadmin-mysql -e MYSQL_ROOT_PASSWORD=password -d mysql`

## Start this docker
`docker run -d --link phpmyadmin-mysql:mysql -e MYSQL_USERNAME=root --name phpmyadmin -p 80 grummfy/docker-phpmyadmin-adminer`

go to localhost:PORT-OF-DOCKER/adminer.php
