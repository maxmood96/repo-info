## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:a3ed2551ceff0f6614c89cba2e0de6bf13c768aa15544e7c764e02d8fd880abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8ef56987777fd5cc83b244bea06f71a52e067d4a3573dd4d9e46426da7e3b794
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366958012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc459e0d4b28f0722a6ad59e7d70cb78c0aa037d87666e9c2ee63e04085fe71e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:31:34 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 27 Sep 2024 04:31:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:13:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678b2c3c62e339c39b9ce218e20e9a22585f2fc41f9f64548989e09691f0854`  
		Last Modified: Fri, 27 Sep 2024 05:17:24 GMT  
		Size: 20.3 MB (20294565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cd5a2233f0950e0047c5ef70615565f18b1eb82b465bd4022186677b3a0e3`  
		Last Modified: Fri, 27 Sep 2024 05:17:40 GMT  
		Size: 66.2 MB (66232209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caec85693b42c7320c4c42dad676e7729de43a3e75de092afc9069f0060a3e5`  
		Last Modified: Fri, 27 Sep 2024 05:18:14 GMT  
		Size: 227.3 MB (227253201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a702af9257ea6649053fdb5c5801607a829b7d01672205b726401c8128e958bc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335462987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322342ca71be45e54db169d641b33b9049fb9f8e9e2db499781674dd529d1c99`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:20:21 GMT
ADD file:3b9d682e7d68f9176882ad1aa7f4dcae0a81c3f93bb197b8d0a3982c411d2ae0 in / 
# Fri, 27 Sep 2024 03:20:22 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:01:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:655ea019a1ac93e4a06df6c69d688fcb77e3e8581a9c73eaec0ab2559d7233f0`  
		Last Modified: Fri, 27 Sep 2024 03:23:36 GMT  
		Size: 50.1 MB (50140675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5a645996979bd86734316a948faaa2699705e7844398497f9933957b686774`  
		Last Modified: Fri, 27 Sep 2024 04:05:36 GMT  
		Size: 19.3 MB (19272320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33a076b656ffa1590cb3af11ac35caa4cafc5418c987ee43ff730ce6667124`  
		Last Modified: Fri, 27 Sep 2024 04:05:55 GMT  
		Size: 63.7 MB (63678959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b391cda3e9681d641f974d78e09b872a28e4dbbc868b58887bc63c79773685ef`  
		Last Modified: Fri, 27 Sep 2024 04:06:30 GMT  
		Size: 202.4 MB (202371033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cf5f7f2b3d1e7e053937847cd1d54aae5660d0b109ec06b1e37407c516026f08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316886587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e66f98eb6616f1e3e4995f88f43cac97b623cdf136f562ae4b5605d03b26d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:15:43 GMT
ADD file:13242b1f67d07c997aa23e4b688f29c3a6c6dd2678f15f8738e88d4e66cd5ad8 in / 
# Fri, 27 Sep 2024 05:15:45 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:37:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2e00dc0285e0f577d99c5fb34081dcf709cc26a9e85129b9e7bf7486f41e9f93`  
		Last Modified: Fri, 27 Sep 2024 05:20:03 GMT  
		Size: 47.6 MB (47633953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39e04951abf97af56dedf87c98cd7cc72052708138c6c90da2eaa7628520ed6`  
		Last Modified: Fri, 27 Sep 2024 07:42:12 GMT  
		Size: 18.6 MB (18628870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d47835426771c44b0620b149b078b002436d04ae0a9cfd024e98d0dfd4660`  
		Last Modified: Fri, 27 Sep 2024 07:42:31 GMT  
		Size: 61.2 MB (61160733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985eaffb50a16b04f512a5978f60707cec0ee2ee400d8df8eed0a4f2ae4e7bb`  
		Last Modified: Fri, 27 Sep 2024 07:43:04 GMT  
		Size: 189.5 MB (189463031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6eb1f5a4d0fbaa0738de62ec4ce5cad85bc0deab8318212832033be1d4e44227
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.8 MB (360841180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5170670a1b59e433d47ac1c2f5b6cbd4cb569be345029c90a37adc178439fa3c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:36 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 27 Sep 2024 04:39:37 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:23:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56925e2753eebe331e1e7850cdb33fa7fabb783a0365763734fb7f7fa68594e0`  
		Last Modified: Fri, 27 Sep 2024 05:27:28 GMT  
		Size: 20.0 MB (20038741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf179f048ad941b2de420899978ae9515fad2b4c8b83bc1eee392b5b7291c03`  
		Last Modified: Fri, 27 Sep 2024 05:27:49 GMT  
		Size: 66.2 MB (66249547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46608e24e871aeb173029569f11931335886e512f79bc654f51a4aa982f67d8`  
		Last Modified: Fri, 27 Sep 2024 05:28:17 GMT  
		Size: 220.9 MB (220936291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2decb729ef9d6a3e32c10577537efc0add6e5f9df995fee2a00a1b3319c51a6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371489677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd72c109ae60fdf2258bd4f815f9c581638526f9fc3d6087eb2a165550b20fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:25:06 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 27 Sep 2024 07:25:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:06:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7697ca3ba43a9b525249b4e05578e38c4d772b5184601fc1ab4ed0d6202612e`  
		Last Modified: Fri, 27 Sep 2024 08:10:48 GMT  
		Size: 21.3 MB (21309695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146c248c1b9df1279d1bc34451bbfaa5ca72d7e3bf28372ac12a9ce2a2af65ad`  
		Last Modified: Fri, 27 Sep 2024 08:11:09 GMT  
		Size: 68.0 MB (68023503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358825efffd1f6da3c20226a36432d1a31ff644b5ead94b4a2cca864377e042f`  
		Last Modified: Fri, 27 Sep 2024 08:11:57 GMT  
		Size: 228.1 MB (228096516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:704b9254b09594d2270a955d0675e6c919c1d8dad1ec492483122e034d75a307
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343787137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7225b32c0c190167eedf5534f1dff2f94160057d2ea72af2ad5fe948cf9130`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:20:06 GMT
ADD file:1d08fc8d7e30f98aa4f42de7aad81e751ab03c9887521ea6bc5e7f7ccdac33a1 in / 
# Wed, 04 Sep 2024 22:20:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:12:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4eb2d8078dccea930e749ede5720f2f057f44ed6d24c4a5fefb751441787ce4`  
		Last Modified: Wed, 04 Sep 2024 22:28:31 GMT  
		Size: 52.2 MB (52218452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de63784d0f56e4996d5d9106fa13fd53636dc15d02107cdba00b53bc662b0af`  
		Last Modified: Wed, 04 Sep 2024 23:19:47 GMT  
		Size: 20.8 MB (20840648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4237e9699f2a42702bbc40ac84636b5bd5b697365781314fa4597f038af203a`  
		Last Modified: Wed, 04 Sep 2024 23:20:37 GMT  
		Size: 65.0 MB (64981816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708770bcaa0a7130dbf5fc08d4f61c4a9e74bd0b9cc8fad9ed65da73a11c090`  
		Last Modified: Wed, 04 Sep 2024 23:22:50 GMT  
		Size: 205.7 MB (205746221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7436b5b7db65cd5a624600a1deeef5c873d96bdad3f435f9fef4b991fa46a014
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377576280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3c82a2612f21cfb3e020d6a1179a1339b2674541a1bdbe7f3aae822f6e52ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:34:36 GMT
ADD file:330305dfad891b7801b7bc1444b22086f483c0101ecad9aa8a8e0d005896f0fd in / 
# Fri, 27 Sep 2024 05:34:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:01:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:03:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1c9d9c0ae5911d02f7f099685f31c9a3bdecfb20000d904113c26e622dbe3be3`  
		Last Modified: Fri, 27 Sep 2024 05:38:22 GMT  
		Size: 57.1 MB (57100357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cae32b1fb8881345e1371c36b7be22b1f7ed12f1c0b8c022946020ef2ea67`  
		Last Modified: Fri, 27 Sep 2024 06:06:52 GMT  
		Size: 22.9 MB (22941201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c552054a471b4255e6efa87c7bc0c63ba0466655c5644bfdade3677310ec65c`  
		Last Modified: Fri, 27 Sep 2024 06:07:11 GMT  
		Size: 71.6 MB (71553163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f28b4807d4b640478c00c941befcc03e7516d529f7038a9e613825c62ecd05`  
		Last Modified: Fri, 27 Sep 2024 06:07:52 GMT  
		Size: 226.0 MB (225981559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d5b8b5e2291d7c8cc065f3f18775309ccd2ba7d9bd1efaa8de0eb044d6793b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342226166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ef9bf1106f34529cc7819079b623b933e37a3488161ce834b76eec5ab53c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:24 GMT
ADD file:62bc4f2057452df8dde276d456f3954e7e27a723040dd9314069695b18b4c75a in / 
# Fri, 27 Sep 2024 02:45:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:17:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d4e554dd357d755b1103e6fac1ca2fe641d4ec4ce0581cc222f4bffe8b54c0c`  
		Last Modified: Fri, 27 Sep 2024 02:48:50 GMT  
		Size: 52.8 MB (52771035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f683d43e465332ea4b3a44a602cd96364371abbd8a8e9766b4a056ad242572`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 21.4 MB (21394423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d90646a4948c3fa2abf48c8eaeef129e9547574cf2370fa04ecaed53f76dfb4`  
		Last Modified: Fri, 27 Sep 2024 03:22:17 GMT  
		Size: 67.3 MB (67256930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f620222e1943a71639f47a8405e2a62c61af833945aaefd53d6e4523b5853a8`  
		Last Modified: Fri, 27 Sep 2024 03:22:45 GMT  
		Size: 200.8 MB (200803778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
