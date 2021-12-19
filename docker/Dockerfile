FROM ubuntu:21.10

RUN apt-get update -y \
    && apt-get install wget tar bzip2 libgl1 libgl1-mesa-dri nvidia-340 -y \
    && wget https://files.ilastik.org/ilastik-1.3.3post3-Linux.tar.bz2 \
    && tar xjf ilastik-1.*-Linux.tar.bz2

CMD cd ilastik-1.*-Linux \
    && ./run_ilastik.sh
