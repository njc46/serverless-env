
build:
	docker build -f Dockerfile -t serverless-env:alpine . --platform linux/amd64

tag:
	docker tag serverless-env:alpine njc2/serverless-env:alpine

push:
	docker push njc2/serverless-env:alpine

publish: build tag push
