FROM debian
MAINTAINER Ndaniell School 21
ENV TS3SERVER_LICENSE=accept
WORKDIR /home/teamspeak
EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011
RUN apt-get update
RUN apt-get upgrade
RUN apt-get install wget bzip2 -y
RUN wget https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_amd64-3.11.0.tar.bz2
RUN tar -xvf teamspeak3-server_linux_amd64-3.11.0.tar.bz2
RUN rm teamspeak3-server_linux_amd64-3.11.0.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
ENTRYPOINT sh ts3server_minimal_runscript.sh
# docker run --rm -p 9987:9987/udp -p 30033:30033 -p 10011:10011 ex01
