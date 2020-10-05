FROM ubuntu
MAINTAINER Ndaniell School 21
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y wget openssh-server ca-certificates postfix
RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh
RUN chmod 777 script.deb.sh
RUN ./script.deb.sh
RUN apt-get install -y gitlab-ce
RUN apt-get install -y tzdata
RUN apt-get clean
EXPOSE 443 80 22
ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null
# docker run --rm -it -p 8080:80 -p 8022:22 -p 8443:443 --privileged ex03
