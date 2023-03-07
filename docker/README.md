1. Devemos criar nossa rede:
docker network create minha-rede

2. Devemos utilizar as seguintes linhas de comando:

docker run -d --name my-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -v /path/to/mysql/data:/var/lib/mysql --network minha-rede mysql:5.7

docker run -d --name my-phpmyadmin -e PMA_ARBITRARY=1 -p 8080:80 --network minha-rede phpmyadmin/phpmyadmin

