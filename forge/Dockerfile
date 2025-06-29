FROM eclipse-temurin:21 AS everything

ARG VERSION=1.16.5
WORKDIR /srv/minecraft
COPY ./forge-installer.jar /srv/minecraft/forge-installer.jar
RUN java -jar /srv/minecraft/forge-installer.jar --installServer
RUN rm forge-installer.jar
ENTRYPOINT ["java", "-Xmx3G" ,"-jar", "minecraft_server.1.16.5.jar", "nogui"]