# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ibotnaru <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/08/26 16:23:02 by ibotnaru          #+#    #+#              #
#    Updated: 2019/08/30 12:00:55 by ibotnaru         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM				ruby
RUN					apt-get update && apt-get upgrade -y
RUN					apt-get install nodejs -y
RUN					gem install rails
RUN					mkdir -p /opt/app
					#make a folder, -p - make another folder inside of a new folder, /opt/app - name of the folders

ONBUILD WORKDIR		/opt/app
ONBUILD ADD			. /opt/app
ONBUILD EXPOSE		3000
ONBUILD RUN			bundle install && rake db:from && rake db:to
					#bundle is the same as apt-get just for ruby on rails
