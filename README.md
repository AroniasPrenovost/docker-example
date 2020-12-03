## Docker + React boilerplate

Requires valid Docker ID
```sh
docker login -u {DOCKER ID}
```

### Scripts
```sh
npm start
npm run build  
npm run eject 
```

### Build DEV image 
```sh
docker build -f Dockerfile.dev .
```

### Execute tests
```sh
docker run {container_id} npm run test -- --coverage 
```

### Build PROD image 
```sh
docker build .
```

### Run an image 
```sh
docker run -it -p 8080:80 {container_id}
```
- port 8080: local machine 
- port 80: ngnix server default 

[http://localhost:8080](http://localhost:8080) 

### Execute volumes 
```sh 
docker run -it -p LOCAL_PORT:DOCKER_PORT -v /app/node_modules -v ${PWD}:/app -e CHOKIDAR_USEPOLLING=true CONTAINER_ID
```

### Deployment 
- GitHub
- Travis CI
- AWS 


### TravisCI




 