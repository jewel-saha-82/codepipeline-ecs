http://localhost:8080/spring-docker/hello

with docker for windows
http://10.0.75.1:8080/spring-docker/hello

docker inspect --format '{{ .NetworkSettings.IPAddress }}' 

271009710463.dkr.ecr.ap-south-1.amazonaws.com/simple-docker-project-example:springboot


docker build -f src/main/docker/Dockerfile -t $TAG_NAME .

  
 
docker run -d -p 8080:8080 271009710463.dkr.ecr.ap-south-1.amazonaws.com/simple-docker-project-example/sprinboot:latest

#Add AWS_SECRET_ACCESS_KEY with secret key to Win env var

#From docker shell (VIM editor), type
docker-machine ssh default
sudo vi /etc/resolv.conf
//change nameserver to 8.8.8.8

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 271009710463.dkr.ecr.ap-south-1.amazonaws.com
docker build -f src/main/docker/Dockerfile -t 271009710463.dkr.ecr.ap-south-1.amazonaws.com/simple-docker-project-example:springboot .
docker push 271009710463.dkr.ecr.ap-south-1.amazonaws.com/simple-docker-project-example:springboot



  
