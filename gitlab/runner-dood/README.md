# gitlab-runner-dood

Docker image with Gitlab-runner installed and ready to use host's Docker service to run containers.

Useful to run containers started from a Gitlab pipeline in host machine.

## Usage example

```bash
docker run -d \
  --name gitlab-runner \
  --restart always \
  -v /gitlab-runner/config:/etc/gitlab-runner \
  -v /var/run/docker.sock:/var/run/docker.sock \
  sumolari/gitlab-runner-dood:latest
```
