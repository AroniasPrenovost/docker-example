## Docker + React boilerplate

### npm start

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

### npm test
### npm run build
### npm run eject

### build DEV image 
```sh
docker build -f Dockerfile.dev .
```

### build PROD image 
```sh
docker build .
```

### run PROD image 
```sh
docker run -it -p 8080:80 {container_id}
```
port 8080: local machine 
port 80: ngnix server default 

### execute tests
```sh
docker run -it CONTAINER_ID npm run test
```

### executE volumes 
```sh 
docker run -it -p LOCAL_PORT:DOCKER_PORT -v /app/node_modules -v ${PWD}:/app -e CHOKIDAR_USEPOLLING=true CONTAINER_ID
```
 