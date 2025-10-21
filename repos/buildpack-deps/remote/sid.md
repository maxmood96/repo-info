## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:1382034a2e2f3c3c5b684d258da54fb3393ff8959ea8e8185f6b96b1d786220f
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
		Last Modified: Tue, 21 Oct 2025 15:13:29 GMT  
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
		Last Modified: Tue, 21 Oct 2025 15:01:00 GMT  
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
$ docker pull buildpack-deps@sha256:3af0d643ae3c03999dd9b8bfa817512deae4faa40052fff85e74cf32aa8cf84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.3 MB (748299018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20d09c0c52074e4c13537645580857b0ef0339088b5ce0868c394e8671714e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022e41d633c4affaf1ac4e552e4213448a292b3aff35eb2748ee936cdab8ed6`  
		Last Modified: Tue, 30 Sep 2025 01:19:38 GMT  
		Size: 28.2 MB (28189334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbc4641a87c97f6e9e6e2361254a7f1b45a142ef503068f7c0cf3708f035a44`  
		Last Modified: Tue, 30 Sep 2025 01:20:22 GMT  
		Size: 70.4 MB (70426965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e039924dde5be80dc8faa6ab0c0cd8cc6919498c24d715f0086082f37e75c63`  
		Last Modified: Tue, 30 Sep 2025 20:42:42 GMT  
		Size: 600.0 MB (599996548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4ab8220f0b5738eafe18ce0b0104b1b8887c38a218e59920731b845238f74dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16224993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86241d58cf254c5f80d97af90128e4d55b650773d271b3e5534e7dac5bcaf3a`

```dockerfile
```

-	Layers:
	-	`sha256:ed757ca8752799dfac5f46813cde62dbbd76f6536820ba101d332b9678beb0ba`  
		Last Modified: Tue, 30 Sep 2025 16:38:23 GMT  
		Size: 16.2 MB (16214839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ab21ce3bd31af5271d573085ddcdc67c6faf13e31f3de82cd8adeaad8f4c49`  
		Last Modified: Tue, 30 Sep 2025 16:38:24 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:effaa099e49c53089ddd87f6100d3948021195f073e39521db1c2c7c307f405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.6 MB (704596123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a18c2b2a29473b052629b68e3c12ae35b6ce414beab34915f0cac27d34cf4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4775def833a620dde4f1cc169ae067301bfe3a34dcf5509c22eb227d3468f1ec`  
		Last Modified: Mon, 29 Sep 2025 23:36:30 GMT  
		Size: 48.5 MB (48517068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e4d8c8e300db469e918627e177662d2c9145c896127a833eae485613de801`  
		Last Modified: Tue, 30 Sep 2025 14:02:31 GMT  
		Size: 26.9 MB (26941858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355dcb4e6f8d4305f466d18918201a1d1987966e7ad83941fc93d52a3f5818a5`  
		Last Modified: Tue, 30 Sep 2025 20:30:18 GMT  
		Size: 67.4 MB (67390921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee46d4ef53fca69838df948d29fb18c713ea0b44c6b9e7f51023792fab32ffed`  
		Last Modified: Wed, 01 Oct 2025 19:23:15 GMT  
		Size: 561.7 MB (561746276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1785e4433ec00819b8ca1549fa98d7e21a76141383a82e702b1fbc32c863f355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bd9fb027f5ad0504f7ca91c9f8e45a75fdc136cd0b4eb1f5839a8cf5207a9c`

```dockerfile
```

-	Layers:
	-	`sha256:badd93ecb9f494d0c44cc33d7bc4448dfd647627ce40097d79dafa74ed67117e`  
		Last Modified: Wed, 01 Oct 2025 19:21:15 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:643e20d3c78e382812fa7f8e19931651dbe5c754b57e10c263e34e5f69ad9b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698586420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af33aa40f9fdec34a3955fa64896cfa9d73a64a842231a4b6e884b36f56c5afd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:77c8b650eb6fce09ed4263c2e250af93b45ee5839eef29ca2155317e0945bc1e`  
		Last Modified: Mon, 29 Sep 2025 23:37:42 GMT  
		Size: 53.2 MB (53152155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111aaffc2c801bff609a6e02c9de336f2bc1ea5c09d43a29d51e58997b20a73`  
		Last Modified: Tue, 30 Sep 2025 19:07:37 GMT  
		Size: 28.5 MB (28522160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984a3c965c22954420e5fc5d6d364efb5b25cb9467e9ee7553350dc94f4ffb93`  
		Last Modified: Tue, 30 Sep 2025 09:23:36 GMT  
		Size: 73.7 MB (73720279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94190c2cacb1fe5eedca0d37327174e55ac461832cc8679c8f42b332933f30ce`  
		Last Modified: Sat, 04 Oct 2025 09:23:08 GMT  
		Size: 543.2 MB (543191826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fa969484877915c6ffa657bace90aa42ec0aae56a986ea18f8afe8e9d6b55d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16229363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb4d966cff5504cd1c8ad2e59e0187ce6a6fc8c7b5fda481b3264c61de0548`

```dockerfile
```

-	Layers:
	-	`sha256:f3d9a82a0cb171fe808276ff6013f7c2a8fdad2a79140f7b548506313ca856e6`  
		Last Modified: Wed, 01 Oct 2025 22:22:30 GMT  
		Size: 16.2 MB (16219155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4ba4e4b3964fab91b4044fa09a705ca4ddc3cb1fb77eddb703cb8bdad39394`  
		Last Modified: Wed, 01 Oct 2025 22:22:31 GMT  
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
