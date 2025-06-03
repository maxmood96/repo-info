## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:4b87c2ce43b264d82daa23fdbd88fb1b5f1bc61cbee338eba7a41a47236f7b9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:25e1aea15f17963c8a998a40c3847044ac062d4ebcc9632c0280ceb2accf04bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249054275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e656c20912876635bd31eb41a0b45b24265979c570f5ad390621406b4916ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e524470d282633f4218fb18055b7a6aa7285ad735cc3f9ab2e51f1a3e8d068`  
		Last Modified: Tue, 03 Jun 2025 04:15:39 GMT  
		Size: 7.1 MB (7103251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d67d652a26d83b6f6ee5f37f93b5099977303a31cd8b5e537025af41ddaea9f`  
		Last Modified: Tue, 03 Jun 2025 05:11:40 GMT  
		Size: 39.5 MB (39485728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04536a8bc10a0c7823e6299236179abf5b7f86be8727eb9de0d872e5b3b227cd`  
		Last Modified: Tue, 03 Jun 2025 06:12:37 GMT  
		Size: 172.9 MB (172932293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e2edc1264c572385be34ce03782b66189d881657a07d61fa73de46bc4b7e144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11560225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cdf4cf0e1429a140231621ff1e239e54239cde347f2e9479709613b25d782e`

```dockerfile
```

-	Layers:
	-	`sha256:d95bf6c8a62df33846d9381e1c0521ca49d7769535e2eb537c384eba1a1a12d4`  
		Last Modified: Tue, 03 Jun 2025 06:12:33 GMT  
		Size: 11.6 MB (11550022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f62457477e3c37358adde517aa1192a248bdf880d2c9d1ce165df597264b1`  
		Last Modified: Tue, 03 Jun 2025 06:12:32 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f58417aeb5b3505ded346b977fed0e854fa92a58b85750a8d2b8668a5469fe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216270592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88652a2de31b72e698adf8cfec89b493025940353232c558a94a3d5362e9099a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Fri, 30 May 2025 23:34:57 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade18f0cb153eb0e80505edf909a0b5fb573468108f73d59398826c27dd2252`  
		Last Modified: Tue, 03 Jun 2025 04:15:34 GMT  
		Size: 7.0 MB (7007661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edfc049546e2833bbae11371047122a90cc58851d9baf3c81cf215428e6784f`  
		Last Modified: Tue, 03 Jun 2025 05:11:33 GMT  
		Size: 42.2 MB (42244551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fbecdf9700ff0462af026066061a3df6eea7ceb45bfa67d8188c3e205ef534`  
		Last Modified: Tue, 03 Jun 2025 06:13:49 GMT  
		Size: 140.4 MB (140377905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d8801bcfccaf49e89d9083905e5f288defe0fd150e5786230e2ccfc7d2fe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec8c77d8ca9c4c53c7d539485a2e0007148e7e4d1ea008e5c0da5ef8182d0`

```dockerfile
```

-	Layers:
	-	`sha256:ac2d479d35cd1c65d782b704ed23a0bc4beadad73d2244361a07830e190894a1`  
		Last Modified: Tue, 03 Jun 2025 06:13:46 GMT  
		Size: 11.3 MB (11339244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef2607ad17512e05a3167158fb3ae5515b193996702957b93643bb0596f3073`  
		Last Modified: Tue, 03 Jun 2025 06:13:45 GMT  
		Size: 10.3 KB (10262 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:19edb3d703bc5f0cda5cb55e1cda5e95405cd91cd2ffedb760ad51ca271182c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240156319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e040cbb08cf56fc76af759a52ce4260c32b087596e2c9b6c0c56aef79e54cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361da20f9ea3e84b4be3f7b9bd0c188ffc116b16329e2023bda5d3f8830133c8`  
		Last Modified: Mon, 05 May 2025 20:43:04 GMT  
		Size: 39.4 MB (39378693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051fdc3b925a55faa4d3e6cd93bf0c0edf77e963c6461a895815c1daef3433d9`  
		Last Modified: Tue, 06 May 2025 01:05:54 GMT  
		Size: 166.4 MB (166374385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:507d79e4c4e6490c1e3e4277548d54be3acfe811aeae33a6848cf9dd1a7005bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11461551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62b1eb60814ed0dbae2dd17399c39fcff445376a90076824aeaf3f98475b688`

```dockerfile
```

-	Layers:
	-	`sha256:15ddea20e6e55148fd9cc4794397a132025a4166d5d4fa3736726c45912d3c6e`  
		Last Modified: Tue, 06 May 2025 01:05:51 GMT  
		Size: 11.5 MB (11451268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f3b6a84bf75b72262e77a6a1df770c03326997ab590fa7ae2b0ebb01450597`  
		Last Modified: Tue, 06 May 2025 01:05:50 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:03791b8399d65f98c4e860afa8c8d650a0d0d266da66e1ce98004e9bf8035df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269772643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdbbda1812ff9778e311632acc52f4c13eabb35f791d2bc2916827edc71f631`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5758b64feb475315648569dcc19f6eed14e004ac6509fc2bbb6103a5d796c3`  
		Last Modified: Mon, 05 May 2025 16:34:42 GMT  
		Size: 8.2 MB (8180679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3889a4754b0feee9a228b59fcfe165963f32939c591cde6e313e5c3f0a2993e5`  
		Last Modified: Mon, 05 May 2025 18:52:15 GMT  
		Size: 43.8 MB (43767061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acc435370c049122210ad90e118a421cd4a5255b84d96ff394ca409b98b079c`  
		Last Modified: Mon, 05 May 2025 21:54:52 GMT  
		Size: 183.4 MB (183381688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6211478f1007990a00cc533f4fb783756fceb9f01cb559591c09488ed35e1f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11424649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bfd761412d39f086e1046e924130c67787363165b35ed83427698e1a30778a`

```dockerfile
```

-	Layers:
	-	`sha256:76d890a277afc4775afe4eeee921fad9c364a39f3e15b0a8af71bffb3fb92d5d`  
		Last Modified: Mon, 05 May 2025 21:54:47 GMT  
		Size: 11.4 MB (11414414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08033f7a4f12c1cc7c5bd13a4747395a03ba1d0bf01e503fe36e3adb60c05bcc`  
		Last Modified: Mon, 05 May 2025 21:54:46 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1635385d5bf3bd7cfd579a8618ac538a0056f62cc916ad763f4b331a942812fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274233698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653b7617beb5e0788d27b8b9998b3d50a785b51ca8b05031918ad85eb8456e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:a912be2a3089b5a563b27ae9282741b713c9ece03916c09152cea320960e7562 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47a929027d1fdf0b4cd10889cdea1d02472669c913e59a827d925ddc426e60b6`  
		Last Modified: Mon, 28 Apr 2025 10:44:10 GMT  
		Size: 27.0 MB (27039778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659e4c4181f5ed1c99b778be6557f6506e560b5c7fbdc1c6c9e734912d6bb34`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 7.1 MB (7115958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0226ea590af05a88ef22f461bc56c43e6f6c54c4dc9c53a2444b6a16746a684c`  
		Last Modified: Mon, 05 May 2025 17:06:47 GMT  
		Size: 42.3 MB (42302846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9064f1e8617159dc1959893f72653ab0d924b3db6109efd0c2f26ababff39`  
		Last Modified: Mon, 05 May 2025 21:06:20 GMT  
		Size: 197.8 MB (197775116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec8a1038268bc20407cd8146e298335a94f3cbbab65939a2ee5672ed861ceedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11407701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a20150e82c3288df37a532e978624bce1cb9831349f595dde6f3ca5eae5774`

```dockerfile
```

-	Layers:
	-	`sha256:7f1b682ab41c8562ff99bb619ba732d4d04b19f3fad50f3ef14074340b54e4ef`  
		Last Modified: Mon, 05 May 2025 21:05:55 GMT  
		Size: 11.4 MB (11397466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a46f4a052555f9d4b7127705e764ba2b896eb345d59e3847132278d769f6939`  
		Last Modified: Mon, 05 May 2025 21:05:52 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:87aec182a3916dd3e7d9d5791562a5b21a04997910d031b103f19cae6d99e191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223036474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af778d8752c852ea5f36996c5d06e9a7ba0e697828690d9369c2ca511196e4d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Fri, 30 May 2025 23:35:16 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d72f21f5960e611ba62223730c2365f458813d47dda4f15dd2001615e7599f`  
		Last Modified: Tue, 03 Jun 2025 04:16:02 GMT  
		Size: 7.0 MB (7014114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2065174a163a6718c68496123e0640ad969ccc9010c78f9bee48547a2aeff9`  
		Last Modified: Tue, 03 Jun 2025 05:16:01 GMT  
		Size: 39.4 MB (39433827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5315ec1b80ed4ad35833b129997fab3ed9770d529eb57240358009895391b2e`  
		Last Modified: Tue, 03 Jun 2025 06:57:10 GMT  
		Size: 148.6 MB (148587933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e0cf54d68cd94c11d7119f026f1883ef632b0455ae3ac6aaa22a7737d02df982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11374113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934e34c65639c6afa9abafdf36ca756e220c441e1eda297ce9b5ddb6e1503a02`

```dockerfile
```

-	Layers:
	-	`sha256:80dbc6195fff0b503e78fcffd04847686409738e816fcb5156a4e055c475aa8d`  
		Last Modified: Tue, 03 Jun 2025 06:57:08 GMT  
		Size: 11.4 MB (11363912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb41e97cd2d512b47f0cdda40de711da480f865e1b102a13a15fee6d6186fc53`  
		Last Modified: Tue, 03 Jun 2025 06:57:07 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.in-toto+json
