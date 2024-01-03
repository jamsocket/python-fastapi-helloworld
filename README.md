# Prequisites
1. Have Docker running
2. Login to Jamsocket CLI `npx jamsocket@latest login`

## Run Server
1. Clone project
2. `cd server`
3. Create a service with `npx jamsocket service create python-fastapi-helloworld`
4. Run `npx jamsocket dev` which builds a new docker image using `Dockerfile` and `jamsocket.config.js`

## Spawn the backend & get a response
1. Run `curl -X POST http://localhost:8080/user/{ACCOUNT}/service/python-fastapi-helloworld/spawn`

You should see a response like this:
```json
{
    "url":"https://i84or.jamsocket.run/",
    "name":"i84or",
    "ready_url":"https://api.jamsocket.com/ready/i84or/",
    "status_url":"https://api.jamsocket.com/backend/i84or/status",
    "spawned":true,
    "status":"Loading"
}
```

2. Use the url in the backend response and run `curl {BACKEND URL}`
You should see a response like this:
```json
{"res":"Hello World"}
```

Or spawn and connect with a client library `@jamsocket/javascript`
