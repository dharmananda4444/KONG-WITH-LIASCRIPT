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

<hr>
<br>
<br>


![kong logo](/images/kong.jpg)<!--style="width:400%" -->

## Introduction to Kong APIGateway

<br>

<!--style="font-size:20px" --> 
**What is Kong?**

*	Kong Gateway is a lightweight, fast, and flexible cloud- native API gateway. An API gateway is a reverse proxy that lets you manage, configure, and route requests to your APIs.
*	Kong Gateway runs in front of any RESTful API and can be extended through modules and plugins. It’s designed to run on decentralized architectures, including hybrid-cloud and multi-cloud deployments.
*	Used to be called **Mashape** before 2015.

<br>

<!--style="font-size:20px" -->
**Problems**

* Repetition of common logic in all backend services
* We need to get an handle on API Consumers
* We need to stop bad consumers from DOSing our API
* We need better visibility of API Usage 
* We need real time information

<br>

<!--style="font-size:20px" -->
**Solutions**

* Move all Repeated logic outside the back end service
* Add a proxy in front of API’s (API Gateway)

### Software response to complex demand

<br>

![software response to complex demand](/images/kong2.png)

### Technology Evolution

<br>

![software response to complex demand](/images/kong3.png)



## Why Kong?

<br>

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

<br>

![kong example](/images/kong4.png)

### Kong Interaction

<br>

![kong interaction](/images/kong5.png)

* Kong Gateway can simplify scaling microservices by being the abstraction layer that routes clients to your existing upstream service while building a new service. 
*   It also applies a common policy for each request and response no matter where the target service is.


### Current Architecture vs Kong Architecture

<br>

![current architecture](/images/kong6.png) ![kong architecture](/images/kong7.png)




* In current architecture, for each api's we need specify and add plugins like basic-authentication,loggging, caching and rate limiting.
* In Kong architecture, there is a kong api gateway where this as all the plugins required by the api's where need not to add plugins for each api's.      

### Enabling Microservice Architectures

<br>

![enabling microservice](/images/kong8.png)

### Kong Plugins

<br>

![kong plugins](/images/kong10.png)
    


* Kong has wide variety of plugins in it from basic authentication to tokenized authentication.
* Most of the plugins are free to use where as some of the plugins are available at enterprised version.
* It Supports multiple installations options.     

### Platform Agnostic

<br>

![kong plugins](/images/kong12.png)


* Kong is platform agnostic which means it can be installed and run in any platform like docker, kubernetes, amazon, ubuntu, debian etc..


## Kong Architecture

<br>

![kong architecture](/images/kong13.png)   


### Kong Internal Architecture 

<br>

![kong architecture](/images/kong14.png)


### Kong Deployment Architecture

<br>

![kong architecture](/images/kong15.png)



![kong architecture](/images/kong16.png)



### Kong Supports Hybrid Architecture

<br>

![kong architecture](/images/kong17.png)


### Kong supports Centralized or Decentralized    

<br>

![kong architecture](/images/kong18.png)


### Kong Features

<br>

<!--style="font-size:20px" -->
**Authentication**

![kong Features](/images/kong20.png)

<br>

<!--style="font-size:20px" -->
**Security**

![kong Features](/images/kong21.png)

<br>

<!--style="font-size:20px" -->
**Traffic Control**

![kong Features](/images/kong22.png)

<br>

<!--style="font-size:20px" -->
**Transformation**

![kong Features](/images/kong23.png)

<br>

<!--style="font-size:20px" -->
**Logging**

![kong Features](/images/kong24.png)


## Kong Packages and modes 
    
<!--style="font-size:20px" -->
 *  **Free** 
 *  **Plus**
 *  **Enterprise**




### Community Edition

![kong Community Edition](/images/kong25.png)


### Enterprise Edition    

![kong Enterprise Edition](/images/kong26.png)


## Kong Gateway Modules And Concepts

### Kong Gateway Modules  

<br>

<!--style="font-size:20px" -->
**Diagram 1:**

![kong Gateway Modules](/images/kong27.png)

<br>

