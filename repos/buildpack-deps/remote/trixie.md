## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:376a9eaa83e69141da7bb34d96318e32f48daba878e5a01d147d0c830f6c364f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3c52d2a6abfc14e39e9b15721269a151f5d457ffce2480bb49c69d96aebd4625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378717115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7766cd4750357a9c7e1e0c2352cbf36181cedd1e61c33a29f6129310600ab003`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:39:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793e3c6bce826c77a6bfec52e3e42691937f0e5701d8efa06d32850314d3f30`  
		Last Modified: Tue, 24 Feb 2026 20:40:19 GMT  
		Size: 236.0 MB (236030458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af317cbf97c3ad429f67acc373cdc5ea6a693606cf8b4952d6d3c57a8229722b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17218972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91164895b54fdac641485c33d85c8503f25a42a2e8af349bdcc1b9b78515c2c4`

```dockerfile
```

-	Layers:
	-	`sha256:99325ae869ee579ba17ea5c457506ec7f5f68760e4aa49f5351d7ebeb310c238`  
		Last Modified: Tue, 24 Feb 2026 20:40:14 GMT  
		Size: 17.2 MB (17208510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e031324271de6369c411645655a7f15122c40cec1d60d70cf2c261d5a300fa`  
		Last Modified: Tue, 24 Feb 2026 20:40:13 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9318275fe17b9ff54ab0b78e5b6ec6310a05e3b0989e24b26a3066a7fc52bc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342888317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82051ceebd3d98f64e1f998a1874b174badb0c1327ebe881839034d0771baf5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:56:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:15:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:18:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6c0530a0840df8a05679f77d095cbed0674c87160dab8f0e65ed5257ed4b0ca9`  
		Last Modified: Tue, 24 Feb 2026 18:42:14 GMT  
		Size: 47.5 MB (47454162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc237884c34f3f7758c4fcaea06d5eb8bbc53d28e124d2e90e646c55a9ccd0`  
		Last Modified: Tue, 24 Feb 2026 19:56:25 GMT  
		Size: 24.4 MB (24361479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667af045e313c4df4ebab8d75985bcd9590a6b8f2ba5798c2335e4044f0dd348`  
		Last Modified: Tue, 24 Feb 2026 21:15:38 GMT  
		Size: 65.3 MB (65318351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104518ec1f97effebacccbf9d0438c1fff0bef6004e07b9f85505e98f238aab`  
		Last Modified: Tue, 24 Feb 2026 22:18:53 GMT  
		Size: 205.8 MB (205754325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:57452a121abf231da243339adbb22cc919f4f371178a4dc940d52a8c0dca43ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16981242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ab49197bac581f6342bd4fb0956aca066939ceb87d4695f2f3fd952ea96347`

```dockerfile
```

-	Layers:
	-	`sha256:93e29ea05b2639b1c9be0bed3aa6d5bb557ece93cf8e79cc65a8cba3759a339d`  
		Last Modified: Tue, 24 Feb 2026 22:18:47 GMT  
		Size: 17.0 MB (16970708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083437a8e1cb6a4c0be17706b39ea58fa0514efb37d05a4dc04f5994ceb745fd`  
		Last Modified: Tue, 24 Feb 2026 22:18:47 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c8fe5c8e93c9b67cc6a0eb05cda2a5e7c738505aab4b1e262bd5c3cc347d2478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325411202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25754b2988b5be6562c07a10ff82331df8e6abb88a6fd0645589a2f27ea0c0f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 22:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf4b90de2b937492c4bacf02a3eeb82d2fd107f5038d0f566247a589e7f935`  
		Last Modified: Tue, 24 Feb 2026 22:17:23 GMT  
		Size: 193.3 MB (193338870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e3218808e3c0b19f6e0de0562e49b4a36332fb0a77a5f792cdab1900d0b3d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0a15734da44297ddcf8a3e56891280b5241611e8a3a653def12951a33dedc`

```dockerfile
```

-	Layers:
	-	`sha256:e6130cc206c5afa302172d25d0b551f1c71d7fbc29ceeeba5d33eff10ea7c85c`  
		Last Modified: Tue, 24 Feb 2026 22:17:20 GMT  
		Size: 17.0 MB (16976498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e80262fab5711773ff74caf9cc25ab4a0662a29224ebcf5d5d7955e22b77f47`  
		Last Modified: Tue, 24 Feb 2026 22:17:19 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b3173c7f0ddde3439da5cc46e28be57a0c26a121b1362c8f9817532f44a8c0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368425040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b818610d45f39e74a5e982ae1f531ce03a2a246a650baddc4edc6024a64f4a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:30:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c8c69ba46d9fc7a70eadebc93f11cafc4cb32146aeb3e3cb9076d26ba5ded`  
		Last Modified: Tue, 24 Feb 2026 21:31:25 GMT  
		Size: 226.2 MB (226163828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf82a4005de7c945b227748e453c1f797bf90d69c85f91ed80a10f0a917ecc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17303358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76db61abf99124c308342812811c72d93af2c4cfa6609ce09155f33854c17534`

```dockerfile
```

-	Layers:
	-	`sha256:044d008ae3cef078b13597ad6e6520cd61363e63f414d0cd07739ea13f92dcbc`  
		Last Modified: Tue, 24 Feb 2026 21:31:21 GMT  
		Size: 17.3 MB (17292804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5667276cd7c7387dcd0a09108a4921880a3ac029528aaa60ded4db921c705bf3`  
		Last Modified: Tue, 24 Feb 2026 21:31:20 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a58dcb5c73545180352c6fbf12b886d401a9e48559dc244f163c2aa8818c493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387506796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c145f9d4d1c9f39eb33a3f799944b7687d0599b2c1d9d4290d792a7b668188d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:19:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5feef17113a2aa83c39ec2ba574788a1b821bc584f7b08f61d771fffd3746a`  
		Last Modified: Tue, 24 Feb 2026 20:19:59 GMT  
		Size: 240.1 MB (240127017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55ee0f3a56b679ac91e999bede70160b21b97e8066bb3a3df3859f20a8cecb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17188537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b246ab1d442b8ae4ffd41af1c59aaee73c9b15d415e08a347fb348fd3a3028`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7697e6956995500c7c34776792c7b9fb54fc22b7c8de620782fbaeaef6cca`  
		Last Modified: Tue, 24 Feb 2026 20:19:53 GMT  
		Size: 17.2 MB (17178102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e69fe29800418d4038e3077852b9147ae657ce9c9c0cdb362f8a08a065e884c`  
		Last Modified: Tue, 24 Feb 2026 20:19:52 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32708b8aeeda716f7d947bc6ddd256b98c07fe9bcbf1e2421b687e03da15fde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384275064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27cd8cc2d656a994ad3bccc55d302ea5429d22df6f19536c53185de179c29472`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 12:44:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee79ae595ce83805d9060f1c610385dfe6280391251ea73a1f48c7cf8bcb3f09`  
		Last Modified: Tue, 03 Feb 2026 10:38:14 GMT  
		Size: 73.0 MB (73032214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7011848dd7a5865dc436775ea09207344e8392221f2687f313bf37e160ebf0f`  
		Last Modified: Tue, 03 Feb 2026 12:45:50 GMT  
		Size: 231.1 MB (231132591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fe4b60e394f3618e7362186ad74dbf57a20f7745b618d326d99d87e7d0b7305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17204561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf74ce93c51a53c6f1f567f6130325f901a52a6ec388892329e962c57f02bd49`

```dockerfile
```

-	Layers:
	-	`sha256:02ead10396132ccdd05ab6ace73ed70dd8e2b058a7ff564e3b57039c267f59c7`  
		Last Modified: Tue, 03 Feb 2026 12:45:45 GMT  
		Size: 17.2 MB (17194061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482403859159d56032ca97d8425ce99798399984eb86c497bc0a2ce22d465dd8`  
		Last Modified: Tue, 03 Feb 2026 12:45:44 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9797b95e7a8024e449483644bae75a9bbd5d7091549703e44b5800e705d990d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462311043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17b11e24b3c12f1036985b3f32b4864816154db90622b524b809e80cae72cc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Feb 2026 23:50:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518328709aef2ec161ee90f4be9eea82346936a41f7fadae6c748b8ca89b81be`  
		Last Modified: Fri, 06 Feb 2026 08:00:06 GMT  
		Size: 66.7 MB (66660429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dd222d089e5ec8525740a9773119127deb4445670cb55d9cfe85879ac17769`  
		Last Modified: Sun, 08 Feb 2026 00:05:56 GMT  
		Size: 322.9 MB (322920690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7577b747f134b7214bd84d83491fceb9642936d0b205180f15438ce17e720e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17275150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2e017b5634fd7dc8d0156d67ebb66a9a722a21a9596506832de14a192a7524`

```dockerfile
```

-	Layers:
	-	`sha256:4635ecb9cafc32287c5227aae8f43c49e3dbc32c7ed54766104adf7c3108dcaa`  
		Last Modified: Sun, 08 Feb 2026 00:05:11 GMT  
		Size: 17.3 MB (17264650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40058a65de2e659032b25c9f7bbd2b60dab483d6d45430dc7e6dd8bc0c1e9ad7`  
		Last Modified: Sun, 08 Feb 2026 00:05:06 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:90dd44caddbbce9d4f3f940d2300a52fb2e82ed51a8c67152562d5aa95f21127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351304847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f38f55b26943f94de47a6e2fcdc2af7dc49ea4ce80a2600821d6d823c3b9cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 06:14:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3c6a3ae754d274216ffbec3754da469ace4e7c5b6e8e123969f0516b4a968`  
		Last Modified: Tue, 03 Feb 2026 05:29:44 GMT  
		Size: 68.6 MB (68623115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef461bcc2a855bcca63ca1d51d438b861a0e2b73096c42b9bb7654c815665d8`  
		Last Modified: Tue, 03 Feb 2026 06:15:17 GMT  
		Size: 206.5 MB (206532637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c14a9965ac0f326069883337a470b10ad1cb89dfa944ab605316aa54778a04ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c3d7040be089ea8ca7b7011b9e4dcec205108d6d2a7f1fdb3f6e0d0d16f650`

```dockerfile
```

-	Layers:
	-	`sha256:99f171d42b622ac8010a76410822d19147bf79dceb2146adb2c77047ac78e0c6`  
		Last Modified: Tue, 03 Feb 2026 06:15:14 GMT  
		Size: 17.0 MB (16985743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded6dddd26068acbd6362f8a09be94a7d18dcd3201791e22eaf94eda5a718303`  
		Last Modified: Tue, 03 Feb 2026 06:15:14 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
