## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:860480ad29d276fd2a4ad492738e5eb7d3b7466505c69146bd983dfe210d13aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d1a16f4a7789c0fa50e05f3820f819b5229f9edef5620172f8bcbae486577f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad82263189b9ddb0b4a213ef9a88bea88681b2a1b7b5ea17c78993ce6628908e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:59:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c353de522f5bf7730064fc02df9ca1a7b840cbcb8260acd278a06a132b92ec13`  
		Last Modified: Tue, 07 Apr 2026 02:00:11 GMT  
		Size: 3.6 MB (3564644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9902b56decf65c99d207e2bfa35674e7dba325bd945e956360622539e4a8f`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836d6413083202467f9df4f69b72a9932be44b96e58826746cac34f2d617b4e`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a27a2093d1d11303a2baae2fbb490e05fb0b6d1507f222e20019810f15a3e1`  
		Last Modified: Tue, 07 Apr 2026 02:00:15 GMT  
		Size: 104.6 KB (104552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ba3e07af16799c418b33c90a5f2a546656d6d3a05623d03ceba4382dfed4fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca1e85a85595e151c30cc576e3a1e530955df573e022248324dff6565846e37`

```dockerfile
```

-	Layers:
	-	`sha256:f141df93540a232a857921deaf6e34d6410a39ed42b962280edcbd5f569ae45b`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32c27b98bc907d2799b42d5c9d8d5d79ae54a89737da34c53f4f618032ba9f1`  
		Last Modified: Tue, 07 Apr 2026 02:00:09 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8f94a7902924b33b11cd397567eecd55144942719776019db2a3ce38a16a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32544146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefd438c90cab87ca61c9333a730956c6588e14c4f048d0e0d64dae9299ba915`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a95b347de9e182f3fd87861cb7a8e9ed1fbed7c3a0525130b13c6cd4f8f3d`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 3.6 MB (3561832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63356e459d23ac85b9482c640aeee2637e648f5345cac58f22b353c015235695`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e685769f3ff6ae1a435c2cffac3d43e37d1e4de266dfac553c66102fd1925`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93dc91c1c65bfa3afb57ffc701a23f1eabeac94cd51d24b983cd3741e6678bb`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8a169d4bf32620832e2b29a8ff5797625e29aa64fd04fb758032bf9c29cbe386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb754eadc6baa9548b6bcd1b4b95eb958be3925bfcc5776bab0af72b07aa69`

```dockerfile
```

-	Layers:
	-	`sha256:e2b613a3a815688d46603d5e1217679bb9e29db75b5a97a47f71e81ec97ccb74`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b88624234200988b8d416085ab7877b80d0dcfeea382e619f5bc3dbc24f584`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json
