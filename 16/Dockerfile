FROM snapcore/snapcraft:stable
RUN apt-get update
RUN apt install software-properties-common -y
RUN add-apt-repository -y ppa:jblgf0/python
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get dist-upgrade -y
RUN apt-get install -y libnss3-dev libgdk-pixbuf2.0-dev libgtk-3-dev libxss-dev libasound2 xvfb libsecret-1-dev build-essential python3.9
RUN curl -fsSL https://deb.nodesource.com/setup_16.x | bash -
RUN apt-get install nodejs -y
RUN apt-get update
RUN npm i -g npm@latest
RUN npm i -g prettier electron-mocha
RUN npm config set python "/usr/bin/python3.9"
COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]

CMD [ "node" ]
