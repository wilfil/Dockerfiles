FROM debian:latest
MAINTAINER wi_fil@yahoo.com.br

# instalando ferramentas iniciais
RUN apt-get update &&\
    apt-get install -y procps curl sudo gnupg2 net-tools ssh build-essential &&\
    apt-get clean

# instalando o Apache2
RUN apt-get install apache2 &&\
    apt-get clean

#Expondo a porta 8080 do Apache2 no container
EXPOSE 8080

# Deixando um ponto de montagem disponível
VOLUME /var/www/

# Ao executar o container o serviço subirá e será feito um attach
CMD /etc/init.d/apache2 start &&\
    /bin/bash


