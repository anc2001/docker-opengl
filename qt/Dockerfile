FROM thewtex/opengl:ubuntu2004

ARG QT_VERSION=6.2.4
ARG QT_PATH=/opt/Qt

ENV ENV DEBIAN_FRONTEND=noninteractive \
    DEBCONF_NONINTERACTIVE_SEEN=true \
    QT_PATH=${QT_PATH} \
    PATH=${QT_PATH}/Tools/CMake/bin:${QT_PATH}/Tools/Ninja:${QT_PATH}/${QT_VERSION}/gcc_64/bin:$PATH

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install \ 
build-essential \
libgl1-mesa-dev \
git

COPY get_qt.sh /tmp/
RUN chmod +x /tmp/*
RUN /tmp/get_qt.sh