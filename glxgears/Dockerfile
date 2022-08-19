FROM docker-opengl:latest

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
  mesa-utils

ENV APP "glxgears"
