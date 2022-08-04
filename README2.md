# dockerJenkins

https://www.jenkins.io/doc/book/installing/docker/
docker network create jenkins
docker run \
  --name jenkins-docker \
  --rm \
  --detach \
  --privileged \
  --network jenkins \
  --network-alias docker \
  --env DOCKER_TLS_CERTDIR=/certs \
  --volume jenkins-docker-certs:/certs/client \
  --volume jenkins-data:/var/jenkins_home \
  --publish 2376:2376 \
  docker:dind \
  --storage-driver overlay2

  c58fffa688ad4cd09091d97eff3e9e83
  docker logs d90f302c63d1d0f096c23137477b31f66eaad229a0c711b278293233d7adba4b

