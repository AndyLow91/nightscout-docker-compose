# nightscout-docker-compose
A Simple, Scalable Docker-Compose Project for Nightscout

copy the repo to your local/cloud machine using:
```
git clone https://github.com/AndyLow91/nightscout-docker-compose.git
```

You can choose to rename the directory if you wish.<br>
Enter the directory and edit the .env file.

```
nano .env
```

I've added some variables to this file but you can edit it as you like.

```
# You can give your app a custom name
APP_NAME=Nightscout

# Create a pw for mongodb - do not make this the same as your API_SECRET
MONGO_PW=

# Create your API Secret
API_SECRET=

# The Port on the host machine where nightscout will be available
NS_PORT=

# The directory of the nightscout instalation
DIRECTORY=
```

Then you can simply run the docker container

```
docker compose up -d
```

The nightscout site will now be available at your.ip.address:[NS_PORT]
<br>
If you want to make this container available to be accessed externally to your network. You can use NGINX Proxy Manager. I Like to use the image from DockerHub - jc21/nginx-proxy-manager:latest
