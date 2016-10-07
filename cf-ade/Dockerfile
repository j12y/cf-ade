FROM phusion/passenger-full
MAINTAINER Jayson DeLancey <jayson.delancey@ge.com>

ENV HOME /root
ENV PREDIX https://api.system.aws-usw02-pr.ice.predix.io

# Install some Ubuntu dependencies
RUN apt-get update && apt-get install -y \
    wget \
    unzip

# Install Cloud Foundry CLI
RUN wget -O cf-cli.deb "https://cli.run.pivotal.io/stable?release=debian64&source=github" && dpkg -i cf-cli.deb

# Install Cloud Foundry UAAC
RUN gem install cf-uaac

WORKDIR /home/app
ENTRYPOINT ["bash"]
