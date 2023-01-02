# Instructions

# Docker build app
`docker build -t node_app .`

# Docker run app
`docker run -p 3000:3000 node_app`

# To copy from local path to container
`docker cp <folder/file> <container-name>:<path>`

# To copt from container from container to path
`docker cp <container-name>:<path> <path>`