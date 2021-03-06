# Ghost Blog #
### Basic configuration for docker compose ###

This repository contains basic files to quickly deploy official ghost blog docker image using docker-compose.

### Basic usage ###

* Clone repository: `git clone git@github.com:theLesa/ghost-docker.git`
* Edit `docker-compose.yaml`: Choose your environment and external port (leave ghost port at default 2368)
* Set your url in config file
* Run `docker-compose up -d`

I use nginx as a reversy proxy, so I also added my config file for the blog:

* Choose your server name 
* Point your upstream to the port you put the docker container running
* Go to `ghost.localhost/ghost` and setup your account
* Enjoy experimenting with ghost

### Custom port ###
If you want to set custom port, rather than 2368:
* Set wanted port in the config file
* In nginx config file set that port to upstream
* In docker-compose set the port as external and leave 2368 as internal
Voila 

### Links ###

* [Ghost Blog](https://ghost.org/)
* [Ghost Documentation](https://ghost.org/docs/)
* [Ghost Concepts](https://ghost.org/docs/concepts/introduction/)