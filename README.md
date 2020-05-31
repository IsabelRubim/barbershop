<h1 align="center">
<img src="frontend/src/assets/logo-small.svg" width="200px">
</h1>

# GoBarber - A barbershop

Containing scheduling, appointments, session and authentication. This app features
all the latest tools and practices in web development.

## Built with (Backend and Frontend)

* Express — A web framework for Node
* Sequelize — SQL dialect ORM for Node.js
* MongoDB — document-based database
* Redis — key-value data model
* Yup - Object schema validation
* Sentry - cross-platform application monitoring
* Nodemailer - Send e-mails with Node.JS
* React — A library to build user interfaces
* Redux with Redux Saga — State management with middleware
* CSS — styled-components
* Reactotron - Helps debugging process
* Lint — ESlint/Prettier/Editor Config

### How to use

**Docker** is required

* ``docker run --name redisbarber -p 6379:6379 -d -t redis:alpine``
* ``docker run --name mongobarber -p 27017:27017 -d -t mongo``
* ``docker run --name some-postgres-name -e POSTGRES_PASSWORD=docker -p 5433:5432 -d postgres``

:warning: If you restart your machine, you will need to start again the server with ``docker start <container_id>``.

1. `git clone https://github.com/isabelrubim/barbershop.git`
2. Go to repository folder
3. Run ``yarn`` to install dependencies. (in Backend and Frontend)
4. Copy the .env.example file and rename it to .env
5. Add all the values for the environment variables
6. Run ``yarn start`` and ``yarn queue`` to run the servers at ``http://localhost:3333`` (in Backend)
7. Run ``yarn start`` to see the example app (in Frontend)

### Routes in Backend

* **post('/users')** - Create a login
* **post('/sessions')** - Log in to an account

#### Routes - authentication is required

* **put('/users')** - Update an account
* **get('/providers')** - List providers
* **get('/providers/:providerId/available')** - Check provider availability
* **post('/appointments')** - Create an appointment
* **get('/appointments')** - List all logged-in user's appointments
* **delete('/appointments/:id')** - Delete an appointment
* **get('/schedule')** - Schedule services
* **post('/files')** - Profile pictures
* **get('/notifications')** - List all logged in user notifications
* **put('/notifications/:id')** - Confirm notification was seen

---

<p align="center">
Made with ♥ by <a href="https://www.linkedin.com/in/isabelrubim">Isabel Rubim</a>
</p>