<!--style="font-size:20px" -->
**Diagram 2:**

![kong Gateway Modules](/images/kong28.png)

<br>

**Kong Manager** is the graphical user interface (GUI) for Kong Gateway. It uses the Kong Admin API under the hood to administer and control Kong Gateway.

Here are some of the things you can do with Kong Manager:

* Create new Routes and Services
* Activate or deactivate plugins with a couple of clicks
* Group your teams, services, plugins, consumer management, and everything else exactly how you want them
* Monitor performance: visualize cluster-wide, workspace-level, or object-level health using intuitive, customizable dashboards.

### Kong Gateway Concepts    
    
<br>

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

<br>

![kong Gateway Concepts](/images/kong30.png)

### Kong Admin API

<br>

![kong Gateway Concepts](/images/kong31.png)

### Services and Routes

<br>

**Service** and **Route** objects let you expose your services to clients with Kong Gateway. When configuring access to your API, you’ll start by specifying a Service. In Kong Gateway, a Service is an entity representing an external upstream API or microservice — for example, a data transformation microservice, a billing API, and so on.

<br>

 ![services and routes](/images/kong32.png)

### Admin API

<br>
    
This Hands-on Session will explain various component and functionality of the Kong Gateway by way of an example.

* To illustrate how the Admin API works, we will perform the following tasks
* Verify Kong Admin API is running
* Create & verify a managed **upstream API** (i.e. a service) called mockbin
* Create & verify a **route** /mock to this service
* Implement an **Authentication** plugin, so the service requires an API Key
* Create a **consumer** (i.e. a user) for the service with valid credentials

#### Services

<br>

 ![services](/images/kong33.png)


 ![services](/images/kong34.png)

#### Routes

<br>

 ![routes](/images/kong35.png)


 ![routes](/images/kong36.png)


#### Plugins

<br>

![plugins](/images/kong37.png)


![plugins](/images/kong38.png)

#### Authentication

<br>

* API gateway authentication is an important way to control the data that is allowed to be transmitted using your APIs. Basically, it checks that a particular consumer has permission to access the API, using a predefined set of credentials.
* Kong Gateway has a library of plugins that provide simple ways to implement the best known and most widely used methods of API gateway authentication. Here are some of the commonly used ones:

    * API gateway authentication methods
    
    * Basic Authentication
    * Key Authentication
    * OAuth 2.0 Authentication
    * LDAP Authentication Advanced
    * OpenID Connect

#### Kong Plugin Hub 

<br>

![Kong Plugin Hub](/images/kong39.png)


#### Consumer

<br>

![Kong Plugin Hub](/images/kong40.png)


![Kong Plugin Hub](/images/kong41.png)


#### Proxy Caching

<br>

 The Proxy Cache plugin accelerates performance by caching responses based on configurable response codes, content types, and request methods.

* Installing the Proxy plugin globally means every proxy request to Kong Gateway will potentially be cached.
* The Proxy Cache plugin is installed by default on Kong Gateway, and can be enabled by sending a POST request to the plugins object on the Admin API
* If configuration was successful, you will receive a 201 response code.
* You can check that the Proxy Cache plugin is working by sending GET requests and examining the returned headers.

<br>

| STATE |DESCRIPTION                                                                                                                                        |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Miss    | The request could be satisfied in cache, but an entry for the resource was not found in cache, and the request was proxied upstream.               |
| Hit     | The request could be satisfied in cache, but an entry for the resource was not found in cache, and the request was proxied upstream.               |
| Refresh | The resource was found in cache, but could not satisfy the request, due to Cache-Control behaviors or reaching its hard-coded cache_ttl threshold. |
| Bypass  | The request could not be satisfied from cache based on plugin configuration.                                                                       |


### Installation of Docker and Configuring Admin API (Hands on)

<br>

<!--style="font-size:20px" -->
**1. Install docker on ubuntu machine**

 Reference link: https://docs.docker.com/engine/install/ubuntu/ 

* Make sure that docker is installed properly and running before proceeding to next step.

<br>

 <!--style="font-size:20px" -->
**2. Create a docker network**   

