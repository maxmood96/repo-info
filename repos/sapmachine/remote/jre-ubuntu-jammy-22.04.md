## `sapmachine:jre-ubuntu-jammy-22.04`

```console
$ docker pull sapmachine@sha256:444664c989624faaacbe86492e89e61da9c15b931ff6c96317c4715c001c0894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-ubuntu-jammy-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:944d2e76e849dc840365ad9c9d076addcf373791190ebb59fc1d782d7f7a4847
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90106424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ee16c6363f2ceaf7954f533b375917719169b91e16dfb593f11ec45e5954c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 03:06:14 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 02 Dec 2023 03:06:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 02 Dec 2023 03:06:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c32c56003e6146bc32186350f4d7ebdf4d905faeb144682fb3fbbadee52a3c9`  
		Last Modified: Sat, 02 Dec 2023 03:13:07 GMT  
		Size: 59.7 MB (59660102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-jammy-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f9d3406acb4c3d7b59d6a965e5e7e284c67aa1d1f762aebf81deeb3070ef1af7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87145195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fb0a2de43223363f97cae36ce034c723290302427cc3fe35aed42669c4841e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 07:10:55 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:10:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 02 Dec 2023 07:10:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc04bbc492b9b7410a9c8599cabe64d9a4f12719baa4e6557224f8867da1a3a`  
		Last Modified: Sat, 02 Dec 2023 07:17:16 GMT  
		Size: 58.7 MB (58745256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-jammy-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:512f3bc6705a0cf9e435cef8192b25d83f9b023185ed00e0a3dd2c0d2bd9edf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96903666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a90c39394fe97576cbb4b95cbeb02979b4d78b84c61604560773f43098b20d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:29:27 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Sat, 02 Dec 2023 05:29:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7461c67158f8b105f545766f73c71ec99b9c2afb57d6b7abeffa7e87d735fc46`  
		Last Modified: Sat, 02 Dec 2023 05:38:42 GMT  
		Size: 61.2 MB (61240925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
