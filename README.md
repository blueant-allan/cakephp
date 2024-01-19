# Docker Development Container for CakePHP

A docker container development for CakePHP.

## Supported Versions

- CakePHP 5.x with PHP version 8.2.2 and Mailpit support
- CakePHP 4.x with PHP version 8.2.2


## Container details

- Ubuntu operating system
- Nginx Web server
- PHP FPM


## Compile the docker file

```
cd to docker file path

i.e 5.x/8.2
docker build -t cakephp5_php8.2-image -f Dockerfile.dev .
```


## Push docker image to  Docker Hub

```
# create a tag
docker tag cakephp5_php8.2-image  blueantallan/cakephp5_php8.2-image


# push image to docker hub
docker push blueantallan/cakephp5_php8.2-image
```


## Test the image

```
docker run -p 8042:80 -dit --name cakephp5-app --mount type=bind,source="$(pwd)",target=/var/www/html cakephp5_php8.2-image
```
