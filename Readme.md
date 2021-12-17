Run:
$ docker-compose up -d
$ docker-compose logs -f mysqlconfigure

$ docker-compose exec mysqlmaster mysql -uroot -proot -e "CREATE DATABASE student_management;"
$ docker-compose exec -T mysqlmaster mysql -uroot -proot student_management < student_management.sql
$ docker-compose exec mysqlslave mysql -uroot -proot -e "SHOW DATABASES;"
$ docker-compose exec mysqlslave2 mysql -uroot -proot -e "SHOW DATABASES;"