``` 
$ docker create network kong-net  
```
<br>


<!--style="font-size:20px" -->
**3. Install Kong in DB-less mode**

<br>

**Docker run command for Kong DB-less**

```
 $ docker run -d --name kong-dbless \
 --network=kong-net \
 -v "$(pwd):/kong/declarative/" \
 -e "KONG_DATABASE=off" \
 -e "KONG_PROXY_ACCESS_LOG=/dev/stdout" \
 -e "KONG_ADMIN_ACCESS_LOG=/dev/stdout" \
 -e "KONG_PROXY_ERROR_LOG=/dev/stderr" \
 -e "KONG_ADMIN_ERROR_LOG=/dev/stderr" \
 -e "KONG_ADMIN_LISTEN=0.0.0.0:8001, 0.0.0.0:8444 ssl" \
 -p 8000:8000 \
 -p 8443:8443 \
 -p 127.0.0.1:8001:8001 \
 -p 127.0.0.1:8444:8444 \
 kong:latest 
```  

<br>

**Test the Admin API base URL in the browser**


```
http://localhost:8001/
https://localhost:8444/
```
<br>

**Kill and remove the Container if needed**


```
$ docker ps
$ docker kill kong-dbless
$ docker rm kong-dbless
```

<br>

<!--style="font-size:20px" -->
**4. Install Kong in DB mode**

<br>

**Install Postgres DB**

```
$ docker run -d --name kong-database --network=kong-net -p 
5432:5432 -e "POSTGRES_USER=kong" -e "POSTGRES_DB=kong" -e 
"POSTGRES_PASSWORD=kong"  postgres:9.6

$ docker ps
$ docker images
```

* both kong and postgres images will be listed on doing $ docker images.

<br>

**Prepare the DB for kong**

```
$ docker run --rm --network=kong-net -e "KONG_DATABASE=postgres" 
-e "KONG_PG_HOST=kong-database" -e "KONG_PG_USER=kong" -e 
"KONG_PG_PASSWORD=kong" kong:latest kong migrations bootstrap
```

**Start the Kong API Gateway**

```
$ docker run -d --name kong --network=kong-net 
-e "KONG_DATABASE=postgres" 
-e "KONG_PG_HOST=kong-database" -e "KONG_PG_USER=kong" 
-e "KONG_PG_PASSWORD=kong" 
-e "KONG_PROXY_ACCESS_LOG=/dev/stdout" 
-e "KONG_ADMIN_ACCESS_LOG=/dev/stdout" 
-e "KONG_PROXY_ERROR_LOG=/dev/stderr" 
-e "KONG_ADMIN_ERROR_LOG=/dev/stderr" 
-e "KONG_ADMIN_LISTEN=0.0.0.0:8001, 0.0.0.0:8444 ssl" 
-p 8000:8000 -p 8443:8443 
-p 127.0.0.1:8001:8001 -p 127.0.0.1:8444:8444 kong:latest
```

**Test the Kong Admin API url in terminal**

```
curl http://localhost:8001/
```
<br>

<!--style="font-size:20px" -->
**Kong default ports**
By default, Kong listens on the following ports:

**Kong api gateway proxy ports :**

**8000**: listens for incoming HTTP traffic from your clients, and forwards it to your upstream services.

**8443**: listens for incoming HTTPS traffic. This port has a similar behavior to 8000, except that it 

**Kong Admin API ports (Used for configuring and updating conf configuration of services, routes etc) :**

**8001**: Admin API listens for calls from the command line over HTTP.
expects HTTPS traffic only. This port can be disabled via the configuration file.

**8444**: Admin API listens for HTTPS traffic

<br>

<!--style="font-size:20px" -->
**Lifecycle commands**

**Note:** If you are using Docker, exec into the Docker container to use these commands.

<br>

**Get into container using the exec command:**

```
$ docker exec -it [docker_id] bash
```

**Stop Kong Gateway using the stop command:**

```
$ kong stop
```

**Reload Kong Gateway using the reload command:**

```
$ kong reload
```


**Start Kong Gateway using the start command:**

