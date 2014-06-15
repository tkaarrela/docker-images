FROM tkaarrela/ubuntu:docker
RUN mkdir -p /opt/java
RUN wget -O /opt/java/jdk-8u5-linux-x64.tar.gz --no-check-certificate -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u5-b13/jdk-8u5-linux-x64.tar.gz 
RUN tar -zxvf /opt/java/jdk-8u5-linux-x64.tar.gz
ENV JAVA_HOME /opt/java/jdk1.8.0_05
ENV PATH $JAVA_HOME/bin:$PATH