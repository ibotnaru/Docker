# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ibotnaru <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/08/26 15:49:21 by ibotnaru          #+#    #+#              #
#    Updated: 2019/08/26 16:15:09 by ibotnaru         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM		debian
ENV			TS3SERVER_LICENSE=accept
			#with ENV TS3SERVER_LICENSE=accept we get a licence first

RUN			apt-get update && apt-get upgrade -y
			#-y - (yes) by default

RUN			apt-get install -y wget bzip2
			#install the package

RUN			wget http://dl.4players.de/ts/releases/3.0.13.4/teamspeak3-server_freebsd_amd64-3.0.13.4.tar.bz2
			#download teamspeak3-server (file) from their website

RUN			tar -xvf teamspeak3-server_freebsd_amd64-3.0.13.4.tar.bz2
			#unzip(extract) the file we just downloaded

WORKDIR		teamspeak3-server_freebsd_amd64
			#create a folder where we keep the unziped file
			#specify the work folder

ENTRYPOINT	sh ts3serer_minimal_runscript.sh
			#inside of the workfolder we gonna have .sh file which we need to run

#~/01_dockerfiles/ex01	docker build -t ex01 .
