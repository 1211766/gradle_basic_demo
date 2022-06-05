# Download base image ubuntu 18.04
FROM ubuntu:18.04

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive

# Install apt-get
RUN apt-get update -y

#Install java-jdk11
RUN apt-get install openjdk-11-jdk-headless -y

# Copy the jar file into the container
COPY build/libs/basic_demo-0.1.0.jar .

# Expose Port
EXPOSE 59001

# Execute server
CMD java -cp basic_demo-0.1.0.jar basic_demo.ChatServerApp 59001