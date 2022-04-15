#FROM node:16-alpine AS node
FROM rustlang/rust:nightly

RUN ln -snf /usr/share/zoneinfo/Etc/UTC /etc/localtime \
    && echo "Etc/UTC" > /etc/timezone \
    && apt-get update \
    && apt-get upgrade -y 

#RUN build-essential \
#    cmake \
#    libxml2-dev \
#    libssl-dev \
#    git \
#    wget \
#    clang \
#    gcc \
#    g++ \
#    zlib1g-dev \
#    libmpc-dev \
#    libmpfr-dev \
#    libgmp-dev

RUN apt-get install -y make python3.7 python3-pip git zsh curl 

#RUN apt-get update \
#    && apt-get upgrade -y \
#    && apt-get install -y libstdc++ 

RUN apt-get update \
    && apt-get upgrade -y \
    && curl --silent --location https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs 

#COPY --from=node /usr/local/bin/node /usr/local/bin/node
#COPY --from=node /usr/local/bin/npm /usr/local/bin/npm

#RUN rustup toolchain install nightly-x86_64-unknown-linux-musl \
#    && rustup default nightly-x86_64-unknown-linux-musl

#RUN rustup component add rust-src --toolchain nightly-x86_64-unknown-linux-gnu

RUN rustup target add x86_64-unknown-linux-musl

RUN npm install -g serverless serverless-rust serverless-domain-manager  

ENTRYPOINT [ "/bin/zsh" ]
