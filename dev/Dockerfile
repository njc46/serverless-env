FROM rustlang/rust:nightly

RUN ln -snf /usr/share/zoneinfo/Etc/UTC /etc/localtime \
    && echo "Etc/UTC" > /etc/timezone \
    && apt-get update \
    && apt-get upgrade -y 

RUN apt-get install -y make python3.7 python3-pip git zsh curl 

RUN apt-get update \
    && apt-get upgrade -y \
    && curl --silent --location https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs 

RUN rustup target add x86_64-unknown-linux-musl

RUN npm install -g serverless serverless-rust serverless-domain-manager  

ENTRYPOINT [ "/bin/zsh" ]
