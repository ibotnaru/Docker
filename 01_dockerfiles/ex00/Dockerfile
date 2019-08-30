# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ibotnaru <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/08/26 15:18:24 by ibotnaru          #+#    #+#              #
#    Updated: 2019/08/26 15:48:16 by ibotnaru         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM			alpine
RUN				apk update && apk upgrade && apk add vim
ENTRYPOINT		["vim"]

#apk - same as apt-get(ubuntu)or brew just for alpine
#update and upgrade are defoult command that we shoud run everytime when we run linux system
#apk add - we install vim because we dont have it yet
#https://docs.docker.com/samples/library/alpine/

#specify the path of the file: ~/01_dockerfiles/ex00
#docker build -t ex00 .
