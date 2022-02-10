FROM ubuntu

RUN apt-get update -y && apt-get upgrade -y
RUN apt install nginx -y && apt install git-all -y 
RUN apt install nodejs -y
RUN apt install npm -y
VOLUME test:/app
RUN git config --global user.email "guillaume.sonnery@ecole-isitech.fr"
RUN git config --global github.token mytoken "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"
RUN mkdir meetme
RUN git clone https://github.com/GuiguiSo/test-docker.git /app/meetme
WORKDIR /app/meetme
RUN npm install
RUN npm run build
RUN cp -r build/* /var/www/html
RUN service nginx start
EXPOSE 80/tcp
EXPOSE 80/udp 





 