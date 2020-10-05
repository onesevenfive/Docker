FROM ubuntu:16.04
MAINTAINER Ndaniell School 21
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y wget default-jre-headless
RUN mkdir minecraft
WORKDIR minecraft
RUN wget https://launcher.mojang.com/v1/objects/bb2b6b1aefcd70dfd1892149ac3a215f6c636b07/server.jar
RUN echo "eula=true" > eula.txt
RUN echo "spawn-protection=16\nmax-tick-time=60000\nquery.port=25565\ngenerator-settings=\nforce-gamemode=false\nallow-nether=true\nenforce-whitelist=false\ngamemode=survival\nbroadcast-console-to-ops=true\nenable-query=false\nplayer-idle-timeout=0\ndifficulty=easy\nbroadcast-rcon-to-ops=true\nspawn-monsters=true\nop-permission-level=4\npvp=true\nsnooper-enabled=true\nlevel-type=default\nhardcore=false\nenable-command-block=false\nnetwork-compression-threshold=256\nmax-players=20\nmax-world-size=29999984\nresource-pack-sha1=\nfunction-permission-level=2\nrcon.port=25575\nserver-port=25565\nserver-ip=\nspawn-npcs=true\nallow-flight=false\nlevel-name=world\nview-distance=10\nresource-pack=\nspawn-animals=true\nwhite-list=false\nrcon.password=\ngenerate-structures=true\nonline-mode=false\nmax-build-height=256\nlevel-seed=\nprevent-proxy-connections=false\nuse-native-transport=true\nmotd=A Minecraft Server\nenable-rcon=false" > server.properties
EXPOSE 25565
ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar nogui
