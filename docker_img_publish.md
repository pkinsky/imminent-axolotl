

build docker image (installs stack, builds deps of current version of this project)
```
docker build .
```


(optional) open container with version of this project's site dir shared (as in CI)
```
docker run -v $HOME/dev/oss/imminent-axolotl:/site -it --rm dff7 bash
```

tag build (in this case dff70030d799) as pkinsky/circleci:imminent-axolotl
```
docker tag dff70030d799 pkinsky/circleci:imminent-axolotl
```

publish tagged image to dockerhub
```
docker push pkinsky/circleci:imminent-axolotl
```
