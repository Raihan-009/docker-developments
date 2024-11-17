img:=fastapi
tag:=v1.0
user:=poridhi
name:=api-container

build:
	docker build --platform linux/amd64 -t ${user}/${img}:${tag} .

build-ms:
	docker build --platform linux/amd64 -f Dockerfile.multistage -t ${user}/${img}:${tag} .

run:
	docker run --platform linux/amd64 --name ${name} -d -p 8000:8000 ${user}/${img}:${tag}

run-ms:
	docker run --platform linux/amd64 --name ${name}-multistage -d -p 8001:8000 ${user}/${img}:${tag}

clean:
	docker stop ${name}
	docker rm ${name}

clean-ms:
	docker stop ${name}-multistage
	docker rm ${name}-multistage