## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:5322a6ada464c7ae66be10436013813b9927d5d2cb3d824ba55cd9a44fcb9d3e
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:49a2b3da37cd499dea1130c7499ba1292cf6df9b0d9bbc31110bdb1f8cd8126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.1 MB (376109677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6424a40167b63cc5bfd53ad8a9fed4471a02461aa8f996b50244a9cee25eb306`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aca1310c7893c8969698b84214f772ad0bb081926610513c433a74753433a6`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 235.4 MB (235397657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd46236b51a0c0457f02a62e58b36d7a2479b238241f6023be4d6f665e9a7203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee490560fe66570d36e832a5d2af23d37a6fb0193b9dd060959382f8722c7c2`

```dockerfile
```

-	Layers:
	-	`sha256:95ea3aa99343091b6c530e5b4003bb9943baa3728eec9189ceaf82ac8f4d10a7`  
		Last Modified: Tue, 03 Dec 2024 04:32:29 GMT  
		Size: 17.0 MB (16956636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347ee90123489714c8c51b8c101dad86568718f1d6cf9349528215be573dd0a5`  
		Last Modified: Tue, 03 Dec 2024 04:32:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:64f60ab32c8ad2e44569bd34aeabfcbcae655596ac34599c5336dcb78f1347f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337698112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fef2df89ec55a84f53ca077a2e2093c773663a924f03a53bdb6116f54dd565`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeecbd78ab8f389d36bc7c389a258f35fcb1d7c525c852264f355392a01b52a`  
		Last Modified: Tue, 12 Nov 2024 13:57:37 GMT  
		Size: 203.8 MB (203846068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d24b2e38e21cc1d214a4e09d6ef1cda2fb1f0fffa2e118fef221c726e42ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da72b7f704e230a29b6d8886bd354cea7afd55b586897a8685011369124695d`

```dockerfile
```

-	Layers:
	-	`sha256:5cf2be7911debe59da7ccf2740ddae1696946eaf5fec6399bba7ceafa9082524`  
		Last Modified: Tue, 12 Nov 2024 13:57:33 GMT  
		Size: 16.6 MB (16624447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a10c1a45b73521ebcf10c889a4ba4d096cb8325e02ba6a3ce6727a8947f2c49`  
		Last Modified: Tue, 12 Nov 2024 13:57:32 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b689eecf5e3ddb65c714aada92e223d285c4ac43f13e91a42bf2d70453e2f3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.7 MB (319686589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d94e816c37f9669fbd10193e39b4d3611aa14e2da8cda9d3ae8ead77abaf4e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b86dacd9090665be47b5966a673c201e9be17e12af3a6b155bc5749678a52`  
		Last Modified: Wed, 13 Nov 2024 07:40:03 GMT  
		Size: 61.6 MB (61581104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793a5bb59c9cc98bd9311baf3dfda09c62cbbdad289968d6fd5656cf3da063b4`  
		Last Modified: Wed, 13 Nov 2024 15:30:35 GMT  
		Size: 191.4 MB (191397203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:530738ff9c47bd069bb02d245ff0123ec8dd415a3532a1dd1e8621051ad5d3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16645114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a801ab949bf85d546299940055d3bf2f3c3e94bb32c4d18787a752812cd89f12`

```dockerfile
```

-	Layers:
	-	`sha256:e35074208bc1e0fcf2be2ab9ef53e3c24eff11330b9eed0f8de0c375af2162ba`  
		Last Modified: Wed, 13 Nov 2024 15:30:30 GMT  
		Size: 16.6 MB (16634879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0260b6276ba30dd6d8f32b40f4415e8c535d07e946b378fbbfb9a22caadebdba`  
		Last Modified: Wed, 13 Nov 2024 15:30:29 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:671281f0eec1276bc2ca656b2b1ffb8425ed67a0e49b294864caedd8fe344762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363298796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53faff9404befb57b76d8c164f5d2ace4a89ec596aab481169cc2203aebf3535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da6ab97bb0c21d31a38290cf57289900a53f954b993db59f27f8cedb1eb175f`  
		Last Modified: Wed, 13 Nov 2024 02:43:36 GMT  
		Size: 66.6 MB (66621232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93041a7102a00ca946f6a90d08ab0c3a9d59d3a03288a28350e8a1ac235ee360`  
		Last Modified: Wed, 13 Nov 2024 08:06:27 GMT  
		Size: 222.7 MB (222667062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71c45282a4a3d4f4ee1dea17c38671d449a920831950d40d29a12b53bd1b9d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5cff6b2c17508fdcba6df91b61b43021773e82df652eb69bbe2b5bedd58098`

```dockerfile
```

-	Layers:
	-	`sha256:c660a0272b5e1de7faeeab0d3f1cb410c5dd067c2142155738f05b844de3574d`  
		Last Modified: Wed, 13 Nov 2024 08:06:21 GMT  
		Size: 16.9 MB (16935582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67bc6b3e84d44fb2ec77aecbbd46c6b065ae361aff2b410a64d8166d094b141`  
		Last Modified: Wed, 13 Nov 2024 08:06:20 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d366ce6267a346f53038978516f23bd4d6ee034c737fe7bdf5d54debb9dd3ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384246787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6f01c0e2e128b69c8f5020fffbdb84045ec77cd5254f9d865979f7e15f3029`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49bfdd692e8513701b0f0d930158f3f4d2aef5d64dff7bc22f6ccce56cf71b`  
		Last Modified: Tue, 03 Dec 2024 04:32:15 GMT  
		Size: 239.7 MB (239687994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7223f9d88774500fc3d64c0972df630401a88904948b414d81db8a6657f26dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16936367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff36bf12fbb75872174d04ce6204332f1de5ce54543955ba832418a0bee14ad`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ef7d7bc0977f2ee04016de60f61d61f1e875ffc5ded21289b535075ef5236`  
		Last Modified: Tue, 03 Dec 2024 04:32:10 GMT  
		Size: 16.9 MB (16926213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ada5f052e281d272d1947417f47424ce48e4072642dfae1ee7e16d1720a591`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ce8aa039e9a6e82c43c475c3fef10d04e2b8123d1061e406889d4b27902238ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347392359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f4a8116380ddc999b74d29f04f5c60cd5557750ff6bcdbdf6b754204fe5fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aac7a2dcb6a719b792ac16c19c2652ad08047befbc851b6ae687255f6838b0`  
		Last Modified: Wed, 13 Nov 2024 02:06:14 GMT  
		Size: 65.4 MB (65354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b021b9b5ef29ca07d0584978e6368d7c104c4da333fb3b2f41e3c5fd0643928`  
		Last Modified: Wed, 13 Nov 2024 07:13:31 GMT  
		Size: 208.8 MB (208811944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c879aa61306b6af21c2966d8d1d1c3b7ef264bd3594436ea3e5368f393c1aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546a610f8060307d18969256b9af525deb7e2d6898ab8ac5b12b4a9eb135d6c`

```dockerfile
```

-	Layers:
	-	`sha256:8a2ea7b2944f183bac3a45fc36453a325c7160840c26f1b60d78a02b64bdc82c`  
		Last Modified: Wed, 13 Nov 2024 07:13:12 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa2bb04dc00e35c862bd85cef6e11376c81dfc145ef71edcf86c2b27bc83bc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379158322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d3e46f31c4cca769ed8baa17c1406024a216cbf674dbfad17680f8112624ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f36575664f661fb4663abf9a54ae38f6714b2f1a53511cc1ffe3d8ddb1acb8`  
		Last Modified: Tue, 12 Nov 2024 16:11:05 GMT  
		Size: 71.9 MB (71859244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa16d103a10149cc71323be1b243e7c5970ffd7abda2adce550572ce6183d1e`  
		Last Modified: Wed, 13 Nov 2024 00:16:46 GMT  
		Size: 228.0 MB (227997573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee6c22b341c37400b40398ad3a5c48edf03c2821e2df1e51e37e5d6d19fd6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16840561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bc0918bff770173a22720926245ea5872f77e77a2a6bcf71c8e1ba073e9b32`

```dockerfile
```

-	Layers:
	-	`sha256:04597ff4f6060e3464b3e1edb39aeca284fc455c65149552bfa1dc3557e395c2`  
		Last Modified: Wed, 13 Nov 2024 00:16:38 GMT  
		Size: 16.8 MB (16830353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c649ff7e0878965ed21c805cdd1d6f0164b2e413054c4086d5b1394932145`  
		Last Modified: Wed, 13 Nov 2024 00:16:36 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:28f75fbff7fea1754f66f2ff9c7640c4c06fd16ffdfc224eb2f8fd1772f538b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.0 MB (456979288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155400acc66a00f8f4f35c553e7f4f9c8e73796171ecaec90abeb17edf42806a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fb889a6cd610a8a181a1ed9f57ffa7abe21fee8ea8ac8ad30325ce0b47c57`  
		Last Modified: Tue, 03 Dec 2024 09:46:02 GMT  
		Size: 319.3 MB (319347858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa374b77f1ca17f70075124a2c8053c4dafb365a746fcadab9fbd94e0e9c1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17012542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a6ebeb6a5606160740b66667e437826698b5d6d0790a7f6fd64dc0e8d105b`

```dockerfile
```

-	Layers:
	-	`sha256:a43d787d954c874af6db8dbc822b7d6e42a06c9c0cef5bcd7c1559891005d498`  
		Last Modified: Tue, 03 Dec 2024 09:45:19 GMT  
		Size: 17.0 MB (17002334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a213c48f55ff98d0845193b83743c6cf5dedca52db3ce6eab0b9aff84a3cf00`  
		Last Modified: Tue, 03 Dec 2024 09:45:16 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7df0d9603d537b9d3c5f1a8a582099e31643edb53b7140068d9af8477337c248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345160340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17453263e2e59ec60ea3dd351f693dd4ef90985f1a64c23abbb53ef8ba5906b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f5c95f0d6355567bbfbef044cac10682ae55767ca48b41b71050883b57bf6`  
		Last Modified: Tue, 12 Nov 2024 23:33:49 GMT  
		Size: 67.7 MB (67747015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef960ce691967777efc4ce38f0da26fa74108dcf45bb4fcff7e681d70ceda1c`  
		Last Modified: Wed, 13 Nov 2024 03:27:07 GMT  
		Size: 202.7 MB (202722903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd3177a0dd921bb2feb75924cfe3587695a304cea8580c1951d0a2c6f6aa8025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8aadf6c308c5edf63fd9014152f51b37b58c11162771288ed33d97585744e`

```dockerfile
```

-	Layers:
	-	`sha256:eb41514791b98768f3a0c6a5557723b8efeb52b01694a6ca70977a5710d8e7d2`  
		Last Modified: Wed, 13 Nov 2024 03:27:04 GMT  
		Size: 16.6 MB (16624690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b818347d73627d6e406ce24efeedffbd20244907dca8b460d44c47aeb13b5d54`  
		Last Modified: Wed, 13 Nov 2024 03:27:03 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
