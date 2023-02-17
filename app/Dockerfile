FROM node:19.0.0-alpine3.16 as builder
ADD . /app
WORKDIR /app
RUN npm install
ARG USER=userapp
ENV HOME /home/$USER
# install sudo as root
RUN apk add --update sudo
# add new user
RUN adduser -D $USER \
        && echo "$USER ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/$USER \
        && chmod 0440 /etc/sudoers.d/$USER

USER $USER
EXPOSE 3000
CMD ["node", "index.js"]
