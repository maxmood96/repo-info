## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:87949dc8a52ab93b2d3b561867aab4d78c56071d351555cb14542cc05f52b0ac
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ed757090c92b4dfba07b522d16daa7c7356e9a37794b71fd2cfc716b5f00df72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375207066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b1c36fa0c38ceed250a0a4e36aac2b80e6c07f522cff8eb8077ebfb6142e86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba00f95a0fc91aa5af7f7128d1d9cb3461821c06ee197cedb64680239a9330fc`  
		Last Modified: Tue, 03 Dec 2024 04:32:21 GMT  
		Size: 235.4 MB (235436055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9c8f539ce39e7b8310b4aa26beaf75d8b1c786c599118c0d371f9c05b88a7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499c1f23296ed70dd90fa678b5fffbcc3db5cdd0ba780ad4d8af8c81152bb1ba`

```dockerfile
```

-	Layers:
	-	`sha256:aeba652bd408371681685be2385bf3915a6ad86227cff4372d75fbd81cf44cf1`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 17.0 MB (16964300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d83ffd4c714db14b14c9bbfae084789a2ff936e4b23cf8b86d02f09a72ec0a`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c636e9375ce9ccdf6de8efa6e3d973ffdce8751197773590d30484535124384a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338494634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460619e39697127cad08ce61ca20ce2c9b6925d9fa694376134c3c7eac13d236`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0d6acc584d696ab456ac89386f5313fd7dbb30f7a4ea1f0fc6fa6832d72040`  
		Last Modified: Tue, 03 Dec 2024 10:11:48 GMT  
		Size: 205.8 MB (205816265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f530a531eb2590391f82e8e4cf42b9419b8e54b1381e532255b22150fa621551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d32ec904a4b93001545f14f059e71cb6ae5158832bee02312bbec5e06e5313f`

```dockerfile
```

-	Layers:
	-	`sha256:f53e2672493aee51835e2d7b671b1b06b1e16d7bd8ebfcf18e7f433cc21ce3de`  
		Last Modified: Tue, 03 Dec 2024 10:11:44 GMT  
		Size: 16.7 MB (16725662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d755ff4cd7ec164c2eea1f946a539eb3f3b3245d9a12843366600c388e0af987`  
		Last Modified: Tue, 03 Dec 2024 10:11:43 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c54092137aef82673b628701fffae1d7bb5cdee16036652cf8c5680b2311507d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320566678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69e8784e9a9a24c7018a57f98312596b243e702223ff357301ebb75ff9f02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2250e50c3b0d1679c6a6f0905a6bb14cdf995965365d96a0ed0af0a1cabeda41`  
		Last Modified: Tue, 03 Dec 2024 20:11:47 GMT  
		Size: 193.0 MB (193044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f0d17f8af67e79adb9ba470f17c5f6f7b4423ebee7b062e14e0213e7ddd14ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16741713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbf3a659f9762253c3305e4a0dcd4ebf822c59152a12c4d414fb236c480a1c`

```dockerfile
```

-	Layers:
	-	`sha256:021ec9171dbfc19c071bd17673d2e89c9aa2b95717e117707175c7f3598da4f0`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 16.7 MB (16731460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e86dd2f315ea5820a2680250233eb394bd4e588be2acb1a7a10b9232f138f95`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37a190a761023c4e140ccf9149b71929db84f08fec40f69f81803e339f665a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366490575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbec0ffdb40aa93cc2227f7e64678ce9711e69280737c2d9d4a8a2a696b515e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95ee2ae477988acf1c4f6dcfc88e1ae5a55fd73cb1208a350d7951447cd5c2`  
		Last Modified: Tue, 03 Dec 2024 16:25:24 GMT  
		Size: 226.8 MB (226790649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b69fd275d0a8e244814ebfebaa3277de3c5c799239fc1179eeb59b49cff6bb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17061306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d61e81a066f2bf03ec9ede670c559770001733b72dccaee56894ce1afe09a2`

```dockerfile
```

-	Layers:
	-	`sha256:10fd39fd24a909e9e91ac353e116e838d10121424f2fb2dd2eb94b5253aef4c7`  
		Last Modified: Tue, 03 Dec 2024 16:25:20 GMT  
		Size: 17.1 MB (17051033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781c922e20f55229b5dc779d96f6a85737b2f5c7ab8068980abbb055be1f8609`  
		Last Modified: Tue, 03 Dec 2024 16:25:19 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1e1cdc198e59acb495d0927ea674cff22326dfa3019424fb0a344a66225ca12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383151595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107ab0c39dc78b9e57ebf91be11e68f4bfea2c3c8274b2817e739d1abd96b2cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0699983953a7cec342f58306a547a993dc86fcdd09293e817b3e01512494b`  
		Last Modified: Tue, 03 Dec 2024 04:32:37 GMT  
		Size: 239.6 MB (239607119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de2d63fd3a08165ba0533d04f1b6b235cf235ac4d014dea6d58b91bc768784f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d1e208a7980646971042bf95ed3c919253fb965855df2f98f7c5d3284d1dd`

```dockerfile
```

-	Layers:
	-	`sha256:d0cb59f5654fc36e2048aa3b18128bf0764b4cba7b7276d4734c553f6b495f85`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 16.9 MB (16933868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bea586dcbbe73941b9db0060e0fb5b46aa2e20eeb654f2758421e9b06508583`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0547dfbac557cc82f91ff9d3cc0a7792aff95a51d762079858b162430e60dd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347422321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7c6f82843a852de7d471b5e790756f6d585c38b58bf810d09dccc2db82fdb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174684d328adb3f37db85b256c1516f8c1ae147bdb5b13929af1a4f6ef492496`  
		Last Modified: Wed, 13 Nov 2024 02:09:28 GMT  
		Size: 65.4 MB (65352502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aed0ac3a3dc812fc413b1c9ecdcb309ad900eb6275093689916b9bc369b08da`  
		Last Modified: Wed, 13 Nov 2024 07:22:11 GMT  
		Size: 208.9 MB (208917590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b40b4ad383bc02f2797fb61361bc793c8d9205f18bfd67c3c348b1e93f307c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e331f80b6125fa27291d60593eea6b39c085608c81601fac7fe5830b933a2fe`

```dockerfile
```

-	Layers:
	-	`sha256:8b8615a05e2498ee49181eb094c112b4d60e845b29d8913e037fa52efecc599d`  
		Last Modified: Wed, 13 Nov 2024 07:21:52 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6664a3df9dc9bec277c19ee01729befd3ce661e183f2a0d86777890babc7a779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382552567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645f0cf430b3644a88d2853e79a959d668b36a2196104d494e19ca8ee0e1e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52a720b71dddcb2a25df1c62f4df5be637ee1b44f6c72e886501e695c3e8491`  
		Last Modified: Tue, 03 Dec 2024 16:21:25 GMT  
		Size: 232.1 MB (232135861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46c273b1c0cfbdacdd361fa947c0ae293856b1182058b608e17adb484abd5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972b3130f5c0e09be05cbf098c2fe9f102fb226330c6a9f77a9e59b4e34ab07`

```dockerfile
```

-	Layers:
	-	`sha256:a680bd893b317b1e20138c7cae82c062fd4718a73928c1fe154c9a60ac52e652`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 16.9 MB (16946559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3348c230fc094aec79e85591b44365b40fe471dceb5ef063384a1515e5721ca6`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59ba1941b5338aeec3a0cfa33e35cbf7a6634dbab19b243d5e1f2ad7ec4edf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348067149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa8ee7b2b6de06d44ececdfdcf93f69002163b468f5578a592d090d370e3f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a64f4307ce70127ee567b338e88f1f2ee649800226efa44ea3c43335519c09`  
		Last Modified: Tue, 03 Dec 2024 10:49:03 GMT  
		Size: 206.2 MB (206192549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:915b11ec0eb96e2382ab827e0c58348af0eb0010af39c06e25906d2554e54c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16750919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92ad08bd30a617ab04ded34f7ee68e3521cbd1873667b36e210d31b28ce4f22`

```dockerfile
```

-	Layers:
	-	`sha256:ffaa49c4f1fce0f42bb1e16887927e5258dce89de673597e30a5b6c1eb3e39e1`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 16.7 MB (16740726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268a900434e3fa87efb67b84131d2f3d4b3d3693ad01f9f225707ca1c505edd3`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
