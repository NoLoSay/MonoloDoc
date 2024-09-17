# Deploying

### On the machine with validated staging branch

1. Build the docker images

```
docker compose build
```

2. Export the images as files

```
docker save monoloback-main-api -o monoloapi
docker save monoloback-api-video -o monolovideo
docker save monoloback-prisma-migrate -o monoloprisma
docker save noloadmin-intra -o noloadmin
```

3. Send them to the VM using rsync

```
rsync -av -e 'ssh -p <port>' <image-file> <user>@<vm>:<location>
```

4. Connect to the VM via ssh

### On the production VM

6. Load the images into docker

```
sudo docker load < monoloapi
...
```

6. Restart the docker environment

```
sudo docker compose up
```
