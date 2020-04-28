FROM jenkins/jenkins:lts
USER root
RUN wget https://packages.microsoft.com/config/ubuntu/19.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN apt-get update && apt-get install apt-transport-https  dotnet-sdk-3.1 --assume-yes
VOLUME [ "/var/ssh_keys/" ]
#RUN apt-get update
#RUN apt-get install
USER jenkins
