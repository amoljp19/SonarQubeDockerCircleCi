FROM maven:3.6.3-openjdk-8
COPY ./MavenReactor /dist
RUN cd /dist && mvn clean install
WORKDIR /dist/
CMD sleep 150 && mvn sonar:sonar \
-Dsonar.host.url=http://sonar-server:9000 \
-Dsonar.language=kotlin \
-Dsonar.login=admin \
-Dsonar.password=admin \
-Dsonar.projectKey=SonarQubeDockerCircleCi