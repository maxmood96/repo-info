## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:45a6997470126fae009eaa4a3b4c46bece6cdfa909f2fbd05980e3ef73d2b17f
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
$ docker pull buildpack-deps@sha256:a0f6698ee6b90404c2e58e87f5800c09d54a9efeecd87cdb77b70032d5bd2496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380886976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019fb6d41c7ac6debd0f32c84608a2bffc0d7908be1b36ecf75790bf9a93688d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f807a61ec306a45196094c9a44cffbe9d5d5a283a87c6e5c2469748ac3a19da`  
		Last Modified: Wed, 11 Jun 2025 00:01:30 GMT  
		Size: 25.6 MB (25601492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f581532859d9e82510a6be0d293f24d77d5efa5a66349c1e74f899cb0e711`  
		Last Modified: Wed, 11 Jun 2025 01:13:24 GMT  
		Size: 67.7 MB (67659870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd66670249f2067f0f871905f91060c13a96842d48099d1719754e277d3b165`  
		Last Modified: Wed, 11 Jun 2025 06:32:03 GMT  
		Size: 238.4 MB (238371755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17e4392ab6cf0e2f30e837bc432772d070ad5471ed7ad8d203ce346c75bf2dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17206855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae8ba93529e71888f88a94f8aadb01224746094ec1abd8f74f5a228ff86f871`

```dockerfile
```

-	Layers:
	-	`sha256:5d9d3a8e96b1a19d7f87bf97ef732f870c2e39bedc8249c6f52fff6ae2357fbe`  
		Last Modified: Wed, 11 Jun 2025 04:21:13 GMT  
		Size: 17.2 MB (17196662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4950961b883f1ae82f21c00e9051d5b013e4f98851afd05260ca6a107d58591d`  
		Last Modified: Wed, 11 Jun 2025 04:21:14 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

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
		Last Modified: Wed, 11 Jun 2025 09:12:48 GMT  
		Size: 207.8 MB (207822364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; arm variant v7

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
		Last Modified: Wed, 11 Jun 2025 13:14:01 GMT  
		Size: 62.8 MB (62772074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090ec91afa7c03aa4f5988d585d6cc13a6481182a187f5a17c072fa8fb25510e`  
		Last Modified: Wed, 11 Jun 2025 18:19:05 GMT  
		Size: 195.3 MB (195329429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; arm64 variant v8

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:73a99fd8f3eefe0dd1ba36ce0db2cf4dd2377dc168d25b35a0400dbc6d923591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389710442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe0103500f1f1a0aa2c4b1e8f9d2413f8e6a5ff3a23eca5eff2b1b22aaa8dbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f24aa3f80422a60637035cbe1e280f72c031e00f6d803abf75d114fc69f38e79`  
		Last Modified: Tue, 10 Jun 2025 23:26:07 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60bf3250137ff5f937387763b677cbdfc73f6e6d8cb191bcb236dadd350bc3`  
		Last Modified: Tue, 10 Jun 2025 23:59:18 GMT  
		Size: 26.8 MB (26755336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a68b17b2aedc3eec75668b4c1f6433dc6f26215d13bf5c707dfb14bb20bfb5`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 69.7 MB (69673683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b73e4b224eac685de5be2c0fdd233b5fc67d4517e97fdc316b550af5b58ca84`  
		Last Modified: Wed, 11 Jun 2025 02:13:16 GMT  
		Size: 242.5 MB (242515811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c6c3e10e7440eb430c1d06805e6f4e4894c06364fd70666b5f49e61dd8d22f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17176434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4bf0d1cb62b227a127b3c4556b711b784a7b81626b9b08dea553899be482e3`

```dockerfile
```

-	Layers:
	-	`sha256:89fb092ef3b400dcadedeb2bc730c425f7cbe0de7071d1dc3f47b2e656389382`  
		Last Modified: Wed, 11 Jun 2025 04:22:13 GMT  
		Size: 17.2 MB (17166263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6dc0008adbbb49b9f067d8fb83097bf0c861d036eaf0b023a657386f6eb72c`  
		Last Modified: Wed, 11 Jun 2025 04:22:14 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

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
		Last Modified: Wed, 11 Jun 2025 20:56:31 GMT  
		Size: 233.7 MB (233704247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:26eb35f4ffe41b11b078cf2582765bb53f419569a1fd9728757d31152da3af8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464710551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8418319ffafb8fc50f39fb63286925e3a9f9b5e811ddc067651408267888ee81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f4f32e32d9aba20b46d2290a43e58210fbeadb10dd55306d3440511ee2020`  
		Last Modified: Tue, 10 Jun 2025 23:38:17 GMT  
		Size: 24.9 MB (24937037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231678d8f7c532f9f566704f742fa3592bcf30ef8ae6eb20175bf220b23e5902`  
		Last Modified: Wed, 11 Jun 2025 12:05:36 GMT  
		Size: 66.7 MB (66681786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134587a8087d9461a7f21b2f0b2ff74933481796558a0ab742930ee2a1ee9707`  
		Last Modified: Wed, 11 Jun 2025 17:42:39 GMT  
		Size: 325.3 MB (325348383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12ba071e7fc7595fa205e5b0e807098245096b5bf55148a85ac259f05cbb5795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17263012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28048fb982956c6fb485c7574e77b71400a49a875aa0c5270a4b5836683504c6`

```dockerfile
```

-	Layers:
	-	`sha256:dc8570097642a7f696048df3929eead7eac9c78ce434f5cf2b43815d35556bfa`  
		Last Modified: Wed, 11 Jun 2025 19:21:59 GMT  
		Size: 17.3 MB (17252788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f13119224b165c3c6e77c0e967375489c62f8b511b91b4bee01fb47266082e`  
		Last Modified: Wed, 11 Jun 2025 19:22:00 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

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
		Last Modified: Wed, 11 Jun 2025 11:02:46 GMT  
		Size: 209.0 MB (209008054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

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
