## `sapmachine:jdk-alpine`

```console
$ docker pull sapmachine@sha256:2fa9caa326e51524a3a81d89d380a4b973c71d3fd7319dcea54a2d0621d4ae22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:891a78d90a96b544be1c53a5096497b476600ec0235bdd2f9ac2f5342d8fb14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236624685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a21ff433440a6bd93566710f07231ed1b851e44c29afda3a65582548b050cf8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jdk=24.0.1-r0 # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jdk
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4dc32ef242b6ecd81c0ac4a4f2e1e73c84fa1a94521977244ea84725a90742`  
		Last Modified: Fri, 09 May 2025 07:04:11 GMT  
		Size: 233.0 MB (232982438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:67967c5e355a51cddee425e5098bcd7c3b8cecae5b5407850da2a3a3e3747327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.7 KB (510730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68946a05a5c402a2396552688b1af57e9187a519d329b1ce8252d0699c8bd9e3`

```dockerfile
```

-	Layers:
	-	`sha256:3e01a87f34e2d5c86c029098f2648c15ef657ec613ab25615cd116a73b3fc077`  
		Last Modified: Tue, 17 Jun 2025 10:01:15 GMT  
		Size: 501.5 KB (501471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac97d7e78a2cb766ff5edce0aa5932bb1c6045825d0c956504e67682d50edc2`  
		Last Modified: Tue, 17 Jun 2025 10:01:16 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
