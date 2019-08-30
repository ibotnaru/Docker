# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ibotnaru <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/08/26 16:42:39 by ibotnaru          #+#    #+#              #
#    Updated: 2019/08/26 17:13:24 by ibotnaru         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

#https://gitlab.com/gitlab-org/gitlab-ce
#https://about.gitlab.com/install/#debian

FROM				debian
					#when we pull it the container is being created
RUN					apt-get update && apt-get upgrade -y
RUN					apt-get install -y openssh-server wget ca-certificates
RUN					apt-get install -y postfix
RUN					wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh
					#https://about.gitlab.com/install/#debian -installation for debian
RUN					chmod 777 script.deb.sh
					#chmod 777 gives all the permitions to the script script.deb.sh
RUN					./script.deb.sh 
					#run the script
#RUN					apt-get install -y gitlab-ce
RUN					apt-get update && apt-get install -y tzdata
RUN					apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
EXPOSE				443 80 22
ENTRYPOINT			(/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-stl reconfigure && tail -f /dev/null
