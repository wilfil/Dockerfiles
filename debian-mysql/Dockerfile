FROM debian:latest

MAINTAINER wi_fil@yahoo.com.br

# instalando ferramentas iniciais
RUN apt-get update && apt-get install -y procps curl sudo gnupg2 net-tools build-essential ssh && apt-get clean

# Downloading and installing mysql-server
RUN apt-get install -y mysql-server

#Expondo a porta 3306 do MySQL
EXPOSE 3306

#ao executar o container o serviço subirá

CMD /etc/init.d/mysql start && \
    /bin/bash

# ENTRYPOINT ["/usr/sbin/mysql"]
# CMD ["start"]

# Deixando um ponto de montagem disponível
VOLUME /shared-mysql


# Para criar o container sobre essa imagem:
# docker run -it -p 12345:3000 -name aves-server -v /teste:/node-server debian-nodejs-server:1.0 /bin/bash
# docker run -it -v /teste:/teste --rm imagem-debian-mysql:1.0 /bin/bash  (ele cria as pastas, se não houver, 
#   --rm mata o container caso eu dê o ctrl + D)
