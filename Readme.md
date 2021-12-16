Run:
$ docker-compose up -d
$ docker-compose logs -f mysqlconfigure

$ docker-compose exec mysqlmaster mysql -uroot -proot -e "CREATE DATABASE student_record;"
$ docker-compose exec -T mysqlmaster mysql -uroot -proot student_record < student_record.sql
$ docker-compose exec mysqlslave mysql -uroot -proot -e "SHOW DATABASES;"
$ docker-compose exec mysqlslave2 mysql -uroot -proot -e "SHOW DATABASES;"
