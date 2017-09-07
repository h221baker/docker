from ubuntu:yakkety

RUN apt-get -y update

RUN apt-get install -y \
        python \
        git \
        python-pip

RUN apt-get install -y xmlto

RUN apt-get install -y \
        openjdk-8-jdk \
        git-core \
        gnupg \
        flex \
        bison \
        gperf \
        build-essential \
        zip \
        curl \
        zlib1g-dev \
        gcc-multilib \
        g++-multilib \
        libc6-dev-i386 \
        lib32ncurses5-dev \
        x11proto-core-dev \
        libx11-dev \
        lib32z-dev \
        ccache \
        libgl1-mesa-dev \
        libxml2-utils \
        xsltproc \
        unzip

RUN curl https://storage.googleapis.com/git-repo-downloads/repo > /bin/repo
RUN chmod 755 /bin/repo

RUN pip install sphinx

RUN git config --global user.email "jamzhao@gmail.com"
RUN git config --global user.name "James Z"

RUN mkdir -p /home/hjz/ && chown 1000:1000 /home/hjz/
