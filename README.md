# Selenium Grid Using Docker
Running selenium parallel test using Docker with Selenium Grid

## Setting up Selenium Docker hub
* Pull Selenium-hub image using command ~  `Docker pull selenium/hub`
* Pull FireFox Debug image using command ~ `docker pull selenium/node-firefox-debug`
* Pull Chrome Debug image using below command ~ `docker pull selenium/node-chrome-debug`

## Running Selenium-hub
* Running Selenium-hub inside Docker ~ `docker run -d -P --name selenium-hub selenium/hub`
* Exposing Selenium-hub port ~ `docker run -d -p 4446:4444 --name selenium-hub -P selenium/hub` ~ here port `4446` can be accessed by external world.

## Linking Browser to Selenium-hub
* Linking chrome image to Selenium-hub ~ `docker run -d -P --link selenium-hub:hub  selenium/node-chrome-debug`
* Linking FireFox image to Selenium-hub ~ `docker run -d -P --link selenium-hub:hub  selenium/node-firefox-debug`

## Useful Docker commands:
* Check all available Docker Images ~ `docker images`
* To check status of all Containers ~ `docker ps -a`
* Check logs of specific Container ~ `docker logs ContainerId`
* Stop Container ~ `docker stop ContainerId`
* Start Container ~ `docker start ContainerId`
* Remove Container ~ `docker rm ContainerId`
* Remove Image ~ `docker rmi ImageId`
