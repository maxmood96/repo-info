## `sapmachine:lts-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:eb67674ba8ee1a22c46e33af67bdee5baab4e8e6dc415cc38c96fcbfbde92f8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:22ac9f6c22ed4498d17943218c29e3ceb839e7ff8ef89d82bcc08e10f6c473a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86721323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40406f0870f4f15b06fd28453b19aba15702e5c07d3c77ded0ce2cc97449d8a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133c598a4b3e89edbdca045b7d6d722c920a305cf577cc045a05315c4925a430`  
		Last Modified: Wed, 16 Oct 2024 18:58:39 GMT  
		Size: 59.2 MB (59210263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b052147d722b7571fae545cf6309f1d87285bc96be09ce9a2fdd6c2e0da63f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484c8a832d3d2902222a428e4533332363857bd6312157a4bd5ce05e520a1a50`

```dockerfile
```

-	Layers:
	-	`sha256:8366f0ffe4c62db154145f77292da589525ca67c55b0ec2ead6c25e4efbd1bf5`  
		Last Modified: Wed, 16 Oct 2024 18:58:38 GMT  
		Size: 2.3 MB (2288220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d259b5599aab8e8993dded83f20a2026d1c7045ad85f09dba18182e3776315`  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bfb15fe9005da62a6064ff212e41374face507c55fe3f8ef701b3f3d31d31c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84319552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e75bbadbb8c6409471e5a2843c32c2099c641f3d43893c1f745173c12ab867d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c5f5705a5216bace9828fd0058c198607495077abf70a73d918eaaf110a`  
		Last Modified: Wed, 16 Oct 2024 19:24:55 GMT  
		Size: 58.3 MB (58345724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:51d3e654b5990ede5f21c87adc15931662bbca20653a35b6d2798193614bfa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a59b4fc045d5f16c66210ef5c9570b3b40a1ed40a92d815e478438826b536ea`

```dockerfile
```

-	Layers:
	-	`sha256:dacb035864caddbd70587729864821dc9c6b9c214702d3b68356d01a54b3972e`  
		Last Modified: Wed, 16 Oct 2024 19:24:53 GMT  
		Size: 2.3 MB (2287880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dde80cb01c897038922c3f9b132d6cf9c6f51bb03c018f75a6647c131fd27dd`  
		Last Modified: Wed, 16 Oct 2024 19:24:53 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f1b38d9d9676e9e66c55ee2a38a7c0f8df99996d6c55c602fa0ed0549e0fe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92475443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6ce12679ee71e1f52386b587ca3ebcb7d26fe6614f54fc0596312889256c6c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840d6729969e525fb0e5d014473dcbc0e22dd8c6abbbe72b99ad9a059b556b4d`  
		Last Modified: Wed, 16 Oct 2024 19:45:29 GMT  
		Size: 60.4 MB (60398937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1a29d720b3cf27a810aae737314acdb068f0693cdce85da2af84c6497edb3c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eabd70b0dd536d1f5c444171f8b571536f7c63ce30030b26160b37da0989aa2`

```dockerfile
```

-	Layers:
	-	`sha256:334d21d93f9b966fdb9eca55e50d49098e184ed3ba7a3777fe37a6278d323fce`  
		Last Modified: Wed, 16 Oct 2024 19:45:27 GMT  
		Size: 2.3 MB (2291997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be07c130b3d089eb5525b25f64bb5a2778fbc91284feb4c295b2c9614e5d4df`  
		Last Modified: Wed, 16 Oct 2024 19:45:27 GMT  
		Size: 9.3 KB (9314 bytes)  
		MIME: application/vnd.in-toto+json
