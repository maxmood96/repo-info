## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:36a6152d992a615bc1d11a8506cd17409184b210bc8b0d57ad3d0fd677afd9c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:50332ada0faa254b85fa3c99a2fb1022451d84260772392e0e6ae137e1769632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324940094fa472191de171a4ba863183350cf4d1a1e43ccc421a71b66e094cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d862268cca33b20dc33b79c6e362573fb742dcd42a2c8a20009493450369ddc5`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.6 MB (3622702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7004f9084ccb849430b7c98f8ef2eb567e8caa461377671d0ac1aba06db6d2`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f70324bbe5ab5ca9fd0e2cf5ea3b95c81703e6cd98a5b415809ceb4638987c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ced8e730e6d5dd8769cd1bdbbdeb4d189659f419d807c42534b5d3654f8c48`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 110.1 KB (110097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f4826a37a310d849e4c83b7f084dee6af9a823f43d94d62ac6a708b6ec638e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326f94e3b16867754bfd251636fdec9ac49e83e1e1cb329c204511c7e7ae1dc`

```dockerfile
```

-	Layers:
	-	`sha256:7246425b0d75d34d4e317919e463322149ad3be8c5ef7e9c58c8dc4712ece091`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 2.0 MB (2015659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ed2ec0795d1e6759f5395fa3f89dc5ecae1e9b4c754824dab0613aa1226807`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:182965a2a88e752d9531ab95095ea3f137ec86496b97f9e82a9df5c92f2338bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0020b4b6b75f3fda2b2fd11190ea6b59ae189b71d7fcd254bb3e3df2d195a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3daf4feaf8b1af264759adfc71c17d64177646bcff852e4c561c28ee3ab4296b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01233855c07d4d99141d81865bfe4168def1876fa3a1ef37be11dbdf4b2281`

```dockerfile
```

-	Layers:
	-	`sha256:b5128b7a8311295bf17b1da5ff28149668958c562a0f3982ea7b363c9a9ee90e`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09216cc84b65a36876b54e5c68b7ad1aafcc4a002ac17e4e904429aae09512e6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json
