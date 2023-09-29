# Run XCMSend in docker  

In order to run XCMSend in docker on port 8080, do the following.


## Build the docker image locally:
```shell
git clone https://github.com/XcmSend/DockerBuild
cd DockerBuild/
docker build -t xcmsend .
```


## Download from Dockerhub
```shell
$ docker pull xcmsend/xcmsend:v0.0.1
```


### Run   
```shell
$ docker run -d -p 8080:8080 xcmsend
```
