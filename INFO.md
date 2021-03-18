# Image Scanning

As a developer you will be familiar with the shift left movement to security, where security is starting earlier in the development lifecycle. One of the things that can be performed at this phase of the build is to scan the container for any known vulnerabilities.

There are a number of tools that can do this, and there are also a number of registries that have this capability integrated, but for this example we are going to download and install a command line tool that we can use to scan our containers.

Execute the following to install the Trivy tool

```

Executing the following command will run the tool against the single image that we created earlier:

```
sudo apt-get -y update && \
```
`````
```
```

# Image Tagging

Once the container image is built, it should be tagged before it gets pushed into a docker registry. The tag should be on the form <docker_registry_url>/<docker_registry_url>/<docker_image>:<docker_image_version> . If <docker_registry_url> is not specified, docker hub is set by default.

You must tag the image using your DockerHub UserID, this will create allow for the push to be performed to push it to your DockerHub repository.

docker login -u <docker_user> -p <token>
# docker push <docker_user>/rancher-demo:0.1.0
docker push <docker_user>/rancher-demo:0.2.0


# docker tag rancher-demo-single <docker_user>/rancher-demo:0.1.0

We are going to need a couple of images in later exercises so we are going to tag the multi image as 0.2.0

# docker tag rancher-demo-multi <docker_user>/rancher-demo:0.2.0

# Publishing app


docker login -u <docker_user> -p <token>
docker push <docker_user>/rancher-demo:0.1.0
docker push <docker_user>/rancher-demo:0.2.0
