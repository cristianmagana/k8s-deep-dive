# ubuntu-sleeper image
# used to show how k8s object file can override docker image 

FROM ubuntu:latest

# Install
RUN \
   sed -i 's/#(.*multiverse$\)/\1/g' /etc/apt/sources.list && \
   apt-get update && \
   apt-get -y upgrade && \
   apt-get install -y build-essential && \
   apt-get install -y software-properties-common && \
   apt-get install -y byobu curl htop man unzip vim wget && \
   rm -rf /var/lib/apt/lists/*

# Add files
ADD roo/.bashrc /root/.bashrc
ADD root/.gitconfig /root/.gitconfig
ADD root/.scripts /root/.scripts

# Set environment variables
ENV HOME /root

# Define working directory
WORKDIR /root

# Set entrypoint
ENTRYPOINT ["sleep"]

# Define default command
CMD ["5"]