## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:bf8dc8bfeb47175df0d2a39a7a0d5a2abb5ca63577ad930351cf3a25833ea226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:a0baacf097d0049239acbf3454df41edbdd348183baca91dc7e84d44315be3af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79706671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27d8dcb7fa77ddb492b990ffdb18cc8b7f8303c70571cf0877040f351638f17`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:24:40 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:24:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:24:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ba84e15cdfe0760daa2ff222bcf12c3fb4ef88b775e31230f10a8dfd44e632`  
		Last Modified: Mon, 17 Jun 2024 23:36:04 GMT  
		Size: 49.1 MB (49140045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:84b5cfc630cd755a5ad4d44516df614235bb92201ff3b9079da0f97604743e67
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7da872d8192047d3a039d8492bb3cac4be6b3f9082f70abaae258773978661b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:32:35 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:32:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:32:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0465b52f5663bca6b54a0a62648261b5408646719e006c0e783295bbedcfdaa0`  
		Last Modified: Mon, 17 Jun 2024 23:43:03 GMT  
		Size: 48.5 MB (48457325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:69001537992761a09e099a7a608927145ca28503db9f42c45ba6e7a85c4b4f24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df0d4382b57e9c910057c3d2c825e35ba881dc41959483c678c7983e7846ab5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:05:43 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:05:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:05:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dad68a2ad14257805d1ace381acb6b00e827d31a92977b57b830b0a1cdaa34`  
		Last Modified: Mon, 17 Jun 2024 23:17:13 GMT  
		Size: 47.7 MB (47703190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
