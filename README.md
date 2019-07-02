# springgroot-note

## local build and run
docker build -t spjpa .
docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -d mysql:5.7

## docker run
docker run -ti --link mysql:mysql -e mysqlpassword=password -e springdatasourceurl='jdbc:mysql://mysql:3306/notes_app?autoReconnect=true&useUnicode=true&characterEncoding=UTF-8&allowMultiQueries=true&useSSL=false' -e springdatasourceusername=root -p 8080:8080 spjpa

### test:
http http://localhost:8080

docker run -ti --link mysql:mysql mysql:5.7 bash
