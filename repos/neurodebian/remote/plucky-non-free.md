## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:5b0c2a225e6329dab3acb4204dc19939b172be86d3b4fb466176333671ef8da9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f2fd2053ab55f4ed0f32335cd7c408a2a49f774023796246410732e2d79eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36684222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e54e1b72b1b30dfd9c532e8cedb42616dae141eaed43398938bea205f04224`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:06:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:06:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:06:32 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:06:34 GMT
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
# Wed, 10 Sep 2025 05:06:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300d91a073c3de45299a9951ce458fdc9dd0726ebe2c3484b0ff2b4a6ce43272`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 6.9 MB (6861937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b0123d6642e0a554854d25d43ca72c8ea91e97630087a39c5a4cf6f6f487`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a00eac3b2ba933fbe20eccc5fe7b75d3cf8676fda517a051e0d52e3b6cce80`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8e3a01396d97b5dd266fbbebaefbe15a336d9ccb6ce73015849692597622f9`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 103.3 KB (103346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ee462167714b0d2d3cde489b2babffa0c01dd6cc4f746da5d2d32faefd9d7`  
		Last Modified: Tue, 23 Sep 2025 19:49:54 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:783d45c2c26278b7ef6837b4aa2d8450c7aced352f4adc6a86e6e162015c2690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b704a6d99a8795b326f247b27fe8e4096b5a24720beb22bbc2b523beb3610`

```dockerfile
```

-	Layers:
	-	`sha256:1b8f8c6ce03fbd59ba66ffd5942cb9d76560076191400c1af5f338dc04d20586`  
		Last Modified: Tue, 23 Sep 2025 22:08:32 GMT  
		Size: 2.1 MB (2129383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0672d816407ee45341f651895fc66f5d7f8df58f36f013d6b0d6885a4c25bd`  
		Last Modified: Tue, 23 Sep 2025 22:08:33 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6610a796644c77428e638f20adaea39e1b352d6df81444cf240b550d9fcc39bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34808280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace4d2fd78a80fb2cfdbb5dacac0c27ef015fc81fce8a4a581a90ae622f77a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:27dc1d8469805e72ba7acb716a3ad7a458b855b3d087a6a329f89b7984665276 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cdaac74006805135fbc40fc717498e32e43f548eeffe2ebe7f6969c6793b30e3`  
		Last Modified: Fri, 26 Sep 2025 13:27:11 GMT  
		Size: 28.3 MB (28308681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f1c25a7007bec82384a2d7b07ce825cbf93fed2b8d5ddf5b79684341db23`  
		Last Modified: Thu, 02 Oct 2025 01:27:59 GMT  
		Size: 6.4 MB (6392231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596143ba030519fbeacce5f8028818d0023b3955641545e7d02c75e6a3c2636c`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333214f1cd6fdef7b238200911fe3f2767cc558bc2aaf38c6bee3f9c0baa65df`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc9617dde3e2759df04f681b1f7813356d3d79dba0d30a8553f82fd6740843`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 104.0 KB (104030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030e59682cd05fb69799eac290fd97eab1237f806966583ebc88a6cd4e931a8a`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e37121db5f0632df5c979126b26e3ff7dc2b85092f31c99953e6013b2e7fde2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35eb4831e0fabe4b2f4f385f3cd447a01a9205dc79823808321c0eba3fd28ea`

```dockerfile
```

-	Layers:
	-	`sha256:a55c84bda7f22c51d223cc14def8f0de9e350f125007252cdf37c9af5d9a5ce4`  
		Last Modified: Thu, 02 Oct 2025 04:08:09 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646d2405aaabb4226273d83bd22d655e641bbbd5c5da52281d759e07884441e0`  
		Last Modified: Thu, 02 Oct 2025 04:08:10 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json
