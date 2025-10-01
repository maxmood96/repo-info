## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:0ed0c0dadf38d390c310bf234ec23c7d96b8869c98213372642bff134c58b59f
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:41c644e872153a1e42417ae8e006b9a3ee6e0f59c74777cb35a2ab741284ed03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348354307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b84ac1382b367863e82ef064c7e5d52e45491d70445cc85a3ff223b46dfc1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ecbfb3e7f8ccd5b04dc161a13218fd7aade8b0235603a879606a4e6887da6a`  
		Last Modified: Tue, 30 Sep 2025 09:49:24 GMT  
		Size: 211.5 MB (211450463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92b7ab74f6c829cf681b63571a25c6cd738c6cda11429bb9ee1816a95ff96722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30753b1a7da32cee31b27f3c415aad07b380c74a9ee434f739ecb337b25544e0`

```dockerfile
```

-	Layers:
	-	`sha256:ed35c8c3a8be390e344b0d211ac9c809ebd56147a07fa9c25882206bd28be371`  
		Last Modified: Tue, 30 Sep 2025 20:46:36 GMT  
		Size: 15.9 MB (15867065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8619db9b2cd144a3569def3ab65518d676755dc0c276f38253fc906a70e1f64`  
		Last Modified: Tue, 30 Sep 2025 20:46:37 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4c769fb2247bff3ae1da3c2c7a520654a0879d1ab079ee2b80a9260905eac4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315426994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05061f5fa7fb31946cb7c850cdb98e2b904e260968db30eb2a32067cf0f180a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f9dd65d850ae18d5d5161e690c6c0b615e72aceac0e3bbc51ed315faf762f0a`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 46.0 MB (46015582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050a4079641da2be39571d354108d87d3709c848f35b60ff42118ae57f90dee2`  
		Last Modified: Tue, 30 Sep 2025 01:01:11 GMT  
		Size: 22.7 MB (22702536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c17be5ee9d11a6e4c78d0f71ee3806a1aed959aff55f037aceb36923ab6ea`  
		Last Modified: Tue, 30 Sep 2025 02:18:29 GMT  
		Size: 62.0 MB (62010842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108d6b17335a11014214790904eba0289ef3e058d93046d7913118b44971477`  
		Last Modified: Tue, 30 Sep 2025 04:13:42 GMT  
		Size: 184.7 MB (184698034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:081caa0f5608b82239672597730afeb3bb4250a014fb017b4e5d9d350837d858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15674345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711169053507d50706333fa3fbda2199364fc2a2d8b0b74a86bfbbe5dc1b9ad6`

```dockerfile
```

-	Layers:
	-	`sha256:beda9a2167a47bdd58da144999713cdd3a5de8365e32df7ceaf2a2a0675267d1`  
		Last Modified: Tue, 30 Sep 2025 06:34:10 GMT  
		Size: 15.7 MB (15664049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb45bc05915dd24a602358c284344897cd194c7d9999df1ebe0f8bc4c0e785d2`  
		Last Modified: Tue, 30 Sep 2025 06:34:11 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fc4ce0dd58ea9ee7907dac8fdc39a234edf1f4cd00769f03a571f9ef6b9cd4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301135392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636623579675046d0d01da268630bc4b758bfdbdeb56a8dfe08c933c0e474033`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b780bdf61c238372fac425e5a202e123f13d1b05edc7863caa0d986cec6322a`  
		Last Modified: Tue, 30 Sep 2025 04:26:31 GMT  
		Size: 175.4 MB (175356228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64332fb491e636afba6df0b15fc773caaa319c20f5a8af72d3514e2ad01adf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a555a43eb5eb05036f56d34a1c5b60acea46a0fe034e88a0a125b53982a4eec8`

```dockerfile
```

-	Layers:
	-	`sha256:7dadc7a16aaf890158f783ed2c0b98d7d14cac4638e956372ce16cff4e58f303`  
		Last Modified: Wed, 01 Oct 2025 19:52:30 GMT  
		Size: 15.7 MB (15669525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9aa803fed2e657688d78b26d81ac784d9fd78113b71c4f15d55d5ea3bd3a8c`  
		Last Modified: Wed, 01 Oct 2025 19:52:31 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:72fc063e4bf381ba9aa1413db4c4af0c90b6e8cec4092a234138f80945b014bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339282835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa69d53898c85291c94f55862fcd968cb80255d3bf0904cbae383a8a9402de35`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9cde803e18b47bb66244c4b16529b3895360524f73e1026f92cd884258213`  
		Last Modified: Tue, 30 Sep 2025 03:13:27 GMT  
		Size: 203.0 MB (202957977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8c9f8961d2e84fa27c9a12a999976ab33f6a2a73a2ec392bffbafff602325cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c6952d786210e55d79368a6d2fb4748cae35aa7065e7c0b39dd832b1c6437a`

```dockerfile
```

-	Layers:
	-	`sha256:bcd401c141d52d6c3f732b3261c826df9abbe9bfcd72c8fff4bb3575bd7ce5c7`  
		Last Modified: Tue, 30 Sep 2025 13:23:29 GMT  
		Size: 15.9 MB (15895567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceeb49f54a8d6bb3f638cc4c96e53d8fb1c75d1c0e3aa1bd8a708a3ce96d410a`  
		Last Modified: Tue, 30 Sep 2025 13:23:30 GMT  
		Size: 10.3 KB (10311 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a7870cd9d50d35bbb1d86d1b14c1feba8de8de78b9e85a550445641fdfcaa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350943711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a6b6617ecd1bf715c3b9038ceaf2458ffd41c57010f9a4037a5780a7a1361c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed8195aa7c3a825d91ca933394244f5da4c679f6206b34a812b833fa1d5882`  
		Last Modified: Tue, 30 Sep 2025 03:13:56 GMT  
		Size: 210.4 MB (210382990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6e618f6141ed0e6cffc1d00df5bbce07764ecd5b3aede58d43ab55b93db247b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15855502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5727da203bad5cda366c3a11e47ba9e65e51bb47765916a89f6d029e1a5fc44a`

```dockerfile
```

-	Layers:
	-	`sha256:c250156876ef25dd6335d6ba615e7f8749079f16f1d38e4b6c2f84ac4427f38a`  
		Last Modified: Tue, 30 Sep 2025 15:24:21 GMT  
		Size: 15.8 MB (15845292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ebee914fd11255f27fa30c7ea270974a42cfc2fa9f91646c2603f7af27896a`  
		Last Modified: Tue, 30 Sep 2025 15:24:22 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c7a5b51075f590cda3dfa2e3339a9912f1bc1dc3064684ab75446eb0ef880e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325900831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2c71236542db2bfd6360dc4c890c450d6be458a6ebcef56041fab305acae25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc37f465cc2e94dc99018cc49653db72338dadeeca4fe996aae9a05bced113f`  
		Last Modified: Wed, 01 Oct 2025 18:32:29 GMT  
		Size: 190.2 MB (190219416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f61fa44475c670e96d7aa7da42d9b7c8fa9d11049e9411b2f920f20aa7cb3f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 KB (10065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a3339c833877514d36debaa01f8c3852e2e380d80f91be786fea31a7029ff2`

```dockerfile
```

-	Layers:
	-	`sha256:a17ef85c5b0599f3fdd4ba7a557e9445a76d2582b24b86e212865b084be8a402`  
		Last Modified: Wed, 01 Oct 2025 19:20:16 GMT  
		Size: 10.1 KB (10065 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9a688d42b841884c12f2de0d5ba6f99a0c50d0b021e95a97105dd5091613fdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362330015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8c261fcd4b210b8805bf287b81bdedb8fb968a594c7e0500a7654f63bd7a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f3e227faf60c24660ef8277c41d877c19b8ec824c80c672a35bd5c41d3bfe0`  
		Last Modified: Wed, 01 Oct 2025 21:20:51 GMT  
		Size: 214.5 MB (214488789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92bbb149a52e1aed111036a5ceafc2478d1b5bc8d329a1b0bd894ad91ca74b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ee80f627e06b624b79bac8ebf98877a304f84ead85f7b72ac9ef1e03f14ab9`

```dockerfile
```

-	Layers:
	-	`sha256:136d0f3d93eaa8018854dc7ed46f724b8b67f530bd104d7e52a836443d7ea5bb`  
		Last Modified: Wed, 01 Oct 2025 22:02:42 GMT  
		Size: 15.8 MB (15843570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5b943a90e00d770df9315616ab882350665f14ec4d0456d90fcc7c1a569789`  
		Last Modified: Wed, 01 Oct 2025 22:02:43 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:489a0c4c31d8359c4767e66f1add391c3266e76eaab2609cccd23259046c52e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318148300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a5ff29a1c0db992822d4b0cd13c4abe8d94e9d65c4508aa521b874ca2ca044`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638c6ce763db618afd6e5ac870aebad4698af0a75be5362f1e49c581094dc4c2`  
		Last Modified: Tue, 30 Sep 2025 19:38:44 GMT  
		Size: 183.5 MB (183485788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e20d0aaf3a022da13d49ee27e41bbb882bf8aad94005d0d00a5cee9f652a338d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677fe397795a1c540e42614331b1a8e2c73eea68d25003379cf8c71de53cc85e`

```dockerfile
```

-	Layers:
	-	`sha256:4179231402eacf8c732c324b80ea02d8f644d9f48bdd6ed5081eafb2c8849f11`  
		Last Modified: Wed, 01 Oct 2025 19:51:22 GMT  
		Size: 15.7 MB (15674663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb47a2643c3c5280df588f5231eb1eef3e4633a59239771d817f54fb0766b86`  
		Last Modified: Wed, 01 Oct 2025 19:51:23 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json
