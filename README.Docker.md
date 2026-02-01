### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:3000.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

### References

- [Docker's Node.js guide](https://docs.docker.com/language/nodejs/)

docker build --target production --tag docker-nodejs-sample .
docker images

Inside the docker-nodejs-sample directory, run the following command in a terminal.
docker compose up app-dev --build
The development application will start with both servers:

API Server: http://localhost:3000 - Express.js backend with REST API
Frontend: http://localhost:5173 - Vite dev server with React frontend
Health Check: http://localhost:3000/health - Application health status

Run the application in the background
You can run the application detached from the terminal by adding the -d option. Inside the docker-nodejs-sample directory, run the following command in a terminal.

docker compose up app-dev --build -d

To confirm that the container is running, use docker ps command:
docker ps

Run different profiles
You can run different configurations using Docker Compose profiles:

Run production
docker compose up app-prod -d

Run tests
docker compose up app-test -d

To stop the application, run:

docker compose down

docker compose up app-dev --build

https://hub.docker.com/repositories/sivanvtk

docker tag local-image:tagname new-repo:tagname
docker push new-repo:tagname

https://hub.docker.com/repositories/sivanvtk/nodejssamples

https://github.com/sapsivan/DockerNodejs

$ git remote set-url origin https://github.com/{your-username}/{your-repository-name}.git
$ git remote set-url origin https://github.com/sapsivan/DockerNodejs.git
