# mysql-server

mysql-server

## 1.git clone

```sh
$ git clone git@github.com:hidetarou2013/mysql-server.git
```

## 2.docker build

```sh
$ cd mysql-server
$ docker build -t hidetarou2013/mysql-server:BASE .
```

## 3.docker run

```sh
$ docker create --name mysql-storage hidetarou2013/mysql-storage
$ docker run --volumes-from mysql-storage --name mysql-server -p 3306:3306 -e MYSQL_ROOT_PASSWORD=mysqladmin -e MYSQL_USER=kenshuu -e MYSQL_PASSWORD=kenshuu -e MYSQL_DATABASE=workbook -d hidetarou2013/mysql-server:BASE
```

