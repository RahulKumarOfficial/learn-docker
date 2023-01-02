# Instructions

Do a docker build as usual with the help of the command: 
`docker build -t feedback-app:volumes .`

Then run it with named volume as:
`docker run -d -p 3000:80 -v feedback-by-rk:/app/feedback --rm --name feedbak-app feedback-node:volumes`

If there are too many volumes piling up and you want to clean them:
`docker volume prune -f`