## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f5d9e4eb2386f494cd13dfbc0a4dc51970e01822bb0c7566052b1d43da3f9a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7e0a008b99a64a8489a54b6198dbbbcd22c1d90ba0346994e7f9910f7fc09390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79828728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13543fb9f30104399314e94c75ac0a996c65e7d0c1403dfeec9d6c17c16ba4ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Feb 2026 20:35:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb2a2cbaaed7a63c9976ca70a6403e9e31ca97ac3cd82705336e78123a46b5`  
		Last Modified: Tue, 17 Feb 2026 20:36:08 GMT  
		Size: 50.1 MB (50101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6eedcd33215b1aee0a246a31db05f476f2ef1c9787e6f81132bf0f566273cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73060177bec2f4236a6cb1979b1d6c1f1dbc0dbab9f73d91985cf8185b19dadf`

```dockerfile
```

-	Layers:
	-	`sha256:8c40d5a3fdc567be71c2a45e8d7d5027ee47826e1be2ac5562104577c6993ed7`  
		Last Modified: Tue, 17 Feb 2026 20:36:07 GMT  
		Size: 2.5 MB (2523645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6429bda4d8f8fcdaee67caab9ace7b8109065ddf3fd7ff616b888a33ceff6194`  
		Last Modified: Tue, 17 Feb 2026 20:36:07 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json
