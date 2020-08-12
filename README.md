# template-docker-full-stack-app

Template Nginx, Node.js Express API, Vue.js Application

- [getting started](#getting-started)
    - [cloning and setup](#cloning-and-setup)
    - [development startup](#development-startup)
	- [api testing](#api-testing)
	- [starting for production](#starting-for-production)
- [auxiliary](#auxiliary)
- [CHANGELOG](#changelog)

<hr/>

### [getting started](#top)

the following applications are required to run in `production`:
- [Docker](https://docs.docker.com/install/) (recommended: v19.03.2)
- [Docker Compose](https://docs.docker.com/compose/install/) (recommended: v1.24.1)

the following applications are required to run in `development`:
- [Git](https://git-scm.com/downloads) (recommended: `>= v2.21.0`)
- [Docker](https://docs.docker.com/install/) (recommended: `v19.03.2`)
- [Docker Compose](https://docs.docker.com/compose/install/) (recommended: `v1.24.1`)
- [Node.js](https://nodejs.org/en/download/) (recommended: `v12.18.3`)
- [PM2](https://github.com/Unitech/pm2/releases/) (recommended: `v4.4.0`)

##### [cloning and setup](#top)

> Note: need help with submodules? [check this out](https://www.vogella.com/tutorials/GitSubmodules/article.html)

```
# clone full-stack template
git clone --recursive git@github.com:mi-sec/template-docker-full-stack-app.git
cd template-docker-full-stack-app/
```

##### [development startup](#top)

```
./start.dev.sh
```

##### [development startup with ui hot reloading](#top)

```
./start.dev.sh

# wait for the UI to finish building in docker-compose startup then:
cd app/ui
npm i
npm run serve
# access live ui at http://localhost:8080/
```

##### [api testing](#top)

```
cd api
npm i
npm test
```

##### [starting for production](#top)

```
./start.prod.sh
```

ui will be accessible at `http://localhost` by default
api will be accessible at `http://localhost/api/` by default

### [auxiliary](#top)

**API testing**:

For testing API things, import the Postman collection in the `api` folder.
Environment should be set for:

- PROTOCOL: `http`
- HOSTNAME: `localhost`
- PORT: `80`
- PATH: `/api`


### [CHANGELOG](#top)

**v1.0.0**
- initial release
