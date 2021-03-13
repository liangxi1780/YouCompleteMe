# JHipster Registry

[![Build Status][travis-image]][travis-url]  [![Docker Pulls](https://img.shields.io/docker/pulls/jhipster/jhipster-registry.svg)](https://hub.docker.com/r/jhipster/jhipster-registry/)

This is the [JHipster](http://u.720life.cn/g/693d2091a36e92921a2709c0142488a4e511e3789a02d105a3356a22d8d1eddc)  registry service, based on [Spring Cloud Netflix](http://u.720life.cn/g/947e344a27d6d8817be37f0194b09df354861817a6bf36c77a9b933abdc46faa816a2bdc00d89e9d089772fa7b45fa7d  [Eureka](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461ed4d33589f67d5102f97e9939f62eb8e8ebcd8f5e78e2a246bea317be36e5b7)  and [Spring Cloud Config](http://u.720life.cn/g/947e344a27d6d8817be37f0194b09df354861817a6bf36c77a9b933abdc46faaa8ebdaf64ae60e9907eaa2e263c9a6f4 

Full documentation is available on the [JHipster documentation for microservices](http://u.720life.cn/g/693d2091a36e92921a2709c0142488a401b569480aecc1adce38b20e5fac1c05dd102e929a8c5856dcf490a50a3c280895928f5fb1291b16d1747a03f22b8753 

## Deploy to Heroku

Click this button to deploy your own instance of the registry:

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

There are a few limitations when deploying to Heroku.

* The registry will only work with [native configuration](http://u.720life.cn/g/693d2091a36e92921a2709c0142488a4c75a8f72aa341798e1ef9b0976c29b48be324cf457015933b340fa5ef680681490a8156df157ce12c251742032c4a62f)  (and not Git config).
* The registry service cannot be scaled up to multiple dynos to provide redundancy. You must deploy multiple applications (i.e. click the button more than once). This is because Eureka requires distinct URLs to synchronize in-memory state between instances.

## Running locally

To run the cloned repository;
* For development run `./mvnw -Pdev,webpack` to just start in development or run `./mvnw` and run `yarn && yarn start` for hot reload of client side code.
* For production profile run `./mvnw -Pprod`

[travis-image]: https://travis-ci.org/jhipster/jhipster-registry.svg?branch=master
[travis-url]: https://travis-ci.org/jhipster/jhipster-registry



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)