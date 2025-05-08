## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:eba35c7ca3198daa68edf71b4732fc42668ff43d9bfa712d66402c66d3628305
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:c88125260bcd0802448076d876b52ccacf5467b5d8cc12648e4ab4067cf61fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312132057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3383df94dd1fc0a802570b8e52dc32680494e242b29821141caf28fdfc2a1fa7`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 09 Dec 2024 12:55:29 GMT
ARG RELEASE
# Mon, 09 Dec 2024 12:55:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 12:55:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 12:55:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 09 Dec 2024 12:55:29 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8edf39e6b158b62285186333ea043966bdc46105bf3daf1317510070c201a5`  
		Last Modified: Thu, 08 May 2025 19:18:31 GMT  
		Size: 1.2 MB (1194689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13187d005e620eba14af8df803fa0d8ceccdaf9e01cc294dd377690c9d7851e4`  
		Last Modified: Thu, 08 May 2025 19:18:38 GMT  
		Size: 5.4 MB (5363846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8feb8127b3e9477073315cf485db6dbcb67b11ad9b085c075970807350d2a9`  
		Last Modified: Thu, 08 May 2025 19:18:33 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5591cfe14cd4b9c6b9f99ec4dbed657e1a4c5ea1c21929e625ad50f93170e`  
		Last Modified: Thu, 08 May 2025 19:18:33 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fd508bad56620d6a5185411692f6325285df9941bd30bba067a042d72551cf`  
		Last Modified: Thu, 08 May 2025 19:18:50 GMT  
		Size: 278.1 MB (278061204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635270dd37a2a5d1d20b33891917a7c8edce8f1b2f38e3e6733021c55367e385`  
		Last Modified: Thu, 08 May 2025 19:18:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:da27218f4644525abe2cc5972cb37293bf523ae0530e4dec996b26b6d32f4fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6616777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b8de4917ddba8ff6a368db78c13e5c00b49c7ead06fba7fd2f81ce4e7252a`

```dockerfile
```

-	Layers:
	-	`sha256:51142690f91f0c221b31be2baa09dc3b21b65f4df45750a8a19d6ce820ffbfcf`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 6.6 MB (6600422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d063290147b62afb386252f5b0c80a3dcadd1a411d70afcc6d011a8a5a0797f3`  
		Last Modified: Wed, 09 Apr 2025 01:17:55 GMT  
		Size: 16.4 KB (16355 bytes)  
		MIME: application/vnd.in-toto+json
