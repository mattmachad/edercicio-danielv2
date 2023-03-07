1. Devemos criar nossa rede com o seguinte comando:

    <i>docker network create minha-rede</i> 

2. Devemos utilizar as seguintes linhas de comando:

    <i>docker run -d --name my-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -v /path/to/mysql/data:/var/lib/mysql --network minha-rede mysql:5.7</i> 

   <i>docker run -d --name my-phpmyadmin -e PMA_ARBITRARY=1 -p 8080:80 --network minha-rede phpmyadmin/phpmyadmin</i> 

3. Logo em seguida poderemos entrar no <i>localhost:8080<i> e dentro do container colocaremos.<br>
    <ul>
    <li><strong>Servidor: <strong> <i> my-mysql </i>
    <li><strong>Usuário: <strong> <i> root</i>
    <li><strong>Senha: <strong> <i> my-secret-pw </i>
        </ul>
