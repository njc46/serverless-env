# Rust base image
FROM rustlang/rust:nightly

# Update and upgade
RUN ln -snf /usr/share/zoneinfo/Etc/UTC /etc/localtime \
    && echo "Etc/UTC" > /etc/timezone \
    && apt-get update \
    && apt-get upgrade -y 

# Install Python
RUN apt-get install -y make python3.7 python3-pip 

# Install helpful
RUN apt-get install -y git zsh curl 

# Install musl-tools
RUN apt-get install -y musl-tools

# Install Node
RUN apt-get update \
    && apt-get upgrade -y \
    && curl --silent --location https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs 

# Add musl target
RUN rustup target add x86_64-unknown-linux-musl

# Instal serverless
RUN npm install -g serverless serverless-rust \
    serverless-domain-manager serverless-wsgi \
    serverless-python-requirements

# zsh to the max
ENTRYPOINT [ "/bin/zsh" ]
