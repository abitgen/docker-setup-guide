### denied: requested access to the resource is denied : docker

While pushing the docker image from local

> Solution

```
docker logout                                   # to make sure you're logged out and not cause any clashes
docker tag <imageId> myusername/docker-whale    # use :1.0.0 for specific version, default is 'latest'
docker login --username=myusername              # use the username/pwd to login to docker hub
docker push myusername/docker-whale             # use :1.0.0 for pushing specific version, default is 'latest'
```
