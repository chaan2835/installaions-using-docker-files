FROM ubuntu:latest

RUN apt update
RUN apt install openjdk-8-jdk openjdk-8-jre -y
RUN java -version
RUN mkdir /opt/tomcat/


WORKDIR /opt/tomcat
RUN apt install wget -y
RUN wget http://www-eu.apache.org/dist/tomcat/tomcat-9/v9.0.27/bin/apache-tomcat-9.0.27.tar.gz -P /tmp
RUN tar -xvzf apache-tomcat-9.0.27.tar.gz
RUN mv apache-tomcat-9.0.27/* /opt/tomcat/.

#WORKDIR /opt/tomcat/webapps
#RUN wget -O -L https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]

