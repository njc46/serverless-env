
build:
	docker build -f Dockerfile -t serverless-env:latest . --platform linux/amd64

tag:
	docker tag serverless-env:latest njc2/serverless-env:latest

push:
	docker push njc2/serverless-env:latest

publish: build tag push
