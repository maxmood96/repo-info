## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:185346493b6f0af6b94d34895b5ccaa44f6470b844de60c01d086d3b83f43247
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7aac72ce01f516b027b96e18bf55c54e347e56ff5a41020387a9b4508b813246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.6 MB (378615125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c866ce0f3e1bfc2684d4024769d0a6035f0f801d713d9853042809c52c6a1f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 10:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d55a674b2e3641a37b7f2053f00af6fe4f2a89576ffb917d4b7b4deaf24591`  
		Last Modified: Tue, 04 Nov 2025 11:23:13 GMT  
		Size: 235.9 MB (235937246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8478fde9287d2fed823e855b54635279e5a375fa8427c8d3874bc9bd76a49f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c356e9d103ad1c031a6e704ffd56263b921e1ebe3c6f16734326ed1aeeacbca`

```dockerfile
```

-	Layers:
	-	`sha256:82ebb800fb9641267b2fe2ad9a316d991136c8202007e321141b22829087b3f5`  
		Last Modified: Tue, 04 Nov 2025 11:23:19 GMT  
		Size: 17.2 MB (17207191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7deb2c475da2ee6e19959b574b9749644ab984ec92865c9492177d0ef4624664`  
		Last Modified: Tue, 04 Nov 2025 11:23:20 GMT  
		Size: 10.5 KB (10461 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:53aed554c6fb3cc08d7304cf6959c8e226baf9a830be3191b2e58159c8f8e719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342777591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90de7df8cb7c180bdf9d3f810b82f53a13f5dd62d338df7ec813463372be555d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:51:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:13:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e91b819b99c2c8690acb5b01465ae84356bc40a50656db0ab817eb28337198`  
		Last Modified: Tue, 04 Nov 2025 02:51:11 GMT  
		Size: 24.3 MB (24343129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6dc99f3137f9645c516987d6a868e6cc6233f36d0a984e9553daeb02a012e2`  
		Last Modified: Tue, 04 Nov 2025 02:52:04 GMT  
		Size: 65.3 MB (65324780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badeeffdf7a41911058577c2b4e7fc8a5587bc32f50c3dd26f5f734563205194`  
		Last Modified: Tue, 04 Nov 2025 04:14:36 GMT  
		Size: 205.7 MB (205660256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbd06b09e01d92c88651a2e5aa1a1a6465c846f72c790120acf888ede24e2176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16979923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4ebf68c4cc359d94cb42e9010e5427932fdc824e88d21d4417df6efb477d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6489652404518f275ce1f6cb5b12cc76fb90944928ef99ceb0cc8b577d34471a`  
		Last Modified: Tue, 04 Nov 2025 07:04:53 GMT  
		Size: 17.0 MB (16969389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcd8f1628e86fe04a4e6e2bfd995f37cf7ca20e2e9848502e50270317a2c3b7`  
		Last Modified: Tue, 04 Nov 2025 07:04:54 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfeb852678155cb35dd9da1cc4511aba223bd3f8807f16edf34009d28513eac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325294498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302ab6e5332e9b756b63726bd41331975ac3fb2457b93fb168d68edce81c5d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:21:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:caaccdf8fb49cd124dc4c23baaca3be5aad18c1263c8afe3356d15af000e612d`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 45.7 MB (45717135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368971cf52e52bedcc9c34f098c9d72d70d67b7064ef11faefe431b570e27f9`  
		Last Modified: Tue, 04 Nov 2025 00:40:16 GMT  
		Size: 23.6 MB (23617115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5622b4d13fac6a61fac2dedf72d7cec257ecd1acee5ddbdff6f27c4b9ebc7331`  
		Last Modified: Tue, 04 Nov 2025 03:07:13 GMT  
		Size: 62.7 MB (62721595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd22e9d15b197fe010a027cbdf8d71ffdc56397d5f87ff67d8ff72d8df1ef46f`  
		Last Modified: Tue, 04 Nov 2025 04:25:19 GMT  
		Size: 193.2 MB (193238653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:723b413771ba70ea731e51b24054c2b766e4b2311302aabfc5462f1598bedef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16985713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a88c48ad94ef79c20d0b5835f0e685bade23fc055a33e4aaea35a9553b77790`

```dockerfile
```

-	Layers:
	-	`sha256:13382048ee3682b9ea9ff27dff121f72fb29e623f17e01ae82e03436346c65d5`  
		Last Modified: Tue, 04 Nov 2025 11:07:22 GMT  
		Size: 17.0 MB (16975179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009f3cad9d423881a1bcece51820940f332dbe6680c00652f37636149267e3dd`  
		Last Modified: Tue, 04 Nov 2025 11:07:23 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:91bf95456da7242a97029ce78fb0b4781afcb2cd61e38a9bc3d888e9664ef582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368331765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bbf78d0293943a803ebf3bf6249a8cd4a1261b460ae2019be57b8bcd137667`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91656fd58bb5f57cac88ac067f1fad07e73ca96589dd592517520d14bd020eb7`  
		Last Modified: Tue, 04 Nov 2025 04:13:49 GMT  
		Size: 226.1 MB (226079884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1179dafe96a7cc52b973b786e1f0a34d4a0f38dc623258bf041ec30305594b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17302039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1b30c398b881530ae7650ea06926946a58f13648f3e39f637ff933b3186862`

```dockerfile
```

-	Layers:
	-	`sha256:886237e50c89b352e728f7f344aec6a408d7f5006e5330fd9362a5985542e198`  
		Last Modified: Tue, 04 Nov 2025 11:07:18 GMT  
		Size: 17.3 MB (17291485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4537956769eef1e8a451d2485e345eea647bd6276ac5504dc2edc26b72d795d8`  
		Last Modified: Tue, 04 Nov 2025 11:07:19 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9c93ee7ec647bab960121abb7bb55d765f0cda17f12382e80ee1b8fdcaa30b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387417992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c45051f31e310d06b0ef49e0cfb04f76bce0eb3033a230c4d6c0ff00433a156`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac49d94324079b69237b0b1612a8d78112618ce6800066877fb7d7a38ff9e74`  
		Last Modified: Tue, 04 Nov 2025 01:32:28 GMT  
		Size: 26.8 MB (26775967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1318169541c4f79fbdfc20cc98993bc7ba60d45d8f2235f647857ce150c6f7`  
		Last Modified: Tue, 04 Nov 2025 02:20:45 GMT  
		Size: 69.8 MB (69793982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea4463fafb8651430fe727af5441c75c68fe8c663ef49e7ebb80b9cf8a55ef7`  
		Last Modified: Tue, 04 Nov 2025 04:19:17 GMT  
		Size: 240.0 MB (240046805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11637db5b6188acbeff4c3171157c89a6c2763ed6e0692dbceff1d2cfbf3cf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17187219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6017fcd739fcc15b936b1233e3a2cbb613d9bd2c763660655214e5b39020a4e0`

```dockerfile
```

-	Layers:
	-	`sha256:c0d45a31244c21219136fac8848252355ed0dead45d92378b7542d7aeadf6396`  
		Last Modified: Tue, 04 Nov 2025 11:07:19 GMT  
		Size: 17.2 MB (17176784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2ae636bbc6632b1c2ff02a94ee6ce64640b7b33cfcb7d028ff247354c066ce`  
		Last Modified: Tue, 04 Nov 2025 11:07:20 GMT  
		Size: 10.4 KB (10435 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e1a80f7ac976cb33bc1c07e496e7e08b8d85e2b2f1854b8e42fdd2b3ea3acb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384237557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6de05983bc466f58dbe905c4e0d91734aaf9081caea2e56b05cc43508853d2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 16:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:53:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbe8662034d4013b7fae91328f939dfb669ce78f36e4a91a9a0c68675f61828`  
		Last Modified: Tue, 04 Nov 2025 16:03:22 GMT  
		Size: 73.0 MB (73035332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c20ef82941d48d9739dd464559bc277a122b8fd20002e75ffb6f6a2fb6ca09`  
		Last Modified: Wed, 05 Nov 2025 00:18:10 GMT  
		Size: 231.1 MB (231095465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:105787bad623cd4a3a178efddb56a66dc4060c7c802f91a0a35591254735d87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d5d1162d3ddedab26ebf173876cc7349835bb651615d184971f78934bc5530`

```dockerfile
```

-	Layers:
	-	`sha256:5e416b077e61a4035beb388d08aecbb9422f338a09e4481095b3813524b03843`  
		Last Modified: Tue, 04 Nov 2025 23:20:46 GMT  
		Size: 17.2 MB (17192740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8793f8a0ea3f9ed02dde39e0ec03b4c937f39322f3e69a2b92bc358dfaa72a16`  
		Last Modified: Tue, 04 Nov 2025 23:20:47 GMT  
		Size: 10.5 KB (10499 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b280733d8d86f75290d11166eff3e5a63087f655aa0cd5bc8801b4556535bbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.2 MB (462217812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8945de365a60e507b42bdff56d4fd3bd0e3cb00d7cbe0a66ed87fbdedd583abb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 08 Nov 2025 04:11:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0e1c49c4b6326e11479d7f89ce5a78336570bca91aa46a373571186f6ab4c`  
		Last Modified: Wed, 05 Nov 2025 12:04:45 GMT  
		Size: 25.0 MB (24953956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed84703a94ab124c54334c41ec37609f785f60feaff7dd12005c2d2dec188e6`  
		Last Modified: Thu, 06 Nov 2025 07:40:32 GMT  
		Size: 66.7 MB (66660260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194d2ccc4b4327e8aa3d6a9c1b621e83479e3948103ff9270212081f43340039`  
		Last Modified: Sat, 08 Nov 2025 08:23:10 GMT  
		Size: 322.8 MB (322832672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b7228691398973c01a38f166779f22bd1a95b643bf60d3b4cbe5c75d21bc6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a4560a0cf832870f70910bdf752ab2edb894382e6b3bcf605900a3053b797c`

```dockerfile
```

-	Layers:
	-	`sha256:dbed58476c55bae9e27e91f5fb8e055ff685039fdcd02767ec2abfdde8d434d1`  
		Last Modified: Sat, 08 Nov 2025 08:20:49 GMT  
		Size: 17.3 MB (17263329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b23f90e8f378c7722f1efd210ac42c3ed3a849c408045f9932a2ab26c30419`  
		Last Modified: Sat, 08 Nov 2025 08:20:50 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c27b9e9dbdc77cc88f4ba4403efc6eb96fa5e6e95589d534048a3f235f325917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351224724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d320a7419763e92849d6ef4faba7587d92d137feac3908a2fffe99f904c710`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:52:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:30:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205358f383faecf1c434c76ac887bd7a626ec58dd373ab479cce2de6c6d63849`  
		Last Modified: Tue, 04 Nov 2025 10:04:16 GMT  
		Size: 26.8 MB (26783618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e263d619c54c23185f97b8200ca156bd013604c1f55c66784ca7069ae48ff`  
		Last Modified: Tue, 04 Nov 2025 14:53:19 GMT  
		Size: 68.6 MB (68638436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0634d2aa9f89c6fe5db66904261bec1da301aa6c1cde54b9c465265b676459`  
		Last Modified: Tue, 04 Nov 2025 20:25:30 GMT  
		Size: 206.5 MB (206450371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a12d141038d259af9d845cff1166b4047082f4d929cfd1312b617dfd723be95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63765f696c60650f47a92a8409eb264849eb1877b3b7346dd0bdafeb5528ee44`

```dockerfile
```

-	Layers:
	-	`sha256:d351a32d8a35b42df161fb7b652c74e711819eadff7124f990937c3472134f57`  
		Last Modified: Tue, 04 Nov 2025 20:21:51 GMT  
		Size: 17.0 MB (16984424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa67c42579c846162d612a2b59fdb2e7e4e04a2c72f6ab6b848e59ae566ac8f6`  
		Last Modified: Tue, 04 Nov 2025 20:21:52 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json
