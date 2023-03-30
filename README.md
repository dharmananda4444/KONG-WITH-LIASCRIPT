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


<!--style="font-size:20px" --> 
**What is Kong?**

*	Kong Gateway is a lightweight, fast, and flexible cloud- native API gateway. An API gateway is a reverse proxy that lets you manage, configure, and route requests to your APIs.
*	Kong Gateway runs in front of any RESTful API and can be extended through modules and plugins. It’s designed to run on decentralized architectures, including hybrid-cloud and multi-cloud deployments.
*	Used to be called **Mashape** before 2015.

<!--style="font-size:20px" -->
**Problems**

* Repetition of common logic in all backend services
* We need to get an handle on API Consumers
* We need to stop bad consumers from DOSing our API
* We need better visibility of API Usage 
* We need real time information

<!--style="font-size:20px" -->
**Solutions**

* Move all Repeated logic outside the back end service
* Add a proxy in front of API’s (API Gateway)

### Software response to complex demand

![software response to complex demand](/images/kong2.png)

### Technology Evolution

![software response to complex demand](/images/kong3.png)



### Installation

* https://docs.konghq.com/gateway/latest/install-and-run/


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


## Architecture

### Kong Architecture


![kong architecture](/images/kong13.png)   


### Kong Internal Architecture    

![kong architecture](/images/kong14.png)


### Kong Deployment Architecture

![kong architecture](/images/kong15.png)


![kong architecture](/images/kong16.png)
 


### Kong Supports Hybrid Architecture

![kong architecture](/images/kong17.png)


### Kong supports Centralized or Decentralized    

![kong architecture](/images/kong18.png)


### Kong Features



**Authentication**

![kong Features](/images/kong20.png)


**Security**

![kong Features](/images/kong21.png)


**Traffic Control**

![kong Features](/images/kong22.png)


**Transformation**

![kong Features](/images/kong23.png)


**Logging**

![kong Features](/images/kong24.png)


## Kong Packages and modes 
    

 *  Free 
 *  Plus
 *  Enterprise




### Community Edition

![kong Community Edition](/images/kong25.png)


### Enterprise Edition    

![kong Enterprise Edition](/images/kong26.png)


## Kong Gateway Modules And Concepts

### Kong Gateway Modules    

<!--style="font-size:20px" -->
**Diagram 1:**

![kong Gateway Modules](/images/kong27.png)

<!--style="font-size:20px" -->
**Diagram 2:**

![kong Gateway Modules](/images/kong28.png)



### Kong Gateway Concepts    
    
![kong Gateway Concepts](/images/kong29.png)


| Concept/Feature           | Description                                                                                           | 
| ---------------------     |:------------------------------------------------------------------------------------------------------|
| Service                   | A Service object is the ID Kong Gateway uses to refer to the upstream APIs and microservices it manages.|
| Routes                    | Routes specify how (and if) requests are sent to their Services after they reach the API gateway. A single Service can have many Routes.|
| Consumer                  | Consumers represent end users of your API. Consumer objects let you control who can access your APIs. They also let you report on traffic using logging plugins and Kong Vitals.|
| Admin API                 |  Kong Gateway comes with an internal RESTful API for Kong Manager is the visual browser-based tool for monitoring and managing Kong Gateway.|
| Plugins                   | Plugins provide a modular system for modifying and controlling Kong Gateway’s capabilities. For example, to secure your API, you could require an access key, which you could set up using the key-auth plugin. Plugins provide a wide array of functionality, including access control, caching, rate limiting, logging, and more.|
| Rate Limiting plugin      | This plugin lets you limit the number of HTTP requests a client can make within a given period of time.|
| Rate Limiting Advanced plugin | The advanced version of this plugin also provides sliding window support, and the ability to limit by header and service.|
| Proxy Caching plugin      | This plugin provides a reverse proxy cache implementation. It caches response entities based on response code, content type, and request method for a given period of time.|
| Proxy Caching Advanced plugin | The advanced version of this plugin supports Redis and Redis Sentinel deployments.|
| Key Auth plugin           | This plugin lets you add key authentication (also known as an API key) to a Service or a Route.|
| Key Auth - Encrypted plugin |The advanced version of this plugin stores the API keys in an encrypted format within the Kong Gateway data store.|
| Load Balancing            | Kong Gateway provides two methods for load balancing: straightforward DNS-based or using a ring-balancer. In this guide, you’ll use a ring-balancer, which requires configuring upstream and target entities. With this method, the adding and removing of backend services is handled by Kong Gateway, and no DNS updates are necessary.|           
| User Authorization (RBAC) | Kong Gateway handles user authorization through role-based access control (RBAC). Once enabled, RBAC lets you create teams and admins and assign them granular permissions either within a workspace, or across workspaces.                        |   
| Dev Portal                | The Dev Portal provides a single source of truth for all developers to locate, access, and consume        services. |    

### Traffic Flow in Kong


![kong Gateway Concepts](/images/kong30.png)

### Kong Admin API


![kong Gateway Concepts](/images/kong31.png)

### Services and Routes

**Service** and **Route** objects let you expose your services to clients with Kong Gateway. When configuring access to your API, you’ll start by specifying a Service. In Kong Gateway, a Service is an entity representing an external upstream API or microservice — for example, a data transformation microservice, a billing API, and so on.


 ![services and routes](/images/kong32.png)

### Hands On with Admin API
    
This Hands-on Session will explain various component and functionality of the Kong Gateway by way of an example.

* To illustrate how the Admin API works, we will perform the following tasks
* Verify Kong Admin API is running
* Create & verify a managed **upstream API** (i.e. a service) called mockbin
* Create & verify a **route** /mock to this service
* Implement an **Authentication** plugin, so the service requires an API Key
* Create a **consumer** (i.e. a user) for the service with valid credentials

#### Services

 ![services](/images/kong33.png)


 ![services](/images/kong34.png)

#### Routes

 ![services](/images/kong35.png)


 ![services](/images/kong36.png)


#### Plugins

![services](/images/kong37.png)




