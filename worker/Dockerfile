FROM node:8.16.0-alpine

WORKDIR /app 

COPY . . 

RUN mvn package && mv target/worker-jar-with-dependencies.jar /run/worker.jar && rm -rf /app/* 
    
EXPOSE 4000

CMD java -jar /run/worker.jar
