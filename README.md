# Prequisites
1. Have Docker running
2. Have NodeJS >18 installed.

## Run Server
1. Clone project
2. `cd server`
3. Run `npx jamsocket dev` which builds a new docker image using `Dockerfile` and `jamsocket.config.js`

## Spawn the backend & get a response
1. Run `curl -X POST http://localhost:8080/user/my-account/service/python-fastapi-helloworld/spawn`

You should see a response like this:
```json
{
    "url": "http://localhost:9090/tYVHfS4PKgufdhwGCnn6LLfAaCo_iAHitbw4Bg8ETjA/",
    "name": "ba-xt8nmtlgti18qx",
    "status_url": "http://0.0.0.0:8080/pub/b/ba-xt8nmtlgti18qx/status",
    "spawned": true,
    "status": "Loading"
}
```

2. Use the url in the backend response and run `curl {BACKEND URL}`
You should see a response like this:
```json
{ "res": "Hello World" }
```

Or spawn and connect with Jamsocket's javascript client library, `@jamsocket/javascript`.
