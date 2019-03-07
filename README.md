# gitlab-ce + gitlab-runner docker version

This repo use gitlab-ce docker image and gitlab-runner docker image to create gitlab + pipelines workflow with custom hostname and port.

## Quick Start

- install docker and docker-compose
- clone repo
- docker-compose up

## register gitlab-runner

Once both services up, gitlab-runner will throw config file not found errror, which we should generate by running

```bash
docker exec -it ${gitlab-runner-container-id} gitlab-runner register
```

You can get host and token from `gitlab-ce -> repo -> setting -> runner`
