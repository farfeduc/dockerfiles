# Webstack

Docker nginx+php-fpm (based on alpine)

## Goal

This docker image was created to fit my needs.
Feel free to reuse or submit pull request.

## Build 

(optional, all my images are availaible on my docker-hub page)

As usual, just do (after downloading all the files in the folder webstack) : 

`docker build -t farfeduc/webstack .`
 
or 

`docker build -t farfeduc/webstack ./webstack/`
(if you are not in the folder where the Dockerfile is)

## Run

After the build or if you do not build, you do not need the webstack folder (in this one).

Then just do : 

`docker-compose up -d`

## Usage

Put all you php/html files inside the `www` folder.

You can add your custom nginx config in `sites-enabled`.

The applications then will be availaible on : http://localhost
