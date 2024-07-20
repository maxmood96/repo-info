## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:b63107af3baf8380ae00f911acd54aaefb9b73b0e2de7ac8ac23ca3390219503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:25dad96b28822fd69f861ac2c3a4618bc49cd98eac502121bbba3dfb8553cce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79558280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213c047926cf6ec11497eef3b7ea17a22a760983f7a182314edee2ea4b669212`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49eea862c58a1faf925d8296a26f5f75bbb95175a3c1e9598b7a4c02f749c55`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 52.0 MB (52046511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37c0e948ec16d8180f22f156ce4adbbf5ea56d6a951624aa063c1a5cf8c1743d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81271dbbda13f8b955d14ab70c025346f847da17ec674608051326f3bfa1e206`

```dockerfile
```

-	Layers:
	-	`sha256:181d0b897c45141dd48ffe704a93b2aa597981002bd3e946af6755292e3041c9`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.0 MB (2042354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70722d47237c4bad0dfc83d002f2b60f10b93f8e2dbed06ae137f7457bd05d7`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3bfe6d63f842fdee3b44735b0388e7aa2c01dc1bdb506a60fb5875dca0e81c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77399541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01426d86f2c51b217ffa99eac6fe389d2bd60a1dbbe126e3a5c8eef897492079`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f517394c11f3987363186cbf1d4f7259abc3ac613fe2b254585d7d1e984bb73`  
		Last Modified: Sat, 20 Jul 2024 00:33:24 GMT  
		Size: 51.4 MB (51425324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6e98a16971ab7cf9f4a1f4d7a9b6c5e76a32ac04b96364bcec02f9b28673e64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2050959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5406f64098d27456e91f033946ef5ed16d1a8708f7f9d3f5f5fb4e375f53df4e`

```dockerfile
```

-	Layers:
	-	`sha256:77f640af66f8d6d9927fabd7404757b522216e64b7725f0b1095e4961639ee15`  
		Last Modified: Sat, 20 Jul 2024 00:33:22 GMT  
		Size: 2.0 MB (2041981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1382e1be8b5bf010ae4eec28903e89fa986fb52e82fcf8e25827ea6cc91613e5`  
		Last Modified: Sat, 20 Jul 2024 00:33:22 GMT  
		Size: 9.0 KB (8978 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:718009634526a449b147ac7b5fbbbab8cc86a64cd585489eaa5973b9aaf9583e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85075597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65253bee11ea906c64ccdcdde05b90795eaa5dcc3135111fdae7537525108c58`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa68f7235927c8d46497cf4313b34df3a98b3015d25265f4e4806055213b219`  
		Last Modified: Fri, 19 Jul 2024 23:48:55 GMT  
		Size: 53.0 MB (52998457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c59d47ae0373d389c12af1ef6dc97d396e25851f46de17bbb3766cd4d4053e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1bd2ce2c4aaeb4f61f3062063f1d04f97dbdd52c58dce2b6c130f29165e566`

```dockerfile
```

-	Layers:
	-	`sha256:c45bee9b691a5d6850a122d522ddd00eba112b31f2eb773652560ef65f42d068`  
		Last Modified: Fri, 19 Jul 2024 23:48:54 GMT  
		Size: 2.0 MB (2046056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3bc5a93ac3974a970a9d3f83206d5bdb8813972eb3c6ead5fe3a981e3d12ab`  
		Last Modified: Fri, 19 Jul 2024 23:48:53 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json
