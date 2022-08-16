FROM anc2001/cs1230_env:graphical

ARG QT_PATH=/opt/Qt
ARG QT_VERSION=6.2.4
ENV PATH=${QT_PATH}/Tools/CMake/bin:${QT_PATH}/Tools/Ninja:${QT_PATH}/${QT_VERSION}/gcc_64/bin:$PATH 

RUN mkdir -p /home
WORKDIR /home
RUN git clone https://github.com/BrownCSCI1230/projects_2D.git

RUN cmake -DCMAKE_PREFIX_PATH=${QT_PATH}/${QT_VERSION}/gcc_64 -S /home/projects_2D -B /home/build
RUN cmake --build /home/build

ENV APP /home/build/2dprojects 