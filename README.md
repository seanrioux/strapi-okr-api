# OKR API
An open-source, API first, CMS solution for managing and integrating OKR into your applications.

Created by [OKRIA](https://okria.io): we help organizations set goals and achieve them with our open source tools and coaching solutions designed to better the OKR practice.

## Table of contents
- [Introduction](#introduction)
- [Getting started](#getting-started)
- [Appendix](#appendix)

## Introduction

### What is OKR?
OKR (_objectives and key results_) is a powerful goal setting model popularized by [John Doerr](https://hbr.org/2018/05/how-vc-john-doerr-sets-and-achieves-goals) in his #1 New York Time bestsellers [Measure What Matters](https://www.whatmatters.com/).

OKR defines simple rules for goal setting whereby:

- **Objectives** are _qualitative_ goals towards a company vision or initiativex
- **Key Results** are the _quantitative_ measures for achievement of objectives

These simple yet powerful concepts have helped propel organizations (like Google and the Gates Foundation) towards extraordinary, ambitious achievements.

### What is OKR API?
Many powerful [software solutions](https://okrsoftware.com/) exist for adopting OKR organizationally.

While many of these solutions often offer excellent user experience and a glut of features, they are also often costly. And while some may offer APIs to enable integration with other related tools (project management, human resources, documentation management, etc.) none offer a fully open, extensible, self-hosted OKR solution.

OKR API has been created with the objective to better democratize the OKR model by offering a free-to-use (extend, and re-distribute) OKR management solution. Offered under an MIT license and built on the open-source Strapi CMS, OKR API can be used to build new OKR based solutions, or to integrate OKR with existing business management solutions of any kind.

#### Use cases
OKR API provides an API first content management system to help managers and developers:
- Create and manage objectives and key results
- Integrate the model in new applications (front-end or back-end), or existing third-party solutions
- Deploy OKR management solutions using the internal or cloud infrastructure of choice

#### Key features
OKR API has everything you need to get started:
- **Intuitive management interface** for creating and managing OKRs
- Ready to use **RESTful (or GraphQL)** endpoints for OKR integration
- **Self-hosted** with a range of instructions and database configuration for deployment
- Robust authentication options, user management, extensibility, and more...

Learn more about the powerful Strapi content management system behind OKR API [here](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start.html) for full documentation and features.

## Getting started
Follow these step by step instructions to get started running OKR API in your local development environment:

### 1. Install

#### 1.1. Install Strapi
First, install Strapi globally using npm.
```
npm i strapi -g
```
#### 1.2 Install OKR API
The OKR API repo contains a `package.json` file with additional application dependencies as well as Strapi configuration files specific to the OKR API.

Clone the repo and install the dependencies as follows:

```
git clone git@github.com:okria/okr-strapi.git
cd okr-strapi
npm install
```

**Note:** If you intend to use OKR API in production (and develop it further) you may wish to fork the repo instead.

### 2. Run the application
Strapi includes a cli and a user interface to be accessed in the browser.

#### 2.1 Run in development
To run Strapi and OKR API in development mode:

```
strapi develop
```

**Note:** To review all commands enter `strapi`.

### 2.2 Login as Administrator
You will then be provided with a URL as follows to access the interface in the browser http://localhost:1337.

Visit this URL in the browser, and follow the provided link to navigate to http://localhost:1337/admin to create an administrative account and access the interface for the first time.

### 3. Create and Manage
Once you've logged in you will be presented with the Strapi interface. You'll find 3 content types that will allow you to create and manage organizational OKR. Let's walk through the complete process so you can see how the OKR API works:

#### 3.1 Create a team
The first thing we will do is create a team or teams who will own OKRs. These could be business units, product teams, or any other organizational grouping to be associated with set objectives.

1. Click `Teams` in the sidebar and click the `Add New Team` button
2. Add an team name in the `Team` field
   - e.g.  `executive`, `sales`, `marketing`, etc.
3. Save your team by clicking the `Save` button
6. You can now access this and other teams by clicking `Teams` in the sidebar

#### 3.2 Create an objective
Second, we'll create an objective:

1. Click `Objectives` in the sidebar and click the `Add New Objective` button
2. Add an objective name in the `Objective` field
   - e.g.  `Release a more delightful onboarding experience`
3. Set a goal date for the completion of this objective
4. Select a previously created team using the `Team` field
4. Objectives have `Results` (key results). Leave this field blank for now
5. Save your objective by clicking the `Save` button
6. You can now access this and other objectives by clicking `Objectives` in the sidebar

#### 3.3 Create a metric
Before creating a key result we'll want to identify the key metrics which we'll use to measure our objective. A key metric is a quantitative measure which teams will increase, decrease, or maintain through their activities and which will be used to measure achievement of our objective (as a key result).

1. Click `Metrics` in the sidebar and click the `Add New Metric` button
2. Add a metric name in the `Metric` field
   - e.g. `customer onboarding support requests` or `customer onboarding completion rate`
3. Add a unit in the `Unit` field
   - i.e. the unit name used for the type of metric
   - e.g. `count` or `percentage`
4. As relevant, add a unit symbol in the `Symbol` field
   - e.g. `$`, `%` or `kg`, etc.
5. If a symbol has been identified, we can also configure positioning for the symbol:
   1. Add a symbol `Position` i.e. `before` or `After`
   2. Indicate if the symbol requires a space between the metric value i.e. `10 kg` or `23.4%`
6. Once you have completed all the required fields, save the metric.
7. You can now access the metric by clicking `Metrics` in the sidebar

#### 3.4 Create key results
Once an objective and one or many key metrics have been created you can begin to define key results. Key results allow you to define the quantitative evidence that an objective has been achieved.

1. Click `Objectives` in the sidebar and navigate to edit your previously created objective
2. Under `Result` click `Add new entry` to add a key result
3. Select a `Direction` for your key metric
   - e.g. `increase`, `decrease`, or `maintain`
4. Select a `Metric` you created in the previous step
5. Identify the `Start` value and a `Goal` value used to grade achievement
6. Set a `Date` for the key result (considering the goal date of the objective)
7. Add additional key metrics (typical 2-3) by clicking `Add new entry`
8. Save the objective to save your key results

#### 3.5 Log metrics
In order to grade our objectives our results need to be measured, and so we need to log metrics. The key metric content type allows you to add dated logs. These logs can be used to calculate the actual (or final) value of a key result (e.g. comparing the actual result to the goal result considering the start result, goal date, and log date).

1. Click `Metric` in the sidebar to navigate to access your previous `Metric`
2. Under `Log` click `Add new entry` to add a log
3. Set the `Date` for the log (current date or date of measurement)
4. In the `Value` field enter the current state value of the metric
5. Multiple logs can be added to allow measurement for key results at different intervals
6. Save the metric to save your logs

### 4. API
Now that you have created example team associated objectives and key results you will be able to interact with this content via a RESTful API. This will allow you to integrate the content in front-end or third-party applications.

#### 4.1 Manage permissions
In production, it will be important to ensure proper authentication of the API endpoint to ensure the security of critical data. While testing in our local environment, however, we'll use a public endpoint as a proof of concept.

To configure access to the various endpoints, we'll use the administrative interface:

1. In the sidebar click `Roles & Permissions`
2. Navigate to `Public` to manage public user role access
3. In the permissions section of the page, we'll activate the `find` permission for the resource endpoints we wish to access. In this case:
   - Metric
   - Objective
   - Team
4. Once the `find` permissions have been selected, click `Save`

#### 5.1 Test endpoints
We can now access endpoints for each of our content types in the browser or using an API tool (e.g. Postman) to consume the input content, via any front-end or third-party application.
- Find all metrics via a `GET` request to `http://localhost:1337/metrics`
- Find all objectives via a `GET` request to `http://localhost:1337/objectives`
- Find all teams via a `GET` request to `http://localhost:1337/teams`

## Appendix
OKR API is new, but we will continue to enhance the offering with further customization to the Strapi interface, documentation, and use case example (including code). For now, please feel free to [reach out](http://localhost:4000/sales) with comments or questions and to browse the resources below to explore further.

### Authentication
To access the API securely, you'll want to set up authentication using one of the recommended authentication [methods](https://strapi.io/documentation/3.0.0-alpha.x/guides/authentication.html#authentication).

The process is (at a high level) as follows:

1. Navigate to the `Roles & Permissions` page and set authenticated user permissions.
2. Create a user with the authenticated user role
3. Retrieve PWT token with `POST` request passing user `identifier` and `password` to the `http://localhost:1337/auth/local` endpoint (note: parameters should be passed in the request body)
4. Access content endpoints with token in header (bearer token)

### Deployment and database
Deploying Strapi to production can be achieved with a range of possible [hosting](https://strapi.io/documentation/3.0.0-alpha.x/guides/deployment.html) and [database](https://strapi.io/documentation/3.0.0-alpha.x/guides/databases.html) configurations.

### Additional users and roles
Before on-boarding product managers or other user roles to the OKR API, you should create a safe permission set that ensures users can create content, but not manage other administrative functions.

We recommend creating a `manager` role, restricting access to the following permission categories:

- **CONTENT-MANAGER**
  - Contenttypes
  - Generalsettings
  - Groups
- **CONTENT-TYPE-BUILDER**
  - Contenttypebuilder
  - Groups
- **EMAIL**
  - All
- **USER-PERMISSIONS**
  - User (all except `me`)
  - Userpermissions (all except `init`)

### Additional documentation
- [Strapi documentation](https://strapi.io/documentation/3.0.0-beta.x/getting-started/introduction.html)
