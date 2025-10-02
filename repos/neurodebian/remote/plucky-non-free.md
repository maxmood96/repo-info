## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:218036880ecd9b532a7076745ec0080bbf962abd4f120667f2d3450a8f38daa1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d508fe986d017990afe7ba9502222462b7ca7975d100f89070fcd94390d571e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df631035a8910269b0d1ee636277f3ff3d59ca3b428d20118ee290216d2d743`
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
ADD file:286c37c491e2efd335e705645951733f957a0b2e5633494beb2f8518a0385b85 in / 
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
	-	`sha256:bf2a53a9f660cf1066700517abeb5a3412cd8e8f329afd700441bfdce24c9d76`  
		Last Modified: Fri, 26 Sep 2025 13:27:10 GMT  
		Size: 29.7 MB (29713836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57321cfb84455069af38560cc1a4000a168996104ddf290e6ec7d811b210f2`  
		Last Modified: Thu, 02 Oct 2025 05:12:57 GMT  
		Size: 6.9 MB (6862034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a15f4e730ed86a7036a7def4baf8b996875745413c75075d02706d2488a8`  
		Last Modified: Thu, 02 Oct 2025 05:12:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508057d818c12b1f7525295144bda4627ff572f6c262ed643b74972ef415407`  
		Last Modified: Thu, 02 Oct 2025 05:12:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a96b8f103065b18d019c0ff2f795fa1797fe3f1ae2212e04dedf81dcb218b`  
		Last Modified: Thu, 02 Oct 2025 05:12:55 GMT  
		Size: 103.5 KB (103464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e640f7e8ee180aece1d2b1a96c48cf7c56a2fa16f7ec65ab165543f811b3be6`  
		Last Modified: Thu, 02 Oct 2025 05:12:55 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2f1c96f302b9163fb315434753073cfc90c2291fe3bb3d030dd44cb09c78b56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0810a966bb26e6d0e836f5376f26032d3e6732fc3a30398b2ac67f2dc972d94d`

```dockerfile
```

-	Layers:
	-	`sha256:17cc98697fe64397496053535162b25185424dc4630136380c55053a9799a881`  
		Last Modified: Thu, 02 Oct 2025 07:08:06 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a835461d38896fba05d4ecb8d61a9d64028f0815a7723e61387d83bad4a307fd`  
		Last Modified: Thu, 02 Oct 2025 07:08:06 GMT  
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