```
$ kong start
```


### Configuring a Service in Admin API (Hands on)  
                                

<!--style="font-size:20px" -->
**1. Add Service**

```
curl -i -X POST --url http://localhost:8001/services/ 
--data name=example-service --data 
url=http://mockbin.org
```

**Verify**

```
curl  http://localhost:8001/services/example-service
```


<!--style="font-size:20px" -->
**2. Add Route**

```
curl -i -X POST http://localhost:8001/services/
example-service/routes \
  --data 'paths[]=/mock' \
  --data name=mocking
```

**Verify**

```
curl http://localhost:8001/routes
```

<br>

<!--style="font-size:20px" -->
**3. Verify the api gateway endpoint using kong proxy port 8000**


```
curl http://localhost:8000/mock/request
```

<br>

<!--style="font-size:20px" -->
**4. Configure  Plugin**

**1.Configure key-auth plugin for example-service**

```
curl -i -X POST --url http://localhost:8001/services/example-service/plugins/ --data name=key-auth
```

**2.Verify**

```
curl http://localhost:8000/mock/request
```

<!--style="color:red" --> * Should get error as No API key found

<br>

<!--style="font-size:20px" -->
**5. Adding Consumer**

**1. Create a consumer through Admin API**

```
curl -i -X POST --url http://localhost:8001/consumers/ --data "username=consumer1"
```

**2. Verify**

```
curl http://localhost:8001/consumers
```

**3. Provision key credentials for your Consumer**

```
curl -i -X POST  --url http://localhost:8001/consumers/consumer1/key-auth/ --data "key=myconsumersecurekey123"
```

**4. Verify that your Consumer credentials are valid by accessing the /mock endpoint using the above key**

```
curl -i http://localhost:8000/mock/request --header "apikey: myconsumersecurekey123"
```
<!--style="color:green" -->* Should get valid response

```
curl -i http://localhost:8000/mock/request --header "apikey: wrongkey"
```

<!--style="color:red" -->* Should get 401 unauthorized

<br>

**Verify all Items with the Admin API**

```
curl http://localhost:8001/services
curl http://localhost:8001/routes
curl http://localhost:8001/consumers
curl http://localhost :8001/plugins
```

**How to DELETE a route**

```
curl -X DELETE http://localhost:8001/services/example-service/routes/<id-of-the-route>
```

### API Request Flow and Plugins


![Kong Plugin Hub](/images/kong42.png)


![Kong Plugin Hub](/images/kong43.png)


![Kong Plugin Hub](/images/kong44.png)


![Kong Plugin Hub](/images/kong45.png)


### API Request flow 

<br>

**Rate Limiting**

* Kong’s Rate Limiting plugin lets you restrict how many requests your upstream services receive from your API consumers, or how often each user can call the API.

* Rate limiting protects the APIs from accidental or malicious overuse. Without rate limiting, each user may request as often as they like, which can lead to spikes of requests that starve other consumers. After rate limiting is enabled, API calls are limited to a fixed number of requests per second.

<br>

**Proxy Caching**

* Kong Gateway delivers fast performance through caching. The Proxy Caching plugin provides this fast performance using a reverse proxy cache implementation. It caches response entities based on the request method, configurable response code, content type, and can cache per Consumer or per API.

* Cache entities are stored for a configurable period of time. When the timeout is reached, the gateway forwards the request to the Upstream, caches the result and responds from cache until the timeout. The plugin can store cached data in memory, or for improved performance, in Redis.

* Use proxy caching so that Upstream services are not bogged down with repeated requests. With proxy caching, Kong Gateway can respond with cached results for better performance.

<br>

**Upstreams and UpStream Targets**

<br>

![Kong Plugin Hub](/images/kong46.png)


### Kong Manager

<br>

![Kong Plugin Hub](/images/kong47.png)

<br>

**Kong Manager** is the graphical user interface (GUI) for Kong Gateway. It uses the Kong Admin API under the hood to administer and control Kong Gateway.

Here are some of the things you can do with Kong Manager:

