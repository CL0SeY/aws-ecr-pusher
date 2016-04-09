# aws-ecr-pusher
Dockerfile for pushing docker images to AWS ECR.

Note: Requires "privileged" mode! Only in Docker >= 1.9.0

How to use
----------
```bash
docker run --privileged -v /var/run/docker.sock:/var/run/docker.sock \
  --env IMAGE="your-image-to-push:latest" --env TARGET="xxxx.yyyy.ecr.aws-region.amazonaws.com/your-pushed-image:latest" \
  --env AWS_ACCESS_KEY_ID="your-aws-access-key" --env AWS_SECRET_ACCESS_KEY="your-aws-secret-access-key" \
  --env AWS_DEFAULT_REGION="your-region" \
  aws-ecr-pusher
```
