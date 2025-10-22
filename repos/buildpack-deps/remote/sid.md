## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:5bf1f73bcf143af9114125b3ecfeab56c576ac7b61826a0f9425d898a16303f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:77cae8876bb4a36214c28ae17116a720e76d18d44790f7e09596d7d2a8b0ca42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.3 MB (745330947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da591e9b94832e9baae7f8299cdbc341b1b5f828f89a480c7d62d992e7e7c2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0041865733f8eac4afbcf0e7351d1bf685e1d3b536723ebe09dcc7b7f34ad22f`  
		Last Modified: Tue, 21 Oct 2025 01:42:32 GMT  
		Size: 27.2 MB (27187028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd69ffbe16c127e7d3c7174dcb8501cef8b21f4527fd8e5e2b9c2d06b6a1611`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 68.5 MB (68494131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb42b4f30208b1ccf77ed5e6be188d4fc410d09dad3c0693b5c14a1b35e26703`  
		Last Modified: Tue, 21 Oct 2025 17:37:43 GMT  
		Size: 601.3 MB (601266481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10b4125072bcd04607ee109cde73b4fb19820d0093c9d0ef2808352e1ef9c39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16259968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174091079d4f1227181cba3149a501c735400644750192b2bfa9f34f1ba3fe12`

```dockerfile
```

-	Layers:
	-	`sha256:a47b2a63ba9fcc2462d7066c9662d3d739f99225b9f961ff4c0f86d190d6cd54`  
		Last Modified: Tue, 21 Oct 2025 16:20:14 GMT  
		Size: 16.2 MB (16249792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4eb7fc88568413ac92b05133904da3ec96152cfb6b9792ca40d72f547a55f0`  
		Last Modified: Tue, 21 Oct 2025 16:20:15 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e0d78bc7eec138fdaaca8a17e3809a472c0eb4d91757354d08887f3577ee0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.7 MB (688653154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9795d902126118581ce535ef36597dd4859ecbb399264ac4c1921c16fa5cc164`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:204bc56c72452e737a2bccff3f4208682016048e825d5ac2bc52dc2c4d4649de`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 46.6 MB (46593513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3882f8d4f2701b8365480052f7e556ff8fd1101d8f1b72e8141c4360f1d695`  
		Last Modified: Tue, 21 Oct 2025 02:32:18 GMT  
		Size: 25.8 MB (25784458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff346c12ee6ee902eef6ce2e57381cdb35b81a53850091071c07fa57c84dbf1`  
		Last Modified: Tue, 21 Oct 2025 03:57:08 GMT  
		Size: 65.9 MB (65940274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db332e0fd6a77bc13162099b406171755e0e40161fb1b3ec1a19cdddb797acbe`  
		Last Modified: Wed, 22 Oct 2025 05:29:40 GMT  
		Size: 550.3 MB (550334909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5369a2ec96f1a4d8b17f3e583284e409106bf5c39abeef268392b6ea86b97bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16012226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a2bb9147a9b9f62f6a2fe8d94d73ab766d05fe46b0d1cf4ed9f5a6df2637a3`

```dockerfile
```

-	Layers:
	-	`sha256:c968fb421aeb1e9684cad4e81ee88660397268501a7aa4fd1dc4c6cc13f4c6e6`  
		Last Modified: Tue, 21 Oct 2025 16:20:30 GMT  
		Size: 16.0 MB (16001986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63482f344754d60ad5eaf7ef984e7c2ce4e6aa26b3a9a2b3c8a6b42d3e1e9e83`  
		Last Modified: Tue, 21 Oct 2025 16:20:31 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4079c56141e64ab1f4ea1bb735422910eb7fe87817917b23101dcecde4f8a9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677055246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6fb5b558fb7b9d9c1f8c2a3c7bfa709b1762d696c708aee84686facc43752`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d46bd548fc78deefe00dfcd2b559377066496f2d6beb8d1543970d5a2164151e`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 44.9 MB (44911556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca5d6a8872c7e1682c82eee718887aef134a416249261516f2ddbf348e5bb1`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 24.9 MB (24922039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa63c9ab104c5969f04bb0672948fcd7f46b1680b5c36ee57bb532b455b361`  
		Last Modified: Tue, 21 Oct 2025 04:11:34 GMT  
		Size: 63.3 MB (63295142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71e6ea6694f2219812f68e9b8e072c0bc1a5b58c7b66bdccc4b7b2d3663ac87`  
		Last Modified: Wed, 22 Oct 2025 05:30:06 GMT  
		Size: 543.9 MB (543926509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:301e15dbcfa5fcb6d39d1873f06d019066cba6b996aaad02183417cb5683a9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16017787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70e9a886be41afe144291865409df4f1d4b2592f2655bd433452cd4f6311c03`

```dockerfile
```

-	Layers:
	-	`sha256:904a023393891d432a34b4cf093539268a958d4a999cbb630861db55395da973`  
		Last Modified: Tue, 21 Oct 2025 16:20:45 GMT  
		Size: 16.0 MB (16007548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450ac0214cb727b4198781908678e5d74f5272f3cc4a64fb1311fb4f15595217`  
		Last Modified: Tue, 21 Oct 2025 16:20:46 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:95038cc0cc3ce14b060ea94a548b7645bfde849d733475796ceaf4e43cbec7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.1 MB (749070717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021f1fa1c84f033d2fc5657188e51d6fb147eee8ed33bcd1957e0791f51821cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d1d3885aec81341d6c3f13d004d1c421d5225a47b5dd56191da09737f82f78`  
		Last Modified: Tue, 21 Oct 2025 01:46:53 GMT  
		Size: 26.5 MB (26496461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88e1c8c165dfa86647e2df68d9d0101605400d05b4a3fee9701c9bdbcf2caa`  
		Last Modified: Tue, 21 Oct 2025 02:35:29 GMT  
		Size: 68.1 MB (68146286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114527a2412335ab15c3318900c1821503b014f57729725977fb66c86090f822`  
		Last Modified: Tue, 21 Oct 2025 18:28:28 GMT  
		Size: 605.9 MB (605921939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f60525350cd14cffc502fa13210879043c12a642cd05155ae3c0b229c557f261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16334597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461750f6cc53d13a66614985808a20fc5aa1ad9c73183601fa457febf95535af`

```dockerfile
```

-	Layers:
	-	`sha256:05ce1241e04fcb16ba26ee82227d41313874ac04d4bf2a35889b634a1de6554f`  
		Last Modified: Tue, 21 Oct 2025 16:21:11 GMT  
		Size: 16.3 MB (16324341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b55dba6ba4316b3fca7a7c7d0afb5c0e9710c2ea54e862a601e5ca7ff16da6`  
		Last Modified: Tue, 21 Oct 2025 16:21:12 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:732863a6390e760fb51146bc595ac8887d85dfa4951503bbc10c118af85b2f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **746.0 MB (745970932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd1020f979db04ee863197a6ee79e7434c1d73fa2ff4ef5f673624269d61fa2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda6499db2a9a6f591335665b50167bb19c3bb91ebb991c34e464fc868a2cca0`  
		Last Modified: Tue, 21 Oct 2025 01:53:31 GMT  
		Size: 28.4 MB (28427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a7d07fbe9a973112bda41167c09a4493891f62e438b759d8affbcdc6011e39`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 70.4 MB (70356437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c68333bac88f2630442d169e4d93cdfe14475bc20c85c027e133adf52df633f`  
		Last Modified: Wed, 22 Oct 2025 05:29:23 GMT  
		Size: 597.5 MB (597468694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dcc2e73122ebedbdbf5049548f26640d5461510d72c2d314aa539bbc890f15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16229727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4c10e449e31e6432d5121cc845917ede1f1fbb564af50b0e497bab93b231be`

```dockerfile
```

-	Layers:
	-	`sha256:5b8c4695a52fc684ff0e1a07fa9c457187b5f9e392c5a3bc0de425dfeaade81a`  
		Last Modified: Wed, 22 Oct 2025 01:21:33 GMT  
		Size: 16.2 MB (16219573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270a3d9e9424d3d9c19aad2140804b3fdc59b764cc6e1d494bef502d9badf3f8`  
		Last Modified: Wed, 22 Oct 2025 01:21:34 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8ed23a7d320429c2b4bc67d69bb89da7c9c43bf40358aeb928904f28f905650a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.1 MB (702125357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595794eec368606ee6c55faecf421a56dc5fd6c6a76ff79bb568885a0a62bea1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dd82e8f3bb693d3ab0a24c9bfd56d40d1be2ec87a80a565bb29ebde51d7a8a9`  
		Last Modified: Tue, 21 Oct 2025 00:21:36 GMT  
		Size: 48.6 MB (48586528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ece089fc78cd5e3356fd704455c8030636434bdf37dbc15a1b8e5f08d992f0`  
		Last Modified: Tue, 21 Oct 2025 17:28:53 GMT  
		Size: 27.1 MB (27137104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dac4a728c1c024723307311b4d3c1931b919b823de1d71a9e5a1adf855f73a`  
		Last Modified: Tue, 21 Oct 2025 23:46:40 GMT  
		Size: 67.4 MB (67376553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d093c27ba1c9ca050711e41a1040395233842be7ee75e0f6706d8a3ed7a48ad`  
		Last Modified: Wed, 22 Oct 2025 01:24:59 GMT  
		Size: 559.0 MB (559025172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e76c6d16377a208bf0bd82d70a65c1fcf490e5d9b8542a5c667270ce63c665d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d5a150b96cef3d4810d72e2744949b8292fa597b5d74bb28b4466169fa50c0`

```dockerfile
```

-	Layers:
	-	`sha256:bd28dd752c0a76c58276484202f154d8d610c06e176d3bc0758cfc443a492b3a`  
		Last Modified: Wed, 22 Oct 2025 01:21:45 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4ce0380ab5f82a6bcde6506976825a8f87a888bb404f5df1d0bc91f392d2f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.1 MB (695062585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8ae6a340b710367227e9d97eccda2342df427006146c928be74ee879445af2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:573dcf794048f7c1a04d7e5caace5a2fd1f7290004272bc4f3dfd960a096f8a9`  
		Last Modified: Tue, 21 Oct 2025 00:23:18 GMT  
		Size: 53.2 MB (53217563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d66ae6d7a7d4ee86e6e6ff963fcaf8df404ad10cfa1d1fd6e312e128f220b4`  
		Last Modified: Tue, 21 Oct 2025 07:45:26 GMT  
		Size: 28.7 MB (28740070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce499c900f022c6bd64723f2ec0116e5a84c4bbd95c63b9450125c67c0d19d`  
		Last Modified: Tue, 21 Oct 2025 17:34:21 GMT  
		Size: 73.8 MB (73816162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915d8deb9f6a59a9c424d0aefaa481574d74b7770297b9849b8f777d2f14a11`  
		Last Modified: Wed, 22 Oct 2025 05:30:00 GMT  
		Size: 539.3 MB (539288790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bda4686170737f9067b2b2ac15871f5afe97b5c6c4838bb76b5289add96667b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16234144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae69a2334bb505b2f59478550fa6ddfffc8eddb85a9fb80e703723bd152c4df`

```dockerfile
```

-	Layers:
	-	`sha256:96041df0dedd459eb2d1b745e792e8df1e46a7cb81039848f0d695a5f672dd50`  
		Last Modified: Wed, 22 Oct 2025 01:21:49 GMT  
		Size: 16.2 MB (16223936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463d4ec8228ccf677704926e8eb4922daf874dc8e01751691f186632c742b848`  
		Last Modified: Wed, 22 Oct 2025 01:21:50 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4c5b86d60c2a47b18f9568df30aade15edc1e03f26778fbeb21ec94094ae6418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1074829384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d93c586aa6c6c26245d0a082e6f566bfffe7e0d3c175899876618afc0aa65d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5296fd171b043d9adeac427b668a2c333e09261704a2befe2a2593421c6da9fd`  
		Last Modified: Tue, 30 Sep 2025 00:53:09 GMT  
		Size: 46.7 MB (46680971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995bc0710c59defc3b6e948b5fec04402ad900b4af1204d7420bb8e2736886a`  
		Last Modified: Wed, 01 Oct 2025 18:09:27 GMT  
		Size: 29.3 MB (29334857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5342a4415df6cfdfa16b453bdb12523178508b905f6d7a7425c52c9dbe807e2`  
		Last Modified: Sat, 04 Oct 2025 09:26:31 GMT  
		Size: 68.1 MB (68132570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8a911f0e9103cc9cbc648070539f00433c38f8d75702cd3a96e2c3edd1bedb`  
		Last Modified: Sat, 04 Oct 2025 20:53:02 GMT  
		Size: 930.7 MB (930680986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d69ef1261c90835189151876e1109c6425dd9e941d2523f54337a6dbc5351017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16329653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adb5022c94b327f59781054b93dceaa314ddeba37aa0b70d8cd01d61905d0bf`

```dockerfile
```

-	Layers:
	-	`sha256:ef5019874f895c7a4d57db5a7552fb6f610e776524fbac8b904acf96fd3da587`  
		Last Modified: Sat, 04 Oct 2025 13:21:44 GMT  
		Size: 16.3 MB (16319445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26da5cc02d10e245991309b0c864a8bb1d9becdd73fab10594bfe86b4f3f929f`  
		Last Modified: Sat, 04 Oct 2025 13:21:45 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:780c0ee56d5a8f411786dd6089e5a1cfe69b53edf322bcbd974459b3aec78b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.1 MB (650137851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd713317b507386e536f25801d3c2d80b17afc9e3f22b5267e81a8b1bea007c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d997811a60a9b9144b07fdb085fc1feb6f43f5adf62ec1daf292a386279413a0`  
		Last Modified: Mon, 29 Sep 2025 23:37:26 GMT  
		Size: 48.2 MB (48234517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263fee109e376d69cd8ab45eebe497b85f6bb9dab4d00421e46048f3b05dbc2`  
		Last Modified: Tue, 30 Sep 2025 03:10:36 GMT  
		Size: 28.2 MB (28155087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c052f36ed7138d27ebb7e300cd8fe66223f9064d8cb89d721192113efa6f0`  
		Last Modified: Sat, 04 Oct 2025 09:22:53 GMT  
		Size: 69.3 MB (69261597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4701bc7ece704ca33a82d3d3f7b7676bef048ab18a728870be4e9a59f82a996`  
		Last Modified: Sat, 04 Oct 2025 09:23:59 GMT  
		Size: 504.5 MB (504486650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fc51cbc7688a442ef8da313d453d7e649e2df7b942b5138376acb5ba440b556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16021893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63be267f112976b1a6dbebc2c8227deb2fdbe09d35bc869d23e07e62c5fe3c5c`

```dockerfile
```

-	Layers:
	-	`sha256:aa112cbc9624b3b7ca0e63e368e3052d052292d3c9797154c0d926a95330a005`  
		Last Modified: Wed, 01 Oct 2025 22:22:53 GMT  
		Size: 16.0 MB (16011717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b69f017155bababf4148bbc77624a745c0d1a383efb6e54659f0c14e7e8e9b`  
		Last Modified: Wed, 01 Oct 2025 22:22:53 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
