FROM debian:latest

MAINTAINER wi_fil@yahoo.com.br

# instalando ferramentas iniciais
RUN apt-get update && apt-get install -y procps curl sudo gnupg2 net-tools ssh && apt-get clean

#baixando o pacote do nodejs 8.x e executando sudo -E bash -
RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -

#instalando o nodejs
RUN apt-get install -y nodejs build-essential python && apt-get clean

#instalando o angular4 + typescript
#ENV NODE_MODULES_PATH
#RUN /usr/lib/node_modules/@angular
#RUN chmod 777 -R /usr/lib/node_modules/@angular
#RUN npm install -g node-gyp node-sass

#Instalando o TS
RUN npm install -g typescript

EXPOSE 3000
VOLUME "/node-server"

CMD /bin/bash

# Para a máquina de desenvolvimento
# RUN mkdir angular-projects-dev

# Para criar o container sobre essa imagem:
# docker run -it -p 12345:3000 -name aves-server -v /teste:/node-server debian-nodejs-server:1.0 /bin/bash
