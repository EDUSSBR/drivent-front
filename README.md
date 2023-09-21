
# DRIVENT - FRONTEND

This is the front-end of a white-label app designed for selling events and facilitating talk subscriptions, with the added capability of booking accommodations in partner hotels.
<div  align="center">
<img src="/public/front-drivent.jpeg" />
</div>

## About

Introducing a web application for easy getting the clients for your events. Key features include:

- User Sign Up
- Secure Login
- Event Subcription
- Ability to sell both In-person and Remote Ticket
- Seamless integration with partner hotels, simplifying the booking process for users across a wide range of options.
- Direct Credit Card Payments
- Capacity Management for event venues.
- Hotel Room Booking Management.
- Users have the flexibility to switch rooms if desired.
- Tracking of subscribed users for each activity.
- Generation of certifications after the event concludes.
This app empowers users to gain insights into their spending habits and maintain a clear overview of their financial balance at all times.

## Technologies
The following tools and frameworks were used in the construction of the project:<br>
<p>
  <img style='margin: 5px;' src='https://img.shields.io/badge/styled-components%20-%2320232a.svg?&style=for-the-badge&color=b8679e&logo=styled-components&logoColor=%3a3a3a'>
  <img style='margin: 5px;' src='https://img.shields.io/badge/axios%20-%2320232a.svg?&style=for-the-badge&color=informational'>
  <img style='margin: 5px;' src="https://img.shields.io/badge/react-app%20-%2320232a.svg?&style=for-the-badge&color=60ddf9&logo=react&logoColor=%2361DAFB"/>
  <img style='margin: 5px;' src="https://img.shields.io/badge/react_route%20-%2320232a.svg?&style=for-the-badge&logo=react&logoColor=%2361DAFB"/>
  <img style='margin: 5px;' src='https://img.shields.io/badge/react-icons%20-%2320232a.svg?&style=for-the-badge&color=f28dc7&logo=react-icons&logoColor=%2361DAFB'>
</p>

## Next Steps

As a next step, here are some plans for further development:

- Implement a dashboard for visualizing financial data.
- Add labels for classifying expenses (e.g., "Groceries," "Entertainment," "Utilities," etc.).

## How to run

1. Clone this repository
2. Clone the back-end repository at https://github.com/my-user/my-project-backend
3. Follow instructions to run back-end at https://github.com/my-user/my-project-backend 
4. Install dependencies
   
```bash
npm i
```
5. Run the front-end with
```bash
npm start
```
6. You can optionally build the project running
```bash
npm run build
```
7. Finally access http://localhost:3000 on your favorite browser (unless it is Internet Explorer. In this case, review your life decisions)






























# drivent-front

Front-end for Driven.t, an event management solution.

## About

Driven.t is a web browser application with which you can manage every single aspect of your event.

## How to run for development

1. Clone this repository
2. Install all dependencies

```bash
npm i
```

3. Populate `.env` file based on `.env.example`. `REACT_APP_API_BASE_URL` should point to your API server (driven.t-back)

4. Run the back-end in a development environment:

```bash
npm run start
```

## Building and starting for production

```bash
npm run build
npm start
```

## Running application locally or inside docker

`.env.development` and `.env.test` must be changed if you and to run the application locally or inside docker. You can populate files based on `.env.example` file, but you need to consider the following:

- Running application locally (postgres and node):

Add your postgres credentials and make sure to create given database before running the application.

- Running application inside docker (postgres and node):

Set `POSTGRES_HOST` to `drivent-postgres-development` for `.env.development` and `drivent-postgres-test` for `.env.test` file. It is the name of the postgres container inside docker-compose file. Docker Compose will start the postgres container for you, create the database and host alias for you.

- Running application locally (node) but postgres is running inside docker:

Set `POSTGRES_HOST` to `localhost` for `.env.development` and `localhost` for `.env.test` file. Docker compose is configured to expose postgres container to your localhost.

## What to do when add new ENV VARIABLES

Please notice that every ENV that should be available on browser should start with `REACT_APP_` prefix. There are several things you need to do when you add new ENV VARIABLES:

- Add them to `.env.example` file
- Add them to your local `.env` file
- Add them to your docker-compose.yml file (just the name, not the value). Only envs listed in the environment section will be exposed to your docker container.
- Add them (prod version) to your github repo secrets. They will be used to generate the `.env` file on deploy.
