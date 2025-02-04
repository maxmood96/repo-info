## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:d80ab415c494069a5a23ee40d89847ce423ca87bab19d2d8ca807ba8690e14b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:cea428758d59e5c037558c4133b13dcacb1148e28864668c244d661b2523bd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5890398ac27e560d4c10381f256468967d8b0fbc6d76a82d310df4d15e9268`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065a20175c23251722dc4127e132e9ae13f1ec1800c748abd3b2e012ce4e35b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a25185edaecc67750bb55945a1d64e695cb4b3c7871764a02574e82be323b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efa89cd8e883848fd2477d5ca3e2dc77111a1ede5baf0624848f26dd3b7c818`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc894a399dda914031caaed968ccafa3fe58734e5abafa23738502812a6d384`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92cb62a10f02dcc605ce37e73ecb53e7933fd5d38ae3f4530603c0fa060d71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab4e963a55ae2118ceced0141383cc6656135531259fa2174092966efc2589e`

```dockerfile
```

-	Layers:
	-	`sha256:7f56d1ae5d6509efe4576574fa7ae17d8942e0ce6808254e404cca6591a9c9d7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cea103e1efcbfc9ef35081d135cc8fc06a943c20599f9f6896e855f14bb3d0`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d64f68ae17f5144e471f9a21a1cda36c1b06ec1f9b28334d51b36756f721afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40fc3afe6374d9c363c91f2623c230a34460eefc40c745d48d530be8be422f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c806577d234470cc5e1375c6c84e7102c2e92ed2f155ce9a119a4b67e98f9e3`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 3.6 MB (3557863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5dc9f05589119104912fa1a1717ff92659e13dab1440dc6b266b58957e5ee8`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2614b4bbf71177097aa4d12c46d11d7578598e10aa3592123e9463cdfb0e7`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2df2b4e0bcd2792b731ac676570a2eeed647f45c932ddece55a8243a41bca9`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 102.2 KB (102155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadec3f89a7e65d06897f8d31756c5c2b70d389671fc741c2ccb854732c6950a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b683ca6c0f1e2df2c80bea9c23df15d7ead46960c997d86d5ecde29072f03e7a`

```dockerfile
```

-	Layers:
	-	`sha256:8f17c09c31cf4b5cd87bde14628854326c2007d643625d168d5ed82a41251647`  
		Last Modified: Tue, 03 Dec 2024 06:15:50 GMT  
		Size: 2.0 MB (1988242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc91794bcf6ed620350bcd79c932cb607a78ee37e21fb3a7ac0cc318172128e`  
		Last Modified: Tue, 03 Dec 2024 06:15:49 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json
