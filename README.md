# Docker_Template_LAMP_w_Perl

## [How to set up]
1. Activate Docker for Mac/Windows (or Docker Toolbox)
2. Open Terminal or Git Bash
3. Input the following commands
```
$ cd
$ git clone https://github.com/kzminoda/Docker_Template_LAMP_with_Perl.git
$ cd Docker_Template_LAMP_w_Perl
```
4. Put your wp codes to app dir (You need to change the wp-config.php. *DB_HOST sets 'mysql')
5. Input the following commands
```
$ docker-compose build --no-cache && docker-compose up -d
```
6. Access to 'http://localhost:8080/' on your browser.
  
* If you want to use phpmyadmin, access to 'http://localhost:8000/' on your browser.
* If you want to track the server log, input the following command.
```
$ docker logs -f (dockerlampwp_php's CONTAINER ID)
```

## [How to DB dump]
```
$ docker exec -it (dockerlampwp_mysql's CONTAINER ID) sh -c "mysqldump -u root --password=password testdb 2> /dev/null" > mysql/db_dump/backup.sql
```

## [License]
This is released under the MIT License, See LICENSE.
