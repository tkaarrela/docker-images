FROM ubuntu:git
RUN mkdir -p /opt/apps/app1
RUN git clone https://github.com/tkaarrela/app1 /opt/apps/app1

# declaring exposed ports. helpful for non Linux hosts. add "-P" flag to your "docker run" command to automatically expose them and "docker ps" to discover them.
EXPOSE 9000 9001
VOLUME ["/backend"]
CMD cd /opt/apps/app1/api && ./gradlew clean server
