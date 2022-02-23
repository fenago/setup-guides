#### Data Jungle (Local Setup Guide)

1. Install Docker https://docs.docker.com/get-docker/

2. Pull Lab Environment Image:

`docker pull fenago/data-jungle-centos`

3. Run Lab Environment Image:

`docker run -d --restart=always --user root -p 80:80 -p 6006:6006 -p 6007:6007 --name datajungle -e GRANT_SUDO=yes -e JUPYTER_ENABLE_LAB=yes fenago/data-jungle-centos jupyter lab --port 80 --allow-root`

*Password:* 1234


Open http://localhost:80 in Chrome browser


**Optional:**

- Restart lab environment: `docker restart datajungle`
- Delete lab environment: `docker stop datajungle && docker rm datajungle`