tag:=v0.2.0
image_name:=ssh-dind-server

build-ssh-container:
	@ docker build -f Dockerfile -t ${image_name}:${tag} .

run-ssh-container:
	@ docker run --privileged --name ${image_name} -p 2223:22 -d ${image_name}:${tag}

rm-ssh-container:
	@ docker stop ${image_name}
	@ docker rm -f ${image_name}

ip-ssh-container:
	@ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' ${image_name}

