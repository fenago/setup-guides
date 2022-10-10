#### Elasticsearch Local Setup Guide 

1. Install Docker https://docs.docker.com/get-docker/

2. Pull Lab Environment Image:

`docker pull fenago/ubuntu-elasticsearch`

3. Run Lab Environment Image:

`docker run -d --privileged --restart=always --user root -p 80:80 -p 9200:9200 -p 5601:5601 -p 5900:5900 --name elasticsearch fenago/ubuntu-elasticsearch`

*Password:* fenago

Open http://localhost:80 in Chrome browser


**Optional:**

- Restart lab environment: `docker restart elasticsearch`
- Delete lab environment: `docker stop elasticsearch && docker rm elasticsearch`