FROM node:16-bullseye
RUN apt-get update
RUN apt-get install -y libnss3-dev libgdk-pixbuf2.0-dev libgtk-3-dev libxss-dev libasound2 xvfb libsecret-1-dev snapd
RUN service snapd start
RUN systemctl start snapd.service
RUN snap install core
RUN snap install snapcraft --classic
RUN npm i -g npm@latest
RUN npm i -g prettier electron-mocha
COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["docker-entrypoint.sh"]

CMD [ "node" ]
