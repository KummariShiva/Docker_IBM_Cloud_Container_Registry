Main Ojectives and Docker commands:
	
1)Pull an image from Docker Hub
	docker image
	docker pull hello-world
	
2)Run an image as a container using docker
	docker image
	docker rum hello-world
	docker ps -a
	docker container rm <container_id>
	docker ps -a
3)Build an image using a Dockerfile
	docker build . -t myimage:v1
	docker image
	docker run -dp 8080:8080 myimage:v1
	curl localhost:8080
	docker stop $(docker ps -q)
	docker ps
4)Push an image to IBM Cloud Container Registry
	ibmcloud target
	ibmcloud cr namespace
	ibmcloud cr region-set us-south
	ibmcloud cr login
	export MY_NAMESPACE=sn-labs-$USERNAME
	docker tag myimage:v1 us.icr.io/$MY_NAMESPACE/hello-world:1
	docker push us.icr.io/$MY_NAMESPACE/hello-world:1
	ibmcloud cr images
	ibmcloud cr images --restrict $MY_NAMESPACE
	