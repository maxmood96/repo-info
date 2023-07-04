## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:1ab5e29b8afd84abae9690722476acf11cb1a7bf57d8134e144eb8c5cac1a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d7690f66016cd5970d3a380c7efe2637dfc73cc93c8d8c3fec62832506976e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243224748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cace1dd9cf5b16e0221c5e29f1dd8f11f63cd06e177052a6377070969a9091`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 04:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7c332f40b32439b131d434ea8fcdd7b6e4822a2709441b2d7fdc45c54b01eb`  
		Last Modified: Fri, 16 Jun 2023 04:14:07 GMT  
		Size: 208.2 MB (208179496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:089d0731d89d4e375fb569e7093c6fcb7201d9d2364015c232d602c9ffb4d723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239407111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d512b6e06b04ac4a9d06e38886610b3aea9ba598f43a672a6ecc7738a7774c76`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:08:51 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:17 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Tue, 04 Jul 2023 15:10:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e6ae4b22365aba9e1da78c480e020f4049ecccd5354bd654afdad59e5617d9`  
		Last Modified: Tue, 04 Jul 2023 15:10:34 GMT  
		Size: 4.6 MB (4566025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ce2a52a21f2e3597ed1d349ac03b32d0606d2a6d9083b5d907a7c197b786d2`  
		Last Modified: Tue, 04 Jul 2023 15:11:25 GMT  
		Size: 206.5 MB (206450075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7048a59aedff017dd2ac831d5f2fa807a656a4a5086c5d34b183de305fbcc3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250460067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c39d18a732192c330e58064b153ec3052a8e37cdf85a138887b754a564b893f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:33 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jdk=20.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:44:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Fri, 16 Jun 2023 00:44:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c669e2fd2913360cb59c8c4e1880f89bad52febcf63d016452c264375b1139`  
		Last Modified: Fri, 16 Jun 2023 00:46:34 GMT  
		Size: 209.4 MB (209367124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
