## `sapmachine:17-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:35decf39d284200509f9d624bc4920196f3cf478629ddbf597b2dd463544354e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a0fe5e5afd60007d3b7e0fc5c5080c76862522f1ec04539efdb36cdd5264e971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226873797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1056a0783b1d4a2861efa9f4960dc26f0144b9de459428e9ea06caa45a7a14f`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc449285f291602f892b16628845399bc8fdbc3a578e6064947a4baa9f692c6d`  
		Last Modified: Wed, 16 Oct 2024 19:00:18 GMT  
		Size: 199.4 MB (199362737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25120453d0c49fa41234e7001fecac1b1f1d7f325599ab3492d2971cfcef0bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4b4d9ff58076c64e55f4747b49952a6b909e10771fb669ba199dd1f188d455`

```dockerfile
```

-	Layers:
	-	`sha256:927bc1376bf661447a1d485ed881a66cd469e4a6ef289ed69a81e1e133d96a47`  
		Last Modified: Wed, 16 Oct 2024 19:00:15 GMT  
		Size: 2.4 MB (2370655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efbe551f07b533bad35f1010e80f7642299fb25ac2dc779a55eb5cb3b84e7c8`  
		Last Modified: Wed, 16 Oct 2024 19:00:15 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:648876230d7bfbc9ebafa87b2f84973a390d6ba6e7c85d10fb2f684b21cb36f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (224041383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a2a6aeba29d35eb3dc3b4d7b55374322a50c601423d4fb37af9b2112cca581`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebbfbc401d840288d0c765d1d861797e9beb27c04a0bfd42467da72ed75972c`  
		Last Modified: Wed, 16 Oct 2024 19:37:41 GMT  
		Size: 198.1 MB (198067555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c82c865b7e821f53cba8f1907f884ebce5e702c0f974ee8cdc72c27dad5a098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76857bbb24dddecae1ed00724400dee5c3c41327c957f8f92bad2d3a0c64c1c8`

```dockerfile
```

-	Layers:
	-	`sha256:46ddffb969f02e7ccb46c02ce802f1baa79023fa034a30b9e73cdb8d48f018bd`  
		Last Modified: Wed, 16 Oct 2024 19:37:37 GMT  
		Size: 2.4 MB (2370339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01d451e210ffa2396050dc26a4654b5cf69bc7cf5e3b7beedc89d9ea2cbc6da8`  
		Last Modified: Wed, 16 Oct 2024 19:37:37 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c9b68046200ca4e40b65f1fe909826174c773dcac6e7457d342bbb330752d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232363314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfbb47fca5182c2a570e392b959db3f3b4f805dee30f81144a93fc0d2062ae5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a6c49495a3009db137cf141f4c6262cbe134a50809aac40919a5737fba3f8`  
		Last Modified: Wed, 16 Oct 2024 03:03:43 GMT  
		Size: 200.3 MB (200286808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6bce7332fb7b2eeadaacc778b7d0877986039cda87196dbe8e8bccdbd52219b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15380992ca60d1a048c19f6eb85a5a83a7bba333adf6cdead345131cdce91048`

```dockerfile
```

-	Layers:
	-	`sha256:5c5d4cf3433371786f86c00866aed6504e647d0e22ee3c70278417b20672d16c`  
		Last Modified: Wed, 16 Oct 2024 03:03:38 GMT  
		Size: 2.4 MB (2365849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fda4029c1aab95c121e813bcb07799aa1834d1d9508f589559964292cb3f1ce`  
		Last Modified: Wed, 16 Oct 2024 03:03:37 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.in-toto+json
