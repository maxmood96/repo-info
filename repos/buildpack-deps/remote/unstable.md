## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:1df53558ff34c0ea6328ba2555a408167f8377a7a59ef08691ccd6146d192d6a
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
$ docker pull buildpack-deps@sha256:fc11ba063b82a26c1aaaf9ff913e2f42b38968fc96aabba5f348fa24bb84e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339648124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2412990718bb4a573f9f18cbe21335f389216ae3a56619ded3e9fe3a2d1b79f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1d176aaf0da811a990a68b00d62be046f5280d8af55d181ec19374dc20c48`  
		Last Modified: Tue, 03 Dec 2024 10:09:16 GMT  
		Size: 206.2 MB (206198824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e16dc7b915d3d0791b2041d90a71ecc8ea1c0bf99101bf3b662e76079e74796e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16726539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66439361d67768c2375720d24cefced238c05f8ac79e1bde6cc06c0da714b789`

```dockerfile
```

-	Layers:
	-	`sha256:866634565228e1d5aa4a5e80f89ce85ac632f579ef0877313377f0be77c0ae38`  
		Last Modified: Tue, 03 Dec 2024 10:09:11 GMT  
		Size: 16.7 MB (16716303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9ad5080cd41fe18f0fc7d92d9fa984cebecf82fc59f5b44440982d9eeb3217`  
		Last Modified: Tue, 03 Dec 2024 10:09:10 GMT  
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
$ docker pull buildpack-deps@sha256:ca61d6852b240556b0c5025d7f1014496fd6dbd6959ba15284125e8f227db88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367594810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c8a6d0a7704491e80b1b6051b22b8da2b45b5ab7c289a8b4b898bdb2403e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5b28a91332cf32753c210d1c85e5266c3b7e92424235f8727d4db4f66ded61`  
		Last Modified: Tue, 03 Dec 2024 16:23:31 GMT  
		Size: 227.1 MB (227082152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7394f0f1c8a9b15dccaa6fefc028952784772f293e1527e33fc2efc01fc6f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf323e37d0ebafb9b1996e2fb4dd9c969df7be1b7497e4bbd149a119488abd`

```dockerfile
```

-	Layers:
	-	`sha256:f4a8d74b3828d20c625ad2d3d2553dfff0eea81de99a2522eaa7d503bbb04182`  
		Last Modified: Tue, 03 Dec 2024 16:23:27 GMT  
		Size: 17.0 MB (17041744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d829fcc8e021404ee2581ca56cf93a9bf72b86fc9de94a648f2798d2f734be`  
		Last Modified: Tue, 03 Dec 2024 16:23:26 GMT  
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
$ docker pull buildpack-deps@sha256:6bc19564fe24be256fafa93692fee2e057f1bfce2a467077582364c36f312501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383146258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b3a3d439cd386298430241ef8eb9396878bfeb4ed9bef7199ba205959d5ef3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a580742dd0d6b25eae1fa9319e34f6aec541ba477a9cef1cdf4484b82dd70279`  
		Last Modified: Tue, 03 Dec 2024 16:17:11 GMT  
		Size: 231.9 MB (231880983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e0b7842efee0560cbb97a8bf463f8ce0017e26ab3fb70853b19dfd42cf19f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16947386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490dc7b944706942ddc307593cfcf31eb6789669a5421161813ca686742e43d3`

```dockerfile
```

-	Layers:
	-	`sha256:adea640ebcb9f657019594233f9ed28bb4fd297667bf3496b4bc59c52d3184df`  
		Last Modified: Tue, 03 Dec 2024 16:17:06 GMT  
		Size: 16.9 MB (16937178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317a52d715af8ed8e9f6aa2c264eaf47458539127bf4f5013692e6e37b8712e3`  
		Last Modified: Tue, 03 Dec 2024 16:17:05 GMT  
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
$ docker pull buildpack-deps@sha256:1df3ba79cb55d883ad913395b36a513bfc917c15b7caf38cd88c8c665777683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349670575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b982bb3ebcb5f081cb00461966a8802023bcb16a8a774a3730540353081667e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f973d95ee4eb4554be6abf2f8a00814eee05529e41a4930c8ffae282529578`  
		Last Modified: Tue, 03 Dec 2024 10:44:48 GMT  
		Size: 206.8 MB (206763028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe39f39f7f1bde3d6c9e5c818bc628469875b2aa3b927edc66c74bf70a22412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16747718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ebe5f6db202526925c56ad1faf6b865d027a0465734a2288e2f1ecc5c74d2b`

```dockerfile
```

-	Layers:
	-	`sha256:3d93d11363e6dc9d7925d0a3b5dbdca207392f40e1f417fe1bace7d8da06f1be`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 16.7 MB (16737543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125fd07fab195f7bfaf54230410ce6eb672c899fbd818dc4533083b58c05c9d2`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json
