---
title: API Hub - Part 01
subtitle: API Hub Architecture Overview
toc: true
tags: [Architecture, MicroService]
---
{:toc}

## Background 
An API hub serves as a centralized repository, allowing several projects can register and integrate all APIs seamlessly, utilizing a single key.
Internal API Hub: serve API for companies projects 
External API Hub: Customers can register and use APIs for their projects, 

## Project goals
- Reduce development cycles 
- creating stickiness to applications and services

## Overview 

### API Hub overview 

<img src="{{ '/assets/img/post/2024/02/20240224-api-hub-architecture.png' | relative_url }}" />

#### API Managment
- Manage metadata about APIs in the API Hub ( Metadata, API docs )
- Serving the UI that developers interact with to discover and view API details

#### API Gateway
- Enforcing gateway functionality: Authorization, rate limits, quota limits, transformations, etc... 
- Is independent of the API Managment. 
  
#### Internal Auth Service 
- Provide the tokens for internal services to communicate seamlessly with one another. Internal services are not required to be aware of the API KEY

#### Config Service 
- Store the setting when register using service such as 
  - Booking with/without payment ( Booking Service )
  - API KEY, Endpoint, Rate Limitation, Quota Limitation

#### Payment Service, Booking Service, ...
- Available services that project can register using 

#### Micro FE/ Component Libraries
- Offered front-end components associated with registered services that enable developers to embed them directly into projects.

### Workflow

#### Register using API Flow
<img src="{{ '/assets/img/post/2024/02/20240224-api-register-service.png' | relative_url }}" />

#### Use Booking API Flow 
<img src="{{ '/assets/img/post/2024/02/20240224-api-use-booking-service.png' | relative_url }}" />