FROM node:16-alpine 

RUN apk add zsh rustup

RUN npm install -g serverless serverless-rust serverless-domain-manager 

ENTRYPOINT [ "/bin/zsh" ]
