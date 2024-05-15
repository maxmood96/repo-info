## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:da4feba6632cc66107586787d7a329637d5c2627ef9632d899384eb704114014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e0960cf9cdf8de93faded87902be68d0ebda45f37694f88dedf8e432fc9ce80c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88017261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bafcebafb661c4aba85ca19f7aa43b20a982416926b1319fa5ab5f573dff39a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:30:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:31:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 May 2024 22:31:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128e49877b6dfae04240769b86fa60b5546ab7be277f61b71e5662321b35bdd0`  
		Last Modified: Wed, 15 May 2024 22:37:59 GMT  
		Size: 59.4 MB (59432962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e024b2c1d37ecbef5f595f82768cace584f1e6fec58418b7fa7df6b332382ca3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85718347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642a6f86f89b7834c0c8490d14d935e1db9adbc87de796b3778a221b432d98f9`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:54:32 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:54:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 May 2024 22:54:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae8678d47aea529fb3f9d419afd3d6fd06aeb6c5968daddbc3ffdb067e48cd9`  
		Last Modified: Wed, 15 May 2024 23:00:49 GMT  
		Size: 58.5 MB (58512202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ce018dbdadb151d191ed14dc081688cd4eaf3205e11b52a9ccc527895040fcdb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93918032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ed2860fe05d0ad474c95a26797188c15a57c55677e6899337d08123a18d7e6`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:02 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:06 GMT
ADD file:de463dcd7b30faec6d782106816b443697c99747238015d4d992786da4888987 in / 
# Sat, 27 Apr 2024 13:33:06 GMT
CMD ["/bin/bash"]
# Wed, 15 May 2024 22:23:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 15 May 2024 22:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 May 2024 22:23:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842f501e2541cf3af2b2c183cb8bc0e8ee178240b7a31e44ca04a5741c69410b`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 33.3 MB (33316011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c0328aeaf3f9f8931577441e96c3ff7ac2927296f371ff83fef70cf7ac2272`  
		Last Modified: Wed, 15 May 2024 22:30:47 GMT  
		Size: 60.6 MB (60602021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
