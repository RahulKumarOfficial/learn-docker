# Instructions

Do a docker build as usual with the help of the command:   
`docker build -t feedback-app:volumes .`

Then run it with named volume as:  
`docker run -d -p 3000:80 -v feedback-by-rk:/app/feedback --rm --name feedbak-app feedback-node:volumes`

If there are too many volumes piling up and you want to clean them:  
`docker volume prune -f`

## Named Volume 
Named volume is simply a bucket of data. Docker maintains the physical location on the disk. We only need to remember the name of the volume. **Named volume is great choice if we want to store the data**.

## Bind Mount
With Bind Mounts we control the exact mount-point on the host. We can use this to persist data, but is often used to provide additional data into the containers. 

Mount example: `/path/to/Data<on Machine>:/usr/local/data<on Docker>`

## Run the docker in this folder
### Build
`docker build -t feedback-node .`

### Spin container
Note the bind mount using -v:
`docker run -p 3000:80 -v $(pwd)/feedback:/app/feedback --name feedback-app feedback-node`

### Open Web Browser
Visit localhost:3000 and it should reflect exact what you type in feedback/ folder of this data-volumes-02-added-dockerfile.