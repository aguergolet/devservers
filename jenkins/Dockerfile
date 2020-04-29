FROM jenkins/jenkins:lts
USER root
RUN wget https://packages.microsoft.com/config/ubuntu/19.10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
RUN dpkg -i packages-microsoft-prod.deb
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get update && apt-get install apt-transport-https  dotnet-sdk-3.1 --assume-yes
RUN apt-get  install nodejs --assume-yes
RUN apt-get install gcc g++ make --assume-yes
VOLUME [ "/jenkins/" ]
USER jenkins
