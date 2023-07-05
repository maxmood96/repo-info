## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:bdcede44bb906fa2d29c3f7cf61dc4d65aaf5013349b4c60d424827df23ea3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:4ccc42cd4233ee6006569d4c77aae0f3f125a6550147bfa37608710ce976242e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233574571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32ea279f46a5075ece209459e0679b196448923a72291b3e37c1c1ef14539cc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:45:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:46:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 18:46:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b838b99d8d1d7a4b6183b65a978d447c802d540910f023746e99e4f76dc57b87`  
		Last Modified: Tue, 04 Jul 2023 18:47:03 GMT  
		Size: 4.6 MB (4614304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281360c02a410a2442426f6cd9cb72939a639eeb225e9b9e39c71940b8d15e`  
		Last Modified: Tue, 04 Jul 2023 18:47:41 GMT  
		Size: 198.5 MB (198529038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2f0f6a1aee75ef1675bf60136c377432a29a2701ac945e83167b5741dde45c0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230091366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18c74b0ad42d22fd8228e6046da6b34ce83c1618bb5f58c3b102295b66b8537`
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
# Tue, 04 Jul 2023 15:09:46 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:09:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 04 Jul 2023 15:09:48 GMT
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
	-	`sha256:e3ef3fb831ee6d2d3ce1723d07c70f13a5553b1c127538e2a4932ab3489ab7c3`  
		Last Modified: Tue, 04 Jul 2023 15:11:04 GMT  
		Size: 197.1 MB (197134330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0984a0cc2cafd7fb770f9244fb048cd8a58abdfd1c09c3356963b473ea7246ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240578188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70d1d922cb8d7e536911bfccb5637262ccaf7e305ea3a19cf4eac0b82edc482`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:26:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:29:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:30:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 05 Jul 2023 01:30:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39d3d1e722fb61a2b5412edf277c0bf8701f2469a1f8ddfc14768bc4bfdf53f`  
		Last Modified: Wed, 05 Jul 2023 01:32:25 GMT  
		Size: 5.4 MB (5381674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e203a18bba3f1a361fb7a304bede6e6369bb96037e9fbe0dff8c790b86a5a88e`  
		Last Modified: Wed, 05 Jul 2023 01:33:21 GMT  
		Size: 199.5 MB (199485045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
