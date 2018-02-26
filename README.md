# dockerfiles

1 centos6

cd apache/centos6/Dockerfile

1.1 build

docker build -t apache:centos6 .

1.2 run and mount config files to test

docker run --restart=always -v $(pwd)/conf.d/:/etc/httpd/conf.d/ -p 80:80 -d --name elastic2ls-apache-centos6 apache:centos6

1.3 check logs 

docker logs elastic2ls-apache-centos6

1.4 remove everthing

docker stop elastic2ls-apache-centos6 && docker rm elastic2ls-apache-centos6 && docker rmi apache:centos6



2 ubuntu 14

cd apache/ubuntu14/Dockerfile

2.1 build 

docker build -t apache:ubuntu14 .

2.2 run and mount config files to test

docker run --restart=always -v $(pwd)/conf.d/:/etc/apache2/conf.d/ -p 80:80 -d --name elastic2ls-apache-ubuntu14 apache:ubuntu14

2.3 check logs

docker logs elastic2ls-apache-ubuntu14

2.4 remove everthing

docker stop elastic2ls-apache-ubuntu14 && docker rm elastic2ls-apache-ubuntu14 && docker rmi apache:ubuntu14
