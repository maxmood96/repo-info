## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:055a20dd4b8446a8addba6da58ca8d47a786acf5f5ef86b9eec858391a7c032d
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

### `buildpack-deps:bookworm` - linux; amd64

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

### `buildpack-deps:bookworm` - unknown; unknown

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

### `buildpack-deps:bookworm` - linux; arm variant v5

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

### `buildpack-deps:bookworm` - unknown; unknown

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

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0d5f5a6564580ad24a9db7a41f07f58059dab1a0c41519092e81ee4a137412de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301106958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8bdee1a5c02b55d269cb27b9fbde593fcd4b941fdaa5c62551a6f6623087a0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 06:17:59 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce01e6286f82afd0f8a0433432ff0d4bb70b6c0a8e6a2da2c4c2417eb37685`  
		Last Modified: Tue, 09 Sep 2025 10:33:42 GMT  
		Size: 175.3 MB (175327055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6d8c424c7d1bfa8fc8bc9ac8be5178098f00a35d7dddb6424cf0f29535cd096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec7a3e891bce437450d51b014a9510f2992397fbc8774e5a2b04d88a420f662`

```dockerfile
```

-	Layers:
	-	`sha256:f4ae5da3a9655b245c1ddddd1a8e3cd8eedcd0cc57f5750156fc13f1ff66d09a`  
		Last Modified: Tue, 09 Sep 2025 07:19:59 GMT  
		Size: 15.7 MB (15669525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86017244f39f37ebf212c27ed550bddd8e2680923910bdc52709c67fea5c49a`  
		Last Modified: Tue, 09 Sep 2025 07:20:01 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

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

### `buildpack-deps:bookworm` - unknown; unknown

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

### `buildpack-deps:bookworm` - linux; 386

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

### `buildpack-deps:bookworm` - unknown; unknown

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

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4b29a8b26fce5018bf146f8a38fa07f2e45f2bfa28862f7c1e022e0909b7eddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325872861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955b80df38894b75bf0d88ae3cd12862f75aab747c3e8c2c78a2e532c99e54ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32b0a76df497911c1adc85f7748d78b916d66733f6d0c87cdc6e9eb06317a625`  
		Last Modified: Mon, 08 Sep 2025 21:14:25 GMT  
		Size: 48.8 MB (48760780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4b1410ff953e9baafd271cda9e27ee11dab33c7404024b5d7f0a941e7606c4`  
		Last Modified: Tue, 09 Sep 2025 04:22:26 GMT  
		Size: 23.6 MB (23611387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49a4f2d47eca9eb39dcaf1cce76f6da099edc10cb571b790f8588eb5731614`  
		Last Modified: Tue, 09 Sep 2025 17:57:06 GMT  
		Size: 63.3 MB (63309380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d72cff33b04fb8a6482db80d9ffc855cfe14c932058cdde4bdbfb6ae68a4`  
		Last Modified: Tue, 09 Sep 2025 20:29:16 GMT  
		Size: 190.2 MB (190191314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a91671a686002eb62b2558b1d1fd692183057afab6905248bc38b7cfe253e50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 KB (10064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0119b02f862a48f01aabbe9d91a485d07afba56779ed70ba36ad8107d83558`

```dockerfile
```

-	Layers:
	-	`sha256:b8fe21198adedf8ecb7b4d993c2876e8f48f83b077e6bea1afb602e0ce328b69`  
		Last Modified: Tue, 09 Sep 2025 22:20:37 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:240ab18eb0329fddd70677037943353aee5bb0b4de5e4ae82d654fea029dea80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362303403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec034864e6724192f4201a1eeab5eafe3eee8af4a353c50e84dc1569863eecec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b92467bcafecf194d3c4efbee466dcb9b2010a0899f7d2b928f9afed69de0`  
		Last Modified: Tue, 09 Sep 2025 04:47:21 GMT  
		Size: 25.7 MB (25668980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aad37d5c4461745e898b391fa21157366a7f13cf28ff4bbb1e1434d87664d3`  
		Last Modified: Tue, 09 Sep 2025 15:23:55 GMT  
		Size: 69.8 MB (69845800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff0b9d70c9c82f7123de124ae3969749d2f2876102f829f1ffecdc23491a704`  
		Last Modified: Tue, 09 Sep 2025 22:19:54 GMT  
		Size: 214.5 MB (214461801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0b421f3d62a8ec132150f0a3affd6ddabd86ec6bec76bae94b427543626f7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe380bef9e0550af5725abf93f9aadb423fdfcf7193a1e455605df838e17b79`

```dockerfile
```

-	Layers:
	-	`sha256:9a0606dfd625b5408c681e6c51cddbf8879025a1164b3b8aedf8792f4649baa4`  
		Last Modified: Tue, 09 Sep 2025 22:20:42 GMT  
		Size: 15.8 MB (15843570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb83382dcaa419edb1b0e89d4e60830aa36d34c1c88cd674eb1b17abcf834ecb`  
		Last Modified: Tue, 09 Sep 2025 22:20:43 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6f51f3352815090e26cb9c2bb729479db5f13c8b3ea21a43530136264a33ac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318122060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f12a4d4717af7abe08cd990936c48e53e0305c847b47acfd416b164b2b23ccf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0c679ec7b70d7fa5065a6e28276437547a7d43502b4e016c2e85aed8c84c`  
		Last Modified: Tue, 09 Sep 2025 01:20:52 GMT  
		Size: 24.0 MB (24023865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed122f74eb7bf77b1109cb95e13be357040ccb22119f5f02e566a491bcc45e`  
		Last Modified: Tue, 09 Sep 2025 17:52:15 GMT  
		Size: 63.5 MB (63501842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1357b3f44237ddc9c069d6ad92462c82b443e45692de7cff2d9406a0aabe5cf2`  
		Last Modified: Tue, 09 Sep 2025 19:20:09 GMT  
		Size: 183.5 MB (183458814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64508a13d76d850600d8262f410e6254757b449ba7230e9fcdc012592c80b4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ac6ec36ff6c1b2e727c579f938b35ad9d0c507ce05769f21f59d29818c9e57`

```dockerfile
```

-	Layers:
	-	`sha256:f691ecca78b6ad8dbfe127a29167a09841b09a29ecccef374a1022fc9ddaf3e1`  
		Last Modified: Tue, 09 Sep 2025 19:20:47 GMT  
		Size: 15.7 MB (15674663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685af9d743abf9a896fe5a6550a569d5a927bc801e07042de06fdbeeed2ee41a`  
		Last Modified: Tue, 09 Sep 2025 19:20:47 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json
