FROM ubuntu:14.04

RUN sudo apt-get update && sudo apt-get install -y curl && echo "root:toor" | chpasswd

#ENV MONGO_VERSION 3.0.8
RUN curl -SL "https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-3.0.8.tgz" | tar -xz -C /usr/local --strip-components=1

VOLUME /data/db

# Create a new user
RUN useradd -ms /bin/bash dba

# Set the working dir
WORKDIR /home/dba/src

# Start MongoDB and a terminal session on startup
# ENV MONGOD_START "mongod --fork --logpath /var/log/mongodb.log --logappend --smallfiles"
# ENTRYPOINT ["/bin/sh", "-c", "$MONGOD_START && su dev && /bin/bash"]
ENTRYPOINT ["/bin/sh", "-c", "/bin/bash"]
