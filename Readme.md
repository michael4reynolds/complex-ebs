# From Docker and Kubernetes

## Tutorial on Udemy

### By Stephen Grider

### Complete AWS Section

### Steps to run

#### Prepare images

```bash
docker build -t michael4reynolds/multi-client ./client
docker build -t michael4reynolds/multi-nginx ./nginx
docker build -t michael4reynolds/multi-server ./server
docker build -t michael4reynolds/multi-worker ./worker
```

#### Log in to the docker CLI

```bash
docker login -u "$DOCKER_ID" --password-stdin
```

#### Take those images and push them to docker hub

```bash
docker push michael4reynolds/multi-client
docker push michael4reynolds/multi-nginx
docker push michael4reynolds/multi-server
docker push michael4reynolds/multi-worker
```

#### Use eb cli to prepare and create elastic beanstalk app

```bash
eb init
eb create
eb open
eb status
eb health
eb terminate --all
```
