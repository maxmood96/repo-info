## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:8c333611985c07a6ee33aa148d255215d598a095ce9741f2c2126c6fc3bb4d37
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

### `buildpack-deps:testing` - unknown; unknown

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
		Last Modified: Wed, 11 Jun 2025 09:12:48 GMT  
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
$ docker pull buildpack-deps@sha256:d907a350ef530da3aee7e71a78ea951dc0d2d7694326873b21f689a9afad015f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327679640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525d0c55c2f653323c15fa2ff8a7d28959f936d1e35e2975b48848ab2d6bda37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d82ad715078dca1bd38ac71d3c9c872661d1bdfae377c84300033db7bf3581fc`  
		Last Modified: Wed, 04 Jun 2025 00:32:15 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80b8be2756aeb2756ee1709c45d1af8640bfca2b89a56244b22bcddaa053da`  
		Last Modified: Thu, 22 May 2025 02:30:07 GMT  
		Size: 23.6 MB (23592590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef402b2ae65b191fb52b33f040b2eef1a8184aee8984cf58e6acc607be371f5`  
		Last Modified: Thu, 22 May 2025 12:14:20 GMT  
		Size: 62.8 MB (62762367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adda2800182c96fd176f8381b15d079bcdaf5e9a84d6204beac83ca2dd0cefb`  
		Last Modified: Thu, 22 May 2025 15:38:55 GMT  
		Size: 195.6 MB (195633865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e5c9f3f2d8838760ddab5dad283617a6b9fe50dfe70105beb0f644b28fcfe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16693633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5914aeaa8a63b41cb13d08d872d1df18eb5b641b90b9c775c0842ef15cc8c3`

```dockerfile
```

-	Layers:
	-	`sha256:1442eead63486739a5336a514fa23a1c99a492831fb0cad5c9846d3d631d247b`  
		Last Modified: Wed, 11 Jun 2025 04:21:44 GMT  
		Size: 16.7 MB (16683381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9f9485bba875bbabd96bb2c574b8e53dc349e1d1cf364e59a2530b8284d762`  
		Last Modified: Wed, 11 Jun 2025 04:21:46 GMT  
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
		Last Modified: Wed, 11 Jun 2025 15:12:18 GMT  
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

### `buildpack-deps:testing` - unknown; unknown

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

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4b2c31781fafd03d143d3ce81d7e6ce9e07b1134976576c273dbb1c06cab5965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387773878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5943672a2fe6a41feaecd74d403a98b49e532937537770ab38b65fa4859870`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e139263efe3c22e2cdab37e8ebc2c1a1759b3b3d0c9c98b6becc0fbbd0bcf2`  
		Last Modified: Thu, 22 May 2025 07:33:02 GMT  
		Size: 27.0 MB (26965977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb27d293c54626589e1325f716f65d323eba25d860b81956ce153386de17da`  
		Last Modified: Thu, 22 May 2025 12:42:41 GMT  
		Size: 73.0 MB (73044873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033924ce71e93f81cd7a60780fefc172c860b3752db498772cbca982401260ce`  
		Last Modified: Thu, 22 May 2025 16:59:10 GMT  
		Size: 234.7 MB (234682484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:121d30f4d0d04995ec95900e136935ca27e923f175879d5ba643e230d41e90f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16917521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f9f8e0995fd495cea954982bddd954498cc999b055092c4cbafe5b1a17bba`

```dockerfile
```

-	Layers:
	-	`sha256:ada0ad41019710106555c66a9be4a640d56f2e2acc2f05178a5abfbb4cd220bf`  
		Last Modified: Wed, 11 Jun 2025 04:22:26 GMT  
		Size: 16.9 MB (16907296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7a6bcc752e90092cb345242ceb9e8e373f5e1ed434c87cb57380a196d8bb46`  
		Last Modified: Wed, 11 Jun 2025 04:22:27 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5bb1f38dd7b4d64e2c9ce9aeac18778844becb3b1a7bb9fc6dff140726721db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.8 MB (461833378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2084ffa170b8c81ee7c47fd3461c0addd0a3d3010b99133cb089eccf7c2b4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eab19773c2912f0a6e7295e8a9ea585980b042ba4f201575fb17ac1763bdae3`  
		Last Modified: Thu, 22 May 2025 01:15:24 GMT  
		Size: 66.6 MB (66603294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857a1e0506f3ca9e098be90caf298ae2d2ea36a8b9f35e1141fb56d896c463df`  
		Last Modified: Thu, 22 May 2025 02:50:56 GMT  
		Size: 322.6 MB (322581079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1b2783ecb9f768a5f0b93f1ae85625b8def39357b83f988a8c63f93cec91906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16981765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce9ca0e4a5440562f509fcc65533ff809455b225000b180223ddfdb3b6cdf68`

```dockerfile
```

-	Layers:
	-	`sha256:52cf4bf183ab1a86f3573562f833d80e6e4c63864ec0170c5f63596bfde34adf`  
		Last Modified: Wed, 11 Jun 2025 04:22:40 GMT  
		Size: 17.0 MB (16971541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4362dd8ef686114ddc1bb8934e492e76e4ed0c42c774ee6be458005a2ee32558`  
		Last Modified: Wed, 11 Jun 2025 04:22:41 GMT  
		Size: 10.2 KB (10224 bytes)  
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
		Last Modified: Wed, 11 Jun 2025 11:02:46 GMT  
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