* Create new Routes and Services
* Activate or deactivate plugins with a couple of clicks
* Group your teams, services, plugins, consumer management, and everything else exactly how you want them
* Monitor performance: visualize cluster-wide, workspace-level, or object-level health using intuitive, customizable dashboards.

<br>

![Kong Plugin Hub](/images/kong48.png)

### Plugins (Hands on)

<!--style="font-size:20px" -->
**Setting Up Proxy Cache Plugin**

<br>

**1. Configure the Proxy Cache plugin at global level**

```
curl -X POST http://localhost:8001/plugins \
--data name=proxy-cache \
--data config.content_type="application/json; charset=utf-8" \
--data config.cache_ttl=30 \
--data config.strategy=memory
```
<br>

**2. Validating Proxy Caching**

```
curl http://localhost:8000/mock/request
```
<br>

**In particular, pay close attention to the values of** 

* X-Cache-Status 
* X-Kong-Upstream-Latency
* X-Kong-Proxy-Latency

<br>

**No Cache invoked actual backend api**

* X-Cache-Status : **Bypass**
* X-Kong-Upstream-Latency: >200ms
* X-Kong-Proxy-Latency : 10ms

<br>

**Cached scenario**

* X-Cache-Status : **Hit**
* X-Kong-Upstream-Latency: 0s
* X-Kong-Proxy-Latency :  less than previous value

<br>

**Note:** If you want to clear the cache manually you can do it using Admin API

```
curl -X DELETE http://localhost:8001/proxy-cache
```

<!--style="font-size:20px" -->
**Configure Upstream Services**

<br>

**1. Create Upstream** 

```
curl -X POST http://localhost:8001/upstreams \
--data name=example-upstream
```

<br>

**2. We need to update the example-service with above created upstream**

```
curl -X PATCH http://localhost:8001/services/example-service \
--data host='example-upstream'
```

<br>

**3. We need to create targets for the given upstream**

```
curl -X POST http://localhost:8001/upstreams/example-upstream/targets --data target='mockbin.org:443'
```

```
curl -X POST http://localhost:8001/upstreams/example-upstream/targets --data target='httpbin.org:443'
```

<br>

**4. Verify the actual endpoint**

```
curl http://localhost:8000/mock
```

* It should load balance between the mockbin and httpbin webpage response

<br>

<!--style="font-size:20px" -->
**Disable the plugin**

* Find plugin id with below command

```
curl -X http://<admin-hostname>:8001/routes/mocking/plugins/
```

<br>

* Disable the plugin with the respective id

```
curl -X PATCH http://<admin-hostname>:8001/routes/mocking/plugins/{<plugin-id>} \
  --data enabled=false
```


### Custom Plugins PART - 1 (Hands on)

<br>

**1. Check if docker and docker-compose is available** 

If docker and docker-compose is not available it needs to be installed

```
sudo snap install docker
```

or

```
sudo apt install docker-compose
```

If it asks for unix password(rps) : enter the password 

<br>

**2. Create a folder ”labuser”  and cd to it**

```
mkdir labuser
cd labuser
```

<br>

**3. Clone the kong-pongo repository**

```
git clone https://github.com/Kong/kong-pongo.git
```

<br>

**4. Setup the pongo**

```
export PATH=$PATH:~/.local/bin
mkdir -p ~/.local/bin
ln -s $(realpath kong-pongo/pongo.sh) ~/.local/bin/pongo
```

<br>

**5. Download the custom plugin template code from kong repository**

```
git clone https://github.com/Kong/kong-plugin.git
cd kong-plugin
```

**6. Test pongo command**


```
pongo --help
KONG_VERSION=3.0.0.0 pongo run
```

<br>

<!--style="font-size:20px" -->
**Useful Pongo Commands :**

<br>  

```
pongo build
```
* This builds the Kong test image. You will not use this explicitly in this workshop but pongo run and related commands will run this command automatically under the hood. 
<br>

```
pongo up
```
* This starts the required dependency containers for testing. This will pick up the configuration from .pongo/pongorc, environment variables, and/or the standard output.

* This command will run automatically when pongo run is executed.

<br>

