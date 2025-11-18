## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:3dfbc5fa6ec05ebbcc967afb7c19991b96b0ca73370e1e9becb989c275d013bf
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:80882520b36b209536046f3f88f96d3c608333a002de5cbbe1972befbae06543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343168565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a286c9960c46898daa20ee31ff72632668bc39c4d9721a08a1bf1588aff6e710`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:14:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f19ac06db907fa72eecf21fa150fd26d99a092e409ed5349cff34755befbc8f`  
		Last Modified: Tue, 04 Nov 2025 00:28:38 GMT  
		Size: 27.2 MB (27195269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ec5cb615961fc44dd0a7c713d96d2a3966c5c0893d5d0298b8055415ec4409`  
		Last Modified: Tue, 04 Nov 2025 04:14:55 GMT  
		Size: 68.5 MB (68451097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907ee23dba4a7a5d75a14a8a6c29c878d8242ab766174bca91e1309e4ee76b0`  
		Last Modified: Tue, 04 Nov 2025 14:30:44 GMT  
		Size: 199.0 MB (199036559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e59ceb5778d005df99246ce464d1ef35df2d4eed83b55fc56b7f6b99d5c315ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16265316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9218b6ab9bce8bf7355069ba1308e04b8527c05215db5c8d09f049ba85b37972`

```dockerfile
```

-	Layers:
	-	`sha256:d420574cd1bcadec301ae7ef80a29121b5602e351f045dc1c1b3385d17bbd278`  
		Last Modified: Tue, 04 Nov 2025 11:22:49 GMT  
		Size: 16.3 MB (16255183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57688ae21eca80046ffaebcb0c506daab67666b7555b6c37c5b583cfb1169f39`  
		Last Modified: Tue, 04 Nov 2025 11:22:50 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a1b1f72af6f6338079f7148e1414e729883132f423295d996e124fd0d7676ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293756718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879640722112188115c407ba72ffe504e9f1cb55ab495f4c1368a6f718c1861`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:22:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:249f143dbba2558bd4f87316a884ba0d2b99358af5b3c63e9ac2b9640e6f9846`  
		Last Modified: Tue, 18 Nov 2025 01:12:47 GMT  
		Size: 45.0 MB (45003691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd7e51b270e55f3a7a9a2d43268061869ee4c4d0b6076dffdec9ff8ef06009`  
		Last Modified: Tue, 18 Nov 2025 03:59:26 GMT  
		Size: 24.9 MB (24946289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b78319f4c6f1757d125d21ba9e88a135787bf828fe59c5234a165914a13aa00`  
		Last Modified: Tue, 18 Nov 2025 05:29:13 GMT  
		Size: 65.5 MB (65528313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df725a769d8719e32d3cc09c4683ab2b9cb9a8b0d734fcdd3bc1d185e839ed`  
		Last Modified: Tue, 18 Nov 2025 06:23:29 GMT  
		Size: 158.3 MB (158278425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:192ef01aed1a92e6dc46f0fdb31977540ae3afdfe0a8ba33dab9bb6f2fb0b1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16021486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6101b8682a5d52af287680d3d83434f568491e741014c15b9c1b7e2a94b9e6`

```dockerfile
```

-	Layers:
	-	`sha256:fe50c8ffd0a9ca0a7166497f210f77086270da4dbf4ebd8838387b5c4cdd0a2a`  
		Last Modified: Tue, 18 Nov 2025 08:22:52 GMT  
		Size: 16.0 MB (16011291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042310df324321e36cd1823df37fff7cb35fbfbfd7c07a0b4d55414c8dd31113`  
		Last Modified: Tue, 18 Nov 2025 08:22:53 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:09b935d1db77f92cfe9ebfe2b68f1cc88b8abf5ecd2a77056eaf00c6370f1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334679300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2d24efbd9fde0f77105660116833e9843f9e3068d3a4827868080ceca52527`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f615e7cb4b13e78f79053e3ff3386cb79b093cd2d91fe819f692264eb1475`  
		Last Modified: Tue, 18 Nov 2025 03:26:37 GMT  
		Size: 26.4 MB (26445334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8961176208fb3c6520aee3a23dd4452025d1885baea507b988ee8fdfe1d8b591`  
		Last Modified: Tue, 18 Nov 2025 05:39:35 GMT  
		Size: 70.5 MB (70473388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf2e288fc97b8ac4d59a1e19623443f9d468782962eb3f4ed050296d55b7f7`  
		Last Modified: Tue, 18 Nov 2025 09:13:47 GMT  
		Size: 189.2 MB (189169189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1256c463e474f81d497ffb124828e27c6f7155e2f867c5654ca97d14180ea27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c945c66cfbe74a5bce3db4dc2ae08c86ed658c548bcc74f8966ffe51a7334ff`

```dockerfile
```

-	Layers:
	-	`sha256:61430c1ddf44684f3fd275b439437107189e4cb49bf8fc75307293ee228a12fe`  
		Last Modified: Tue, 18 Nov 2025 08:23:06 GMT  
		Size: 16.3 MB (16328892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d93e86de7d873bcde12b7b009830dee3e34c46bffd91f11df084712c041a4ce`  
		Last Modified: Tue, 18 Nov 2025 08:23:07 GMT  
		Size: 10.2 KB (10212 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4be685340503a9a03a404f05ed39e97c8faad113923190eb0806e306753fd00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353746873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73306812d9e33e61f02f5e86539bdb9eebee3bddb3cc5a2b88c048b145454220`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:10:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b1df74e42eaae76d71bf2c2aa402328d711dcdb63b4080ae4e7050388c00bad0`  
		Last Modified: Tue, 18 Nov 2025 01:12:57 GMT  
		Size: 49.8 MB (49833161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f52a4943d5de6ba698c20cbf767503261cc0eb7a108778d7a744e58da50d69`  
		Last Modified: Tue, 18 Nov 2025 02:57:26 GMT  
		Size: 28.4 MB (28445026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c64ad57b1efbe9eee5d9f5467a2b33ba6f6ba2ddf2dc652251bee45a3cc32f`  
		Last Modified: Tue, 18 Nov 2025 04:10:48 GMT  
		Size: 73.0 MB (72966735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480e8cd920336bd68820ef5b18788d283fe9a92889b63f50618ca85845e5903`  
		Last Modified: Tue, 18 Nov 2025 05:56:27 GMT  
		Size: 202.5 MB (202501951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:966d8d4c4cd7285c6b728fc7b78b9121375da87e47c5472f5b259618a1d7bcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16234234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c703f61c81cc021e755d18285462244225212909c4b2b4869c6dbb5eeb5f1ab`

```dockerfile
```

-	Layers:
	-	`sha256:921d4dd0abe2fbbf9b8315864302fa6f64a08e2de4fec5ecc264d3a2db717670`  
		Last Modified: Tue, 18 Nov 2025 08:23:20 GMT  
		Size: 16.2 MB (16224123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d6e292b5065f902a4c4eb5e4bab7dd4da2f90bb1a690264adb7df3ed477407`  
		Last Modified: Tue, 18 Nov 2025 08:23:21 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c61a87759a60fc6c2dbe2ecb1470c1b782e48dcb6aa83e72c454d39534c2a124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347838903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ece86a81f66379fb397d2fe5df00997f229a6354a4c68f6acf92b121b45e5d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 06:27:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 16:00:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:48:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:030897837715e5a3cb573dbccbde37df9e71014e141907c9a871969c5845717b`  
		Last Modified: Tue, 04 Nov 2025 00:16:41 GMT  
		Size: 53.3 MB (53318000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e937e4e09e15f972661a8c6ed2f0ea78f89b82022e280a058f528fdf12a10ad9`  
		Last Modified: Tue, 04 Nov 2025 06:27:54 GMT  
		Size: 28.8 MB (28800901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ae50ca45c68485a1e0779cd0d1677ab8264294e3955f02934433dcd62e86e`  
		Last Modified: Tue, 04 Nov 2025 16:01:50 GMT  
		Size: 73.9 MB (73870257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee8c8642ebea4ba7aec7260a60e3ac4007dd6f27022e16d551e7a03954b4e7b`  
		Last Modified: Wed, 05 Nov 2025 03:19:00 GMT  
		Size: 191.8 MB (191849745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f0f507b80c8ff2bd2877a6f367f84195d737632223087f5d9f20be4c2f92f5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16239496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d736a0b23bf06c88fbee5205665782f06d1bf217807f3e08628777b2ddddcbc2`

```dockerfile
```

-	Layers:
	-	`sha256:53049be360f65facdc4e6152295b3e979a2de799eaa40d1393a17f9ba07bc431`  
		Last Modified: Tue, 04 Nov 2025 23:21:06 GMT  
		Size: 16.2 MB (16229331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b29aadb34238600f61236f3732b7bdd2b3e17b0c5a6ae4daf40671a49b3fae`  
		Last Modified: Tue, 04 Nov 2025 23:21:07 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c9dc948317a779a22be5f9d55d22d8de14ae1b28f113b49803ca352ae9e8d514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448117206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa487ce96cb4194fe28a193d33c66add1a756116f6f133688b3aa4851ae629`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1762202650'
# Wed, 05 Nov 2025 11:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 08 Nov 2025 03:50:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d83aab6f1b53b0725edaae6679e08548e39316074675f21600df7f5620f7fb5`  
		Last Modified: Tue, 04 Nov 2025 00:17:08 GMT  
		Size: 46.8 MB (46794261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cbd09f8069207ccfebd2b0e21dcb66c15200b5b8eab72b328a2c4f3d36206`  
		Last Modified: Wed, 05 Nov 2025 12:01:22 GMT  
		Size: 26.4 MB (26390857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041459d61bd8ccafd4863eb62da1abb5c44e1055873a494db7650c8b3d6efe57`  
		Last Modified: Thu, 06 Nov 2025 07:34:31 GMT  
		Size: 67.2 MB (67202955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ed61d51cef443d422c0a06e6b1011e8f0a8dc0d81ebc19a81bc79e7ccd727b`  
		Last Modified: Sat, 08 Nov 2025 14:22:27 GMT  
		Size: 307.7 MB (307729133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f853d151c965deae4c986bf278d93725475bd29373b809afd3d78bd759cfb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16311291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17382248bf6830f2f5a1bae17d0436a5b60bbb50042239d0ba07dc5b87f6e7`

```dockerfile
```

-	Layers:
	-	`sha256:ba8bc224a96cdec55cb1afec0d6209ddfc75468a243297e890a8964f068aff9f`  
		Last Modified: Sat, 08 Nov 2025 05:20:59 GMT  
		Size: 16.3 MB (16301126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:527c048eeac1d8a6719b437695e92c818fc9c3697a95fa8e909cab9e37daaa85`  
		Last Modified: Sat, 08 Nov 2025 05:21:00 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dc44beecb5d3948f9e1f1201bf176701993a925357b9d226fa66213fff814848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311385121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97454f7580357edda1d6a16f6c7b34473d81a23a5d60553d4292d2f3fbbb1323`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 10:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:28:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ee07654f71bb163a06c3532a844efe8d75683f4dd53a88a8109fd9ed1b66fc1f`  
		Last Modified: Tue, 04 Nov 2025 00:16:26 GMT  
		Size: 48.3 MB (48346444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e24f5b3ee730a867fae54f44e0b43c0311d9bd66c565a7c2a2b0d7a887c220`  
		Last Modified: Tue, 04 Nov 2025 10:03:07 GMT  
		Size: 28.3 MB (28324175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137dedc8726298d18bf0cbb080b8d89391fa9483e0163fecf362cfc0f0c4e9a8`  
		Last Modified: Tue, 04 Nov 2025 14:52:14 GMT  
		Size: 69.2 MB (69187515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f5346c1e59fbc781c938ac583a768412fb4b756c403402f2554b1cb24d153`  
		Last Modified: Wed, 05 Nov 2025 03:18:51 GMT  
		Size: 165.5 MB (165526987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cbbae2a74b33a279d5696b55388d0fff4052e6fa98a546e2642dfecff09a4075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16031980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedeaccfc067afed430681d2d02a2091fcdccf05047bf5e617b8adb3609d62c7`

```dockerfile
```

-	Layers:
	-	`sha256:628f765237fdba55c86092221e6d8eb6a4300e9875a213abe1da95de43fda825`  
		Last Modified: Tue, 04 Nov 2025 20:22:00 GMT  
		Size: 16.0 MB (16021847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677b41396d500c6b5bd20019db7eaa8d26800797095caebfdf6fc81eaa8c4e45`  
		Last Modified: Tue, 04 Nov 2025 20:22:01 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json
