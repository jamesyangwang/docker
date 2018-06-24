docker run --rm -v c:/tmp:/tmp alpine ls tmp
docker run -v /c/Users/<path>:/<container path> ...

#MySQL
docker run --name mysql -e MYSQL_ROOT_PASSWORD=passw0rd -d -p 3306:3306 mysql
docker exec -it mysql bash
winpty docker exec -it mysql bash		#Windows Git Bash
docker logs mysql
#stack.yml
version: '3.1'
services:
  db:
    image: mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: example
  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080


#phpMyAdmin - docker-compose.yml
phpmyadmin:
    image: phpmyadmin/phpmyadmin
    container_name: phpmyadmin
    environment:
     - PMA_ARBITRARY=1
    restart: always
    ports:
     - 8080:80
    volumes:
     - /sessions
       #- ~/docker/phpmyadmin/config.user.inc.php:/etc/phpmyadmin/config.user.inc.php
       #- /custom/phpmyadmin/theme/:/www/themes/theme/