```
pongo run
```
* This runs spec files and applies busted options set in .busted file. This will automatically run several commands as needed, such as pongo build , pongo up , for example. 

* Busted is a unit testing framework with a focus on being easy to use.

<br>

```
pongo down
```
* This will stop the environment and remove all dependency containers (eg. postgres, etc.). 
* This also means that any state in those containers will be lost. 
* Also note that this command will NOT be run after the pongo run command has completed.

<br>

```
pongo shell
```
* This will attach a shell to a Kong test container (started from an image created by the pongo build command) and enbales you to run commands inside of it. 
* This is a good tool when you want to test your plugin code manually.

<!--style="color:red" -->Note: the container will be destroyed when you exit the shell. 

<br>

```
pongo lint
```
* This will run the luacheck linter on your plugin and test code. 
* Since Lua is a dynamic language it is very easy to make typos that go unnoticed and create hard to find bugs. 
* We strongly recommend to run this command while testing and add it to your CI setup.



### Custom Plugins PART - 2 (Hands on)

<br>

<!--style="font-size:20px" -->
**Structure**

<br>

A Kong plugin in its simplest form consists of a directory structure with at least two lua files :

* simple-plugin (directory)

* ├── handler.lua (file)

* └── schema.lua (file)


**schema.lua** defines the schema of the plugin like configuration options to assure users can only enter valid configuration values when configuring the plugin.

**handler.lua** determines which phase the plugin will be running during the network interactions of Kong with the client upstream service.

* The plugins interface allows you to override any of the following methods in your handler.lua file to implement custom logic at various points of the execution life-cycle of Kong.  Custom plugins can be written to execute on a number of methods, which are shown in the table below. However, most custom plugins will be written to execute logic in the access() handler (on the request) or header_filter() handler (on the response).

* To help users get started with developing a custom plugin, Kong makes available a template plugin found on Github here to start developing with. The template plugin sets headers and logs messages at various phases of the request/response lifecycle.

<br>

<!--style="font-size:20px" -->
**Modify the handler.Lua file to make the integration test case fail**

<br>

**Modify the request flow and response flow to return a different value**

* Then run

```
KONG_VERSION=3.0.0.0 pongo lint
```

* Check if any typos or syntax errors are there

```
KONG_VERSION=3.0.0.0 pongo run
```

* This will setup the kong environment and run integration test

* The test cases will fail

* Now fix the spec files pointed in the error to match the asserts and re run pongo run

```
KONG_VERSION=3.0.0.0 pongo run
```

<!--style="font-size:20px" -->
**Deploy the customplugin to kong and test manually**


```
KONG_VERSION=3.0.0.0 pongo shell
```

* If migration scripts are there

```
kong migration bootstrap

kong start
```

```
http localhost:8001
```


* Let’s add a service, a route and your plugin to the Kong configuration so that we can test the plugin's behavior manually.

<br>

**Add service**

* Add a service to the Kong with the command shown below.  The mock service in http://httpbin.org will echo the request along with providing the response.

```
http POST :8001/services/ name=mock-service url=http://httpbin.org
```

<br>

**Add a route**

* Add a route as well by the command.

```
http POST :8001/services/mock-service/routes name=mock-route hosts:='["httpbin.org"]' paths:='["/mock"]'
```

<br>

**Add your plugin**

* Add your plugin to the service by the command.

```
http POST :8001/services/mock-service/plugins name=myplugin
```

<br>

**Verify your plugin is working**

<br>

Let’s verify the plugin is working as you expect by the command.

```
http :8000/mock/anything Host:httpbin.org
```

* Check the response header section and notice the modified header
 <!--style="color:green" -->“Bye-World:” this is response by custom plugin”.  


* Also checkout the echoed request and see the request header set by the plugin 
<!--style="color:green" -->"Hello-World": "this is on a request by custom plugin".


## Enabling Monitoring in kong (OSS) with prometheus plugin and prometheus server (Hands on)

<br>

* Prerequisite is to have the kong up and running in the docker environment 

<!--style="font-size:20px" -->
**1. Enable the prometheus plugin** 

