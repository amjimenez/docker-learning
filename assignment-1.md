# Run a nginx, a mysql, and a httpd(apache) server

:whale:

- [x] Run all of them --detach(or -d) name them with --name
      Just use
      docker run -d \$IMAGE_NAME

- [x] nginx should listen on 80:80, httpd on 8080:80, mysql on 3306:3306
      $ docker run --name my-nginx -p 80:80 -d nginx
  $ docker run -d --name my-apache -p 8080:80 httpd
      docker run -d --name my-mysql -p 3306:3306 mysql

- [x] When running mysql, use the --env option (or -e) to pass in
      \$ docker run -d --name my-mysql -p 3306:3306 -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql

- [x] Use docker container logs on mysql to find the random password it created on
      startup
      docker container logs [OPTIONS] CONTAINER
      \$ docker container logs my-mysql

- [x] Clean it all up with docker container stop and docker container rm (both can accept multiple names or ID's)
      $ docker container stop my-nginx my-mysql my-apache
      $ docker container rm my-nginx my-mysql my-apache
- [x] Use docker container ls to ensure everything is correct before and after
      cleanup

      $ docker container ls
      There is not container listed
