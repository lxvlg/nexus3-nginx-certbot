# Nexus 3 with SSL through nginx+certbot on docker-compose

`init-letsencrypt.sh` fetches and ensures the renewal of a Let’s
Encrypt certificate for one or multiple domains in a docker-compose
setup of Nexus 3 with an nginx proxy.

## Installation
1. [Install docker-compose](https://docs.docker.com/compose/install/#install-compose).

2. Clone this repository: `git clone https://github.com/Digithurst/nexus3-nginx-certbot.git .`

3. Modify configuration:
- Add domains and email addresses to init-letsencrypt.sh
- Replace all occurrences of example.org with primary domain (the first one you added to init-letsencrypt.sh) in data/nginx/app.conf

4. Run init the script:
```
chmod +x ./init-letsencrypt.sh
./init-letsencrypt.sh
```

5. Run server:
`docker-compose up`


## Acknowledgements

 * https://github.com/wmnnd/nginx-certbot
   [accompanying guide](https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71)
   
 * https://github.com/SergK/nexus3-ssl


