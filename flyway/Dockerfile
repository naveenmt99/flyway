FROM openjdk:8-jre

WORKDIR /flyway

ENV FLYWAY_VERSION 5.2.0

RUN curl -L https://repo1.maven.org/maven2/org/flywaydb/flyway-commandline/5.2.0/flyway-commandline-5.2.0-linux-x64.tar.gz -o flyway-commandline-5.2.0-linux-x64.tar.gz \
  && tar -xzf flyway-commandline-5.2.0-linux-x64.tar.gz --strip-components=1 \
  && rm flyway-commandline-5.2.0-linux-x64.tar.gz \
  && ln -s /flyway/flyway /usr/local/bin/flyway
ADD ./sql /flyway/sql

ENTRYPOINT ["flyway"]
CMD ["-?"]