```
curl -s -X POST http://localhost:8001/plugins/ \
 --data "name=prometheus" 
```

<br>

<!--style="font-size:20px" -->
**2. Create a prometheus config yml file in local folder**

**prometheus.yml**

```
scrape_configs:
  - job_name: 'kong'
    scrape_interval: 5s
    static_configs:
      - targets: ['kong:8001']
```

<br>

<!--style="font-size:20px" -->
**3. Run the Prometheus server in same docker network as kong**

```
docker run -d --name kong-prometheus \
   --network=kong-net -p 9090:9090 \
   -v $(pwd)/prometheus.yml:/etc/prometheus/prometheus.yml \
   prom/prometheus:latest
```
<br>

<!--style="font-size:20px" -->
**Kong metrics that will be shared and available in prometheus can be viewed using kong admin url**

```
http://localhost:8081/metrics
```

<br>

<!--style="font-size:20px" -->
**5. Access the prometheus server using below link**

```
http://localhost:9090
```

* Access http://localhost:9090/graph and in the search tab search for kong_node_info you will see the information about kong server version

<!--style="font-size:20px" -->
**6. You can also access it using command line with below command**

```
curl -s http://localhost:9090/api/v1/query?query=kong_node_info
```


## Kong Vitals

![kong vitals](/images/kong49.png)


### Workspace

![kong vitals](/images/kong50.png)


### Teams


![kong vitals](/images/kong51.png)



## OpenAPI

<br>

<!--style="font-size:20px" -->
**Specification**

<br>

![kong vitals](/images/kong52.png)


### History of OpenAPI

<br>

![kong vitals](/images/kong53.png)


### Open API specification Uses

<br>

![kong vitals](/images/kong54.png)


### Sample OpenAPI Document

<br>

![kong vitals](/images/kong55.png)


### OpenAPI Document Format

<br>

![kong vitals](/images/kong56.png)


### OpenAPI Document: Openapi Section

<br>

![kong vitals](/images/kong57.png)


### OpenAPI Document: Info Section

<br>

![kong vitals](/images/kong58.png)


### OpenAPI Document: tags Section

<br>

![kong vitals](/images/kong59.png)


### OpenAPI Document: paths Section

<br>

![kong vitals](/images/kong60.png)


### OpenAPI Document: externalDocs Section

<br>

![kong vitals](/images/kong61.png)


### OpenAPI Document: servers Section

<br>

![kong vitals](/images/kong62.png)


### OpenAPI Document: components Section

<br>

![kong vitals](/images/kong63.png)


## Insomnia
 
 <br>

![kong vitals](/images/kong64.png)


### Prerequisite

<br>

![kong vitals](/images/kong65.png)


### Insomnia Design Mode

<br>

![kong vitals](/images/kong66.png)


### Insomnia Debug Mode

<br>

![kong vitals](/images/kong67.png)


### Insomnia Test Mode

<br>

![kong vitals](/images/kong68.png)

<br>

### Inso

<br>

![kong vitals](/images/kong69.png)


## Imperative vs. Declarative

<br>

![kong vitals](/images/kong70.png)

### Imperative Configuration

<br>

![kong vitals](/images/kong71.png)


### Declarative Configuration (decK)

<br>

![kong vitals](/images/kong72.png)


### decK Commands

<br>

![kong vitals](/images/kong73.png)


### Working with decK

<br>

![kong vitals](/images/kong74.png)


## Introduction to APIOps

<br>

<!--style="font-size:20px" -->
**How?**


![kong vitals](/images/kong75.png)

<br>

![kong vitals](/images/kong76.png)


## Deploying API Gateway Within a CI/CD Pipeline

<br>

<!--style="font-size:20px" -->
ReferenceLink:

<!--style="font-size:20px" -->
https://konghq.com/blog/api-gateway-ci-cd-pipeline


## References

<!--style="font-size:25px" -->
* https://docs.konghq.com/gateway/latest/
* https://docs.konghq.com/hub/
* https://docs.insomnia.rest/
* https://docs.konghq.com/deck/latest/
