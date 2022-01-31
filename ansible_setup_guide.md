#### Ansible Local Setup Guide 

1. Install Docker https://docs.docker.com/get-docker/

2. Pull Lab Environment Image:

`docker pull fenago/ubuntu-ansible`

3. Run Lab Environment Image:

`docker run -d --privileged --restart=always --user root -p 80:80 -p 81:81 -p 3306:3306 -p 8080:8080 -p 8081:8081 -p 8443:8443 -p 5900:5900 --name ansible fenago/ubuntu-ansible`

*Password:* fenago

Open http://localhost:80 in Chrome browser


**Optional:**

- Restart lab environment: `docker restart ansible`
- Delete lab environment: `docker stop ansible && docker rm ansible`