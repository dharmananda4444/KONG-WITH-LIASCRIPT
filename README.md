<!--
author:   Dharmananda G

email:    dharmananda@swayaan.com

version:  3.0

language: en

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

import: https://raw.githubusercontent.com/LiaTemplates/algebrite/0.2.1/README.md 
        https://raw.githubusercontent.com/liaTemplates/TextAnalysis/main/README.md

-->
# KONG API-GATEWAY

    ![kong logo](/images/kong.jpg)

## Introduction to Kong APIGateway

    ![kong logo](/images/kong.jpg)

### What is Kong?
*	Kong Gateway is a lightweight, fast, and flexible cloud- native API gateway. An API gateway is a reverse proxy that lets you manage, configure, and route requests to your APIs.
*	Kong Gateway runs in front of any RESTful API and can be extended through modules and plugins. It’s designed to run on decentralized architectures, including hybrid-cloud and multi-cloud deployments.
*	Used to be called **Mashape** before 2015.

### Software response to complex demand

    ![software response to complex demand](/images/kong2.png)

### Technology Evolution

    ![software response to complex demand](/images/kong3.png)

### Problems and Solutions

**Problems**

* Repetition of common logic in all backend services
* We need to get an handle on API Consumers
* We need to stop bad consumers from DOSing our API
* We need better visibility of API Usage 
* We need real time information

**Solutions**

* Move all Repeated logic outside the back end service
* Add a proxy in front of API’s (API Gateway)


## Why Kong?

    ![why kong](/images/kong1.png)


* Open Source - community edition
* Built on top of NGINX + Lua + LuaJIT
* Light Weight
* Minimal latency
* Supports multiple installations options
* Cloud Native & Platform Agnostic
* Supports Hybrid Architecture from Monolithic to Microservices
* Extensible with Plugins
* 15M+ Download since 2015 and huge community
* Also supports Enterprise edition and support for advanced use- case


### Kong Example

    ![kong example](/images/kong4.png)

### Kong Interaction

    ![kong interaction](/images/kong5.png)

### Current Architecture vs Kong Architecture

    ![current architecture](/images/kong6.png) ![kong architecture](/images/kong7.png)

* In current architecture, for each api's we need specify and add plugins like basic-authentication,loggging, caching and rate limiting.
* In Kong architecture, there is a kong api gateway where this as all the plugins required by the api's where need not to add plugins for each api's.      

### Enabling Microservice Architectures

    ![enabling microservice](/images/kong8.png)

### Kong Plugins

    ![kong plugins](/images/kong10.png)
    

* Kong has wide variety of plugins in it from basic authentication to tokenized authentication.
* Most of the plugins are free to use where as some of the plugins are available at enterprised version.
* It Supports multiple installations options.     

### Platform Agnostic

    ![kong plugins](/images/kong12.png)


* Kong is platform agnostic which means it can be installed and run in any platform like docker, kubernetes, amazon, ubuntu, debian etc..










 

