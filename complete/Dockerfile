FROM java:8

ADD target/gs-rest-service-0.1.0.jar /gs-rest-service-0.1.0.jar
COPY run.sh /usr/local/bin/run.sh
RUN chmod +x /usr/local/bin/run.sh
COPY tomcat.yaml /etc/dd-agent/conf.d/tomcat.yaml
COPY install-dd.sh install-dd.sh
RUN DD_API_KEY=08f0919a2870755d36124ee54b1fd482 bash install-dd.sh
CMD ["run.sh"]
