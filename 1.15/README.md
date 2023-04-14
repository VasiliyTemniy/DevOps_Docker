# DevOps with Docker exercise 1.15

### Uses bloglist app made for Fullstack open course

### Backend

https://hub.docker.com/r/vasiliytemniy/bloglist-backend

To run, type

```
docker run -it --name [container-name] --env-file [your-env-file] -p 127.0.0.1:8080:[specified-in-env-port] vasiliytemniy/bloglist-backend:0.9
```

Port 8080 is fixed because frontend is built with this port for backend and it cannot be changed during runtime.

Necessary env variables:

MONGODB_URI - Uri of your Mongo DB
PORT - Port for backend
SECRET - Secret for token creation and validation

### Frontend

https://hub.docker.com/r/vasiliytemniy/bloglist-frontend


To run, type

```
docker run -it --name <container-name> -p 127.0.0.1:<frontend-port>:3000 vasiliytemniy/bloglist-frontend:0.9
```
