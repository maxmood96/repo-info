## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:662247af5e1c6be0e441fc44b39e7d6de544ec452611a31ecf8df88b6e9b0a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b7271e4c465c3fe1dd4caf5665915e4de5c37ba8cb0b6a693774e7413043349b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321494235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31f6a54f55caf105ab90b9b44c7547866806549d153ebfef97c82ee9e476d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:36:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512e35a226296c3166e8ce55b556c5fe6daeebccf71cdb13eccee234e17765e`  
		Last Modified: Tue, 30 Dec 2025 01:23:49 GMT  
		Size: 54.8 MB (54755226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a02f77a11e56b83bcea519986069889a0de4be2bffa5e238ee4e26de179464`  
		Last Modified: Tue, 30 Dec 2025 02:37:38 GMT  
		Size: 197.2 MB (197218457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba9d8857066517322b181af5a20814bcba9343a031d2bbafdc606411174bfdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf8f5492fb4b46e8e9068539b368d3968e30bafd24f5a3ca6545ea9a017b527`

```dockerfile
```

-	Layers:
	-	`sha256:5d89e60db9bd88ab6d4d3f3a6573186ad31a3e8c08ad05b7998eab3e4a73b686`  
		Last Modified: Tue, 30 Dec 2025 05:20:31 GMT  
		Size: 15.5 MB (15462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f9edfeabec05c8e06417f2004a2288d230f688dcf1184b981a6107f34cab00`  
		Last Modified: Tue, 30 Dec 2025 05:20:32 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7f4b86cb9ce87e815697138365fa292b6eb09c42b2bf3298c684cbdf5aadf922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282201056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe85506be204b13c54f391208e710ae66d376f2e8b6d15130bdfdb468ea35e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b46683c1e86f7a120aca01c56dfafa77513b188a88759ff45f42ce118f9a337c`  
		Last Modified: Mon, 29 Dec 2025 22:25:41 GMT  
		Size: 49.0 MB (49046401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf8c40ad8b4e8cd6362fd57fbf345b792e3a334f7cfacc579cfaeef4447f6`  
		Last Modified: Tue, 30 Dec 2025 00:34:10 GMT  
		Size: 14.9 MB (14879533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318980c2ab1381876582d11a8701c769d018a68765de938c093203d5fb485b94`  
		Last Modified: Tue, 30 Dec 2025 02:06:57 GMT  
		Size: 50.6 MB (50628825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e20ad9034e29b862e54139afb5ad3088a0eaa66ff57507e0c966b81af518ed`  
		Last Modified: Tue, 30 Dec 2025 02:35:52 GMT  
		Size: 167.6 MB (167646297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7db7e8895f874e2b6c9ce3ad472e22ee7a4901f41eff002cbedc779426cbd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12762b60c57c6895521096690a4f942ee97afc9ebf663f4819b44dc64a00611`

```dockerfile
```

-	Layers:
	-	`sha256:497acf42b1e2fff9c11969ce770a093eaf1e0585cb4fcf01e5942db4ef943fca`  
		Last Modified: Tue, 30 Dec 2025 05:20:47 GMT  
		Size: 15.3 MB (15261544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637d118c320afe6131d23f971dde633cf22fa8ea6e20b1935afc5cfc464ece89`  
		Last Modified: Tue, 30 Dec 2025 05:20:48 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c994f004b8184d846ab13f92099c2deb6c7ebf584be2187c70feee95b1aeef83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312984232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95c413275bee0a030ec64b6d29c6a9ee258a22d1ea186ee12b96cc7e2b3461e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aeb16c8cc7bc154fba2dfa61907bbdbcc96a5a7b348a6376fb17c7ab1fe61`  
		Last Modified: Tue, 30 Dec 2025 01:26:00 GMT  
		Size: 54.9 MB (54865435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821c1c97ed0c0b535fe64f1b97780f9f62fe5ee7181cf3046d79708952fd6a6e`  
		Last Modified: Tue, 30 Dec 2025 02:36:37 GMT  
		Size: 190.1 MB (190111646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de01094d9ee0d67a89372e807ae24d7d0d94e95af133850da65fec6c1034ab58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cb882a524999dc28c76517437a88289344d197232fcadd78835d749719f2ba`

```dockerfile
```

-	Layers:
	-	`sha256:1e70fc91b32c4963d78666382fba5dd7fb9899862d0c013f74a4cb8ceba9e253`  
		Last Modified: Tue, 30 Dec 2025 04:42:36 GMT  
		Size: 15.5 MB (15464171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a524044dc534203c12e90d9e7b7391c8da4b02d31101a7c5e0bc4e063be6ada4`  
		Last Modified: Tue, 30 Dec 2025 04:42:37 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a5ef1072653db25e396cfc0d685a4819b0c22e02cd579ed834f33d895e168b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327129462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a06d72fbaeb914200ef467b3dd4110e4c2ddacc8d2b4830ab7a514dafd3049`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:42 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:46 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad7ad875273afc9f1824115dad6d50ae84fba747da8a0b124f82d730bcb8bae`  
		Last Modified: Tue, 13 Jan 2026 04:23:38 GMT  
		Size: 200.1 MB (200113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:637b9b6e5d83e02b33457d3a28ecd2d70f215fc1bcc96de03f2ebbdba40be067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7f9e72e7b42ec1b2549ba1ea8f167d0baea66bc0494d87afe735429b777f98`

```dockerfile
```

-	Layers:
	-	`sha256:0d5dbd9c424a60e680a31a2550374d9d74c9e1cc3403249b5e17546d3b1b5856`  
		Last Modified: Tue, 13 Jan 2026 05:22:50 GMT  
		Size: 15.5 MB (15450241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a97f7cab03dc1f50f6ae592ccb5f186296b7cf75d0a4ef3fa85a6bfa854cdb8`  
		Last Modified: Tue, 13 Jan 2026 05:22:52 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
