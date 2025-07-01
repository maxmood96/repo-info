## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:3c4562a0ef0c7638b647d69c352245e1b1feb5204eb7cc7bba8961da504a7cdf
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
$ docker pull buildpack-deps@sha256:8074649c4935e01259d77bcb1dcc8bc65da73ff11d307067d21af430db474346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378435673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ce65e154041891317e9d99943c17dc603d89ee25ff80d9db6224dcf8632ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76da92f9efb17dc4a68c682bacce1ec791a87b62ee76639b08bfc2ee4577cd`  
		Last Modified: Tue, 01 Jul 2025 12:07:57 GMT  
		Size: 235.8 MB (235764377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a39640015c454c546fec1a397450e6bc031c2bb34b79bbd325171c64c7b5a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17210900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a973170ab9ee6839f1915b08583f99e7f3f71bef9da59e7c0fc986d2387b4c59`

```dockerfile
```

-	Layers:
	-	`sha256:c632c01331e3e21745fda0d2229b814f8314d9d7441143b3ec1b004ff56f866f`  
		Last Modified: Tue, 01 Jul 2025 07:21:26 GMT  
		Size: 17.2 MB (17200707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a619b6ae879ce638b67ba4c5b71ac52111eb22cafc2a321d018153447ecd7e6`  
		Last Modified: Tue, 01 Jul 2025 07:21:27 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f4af360465d19d2861541b4d7dc96f734de71462b4f8eda9102b313c0747e13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344952178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87e61403cddde328410421dd1b39b4f56423556703ca2d42b2572a3a20ed70a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be3896271877b3e95aedbf07f86334bdb2f5374ed0d8dca30695208865ab49`  
		Last Modified: Wed, 11 Jun 2025 03:14:18 GMT  
		Size: 24.3 MB (24326796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1d6b386d300f718bd8ac1ab335ab4f9b2054343e637522505e1fa47faa99`  
		Last Modified: Wed, 11 Jun 2025 06:36:03 GMT  
		Size: 65.4 MB (65357608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74622eead94566d00be7710330525d355332f11631c2a1233d74002f0be1ca`  
		Last Modified: Fri, 13 Jun 2025 23:04:43 GMT  
		Size: 207.8 MB (207822364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34e1f91fa4df12281dfbf3407b7c192ca6c3934653de80cf1921e5aca005d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16978358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2580842030bc2a4eaef0f5fe7be35a81f10d9c4a293994b5231c4d5ac990db`

```dockerfile
```

-	Layers:
	-	`sha256:5847b7b03a6cb73cfd14b43aaff14b5a7b27291af9abd847e15a23a2615f4924`  
		Last Modified: Wed, 11 Jun 2025 13:21:07 GMT  
		Size: 17.0 MB (16968105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8efea4cd1eedd95d4e83b9ca2fca1cb27846d2e3fd58557160a2d2dd71c2dc3`  
		Last Modified: Wed, 11 Jun 2025 13:21:08 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a9c2b86f26adac7406844a8ac104f6e3da4ce945af76dabd4136b1cec543d9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327403081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c3ffdd95e6d945685ebda1efbd8c549997fbc0925b59149304c80a5d45e43f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6c3b2ac1d8de7f6b9efb67d4f8df7036728aec7a9268a04eebbdddea82d555f`  
		Last Modified: Wed, 11 Jun 2025 00:29:31 GMT  
		Size: 45.7 MB (45702045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b97e79d9850f63633fd52187a6c3a6855596f84e391aa2167c27363cd92c43`  
		Last Modified: Wed, 11 Jun 2025 12:02:56 GMT  
		Size: 23.6 MB (23599533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0250cd76d089e47a026dd511a8391d815ac5e1cd3ef860f0d3c434d13a9d0`  
		Last Modified: Fri, 13 Jun 2025 23:07:15 GMT  
		Size: 62.8 MB (62772074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090ec91afa7c03aa4f5988d585d6cc13a6481182a187f5a17c072fa8fb25510e`  
		Last Modified: Fri, 13 Jun 2025 23:05:13 GMT  
		Size: 195.3 MB (195329429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:639c3e232ce9358fcd67dca25499dd2709db5e561d43cf5a7f642e480f07ba0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dd1bb28d8d4c961b3e6b48e905765ca5feb0f8a514fe9013907cb14015be27`

```dockerfile
```

-	Layers:
	-	`sha256:c7d21463138ff67e22f47848122ef2ff6cdf0f707b20178c1fe7a80716469b92`  
		Last Modified: Wed, 11 Jun 2025 19:21:17 GMT  
		Size: 17.0 MB (16964642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17de593ca8ab5611844763d320a703450f39f3ae7269f810bee910c72a9459b0`  
		Last Modified: Wed, 11 Jun 2025 19:21:18 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8644b40da73dde92846d13e37b295251a450ca8c09ccc4a18b461b937ea1dd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370893130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0f54c46f0ee3bbad0f18f65fa72362399f948b7c2f34bb0912cf6afb978fb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439ee882f07f6b24af6e46850d9521759d30430f3be41cdca454de5566ec0ab`  
		Last Modified: Wed, 11 Jun 2025 02:57:26 GMT  
		Size: 25.0 MB (24994209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded0afb06efd2b7ed68e17cae5e6e1baaad41593041fa16eb9d856160e2bca6d`  
		Last Modified: Wed, 11 Jun 2025 10:34:07 GMT  
		Size: 67.6 MB (67636505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a837c416f8b0f1f2b6dc4747709aad655837561f5177de39124426c523fdd0d`  
		Last Modified: Thu, 12 Jun 2025 04:52:10 GMT  
		Size: 228.6 MB (228640888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84864e8b6e6383305a1fa5661eea93d50c2169e5d5d46b06a91e4c7a6b1431c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17291215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb1b2777f1bd4c23db3cba05a014d7df0de2bd709cd67d31a39737aa9682be3`

```dockerfile
```

-	Layers:
	-	`sha256:21a15ee6142af2ca8e9db5717cf715f334d0a25011f27b3fa455551ba0dc32a2`  
		Last Modified: Wed, 11 Jun 2025 16:21:09 GMT  
		Size: 17.3 MB (17280944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0d01cf4e81e1a42611a342822f79fad2cacb78eaca445541d598968289f25d`  
		Last Modified: Wed, 11 Jun 2025 16:21:10 GMT  
		Size: 10.3 KB (10271 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fa340208f4deeb14ee13405126e15633c9d1ffe46ead55a43399ef60f01c209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387249638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0729e310aa145c6bf0ef0f202db76ec71ed304ce0e7f0361cc8d7e6b775c78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f64900f9b3ef26b18f567a74a96e250e42a8eed2ff1fadd54a41cc0359ad74`  
		Last Modified: Tue, 01 Jul 2025 04:13:45 GMT  
		Size: 239.9 MB (239860428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:abf0fb8e681eb21710e50c8450ceee317f74e14dedaf33fee4e669ee33b11d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17180474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2caba0bd824b4842c45cba9a72e2c1705bbbe0f5154f8940a3d8fedb45c5abb`

```dockerfile
```

-	Layers:
	-	`sha256:534765ed04677f226ac89212de87e906cdbc674a5339a3ab2d41d9b0f984aa3c`  
		Last Modified: Tue, 01 Jul 2025 07:22:18 GMT  
		Size: 17.2 MB (17170303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f0f36bc6abd52ff703a8e29c126c80d57b566da0cb0f56ece0728171a90c163`  
		Last Modified: Tue, 01 Jul 2025 07:22:19 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4cc850f22ab6c599561ee8298c5a16796a1bb7a2a2fff07c486b3fecea43167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.8 MB (386797076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ce45ea21e6e6c9c0f3c92eebad0ee08473a7903b7215ed780a74aff59b566d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d7ca19325e1e81102ab8668168b260e6e57b98b333eee8bca0ca1d7fb15d`  
		Last Modified: Wed, 11 Jun 2025 17:42:50 GMT  
		Size: 27.0 MB (26982398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1399fac31c7028d2f04582eb0c8d6877de851a1d1a0a7124a505b94c5460abb`  
		Last Modified: Wed, 11 Jun 2025 19:17:13 GMT  
		Size: 73.0 MB (73019498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4273f7599856b3df4ec8f166defbf5beb0f714c717223f16b5067cff4eaa3d`  
		Last Modified: Thu, 12 Jun 2025 12:14:49 GMT  
		Size: 233.7 MB (233704247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:618d0b3ee842246440604eafbd8079998f7eb24000b4e8a01ec9db69f43a134a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17201677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027d2e1c74514b9bd5ad51db3df7a223d958b6249f51bb893ff4da5d092b55b1`

```dockerfile
```

-	Layers:
	-	`sha256:e03812d32469f710aedd956e3243c253bbd080548106c98746a70ebae0fb42f7`  
		Last Modified: Wed, 11 Jun 2025 22:21:30 GMT  
		Size: 17.2 MB (17191452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3705aa0bfef3874901dde674d102952f2792a4640eb942487fc1cbfa98dbcca2`  
		Last Modified: Wed, 11 Jun 2025 22:21:31 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ef50831367070cc5995506890721e188ac6bb3aa723a1bae436cc16e4a35d715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.1 MB (462076216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9371f2b4ce8657c9c5f7dd0ae7ee9f9f896c0d5d0269e1f8aabea15bf7a578af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5ba72abe20b30be07f6ab1e6cdb1c6d040c269e383e9066cef6f8229dea893`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 25.0 MB (24952958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4236a35a94e37c928bea093f065f7444cfd390eed1e2bcb50207c2c1b8a97`  
		Last Modified: Tue, 01 Jul 2025 04:21:37 GMT  
		Size: 66.7 MB (66669095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca232e16bc60a0f2b03360eef0092d93818f6c4a4b479fc91bb7d82b525c5a90`  
		Last Modified: Tue, 01 Jul 2025 04:50:43 GMT  
		Size: 322.7 MB (322704005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5a016fe2ae7c666ef158b7dce0b8b24c25db8b7a27da73a78fd0514eace03aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17267068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba81616d52b4b6e9412a54fe28e29630518cbc8edefd599d383ffceae8bb573c`

```dockerfile
```

-	Layers:
	-	`sha256:c94a6683ad51b3f31dfacc9b609aad2c7231d162502939f60f0c024cdfd94f54`  
		Last Modified: Tue, 01 Jul 2025 07:22:42 GMT  
		Size: 17.3 MB (17256843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856390e1ada400c1b41f9ad3a2dd25e3f110baf8429ea231a9786bcd9b36e0c1`  
		Last Modified: Tue, 01 Jul 2025 07:22:43 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0dbd5bd7313f4642e891a325aa2ad4f862fde61b0ad4ec4d5b0124807444b649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353789135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e62ad448c65795fc3099e97745e899cef93e2cc3eda85c9fa38e768880092a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588affbec95a011eae8d19fbc59b872f3d6089f972f16713469d6820e2e3fe6f`  
		Last Modified: Wed, 11 Jun 2025 12:02:59 GMT  
		Size: 26.8 MB (26767425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a368896f3f74324a185b32673baa96c49954c4d84388e3238beb96d3b4ffc0`  
		Last Modified: Wed, 11 Jun 2025 07:22:09 GMT  
		Size: 68.7 MB (68683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966b58a8e55ae7cee4c795b40b399b9264e90d10fe8ae288a58a3ca9311f3d3e`  
		Last Modified: Fri, 13 Jun 2025 23:04:18 GMT  
		Size: 209.0 MB (209008054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08091d48e7f9a8ed1334c596a126b436eddc0dbfdeaaaf8d2cb9d03be9f797e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f68b92be4223342324cd1bbb3353c560c8bf099c7a22989405bd11ffedb1e3`

```dockerfile
```

-	Layers:
	-	`sha256:a37d328f38ace0ebcd1a134bbe99bc0070327d99afab147d531f1e40f3434126`  
		Last Modified: Wed, 11 Jun 2025 13:22:07 GMT  
		Size: 17.0 MB (16983148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90969ed29f03c29fd5f072757ff76fa176dea552242d90ae48d8227e57e2a6f8`  
		Last Modified: Wed, 11 Jun 2025 13:22:08 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json
