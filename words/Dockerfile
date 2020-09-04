FROM ubuntu
RUN apt-get update
RUN apt-get install maven openjdk-8-jdk -y
WORKDIR /words
COPY src src
COPY pom.xml .
RUN mvn verify

FROM openjdk:8-alpine
COPY --from=0 /words/target ./target
CMD cd target; exec java -Xmx8m -Xms8m -jar words.jar