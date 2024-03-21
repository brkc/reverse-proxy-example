# Reverse proxy example

Run the command below to get started:

```
docker compose up --build --detach
```

This will start a server where content (such as a React build) will be displayed
as normal, but any request path that starts with `/api` will be passed by nginx
to the backend to execute arbitrary node.js code.

For example:

- Navigating to http://localhost:8080 will show content from
  [frontend/html](https://github.com/brkc/reverse-proxy-example/tree/main/frontend/html).
- Navigating to http://localhost:8080/api will execute
  [backend/app.js](https://github.com/brkc/reverse-proxy-example/blob/main/backend/app.js).
