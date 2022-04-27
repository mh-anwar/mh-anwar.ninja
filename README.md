# Testing with Docker

`npm install`

`docker build -t devenv .`

`docker run \ -it \ --rm \ -v ${PWD}:/app \ -v /app/node_modules \ -p 3001:3000 \ -e CHOKIDAR_USEPOLLING=true \ sample:dev `

# Building

`docker build -f Dockerfile.prod -t prod .`

`docker run -it --rm -p 2500:80 prod`
