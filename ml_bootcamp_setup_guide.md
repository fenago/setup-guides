#### Local Setup Guide

**Using docker**

1. Install Docker: https://docs.docker.com/engine/install/
2. Pull Docker Image: `docker pull fenago/ml-bootcamp`
3. Start Lab Environment: 

`docker run -d --restart=always --user root -p 80:80 -p 5000:5000 -p 6006:6006 -p 6007:6007 -p 9696:9696 --name bootcamp -e GRANT_SUDO=yes -e JUPYTER_ENABLE_LAB=yes fenago/ml-bootcamp jupyter lab --port 80 --allow-root`

Open `http://localhost:80` or `http://<DOCKER_HOST_IP>:80` in browser and login with `1234` password.


**Optional:**

* Restart Lab Environment: 

`docker restart bootcamp`

* Delete Lab Environment: 

```
docker stop bootcamp
docker rm bootcamp
```
