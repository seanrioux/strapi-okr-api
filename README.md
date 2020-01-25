# OKRIA Strapi
An open-source API solution for managing and integrating OKRs, initiatives and activities into your applications.

## Introduction
OKRIA is a setting and strategic planning model designed to better the objectives and key results model popularized by John Doerr.

### What is OKRIA?
If you’re familiar with OKR, it’s pretty easy to summarize OKRIA (it’s in our name). OKRIA stands for Objectives and Key Results, Initiatives and Activities.

In the OKRIA model, we have explicitly delineated the often compounded process of planning initiatives and activities from that of setting objectives and key results. In doing so we have worked to define a more holistic strategic planning model. Following the OKR example, we’ve defined simple (but opinionated) rules for the application of the process, considering organizational hierarchy and scalability.

Put simply, we’ve extended OKR to help connect the dots (and ensure a clear separation) between the goals companies set and the work teams do to achieve them.

## Getting Started
OKRIA is committed to offering free tools to help support adoption of the model. You can learn more about OKRIA [here](https://okria.io/). To help companies adopt the model in software application, We've created this open-source Strapi based OKR management solution.

### Introducing OKRIA Strapi
OKRIA Strapi provides an API first CMS to help product managers and developers:
1. Create and manage objectives and key results
2. Plan initiatives and activities
3. Integrate objectives and initiatives with products

### Features
OKRIA Strapi has everything you need to get started:
- CMS interface for managers
- RESTful API for developers
- User management, plugin architecture, and more...

Learn more about the powerful Strapi CMS [here](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start.html) for full documentation and features.

## Quick Start Guide
Getting started is easy.

Please make sure Node.js and npm are properly installed on your machine.
https://strapi.io/documentation/3.0.0-alpha.x/getting-started/quick-start.html#_1-install-strapi-globally

```
npm install strapi@alpha -g
```

Install dependancies.
```
npm install
```

Start a Strapi application with autoReload enabled.
https://strapi.io/documentation/3.0.0-beta.x/cli/CLI.html#strapi-new
```
yarn strapi develop
```

Access in browser
http://localhost:1337


Authentication
1. Set user permissions to access objectives and initiatives endpoints
2. Create authenticated user
3. Get PWT token with POST request
4. Access objectives and initiatives endpoints with token in header


Testing with Postman
1. POST http://localhost:1337/auth/local
   1. BODY identifier, password
