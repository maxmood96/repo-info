## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:f5405c04fb94d52687434afad8591f4f0dab78bef459fe40e0d110c0ebd3cc95
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

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c08c4f5591328e42426843f18c2f68895be765b35dc2253f65b346b5413e58c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321624461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ae39401e2c7ab85dd328a138a06a5fb0f58115bbf175686834391ecb538522`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9888e096307133d2fbd60bcb00b491486db0aecbd10ad65207abf37059a9af`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 15.8 MB (15790695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f960812f05fbc5416b446a8fd445ccdc345be2a630ee73fbe4b2644bb91848`  
		Last Modified: Fri, 08 May 2026 20:26:40 GMT  
		Size: 54.8 MB (54760810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeed64561784d1cd96dfd78f461b7eaf16af77b6bfca7c0caf1278729e02a05b`  
		Last Modified: Fri, 08 May 2026 21:17:48 GMT  
		Size: 197.3 MB (197309613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f1f2bb030260b13769d19455dba03c544ee5d8271e5f0275bafe5c5a489ba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae632b55bb22efdebcbbd0d2d900009634d3637595fcdc18b88bf8b83d0c8bf`

```dockerfile
```

-	Layers:
	-	`sha256:58216e03fccce1d0e3af587014040db2791f162f4233f9a9fe83a4673c7470ea`  
		Last Modified: Fri, 08 May 2026 21:17:44 GMT  
		Size: 15.5 MB (15471577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0d0685090861169725fe6b5618256eb9bfa8f2295b4ebcda35cf348809abb8`  
		Last Modified: Fri, 08 May 2026 21:17:43 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f63b3ab9da6a2b52705e24f7507cfbdf2632dc926b36f86081e0d642c19cbcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282327683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4013cd12fcb72fd1d5a24a881096f90ebe9fafb17d4e08ff87e0f2a0fa586ead`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4cb33fa51e00f2c5cad3e12a59f701c1cb73526295425e2f64b4cb13b9375c4f`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 49.1 MB (49055106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba52e9af1266c17416a17c315f698fb07fc71701dcf95b70a57e9d0f65c70ea`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 14.9 MB (14905070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd446ccde0d71af76f958e25aea6b705f55351a4c8727e3397b0e759244004a`  
		Last Modified: Fri, 08 May 2026 21:35:04 GMT  
		Size: 50.7 MB (50651505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f862bea187cb46c212aa6da5f355ebf4c26db2ef51b6fb3a6bdafc2d503f34`  
		Last Modified: Fri, 08 May 2026 22:13:23 GMT  
		Size: 167.7 MB (167716002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e7fdcaba0c76f436ca98b661a20eae4238de108f86a5f51fa5df1ba7ec2c296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632b0ef6b1bde729bc988df60c1edac5ee4b848d0f9d5949896083ee9cafbe90`

```dockerfile
```

-	Layers:
	-	`sha256:7c091a8dbe44c03c22795bd1a749a1e78c8d2c0eb39e250889507748436e06cc`  
		Last Modified: Fri, 08 May 2026 22:13:19 GMT  
		Size: 15.3 MB (15270895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c2e645035c3a0f1bd52671babe00d0758377e2b0abb0b7adba28b81d90ce82`  
		Last Modified: Fri, 08 May 2026 22:13:19 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:521d119cc1c9483b1ce70ae9fdadc08b2421acec8071c4db6395d55462c00f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313123001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60719e56a15ee750665abb86c5540a42ada156610260467ad55a9d0d943150`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d20a72a3ae72af0f6239652b45dcc6f5eda87bb797e4c05972c586c32afca3f`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 15.8 MB (15774834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de92af39e07f00fd21cc384e0f5108a74acadedc0acecf16d700d606eedccd3`  
		Last Modified: Fri, 08 May 2026 20:32:13 GMT  
		Size: 54.9 MB (54886410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc943fbfcf4513ea392f60742ca835596dbac2f1542abbf52e3b28b25333c14`  
		Last Modified: Fri, 08 May 2026 21:17:50 GMT  
		Size: 190.2 MB (190208547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92bd77e705bebed4bfa187570d9763d015e5a957276f07fef6ecfca7421d5319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc21f4f5f98f48b37210be60c6bf8b96bbf9f15c0a6db4afcc192a0827753d29`

```dockerfile
```

-	Layers:
	-	`sha256:2bfeb37534f09a2b16e113fd3c9b07def67ce37f05a96946f5a995b1f99e10f2`  
		Last Modified: Fri, 08 May 2026 21:17:46 GMT  
		Size: 15.5 MB (15473522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554547c7896d6ac1e2eacdd5aaeb06ce9c6aae62bfa7601a72f4dbf52bd1c674`  
		Last Modified: Fri, 08 May 2026 21:17:45 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e6d1eb63686848e4454eac5aa13ded9760aba82253856cf829a37efefe29d5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327216540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401e377f0e7b54775851e86552b0be0cb1e0290f4c1e7b76a93169eb1b11ecc0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:26:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bebb3bb20b05d30c1a5354688795bd554c50c12bfa7e9190aa4a54c7dce2a8`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 16.3 MB (16295597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5882cc2f0705ce8b109017f0de582bdb1d4e67ec5740dba7f8635d30c4b832c6`  
		Last Modified: Fri, 08 May 2026 23:05:02 GMT  
		Size: 56.1 MB (56061157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7226b1417fe6d33d44e75557d981eaed1351a54abf2e427ded180dbac85c616`  
		Last Modified: Sat, 09 May 2026 02:26:58 GMT  
		Size: 200.2 MB (200154443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45a06396197b68bb55fc12c0552da43eb9a49519fe8cfa205c94e5cd35097df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489e8dcb8d48455bbb2c3440b6496f09b4933e766aa2486f41f43931c4a37b03`

```dockerfile
```

-	Layers:
	-	`sha256:119e09ad00f3a10007b7034b6278193fb166bd983a77b9f8e9a54200b911fc88`  
		Last Modified: Sat, 09 May 2026 02:26:54 GMT  
		Size: 15.5 MB (15459592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae21fb9a83684e3e26f064036fd0885f37f4c97c0d11d000d6400862ea62d385`  
		Last Modified: Sat, 09 May 2026 02:26:53 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
