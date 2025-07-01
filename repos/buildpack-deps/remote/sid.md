## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:f75addac5cd39ba1ccac2c3806a60b124bb0539a0f1bcd7c22e7694249207729
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
$ docker pull buildpack-deps@sha256:c4164a88e5d9d0c29a9455813c35d6442e0be8884948a1c334e1b006156ca0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334764099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea577f8b0051e5868605c3778231bb4a5bfda5b8c733aca84e7e8fdec3229af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:603de70df79137e44ed9b8e9d2eec3a1b8eb889b8a8650df1a6bfc2ba9798f72`  
		Last Modified: Tue, 01 Jul 2025 01:14:45 GMT  
		Size: 49.3 MB (49267699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b752883ea09044589f48c52df49289712f416806e7b67e6d3b283e6c96ac266`  
		Last Modified: Tue, 01 Jul 2025 02:25:34 GMT  
		Size: 25.6 MB (25619155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14a16253ea0df4ebeb77b1db25ac37e73812925ccf4de831d1f7bc411f2c38`  
		Last Modified: Tue, 01 Jul 2025 04:11:59 GMT  
		Size: 68.2 MB (68209103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a7e6712aba6de069b3bb66c090c22b9c48d12c91f5125d308722d20000d452`  
		Last Modified: Tue, 01 Jul 2025 13:41:18 GMT  
		Size: 191.7 MB (191668142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179fe3fee18d736ef5451ef970f7f83369690992bdd922c6543b9c4e266cc390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16325075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2415d21f10d0419f78786da88908449bec3477c20cf2aa40769e8fc78589e2bd`

```dockerfile
```

-	Layers:
	-	`sha256:69fad41b22438173645da091585cbc19b78c9005c587bd0612eb3ccd89413f5a`  
		Last Modified: Tue, 01 Jul 2025 07:20:53 GMT  
		Size: 16.3 MB (16314900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12da18078ce36f0258c7c011197fc80817829ae9ceff763d34cd032dab998388`  
		Last Modified: Tue, 01 Jul 2025 07:20:54 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a79dd4363377eb55a56f534837806281668fe3daee6a91514f2c301996a9a504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299783149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57e55816b46c11c9e3372653c6b34ce88c1e368e79f412baf0800338277e426`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd39e087bd20994f06786e43ae83cecd3968cf0c8e31fda1f457b3222b6b6540`  
		Last Modified: Tue, 01 Jul 2025 01:15:07 GMT  
		Size: 47.4 MB (47440208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cf909077bd520f713ad0bb67e6ba6cb18dc45cf617fb6f8d5e7a63b048c164`  
		Last Modified: Tue, 01 Jul 2025 06:08:19 GMT  
		Size: 24.3 MB (24345967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df6e38020028956bdeaa81464be7d4bdbf7dcfe67640edf45bca2f56aea465c`  
		Last Modified: Tue, 01 Jul 2025 09:29:07 GMT  
		Size: 65.7 MB (65731968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39118c1d17da3027cab228f9a132eee3d7c6a0046bfe45fca6f8316e6a79e91`  
		Last Modified: Tue, 01 Jul 2025 11:32:38 GMT  
		Size: 162.3 MB (162265006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e3a050e4861aba08a27e315fa8d8da8af9b148ab1ef8598b5291d33e8516270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16096456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d24869486517d1c7a05d107967826a68e34480a531832aa9a9b13700b1e2283`

```dockerfile
```

-	Layers:
	-	`sha256:222577c7ee976706a3f85ccb985a316ba87b61658c01803da906c138054cd306`  
		Last Modified: Tue, 01 Jul 2025 13:20:53 GMT  
		Size: 16.1 MB (16086220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89729bc616d8d49b79e7be069d608ef2d3999ea50aa93f0c6166e9f359082e4e`  
		Last Modified: Tue, 01 Jul 2025 13:20:54 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7f25d96f8778c197f9a39c8557dd85be4401dc853cc5ebf2520c493763e46962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283118071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2faaa371e9f5cab4cc96ec8fbc0303ba286975814ddff359736d615b5a699648`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c9f75345f8518e5dbbf40af904c00f3e014f0846ed6946f7fe425ac03a8e75b1`  
		Last Modified: Tue, 01 Jul 2025 01:16:26 GMT  
		Size: 45.7 MB (45709047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f7f9ff4c752d1f9e8936db04d44226667ece5c3bad3798a0f88a5404d9f206`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 23.6 MB (23618470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59681cc62ca4eb6c592f99e5bde64f4b1fc54a1a76864ebda73f827aa1b4361a`  
		Last Modified: Tue, 01 Jul 2025 18:31:01 GMT  
		Size: 63.2 MB (63153351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d3928969f5557af0549e2c21f071420200ba072ed9d3c491efcc30afaea2a8`  
		Last Modified: Tue, 01 Jul 2025 21:42:05 GMT  
		Size: 150.6 MB (150637203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:33322eed4adec1c0f346714eb4c4b342872fa20ec1585263ea44e7607334b1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16092747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81544bc1c3d03a864eba867bc5252299f0a230e52b2f873fb31f8359be056fd2`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d544c2fdb091cd407e2b2f61b040b687815847ecfef57b029ac3c2f9c6d8f`  
		Last Modified: Tue, 01 Jul 2025 22:20:36 GMT  
		Size: 16.1 MB (16082511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588bde7eea09d5b4fe75eb7c7d7cd835c625de39e01987894f949f548c082630`  
		Last Modified: Tue, 01 Jul 2025 22:20:37 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:243b81afa2ff1dbf9d5e5d3fa2e32bc117804e2f2450eef088e6d9a81b7e50b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324591714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233457507b321403f789432a8bcac34ae2aeec07719dfd5f2f93a7a75fdd1e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:22b8dcea0b04f0cc6c2f22278513a305f4657bbd6ff8b7b3b8d205b40cebc22e`  
		Last Modified: Tue, 01 Jul 2025 01:16:26 GMT  
		Size: 49.6 MB (49633737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba22b3a401d582005c703416897d35ba010c24db8d110f9011886e05173de3`  
		Last Modified: Tue, 01 Jul 2025 06:52:58 GMT  
		Size: 25.0 MB (25009526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35fdfd4f8345d7a21ff603855a2ab09ed78a0c3589580e64572c63d5d766676`  
		Last Modified: Tue, 01 Jul 2025 13:30:24 GMT  
		Size: 68.0 MB (67986192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92c041748e4f79727291fcf7ecbc709fca99226b2a1aac9314890e041fab873`  
		Last Modified: Tue, 01 Jul 2025 17:14:58 GMT  
		Size: 182.0 MB (181962259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44c50c898c904d2dd4475b8869ac7be8ccdebb9c9b808596fbb9bb1b54ae2571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16409315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b539052318ff79c7dff01e2c0705478d6261273c91783f3988e5265a723764a`

```dockerfile
```

-	Layers:
	-	`sha256:002a631f915309f1a8d2bd343d7421ec98d57ae742e0e79bb8387f9fc9472668`  
		Last Modified: Tue, 01 Jul 2025 19:21:03 GMT  
		Size: 16.4 MB (16399059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7fb827a6625bc746e53f28bb2d715665cf0c3fcd00b6be546a19e550532f4e`  
		Last Modified: Tue, 01 Jul 2025 19:21:04 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4fc103f996e35de2cd316f75bcadbe42304eebf2596bb401aaf65f3631d12fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343056822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc34ec94a13f524654d76addf8be866b252892eb47e36311b5d8a6e811ffa2e9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41ea081e29dc4034ec31a49ac48ddbf738b840fd4d226f5678cb63f00b10ab33`  
		Last Modified: Tue, 01 Jul 2025 01:15:01 GMT  
		Size: 50.8 MB (50790707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d224078a83c5498b9115edbeec34eecaddc04a9e2e47f0e71d34a7e780a2059`  
		Last Modified: Tue, 01 Jul 2025 02:24:36 GMT  
		Size: 26.8 MB (26773974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6014d1af113edbca3a63a8a8aff65bf03bbb831dcab023e346303a638c1250`  
		Last Modified: Tue, 01 Jul 2025 03:19:59 GMT  
		Size: 70.3 MB (70286001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3b4b6aef8ffc726b6e5209bdf37883d83d71e08f64c1f66f265682fb1d8c35`  
		Last Modified: Tue, 01 Jul 2025 13:41:19 GMT  
		Size: 195.2 MB (195206140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8ea4ded8436acf53fef42176583fa4f6f170d064452512baf566721e06c02ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16294914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55f9eaefa62c700b72769806dae70408791a9342eb47681e5f0ea8b9c6c1f22`

```dockerfile
```

-	Layers:
	-	`sha256:3920cbaa88391d7c35b068c7acd34712cab409cd37404f397cc39e021fbeb313`  
		Last Modified: Tue, 01 Jul 2025 07:21:43 GMT  
		Size: 16.3 MB (16284760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c958c7f547e5d5876de665c59af41c37ae2d1e9c6d9ae6a10bbc04b3d1bcb296`  
		Last Modified: Tue, 01 Jul 2025 07:21:44 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6d01c567bb16df88fc5122452179444291b271126f62189fe965656a8fab5df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313950586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5051cb5a5ab58f4824e0e420e7742cc16d4b0b7b1dda316d083c6c3bbddcc6a8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54a8735d26fa76df64dcf3824b7f78b58d44ea01ab0788f2fc33afa2bac4f1ad`  
		Last Modified: Tue, 10 Jun 2025 22:48:52 GMT  
		Size: 49.6 MB (49553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ee97fbcbae75cf1777c40791b1a1c25100c4b6ad8a9ed9323cceb66a38ba5`  
		Last Modified: Wed, 11 Jun 2025 13:02:36 GMT  
		Size: 25.7 MB (25652069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd97199828602994822322c66b6b3a65083d16ea25127f0a48c6b159108cd4`  
		Last Modified: Wed, 11 Jun 2025 22:23:25 GMT  
		Size: 67.1 MB (67072610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0870155614264814890e54a8cb3796604707e92918a524a16a2b3c9198cb976`  
		Last Modified: Thu, 12 Jun 2025 07:23:03 GMT  
		Size: 171.7 MB (171672652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2e3c6d5a41f6932884d552b0b2f81bff40b48067a29dc3826c62586dacbf0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea1e26f971bdb9d3f4431086fec8f49096400a1122d71cac27a778dfcd22adc`

```dockerfile
```

-	Layers:
	-	`sha256:0ef860f332fba2152991b0c2090ca64df71eb5f14b7a7c7ed19934d3178e97f9`  
		Last Modified: Thu, 12 Jun 2025 07:21:03 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:46a1c96d0543acdcbdb257c41f329321a4a9e92e513a92e4642a66de11bc7fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (339039001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e8c0dce6d888cebdeef630e26b9242c6f4723a310835e84c16dc1aacc04983`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ffa7252988b58d241b86b58e553a13c9ab6ded3d6fbdc73ace28ee71d043ceae`  
		Last Modified: Tue, 01 Jul 2025 01:15:58 GMT  
		Size: 53.1 MB (53101309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770aa93e38d20512e91dacc6e2f7a3a7358bc81f356fbf0317b659cafa8ac481`  
		Last Modified: Tue, 01 Jul 2025 05:07:54 GMT  
		Size: 27.0 MB (27003579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be88bce329950d3d92db09ce4cf3130958aaf32bd985856e638aa08ff050d4`  
		Last Modified: Tue, 01 Jul 2025 10:11:01 GMT  
		Size: 73.5 MB (73477356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e93c27ba3df5c9579debe99bf398e35fda7ab54ddae2cbe39c59c6c975c43c`  
		Last Modified: Tue, 01 Jul 2025 15:04:01 GMT  
		Size: 185.5 MB (185456757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a14b5e0446dc7d65213cd34611afedb55e08b7111167ec6ba345e084e0cef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16319101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff22ed2e4fabf202b8659667e03c6c83a4ce85209f9902b6bee1943ea5744f7b`

```dockerfile
```

-	Layers:
	-	`sha256:aaf292dd0ce9503433e9858a939fbfdfc06a08a7eeb81e975775961f3ef05fe3`  
		Last Modified: Tue, 01 Jul 2025 16:21:20 GMT  
		Size: 16.3 MB (16308893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35f82ee36a69fc34b8248281973336a0199d92433b3e74ac5d99e30cc722207`  
		Last Modified: Tue, 01 Jul 2025 16:21:21 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:29cd3278281f582ad5cd57b939d1284ad99df3eebae2c7fbabed6de117c7722f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.8 MB (408765791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bfeaee9d71d7bc1888562d29e9a9a29bfee53216b4996013e45c07038e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:42f7c08d656e09c01f14d35a847143f84e881d1ac3f16f3ba511348bbbaa7d82`  
		Last Modified: Tue, 01 Jul 2025 03:27:03 GMT  
		Size: 47.8 MB (47756066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4ef3bea202b6f661456b37f5106a6a6e0acda6439394bd6618c6150a35c24`  
		Last Modified: Tue, 01 Jul 2025 02:22:42 GMT  
		Size: 25.0 MB (24954336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f59f94fee11898b889be78db1b26357b77690be8753df91b533098e18b75eb`  
		Last Modified: Tue, 01 Jul 2025 03:58:27 GMT  
		Size: 67.1 MB (67092192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5105cd5e447d85c1f29b081d53f831277bf3fc355a0e4055af207a99f0da902c`  
		Last Modified: Tue, 01 Jul 2025 13:41:04 GMT  
		Size: 269.0 MB (268963197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b1d1a3cc531f6c108f69dfa48143d509611ec16681a646d1ec09711bfb253bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16380929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db7e11bd3c98961708bd002af9351c178ac22039c3d2c0bd71a41d65f0dd571`

```dockerfile
```

-	Layers:
	-	`sha256:3810125539ce82c0d26a080afe93db147515d71940cf1be0198ec978a2a2e08a`  
		Last Modified: Tue, 01 Jul 2025 07:22:11 GMT  
		Size: 16.4 MB (16370721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4529d741b7463f6429cd17e4d2f240111d3a5dcfb5ee905cb362c1329b230eb`  
		Last Modified: Tue, 01 Jul 2025 07:22:12 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:981f4a0bdd95ccf3fdacc2fec2002836b4c286f3b36890d50e565b6c04c7236d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306799070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d18b49fcffcab43dcf5e0071b6edb6031091e6598143c94985234521d90671`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acd445fdd6fc8a863e2e2fbc1f6d0dd614a42ad5a89118b6cd287f18c027f79`  
		Last Modified: Tue, 01 Jul 2025 01:16:17 GMT  
		Size: 49.3 MB (49346648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d516536545f6fd66256972b93b51614ab1c9f96883e1f5c8990597ce59c040`  
		Last Modified: Tue, 01 Jul 2025 05:31:15 GMT  
		Size: 26.8 MB (26786410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1529b246d5d5bf9d3254f1e2eb47235c74e91731ad440f78e506bbce83b45`  
		Last Modified: Tue, 01 Jul 2025 08:57:01 GMT  
		Size: 69.1 MB (69050301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbe35be97a87d8a3005c2cf1206b23fa3ab8c4825dec4de51f8aed0b29eee2`  
		Last Modified: Tue, 01 Jul 2025 11:33:30 GMT  
		Size: 161.6 MB (161615711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c216a529dff0f442991305d4aa82e36af373721d4aa68724adfd176f4be61368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16111685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8529d527c62b0d82b508bcebee88ed326d659181f4c93223cd7f24093b252fbe`

```dockerfile
```

-	Layers:
	-	`sha256:66b1ae7d4ef29c8b94979109bb61e9bc9e91a670501fa12a3e6db292f7e46006`  
		Last Modified: Tue, 01 Jul 2025 13:21:58 GMT  
		Size: 16.1 MB (16101509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fc085defaf6f99f8aa8bf19cf9e968a3d0c7974e756a634c2b03681cfaf3f0`  
		Last Modified: Tue, 01 Jul 2025 13:21:58 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
