# Day 1 of Docker Learnings

**Docker Workflow:**
* Docker Client -> Docker Host -> Registry
    - docker run, docker build, docker pull all are Docker Client.
    - Inside Docker Host - Docker daemon, Docker images, Docker containers are there.
    - Inside Registry Docker images are stored.
    
So, the workflow is - Docker Client gives the instruction, then Docker daemon performs operation based on that, e.g. - we want to run nginx container, so for that the client will send a request to daemon then daemon will look for images inside Docker host, if not found then it will pull the image from Registry and on the top of that image the container will be created.

**Docker Basic Commands:**
* Check all the namespaces: lsns
* Check the namespace for process id: lsns -t pid
* Run nginx container with name app1: docker run --name app1 nginx:latest
* Check all the containers(stopped and running both): docker ps -a
* Run nginx container with name app2 in the background(in detach mode): docker run -d --name app2 nginx:latest
* Stop a running container(app2): docker stop app2
* Run 10 containers at time: 
    - for i in {1..10}; do
    - docker run -d nginx:latest
    - done
* Stop all the running containers: docker stop $(docker ps -aq)
* Remove all the process/container(which are stopped): docker rm $(docker ps -aq)
* Remove container/process as soon as I stooped the running container container(app1): docker run --rm -d --name app1 nginx:latest
* Run a container and open port 8000 for user access: docker run --rm -d --name frontend -p 8000:80 ngin:latest
* Find the log files inside: /var/lib/docker/containes/xxxxx/xxxxx-json.log
* Check the logs jq format for better visualization: xxxxx-json.log | jq
* Check container(frontend) logs: docker inspect frontend