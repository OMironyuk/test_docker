FROM tomcat

RUN apt-get update && apt-get -y upgrade && apt-get -y install maven git
RUN mkdir -p /home/user/ && cd /home/user/ && git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN cd boxfuse-sample-java-war-hello && maven package
RUN cd target && cp hello-1.0.war /usr/local/tomcat/webapps

EXPOSE 8888
