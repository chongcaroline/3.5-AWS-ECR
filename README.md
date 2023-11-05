# Build hello-node image to Private ECR

## Command to build an image

```sh
docker build -t hello-node .
```

## Command to tag an image with latest

```sh
docker tag hello-node:latest 255945442255.dkr.ecr.us-east-1.amazonaws.com/ecrmi5:latest
```

## Command to login to the repository where the regional is. 

```sh
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 255945442255.dkr.ecr.us-east-1.amazonaws.com
```

## Command to to push the image to ECR

```sh
docker push 255945442255.dkr.ecr.us-east-1.amazonaws.com/ecrmi5:latest
```
