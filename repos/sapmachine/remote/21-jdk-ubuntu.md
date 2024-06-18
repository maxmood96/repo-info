## `sapmachine:21-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:2355e28772c81e1dae45b90dcf27a0479c432bb342d16246c985219da8ac57a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:21-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:5a3aa0023727647109693bbf632e0b83a1900edac51f3837dac3c624747d99fa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246023470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a2fa4dc0fed60680fb998818ecbf59a15e761c5f108c9ef80b31613efed6cd`
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
# Mon, 17 Jun 2024 23:18:34 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:18:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 23:18:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de44c14fa70ddf63252b0cae7a2141bdbf20da1144f121287213ee8f5d90e71e`  
		Last Modified: Mon, 17 Jun 2024 23:30:13 GMT  
		Size: 215.5 MB (215456844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e84dcd008470e551c72ec95afdbe8a2fa5952f84a94c232bcf5561c6eef48f23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243468210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7653222c7de8f8a22bc651cb2691fc16dea1b2c03a04ac5faac1c3692b504fa`
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
# Mon, 17 Jun 2024 23:27:49 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:27:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 23:27:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88a9145a93588cf400771b8ccef8e27359bdfc30d0d7ba0fa748eecc20886e5`  
		Last Modified: Mon, 17 Jun 2024 23:37:36 GMT  
		Size: 213.6 MB (213560230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9661f11c7ee40b17c402e9fcc2507278aa8ca89850f44728c4c5400f6755cc9e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252542419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085073298f1e0734310c0161e86905ab1d39648e7233a665a0f115d043a3b74d`
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
# Mon, 17 Jun 2024 22:55:44 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:55:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 22:55:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d03952f1ef0b93942eb4a115658ba187c7c63ef5e41c36c631306e050f50bd`  
		Last Modified: Mon, 17 Jun 2024 23:11:03 GMT  
		Size: 216.9 MB (216915461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
