# Docker Projects
------------------------------

10+ Docker projects will be added to this repository.

**If the `docker-compose up` throws a permission denied error, like this**

`permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "..." : dial unix /var/run/docker.sock: connect: permission denied`

Then either change the permission of the /var/run/docker.sock file by using `sudo chmod 666 /var/run/docker.sock` (not the best practice) or change the ownership of the file using `sudo chown $USER /var/run/docker.sock`

