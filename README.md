# Testing with Docker

`npm install`

`docker build -t devenv .`

`docker run -it \ --rm \ -v ${PWD}:/app \ -v /app/node_modules \ -p 3001:3000 \ -e CHOKIDAR_USEPOLLING=true \ sample:dev `

<pre>
docker run \
    -it \
    --rm \
    --network host \
    -v ${PWD}:/app \
    -v /node_modules \
    -p 3001:3000 \
    -e CHOKIDAR_USEPOLLING=true \
    sample:dev
</pre>

# Building with Docker

`sudo docker build -f Dockerfile.prod -t mhanwar .`

`sudo docker run -it --rm -p 2500:80 mhanwar`

To run container in the background: `CTRL` + `P` and then `CTRL` + `Q`

To stop the container: `sudo docker stop mhanwar`

To remove the image, find the ID with: `sudo docker image ls`

Then: `sudo docker image rmi image_id`
