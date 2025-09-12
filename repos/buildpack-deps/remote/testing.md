## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:fa973081147fd6f867d02216f9855929b1d806f4d4624a568c435a9b94912ffe
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0671dd909626fd8c20aeebd69e0398ea1ddced50f49d105ccda3d11188e0e6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337211268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ae72ac796003b6f98352d50c6615b0774b18e4a1d40e0726432dda7261201`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3cdde7daa1c8617934a7f6fc5999acbd8f13f45edd54e774f4a3af8f31fa8`  
		Last Modified: Mon, 08 Sep 2025 21:54:27 GMT  
		Size: 25.7 MB (25659714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c7415b1ab77e9af8efc826d62011c5a0c0c5ea052f4de5c46ff0ed4fc8b2b4`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 68.3 MB (68266149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee5514490a257530e1199c21bebc026e02392c336771451b453d5eb90b6115`  
		Last Modified: Tue, 09 Sep 2025 17:28:20 GMT  
		Size: 193.7 MB (193710370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41b5a93efc7dd73975eee1d6dcb2c52e80d27331700a60fe570a45682caeefa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16285471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b32a83e51ac74ab448eb05fd74da8115ee83041c832da2837aa62d2d206e98a`

```dockerfile
```

-	Layers:
	-	`sha256:ad5929115a0ee37c71aec49832bb818896e5ee32e82772e83de28044f681faa2`  
		Last Modified: Tue, 09 Sep 2025 01:20:16 GMT  
		Size: 16.3 MB (16275284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944c42f7f911f06b2f3be8c882a19e686aaa986b6fc4a04b1f7ddfc33e96359d`  
		Last Modified: Tue, 09 Sep 2025 01:20:17 GMT  
		Size: 10.2 KB (10187 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b6d456ea48e54c18b7221ba08b7f98ff67258d9856e7cba1ed7f0d6cd268b428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342770080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4099cff28979d6cfc4fd581b4e674fa87d61d39c3c2183d9e9a03a0c4014c63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'forky' '@1754870400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2fa5a98b9608d692994d9abcc2a7007473cf39d4da546665901804b35bd8b320`  
		Last Modified: Tue, 12 Aug 2025 20:45:48 GMT  
		Size: 47.4 MB (47442421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e8c08416a0595c07b904b87179f903faee6f0a25e5b00b485a3c0b0df46b2f`  
		Last Modified: Wed, 13 Aug 2025 06:07:53 GMT  
		Size: 24.3 MB (24331053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1486224fc8f64dbe0bf66d7516691f5822dfff3ac064ce9811427c63fb10b9c`  
		Last Modified: Wed, 13 Aug 2025 12:58:51 GMT  
		Size: 65.7 MB (65730182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67446a3d10ae9d03ae843fc879c4f1736fb18c208963a5bb5259ca4d4ee16227`  
		Last Modified: Wed, 13 Aug 2025 12:59:04 GMT  
		Size: 205.3 MB (205266424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61b9ec4000332e992e33599b138ae6a7151efd3e606849fe7f85fd96873c7cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16995194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70ef1311c3a186e25d9f6d549b40284f4a8450bb720af3d0357472d373fcd5c`

```dockerfile
```

-	Layers:
	-	`sha256:211702e95625ad2127681bbca87f797abb53ef66c5cd15f4af1c415150d9906a`  
		Last Modified: Wed, 13 Aug 2025 13:20:26 GMT  
		Size: 17.0 MB (16984946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3d11f9002a4789a13f8a199d8ee6a7e6f3db671bf7f34555007d76a8abc0b8`  
		Last Modified: Wed, 13 Aug 2025 13:20:27 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

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

### `buildpack-deps:testing` - unknown; unknown

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

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8751e84a5f4db9b1909db4384269e686b75a2cd36fd94960bbed4ad3367ba07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326355813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf56f7c454bd332574053055211c35c60deb95c44844414df3ad2a7a80469110`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ec7eb396047bfcd475c3064af0e813d0c880bc68b69e6192c860aa1172659`  
		Last Modified: Tue, 09 Sep 2025 01:25:47 GMT  
		Size: 25.1 MB (25079091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af77d2a7de68721cd0ac42531f98bd04847eafbed443a4058e3fef3d9fe456`  
		Last Modified: Tue, 09 Sep 2025 02:13:14 GMT  
		Size: 68.0 MB (68027155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739088ea7018af75be2181f60631cec7c6314a34e83516eecc5f68e3b422155`  
		Last Modified: Wed, 10 Sep 2025 05:16:32 GMT  
		Size: 183.4 MB (183386071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:705abfcdae39e4682fa18191914f537945abcdafedab22487578a51cc207d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16369691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d2d8a86d996b808dd9969c1f9ed2bd620d7bb93201d69a9d27f312c89b8034`

```dockerfile
```

-	Layers:
	-	`sha256:74d114ca009ae7f4ff525441bfd9815599d6bb0391611418b8bf4a81c4da5ddf`  
		Last Modified: Tue, 09 Sep 2025 04:20:51 GMT  
		Size: 16.4 MB (16359423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c5d8a9d10f7e1b4679a380f0fc5b2a2a6160671c5cdd5990bf98f9f30762ba`  
		Last Modified: Tue, 09 Sep 2025 04:20:52 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:08eaedda36542e61fc65553d9f1d53f2d5a2e4330a9af65468b5e7060eb76a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344619444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21bbce0b8a37c1f1adb316d7deda3d102e7ee4ff9700e9c23d47759914210c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160456f8adc4b90f7d6b65b9febd09b29220d231ef5935250170717564dfc2ef`  
		Last Modified: Mon, 08 Sep 2025 21:54:42 GMT  
		Size: 26.8 MB (26824472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73639472e8dad9dfb716e8a6bbce77939664b0fab7a79dae0ea141902d199b`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 70.3 MB (70328423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a3adacc8033e0fcffe64a6266d1b994745bcc975f06392418750d911aad457`  
		Last Modified: Mon, 08 Sep 2025 22:14:56 GMT  
		Size: 196.4 MB (196416739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ba999df8ffea0425f7cdc56088842ed6a616ae7d260660bd5c66dc85b00323c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16255263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212070e1d5a2e8a2164a8e38f7fb89b2db857531a42f8893146b58e4f0d7d36a`

```dockerfile
```

-	Layers:
	-	`sha256:34133ebbf169d898c84974f9dd1b634581b915cc734f8e1cd56b8525f71fe780`  
		Last Modified: Tue, 09 Sep 2025 01:21:04 GMT  
		Size: 16.2 MB (16245097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09478d013a06b76f42404fad777bc129f6b64e157adccb2e3d314bc643773e0c`  
		Last Modified: Tue, 09 Sep 2025 01:21:05 GMT  
		Size: 10.2 KB (10166 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

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

### `buildpack-deps:testing` - unknown; unknown

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

### `buildpack-deps:testing` - linux; riscv64

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

### `buildpack-deps:testing` - unknown; unknown

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

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6d644cbeefab84fef619db8ae335e9e06b8a4ca0baf3bcf612688569d5c40fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308432937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f4ec57ef879326d67939b701dbbbbc8583ec5e1f1496bd8f46e3a63047ddbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d70c4639b1bb56ca2bfa88a8dedfb6d14d5f6a857613b672fef601229bcd766f`  
		Last Modified: Tue, 09 Sep 2025 10:20:05 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23441d4a53386d92d68dfd117aef1e221cdf7c5c29e7c8841eb200ce14f89465`  
		Last Modified: Tue, 09 Sep 2025 10:20:02 GMT  
		Size: 26.8 MB (26840296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aced33c6860e9f1fad4c8609ff123d675ddb56caf85a90370df68696f49dccdd`  
		Last Modified: Tue, 09 Sep 2025 11:45:43 GMT  
		Size: 69.1 MB (69145858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6090314d9433b4ff810427f14b42d895fa789f61284eb5014414e5c9deb4c1`  
		Last Modified: Tue, 09 Sep 2025 17:24:41 GMT  
		Size: 162.9 MB (162863601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:370ea169c89c637346ef91b16542a10953b8b8eead7271bf3b219721636bf387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16062733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6367395779e111c88081b4c966193179fed94baecd8be11136c8419f3bb52a55`

```dockerfile
```

-	Layers:
	-	`sha256:f4353467ab3cf22e8e1317c584c85b689a78e58839d36a76c875988e38866424`  
		Last Modified: Tue, 09 Sep 2025 19:21:28 GMT  
		Size: 16.1 MB (16052545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54358e5d594b4dd5389bab94ae93d8f448ba491a8ec62f4fe6eb131d2a7eb2e`  
		Last Modified: Tue, 09 Sep 2025 19:21:29 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
