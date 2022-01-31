#### Data Jungle (Local Setup Guide)

1. Install Docker https://docs.docker.com/get-docker/

2. Pull Lab Environment Image:

`docker pull fenago/data-jungle-centos`

3. Run Lab Environment Image:

`docker run -d --user root --restart=always -p 5901:5901 -p 80:80 -e NO_VNC_PORT=80 -e VNC_PW=fenago --name datajungle fenago/data-jungle-centos`

*Password:* fenago


Open http://localhost:80 in Chrome browser


**Optional:**

- Restart lab environment: `docker restart datajungle`
- Delete lab environment: `docker stop datajungle && docker rm datajungle`