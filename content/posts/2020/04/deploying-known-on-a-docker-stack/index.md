---
categories:
- Tech
- Tech
- Site
- Tech
coverImage: Known.png
date: "2020-04-28"
month: 2020-04
tags:
- docker-build
- docker-stack
- idno
- indieweb
- known
- php
- withknown
title: Deploying Known on a docker stack
year: 2020
---

To migrate my php applications that did not have a handy docker-compose available, I needed a vanilla setup for my stack-based docker environment. [Known](https://withknown.com/opensource/) is one of those apps and so the first step was to build that PHP environment.

**Setting up a Dockerhub repository and building a custom PHP image**

\[If you decide to use my image, you would not have to build this yourself. Skip ahead to the Deploying Known section\]

Most php based apps also need specific extensions built-in. While I am sure they're out there on the Docker hub repository, I was not able to easily find any images that met my specific needs \[php extensions for gd, zip, pdo\_mysql etc\]. So I went ahead and [setup my own repository on Docker Hub](https://hub.docker.com/r/sriperinkulam/php-7.4.3-apache-buster-plus).

Something I learnt today was that a docker stack only accepts pre-built images. Which essentially means you cannot use the regular [build command](https://docs.docker.com/engine/reference/commandline/build/) on the fly in your docker-compose file. A quick work-around to that is to build the image locally and then publish it to a public repository from where the stack can easily access it.

- Create a dockerfile: `sudo nano dockerfile`
- Copy over contents from [my dockerfile gist](https://gist.github.com/sriperinkulam/26d8702d946a8bad22d7623892be816c). Edit or update if you need any additional extensions. Do note that I am pulling a debian buster image here. An alpine image would be optimal but lets' run with this for now.
- Build the image locally: `docker build -t sriperinkulam/php-7.4.3-apache-buster-plus:latest .`

Edit the image and tag name as needed. If your gist file is defined correctly, the image should be ready in a few minutes. It took me a few iterations to get this working with all the extensions I needed and shouldn't give you any errors during the build process.

- Login to your Dockerhub repo: `docker login`
- Push your image over to your repository: `docker push sriperinkulam/php-7.4.3-apache-buster-plus:latest`
- Within a few minutes, your image should be available for easy fetch whenever needed!

 

**Setting up and deploying the Known install**

- Create a folder for the known installation:

`sudo mkdir known && cd known`

- Copy over my 'known.yml' gist from [here](https://gist.github.com/sriperinkulam/9ea9b57a052629ed5b75071c2bafdb00) and paste into a known.yml file.

`sudo nano known.yml`

This is where we use the image we built earlier! Make sure you update the passwords there-in.

- Create an 'app' folder. This is where we will copy in the core known package.

`sudo mkdir app && cd app`

[Marcus Povey](https://www.marcus-povey.co.uk/known/) does the heavy lifting of packaging the known install 'unofficially'. Download his latest pre-packaged release from [his portal](https://withknown.marcus-povey.co.uk/).

`wget https://withknown.marcus-povey.co.uk/<package>`

Finally unzip/untar the package.

- Step back into the main 'known' directory and deploy the stack that we defined in the known.yml file.

`cd ..`

`DOMAIN=known.domain.org SCHEME=https docker stack deploy -c known.yml known`

- Assuming you've already setup the traefik container, as mentioned in my [Jitsi post](https://srikanthperinkulam.com/2020/04/19/self-hosting-jitsi-video-conferencing/), you should now have Known up and running. Navigate to the domain and you should see the warmup page.
    
- Key in the db credentials that you setup in the _known.yml_ file. The database would need to be set as _mariadb,_ since that's how we've defined it in the known.yml file. Also make sure you have the _Uploads_ folder writable by www-data:
    

`sudo chown -R www-data /var/www/html/Uploads/`

Setup your user account and proceed with the regular administration controls!
