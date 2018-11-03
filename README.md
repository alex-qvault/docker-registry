# docker-registry
------------------
## linux local docker registry

### Why

- Run a local dockerhub registry

### Usage

- start new dockerhub
```
  git clone https://github.com/alex-qvault/docker-registry
  cd docker-registry
  ./bin/gitCheckOut
  ./bin/startDockerRegistry
```

### To update repo
- pull docker images
```
  ./bin/dockerInit
```

- split images to 100MB for git push
```
  ./bin/gitCheckIn
  git add -A .
  git commit -m MY_NEW_COMMIT
  git tag -a 0.0.2 -m MY_NEW_COMMIT
  git push --follow-tags
```

- Merge files after git pull
```
  git pull
  ./bin/gitCheckOut
```
