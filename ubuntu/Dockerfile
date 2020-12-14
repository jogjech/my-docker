FROM ubuntu:20.04

# Give root user a password 123
RUN echo 'root:123' | chpasswd

# Add a user 'kevin' with password 123. To better hide the password, we should use ARG and pass in the password when building the image.
RUN useradd kevin -p 123

RUN apt-get update

# Install vim
RUN apt-get install -y vim

CMD ["sh"]

# Steps to run the docker file:
# docker build -t my-linux .
# docker run -d --name my-linux -it my-linux bash
# docker exec -it --user kevin a9 bash

# References:
# https://medium.com/@dayuoba/%E8%BF%98%E5%86%8D%E7%94%A8%E8%99%9A%E6%8B%9F%E6%9C%BA%E5%AE%89%E8%A3%85linux-docker%E5%B0%B1%E5%A4%9F%E4%BA%86-%E4%B8%8B-aa7b7907c08f
