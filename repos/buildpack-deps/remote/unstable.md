## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:9fab4385ed240097edc85c04d18da385ddfc7896d717b079d0563be5f9e20f21
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
$ docker pull buildpack-deps@sha256:c0dd9aa770a0f15fc5f4285d4c9b3e4d6c9fd3f2f1003dd6499cbc823d3c4279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291493609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb455e4bce3c14f4b59e7d2ca3285529fde8fb524f46218e0460ff214370d520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 02:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:21:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:15:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cf40c8870d4fc31c85e1981d6e2ac2787a589f1e553cccffe9aca41df353fd5`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 45.0 MB (44990635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb447e96331843e57f9f8c2921b90731b9e4529a8a58e3def300ae395aa899`  
		Last Modified: Tue, 04 Nov 2025 02:19:17 GMT  
		Size: 24.9 MB (24929773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a2af30582e54ebd41ab69f1a6aa5dd01e372deffa02d94d9a43958a0d3d77`  
		Last Modified: Tue, 04 Nov 2025 03:21:54 GMT  
		Size: 63.4 MB (63360418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bf9c635af3265a50f4b01704a4e39f3af45fd6a665315a801ea453925f19a`  
		Last Modified: Tue, 04 Nov 2025 14:30:38 GMT  
		Size: 158.2 MB (158212783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23ca5df5391b0e5c73fb6b08ef4ed9bcf0331da4309e5541361d20efa277dc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16022327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f05f5c0dcbb3d052e4997034c099293addc4fabbf830d344d9ca9f41f47fca`

```dockerfile
```

-	Layers:
	-	`sha256:37eeb8de390f4e1c834ae4cf4cd706704ef7baa1a9802faa4972be2c181ce953`  
		Last Modified: Tue, 04 Nov 2025 11:23:59 GMT  
		Size: 16.0 MB (16012131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18f3f01a64b7d49713648dd17f34b7df19215755b1a82f0f0db316fbfe516fe`  
		Last Modified: Tue, 04 Nov 2025 11:24:00 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f5cc923e324587f30d37a74e9164074774f26fd36144122878c0ed5365283379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332362715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deecf73d4c551ebb41eea82fb42b344eef20984cb19330c9806596ad55591eb8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee2464e4f33b113343bb1ab557ca8f41d3b10032adfee93dfe6afa6fc0c4b0`  
		Last Modified: Tue, 04 Nov 2025 01:30:07 GMT  
		Size: 26.5 MB (26462272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaec26cc42fbd50193073025d81257d88d937883055aad460dae174f544107e`  
		Last Modified: Tue, 04 Nov 2025 02:21:08 GMT  
		Size: 68.1 MB (68112770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab38f637a03b54502352976fec6cd773ed316db9cccb36cd0b5e4ed670558b`  
		Last Modified: Tue, 04 Nov 2025 13:52:51 GMT  
		Size: 189.2 MB (189201655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:438d43875b8c5da664b01e99514e7cf3a37e7d77800cf0c6145ff08b2ab85202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16339945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e029ad1c03ecf08ee2f4b1fb58efa2b2d9caa27d4ca2a826ac4588eb495babf4`

```dockerfile
```

-	Layers:
	-	`sha256:9c66cbd09fd6a41aee2957211766c4d4524794f967103ad25d3187b6485d5502`  
		Last Modified: Tue, 04 Nov 2025 11:24:13 GMT  
		Size: 16.3 MB (16329732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad243c1c86d9fe4689ae7da9e29fdd9e6e66c1a71479d42dd774b56a065cfa77`  
		Last Modified: Tue, 04 Nov 2025 11:24:14 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:30338d67480456afae4ffbfb8128c5d1b73fc7796e916d5af18ba276ad7000c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351105760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1738ad218550576aa47911bedce7173d62284048fd182b121fcb536deb1a7966`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:31:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e227b380623fcba2d9150034228fcc8257fa11236e7ccca0e2f9cad3a24c603a`  
		Last Modified: Tue, 04 Nov 2025 01:32:02 GMT  
		Size: 28.4 MB (28436262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02a601986dfbe157c15ec69c5f585f418cc3b60d6c2afde0f0222a7f25d5930`  
		Last Modified: Tue, 04 Nov 2025 02:20:39 GMT  
		Size: 70.4 MB (70357090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abd1257eda02fe96b5b7333fb0318918b52d072e868052badf432bd609c8833`  
		Last Modified: Tue, 04 Nov 2025 14:30:35 GMT  
		Size: 202.5 MB (202503401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9fc478b5ab1543cdf4900a593bccf9087050b91f0b7428aa3b850860c3160ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16235073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf8332498ab881f4bcf3ae29d6200e95fd64d15b15359b765814dfd4f2025a0`

```dockerfile
```

-	Layers:
	-	`sha256:8d1905da73f962530f7c3158381b951def97c44ed2cc0bd31004a11551213237`  
		Last Modified: Tue, 04 Nov 2025 11:24:26 GMT  
		Size: 16.2 MB (16224962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cf396e7ae3ca134035fed99af022c075b5328f613b6e830933839e552ed84a`  
		Last Modified: Tue, 04 Nov 2025 11:24:27 GMT  
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
