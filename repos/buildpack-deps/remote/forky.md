## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:37bbbfbf14221762c91998f2b2b257ea3cc64a0543f7ca7421cdb94d7ca0b83f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3ae1007b07c34379ceacb1fc481ff78f9c02e890f573208272d47eab59a6bd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.3 MB (745326143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda77fb0fe16c6775506d1f8d209dd9cd327a40cb7ff60ff4bf171c35272d983`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075219ece41f099ca8ada652efeda87c6ef755098af129d14764aea953222807`  
		Last Modified: Tue, 30 Sep 2025 03:17:10 GMT  
		Size: 25.9 MB (25851839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf321420777749b1953b35d223d4252c4f58791cfbd9906817af3697f147d98`  
		Last Modified: Tue, 30 Sep 2025 03:18:15 GMT  
		Size: 68.5 MB (68536909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2eb493ace1171a85987ade8143b8da3d472afc17460bfbb60b9d221423333a`  
		Last Modified: Tue, 30 Sep 2025 06:42:06 GMT  
		Size: 601.2 MB (601200577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab22b5121c090659e928b1d384ea120d5e72779b6fda3f79edb17545a0af4677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16283595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d883eea275b1ada008111979e65fae45f5c62f6f9fa646374b52ae4e28d11148`

```dockerfile
```

-	Layers:
	-	`sha256:45bb7438e1e9def2dd9b29ff95993cb640dc68577c538b3f629bfc39ce6b4ac3`  
		Last Modified: Tue, 30 Sep 2025 22:35:22 GMT  
		Size: 16.3 MB (16273408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f6fac12548a6fc4694d2ac3d49d9673266677dfca2e277169c1d4b9f74d318`  
		Last Modified: Tue, 30 Sep 2025 22:35:23 GMT  
		Size: 10.2 KB (10187 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:02385d4a4aa5cd517db8a7448c9aa5708daeb18cebc55a18ddd065a0c4f02191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284312348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee766f4631d8b31b1a99599ba41ed9fef794efa88f1176fbe8b5c246806789e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86adee590a893d066c841440cd9d1bbc41753c40fc6a723dd85c4ca79b9b96`  
		Last Modified: Tue, 09 Sep 2025 03:20:59 GMT  
		Size: 23.7 MB (23664786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed6e10bf1b9316986fb492bbe0bac3e1cf59a04a08869527f7e66262ef8c0f1`  
		Last Modified: Tue, 09 Sep 2025 04:45:46 GMT  
		Size: 63.2 MB (63212789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9a61cc66960400a360b684dc02bca8f856db7ffd1f8bde5a6c41b39b16b8f4`  
		Last Modified: Tue, 09 Sep 2025 19:03:21 GMT  
		Size: 151.5 MB (151491553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5149ce4ddea4c82e03cb440b02ec7b75bbf48ca9f9dc73e6c89d7aa824ae3e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16053861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e3b765c033393d8e541e00fb1ea6a59159a91c1720944ea950b4e9d0218862`

```dockerfile
```

-	Layers:
	-	`sha256:dd15b9da8ad1e0ab752eab69f8e3a5166e54f64d95b5e5e9bc1eaf8dc701a77f`  
		Last Modified: Tue, 09 Sep 2025 07:20:19 GMT  
		Size: 16.0 MB (16043609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d244920b7ae16c6579e332381c4337b9ca0e2f04b6d8bc5ee68c717b2487e3`  
		Last Modified: Tue, 09 Sep 2025 07:20:20 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cd8a3b6beb54e96520bb97472550150c67f8ab1e9b03cd66257320f6365eb758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.8 MB (748808135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf4425f3f96f17b375ec33adc741964b346102349b012e8a4b7debd07a51211`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009e42d3323422f2397c63e68313d31e460dfa892d093803cd931e5199733e2`  
		Last Modified: Tue, 30 Sep 2025 01:18:56 GMT  
		Size: 25.2 MB (25209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde70c2343e98e974396577ed833e905203bb8d9de40b076f03dd816afd1872c`  
		Last Modified: Tue, 30 Sep 2025 02:14:07 GMT  
		Size: 68.2 MB (68179749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6ecc528ae469bc5e29a2dae589536819b3ebfe56d54e752962ef8a0831c5c`  
		Last Modified: Tue, 30 Sep 2025 19:50:00 GMT  
		Size: 605.5 MB (605539148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83bd702c7fc2655dcf8201f8996ccb0e8b6e90f98ea170e68adee1d47ce8ac55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16358859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dc24130da2aa76d032422b254fcb9cf97057ae157725916eb8af98a5f1f93b`

```dockerfile
```

-	Layers:
	-	`sha256:4173be0912f863fcb7ff765f63a4ccce686adc09f4a5d2824f6d6679cdf354c8`  
		Last Modified: Tue, 30 Sep 2025 13:23:55 GMT  
		Size: 16.3 MB (16348591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e45ff5a98673c0d6dfdbb980b3cde4097989703ee34a0f15d04154409e30dd`  
		Last Modified: Tue, 30 Sep 2025 13:23:56 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff7b5985c97b23ceb6b600e2a1246dd3ced2c1a86d54d3fecf4f8fd05e73376d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.2 MB (745230064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a8fb54627ae184aa553657c4ecf582bf1c077655fb0e775a6e6af5cc4631c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf114b881a561e278525714169b788115fe512463f3cf36ea76912c59a87cb`  
		Last Modified: Tue, 30 Sep 2025 01:18:44 GMT  
		Size: 26.9 MB (26896436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ce394ea3b0f58521d466c625f21c99b1a0c4601ea3a202665effb24b708c5`  
		Last Modified: Tue, 30 Sep 2025 01:19:29 GMT  
		Size: 70.4 MB (70426922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec445626e476a6170f9be6ecec88ee21cff3f6268deefc5286666c99685f67`  
		Last Modified: Tue, 30 Sep 2025 20:41:36 GMT  
		Size: 596.8 MB (596787286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf68bfefe9651955b3e1f852168115297c7bb154b1ff120b3dd32bf0a3c884c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16253363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d914bb8a4ed17c63c1f878ff97dfc3e0ab0c22e5093f01c6be5343092e5c43`

```dockerfile
```

-	Layers:
	-	`sha256:ac36602f28b7275b3b14864a21f11f568c4514bc6189b89f4e9e33dd80d418fa`  
		Last Modified: Tue, 30 Sep 2025 16:37:12 GMT  
		Size: 16.2 MB (16243197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6f49c3b3f5ab02cef23f8a57d340cd4fc854a80bad6a16373a5056fe305eb9`  
		Last Modified: Tue, 30 Sep 2025 16:37:13 GMT  
		Size: 10.2 KB (10166 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fabd4837774595d3cfb90ba6a183075b57e9caabf05d999889bd61c13f57737f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341647544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f7db6128ee81a86cbda47d9431e7de6183472b48c40d68d36f12e654794a6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4e4a2bdd2295cd2a4f3315805533676c7f12dc54b360ff3c285c5614051d45d`  
		Last Modified: Tue, 09 Sep 2025 02:16:14 GMT  
		Size: 53.4 MB (53391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a918fedc73bd98652f37087b2219a9384ea0986c8affd0a0d0679091c621a`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 27.1 MB (27054637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a37b1c09db430f1439f2b1593baf02b266038e8525ca1684329d8133359a2a`  
		Last Modified: Tue, 09 Sep 2025 15:26:09 GMT  
		Size: 73.6 MB (73596047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c3d6c8cac8ac1dc5760901020dc563032009b2f8fb1fa19650dc4bb5d285e`  
		Last Modified: Tue, 09 Sep 2025 21:35:14 GMT  
		Size: 187.6 MB (187605162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ca8be219bf8541f7e9d605cb960a5a6acae408fd65f212cfbcd2687e72597a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16270215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0dedf92d14fcb5ab34bb8726b85a59948e2e80d7d173e7d85b568a4d3c1534`

```dockerfile
```

-	Layers:
	-	`sha256:553d5c663ab1656e95b22a4f281893b83b22153c52667fdb7620f66bf62e7a09`  
		Last Modified: Tue, 09 Sep 2025 22:20:36 GMT  
		Size: 16.3 MB (16259995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6879290a3fb2d2c5b53f537f972c0f7b041fc392f317290a2081900193671fe1`  
		Last Modified: Tue, 09 Sep 2025 22:20:37 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:969b4dec2090a02e5daaa71321b89e587720f1bd49f6c56ad464e49421bbda76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1115492899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a999b118207072b93a84999d64912d3c74f26de64126ef11db2d7a23c7325c4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b69968429eb7c4ddc55330629f921afc4125b1edb6cd3eb02edfe67c09cb248f`  
		Last Modified: Mon, 08 Sep 2025 22:03:44 GMT  
		Size: 48.0 MB (47990884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afcfb97f0f574c8205b47fdf227a9c9ba730a3a1ce377de450a5ca2828ba055`  
		Last Modified: Fri, 12 Sep 2025 01:39:01 GMT  
		Size: 25.0 MB (25025845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e67756886f1c8cf9722970b775438594a7ea05fd03804456510ee3f3eb18e`  
		Last Modified: Thu, 11 Sep 2025 01:32:48 GMT  
		Size: 67.2 MB (67191678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b6a70de14af1194df559f9b865aed725170e31adbfa78f9a8e37138a171dfa`  
		Last Modified: Fri, 12 Sep 2025 19:20:32 GMT  
		Size: 975.3 MB (975284492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c237c035e746c5cf365e10bb5ea1fd054230f4ffac6c49eccf37c7e9669922c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16341802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454a8a2a92ccf5555585e3087252782fa67234cd330da03199cd5cd9f5a6684`

```dockerfile
```

-	Layers:
	-	`sha256:289c611bbeba2f4efe6254fa5cba64f503fc40b962889bbc0ebb45f094a1a328`  
		Last Modified: Fri, 12 Sep 2025 04:20:40 GMT  
		Size: 16.3 MB (16331582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bd7c0b19f0415c34df67142035da4fb055c26f8944dbaefd6babc3ccc61f43`  
		Last Modified: Fri, 12 Sep 2025 04:20:40 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:94c87243fb9a7623cdf2c6732673d9cc6915e70c7ce2d301d464123fb8d13328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.4 MB (647350745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bb11104d2e0fc484e493d26a53a8b39a584b1c788410c5fc7c5a0c381af73a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f12f0b09af6c73f5ac02ec4057426f99780ba4cc2b7ffa5da8754ce19dc3c40d`  
		Last Modified: Mon, 29 Sep 2025 23:35:21 GMT  
		Size: 49.6 MB (49576014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd2fa0437cfacaf00281ef1e68d7f757d4929c7cd7fef87c86f4fd3b95f9df`  
		Last Modified: Tue, 30 Sep 2025 03:09:29 GMT  
		Size: 27.0 MB (26987131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0807bf042d979330a7fd99ac96e452f05bf73f9d878b1183e51f9b13a14fa197`  
		Last Modified: Tue, 30 Sep 2025 09:33:41 GMT  
		Size: 69.2 MB (69245413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaaf8821842f8ecb62d7e44ccb17ac9df6c6b8e7353ecc399ed39b063f344a2`  
		Last Modified: Tue, 30 Sep 2025 15:49:59 GMT  
		Size: 501.5 MB (501542187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9354b940c7c3c3754bc439757c79e4c9ba6e934c6a8493b4af8a8552a6a4c1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16050264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae38a3154082038daba6753aff3fa570266c770bb6663b30a84068742f2d411a`

```dockerfile
```

-	Layers:
	-	`sha256:4957a6764e451287035d0ebd30a38eb61480c5c989f16644adb9fed7a18da01b`  
		Last Modified: Tue, 30 Sep 2025 15:49:51 GMT  
		Size: 16.0 MB (16040076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1139fe7173f93e1fb85a622977e628b7ee826bc9e6b5a843de1831397e847b7e`  
		Last Modified: Tue, 30 Sep 2025 15:49:49 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
