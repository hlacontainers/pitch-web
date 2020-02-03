# Pitch Web UI image
This image is the Pitch Web UI. The Web UI can be used to monitor and control CRCs, federations and federates.

An example composition to run the Pitch Web UI can be found under the examples directory in this repository. The Pitch Web UI requires a licensed RTI and does not work with the Pitch free RTI version. 

**This repository does not include any Pitch files**

## Container synopsis

````
pitch-web:<version>
````

Ports:

`8080` : Pitch Web UI HTTP listen port.

## Build instructions

To build the Pitch Web UI image, perform the following steps.

### Clone repository

Clone this Git repository to the directory named `${WORKDIR}`.

### Obtain Webview installer

See http://pitchtechnologies.com to obtain a licensed RTI version and a `webview` WAR file.

Rename the file to `webview-${VERSION}.war`, where `${VERSION}` is the version number of the product.

Copy the file to `${WORKDIR}/pitch-web/docker/context` and remove the placeholder file already present in that directory.

### Build image

Change into the directory `${WORKDIR}/pitch-web/docker`.

Check and if needed adapt the environment variable settings in the file `.env`. For example, set the product version number.

Build the Pitch Web UI container image with:

````
docker-compose -f build.yml build
````