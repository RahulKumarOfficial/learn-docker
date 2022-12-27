# How to remove docker containers and images

## Containers
`docker stop <container-name/id>`
`docker rm <container-name/id>`

# Important
Remove containers automatically after they are executed.
Example:
`docker run --rm <image-id/name>`
`docker stop <container-id/name>`
`docker ps`
The docker ps will have no output of that respective image container as we gave --rm to remove automatically after its removed.

## Images
Can only be removed if no container is running including stopped containers.
### For docker images that are not getting used
`docker prune <image-id/name>`
### For docker images those containers are already removed
`docker rmi <image-id/name>`

## Note
We can mention multiple container-names/image-names or their IDs. 
Example: `docker rm <id1> <id2> <id3> ...`
