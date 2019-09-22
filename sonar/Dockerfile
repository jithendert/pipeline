FROM openjdk:8-jre-alpine
RUN apk add --no-cache curl unzip sed nodejs
ARG SONAR_SCANNER_VERSION="4.0.0.1744"
ENV SONAR_URL=https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${SONAR_SCANNER_VERSION}-linux.zip
ENV SONAR_RUNNER_HOME="/usr/src/app/sonar-scanner-${SONAR_SCANNER_VERSION}-linux"
ENV PATH=$PATH:$SONAR_RUNNER_HOME/bin
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
RUN curl -o ./sonarscanner.zip -L $SONAR_URL
RUN unzip sonarscanner.zip 
RUN rm sonarscanner.zip
RUN sed -i 's/use_embedded_jre=true/use_embedded_jre=false/g' $SONAR_RUNNER_HOME/bin/sonar-scanner

