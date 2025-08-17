## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:cd76b20e6443785710b69d42799b4e34a1846ad589debb79b0228e56353ad27e
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5b7020a981251576aa0ec7ce404a76178d2d5ab2d19993ce7b85a11576eef647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342336083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f45704a6b30e9c2581a4e2b79b8cd0e5d486b0702264ae296a9fc178582614`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91617643e569834fa54ae3c641bfe51cb7c336b5d4c84459fe06ad34797a9b56`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 49.3 MB (49311006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6147febc7eaaf987437ba1cec086fc417009e9ea749cf4a8e05425f6ae2ecd`  
		Last Modified: Tue, 12 Aug 2025 21:22:06 GMT  
		Size: 25.7 MB (25671763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5764333da2b14e2853ea365c029697a9b2d16d890203808413dd3e27a98c7bc`  
		Last Modified: Tue, 12 Aug 2025 22:15:01 GMT  
		Size: 68.2 MB (68158073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17015ce8d4b00eacf09bec5710a8f9a19c7cb4f15fb6713cc24e7b900d9306b9`  
		Last Modified: Wed, 13 Aug 2025 06:43:57 GMT  
		Size: 199.2 MB (199195241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e60f8e26414a61ad656bfa5255720c0ca0253931a45c2e121a08da8bf18e7aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16356171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a1db507be919b8a2a48607f082bb1957bead6e118e28e4b21eb6047f930bdd`

```dockerfile
```

-	Layers:
	-	`sha256:7a181dd2a9e87e645af01857a0c7d142f599a13ad27ad06cd9a4a1efdbd0996b`  
		Last Modified: Wed, 13 Aug 2025 01:22:08 GMT  
		Size: 16.3 MB (16345995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec461a4cf607321525876f1b5092d07f87b89cc4081aa63daa9faf757b76384d`  
		Last Modified: Wed, 13 Aug 2025 01:22:09 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4f62918ab73e4d15dea13df32d6375731da08ab5ec90d36c4203331fa44ca8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308455423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0d8dcfe78f348f80aa85c9e95509b714729e3dcfd17290d5fccda6d8f93dd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5748e2c98ab94a513cbe6704d8aa158304698c52babb6c14538afdc0d2da4d79`  
		Last Modified: Tue, 12 Aug 2025 20:46:52 GMT  
		Size: 47.5 MB (47481153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8674f20f211a0a5df7e43fa4413500efffe4f69e9a5f53119c86c35ab3bfc85a`  
		Last Modified: Wed, 13 Aug 2025 00:00:46 GMT  
		Size: 24.4 MB (24409281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd16b6b97e2e3cd2021a0bcd7f18a25ab7c75e9e2a4a58e680359594cf2f951`  
		Last Modified: Wed, 13 Aug 2025 06:09:26 GMT  
		Size: 65.8 MB (65774363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2b96c8da52e51ce253d683b76da67a9643ffbd6af0765c46fff6b1b33ca900`  
		Last Modified: Sun, 17 Aug 2025 07:12:41 GMT  
		Size: 170.8 MB (170790626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd5aa18bb352fa1e97e258e76685f8412c85d4816b8435c8af7e1274f20b1158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16119019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da74dbe70df0ecc9774cbe312dc3ff10ce58b539f2c24edb278e270f482e23c6`

```dockerfile
```

-	Layers:
	-	`sha256:3b2d111e936568315948b7ab3efd9ee1e1d6ebf716868986f30168f2b99919bb`  
		Last Modified: Wed, 13 Aug 2025 13:21:24 GMT  
		Size: 16.1 MB (16108783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de86717558c76147d95b932c6a3b75bfdafb87880c12e55991253526193872a`  
		Last Modified: Wed, 13 Aug 2025 13:21:25 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c272bd18f9ee1853793ed416d870e4f9624d15340d8c3d95ca574b87413e1516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291090781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a765e8860797113b4d25ad5e096841bbd86a15423e5fbd10d8dc958d908139`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51c05ed00e703a3cf5143ee59e5e4f274a1b80aa10078d7b24eafce226544dde`  
		Last Modified: Tue, 12 Aug 2025 20:49:45 GMT  
		Size: 45.7 MB (45743292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f4c6e871209c22d9147d58afa57aceed37d2c4246961ef6f33220a727e664c`  
		Last Modified: Wed, 13 Aug 2025 00:16:33 GMT  
		Size: 23.7 MB (23682193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31604b828c3328f78e4b41c62e665eed8e937b5c601513032185e28df4cf0ac8`  
		Last Modified: Wed, 13 Aug 2025 06:49:23 GMT  
		Size: 63.2 MB (63181867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d9c6fd6c479f267391c136ac238b7d7985506c7f0a1d15cba47467324e963f`  
		Last Modified: Sun, 17 Aug 2025 07:12:47 GMT  
		Size: 158.5 MB (158483429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06efb2868c10f3b8e8edd3fd019240aa428c4e8f24cb7c3c3f48c70fafe4bde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abbec2731d3dada47c8a46211f98fd589af05290bd07353444dc6477066e610`

```dockerfile
```

-	Layers:
	-	`sha256:636211d5bab89725bc8f416a92fae6bff1a0e54b6c7e09348c1171642d614eb6`  
		Last Modified: Wed, 13 Aug 2025 13:21:38 GMT  
		Size: 16.1 MB (16114353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aeaccda3506961e64989b01bd645c53632ca4a1e31f15e189ce323796e53122`  
		Last Modified: Wed, 13 Aug 2025 13:21:39 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c01951934fc51177608b6435ff404fd250332a6bd0cbc0c1fee788a086b1b5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333482401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a9bfa2aa4cbc4bc83985af68fb0de2b83c28884c66e29d4a6d6b62e46bc4da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:406c75c505cd140952825ea55560dd596c3ac81bd28e8acd75409de77c63efed`  
		Last Modified: Tue, 12 Aug 2025 22:10:46 GMT  
		Size: 49.7 MB (49665758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42948f27bd259c3af4df8bb9642f9b13a961850fc18b0d0d704e4d8bd4184ce`  
		Last Modified: Wed, 13 Aug 2025 06:44:51 GMT  
		Size: 25.1 MB (25094159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37825ed6d653aa51fd40eb5d018e0ac28bfaaa55f25ee15e26fde25f0d23f94a`  
		Last Modified: Wed, 13 Aug 2025 21:41:14 GMT  
		Size: 68.0 MB (68000551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a81fbd2091b168563e51f3a300085f5ddff8303c6afd9edf82132fbe86bdb9`  
		Last Modified: Thu, 14 Aug 2025 14:01:56 GMT  
		Size: 190.7 MB (190721933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ed7ac3a768b60d547972ceffb143d16c8035505a1970cdd1980b1c93f289a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16440389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f5ca442e0634ac0c3f6684ff2718adf8d9ecfd9d3ca7ed1107d34964aaf85a`

```dockerfile
```

-	Layers:
	-	`sha256:ff1d625bb483e1ef807fbb0feee843e68e6839650949a434b1f17f3625263373`  
		Last Modified: Wed, 13 Aug 2025 22:21:39 GMT  
		Size: 16.4 MB (16430133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89bb99899f935868e023021ff69dfe828841dedaced3b688d38f4f83eaa1b7c0`  
		Last Modified: Wed, 13 Aug 2025 22:21:40 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:df0c562db20dbfe9325e3d0809a9602817fd8af66cc54e2e73faedd37e154078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350968781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4567b8cdd921d8ec184afd69927393649d54c9b37004a8eb9d3de7cb07b85025`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b72ff759cae89a47c9827cbc3981a075f421742ace3eaf0d3c40f8d242d2eda8`  
		Last Modified: Tue, 12 Aug 2025 20:45:13 GMT  
		Size: 50.8 MB (50819082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bb2ee090cfdfaa39c0d6ccc1bcda36a80f4080c6cc16e7b75c64cf990c8bf`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26837373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaaaf9e7098421af8e154d4b4462b5597c12f7d1e78455cd1a1c8a16f9966d1`  
		Last Modified: Tue, 12 Aug 2025 22:15:00 GMT  
		Size: 70.2 MB (70237796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce214af80c4c501923656d98ab821ab871581d5a51bad5c17676a6092ded50`  
		Last Modified: Sun, 17 Aug 2025 07:13:00 GMT  
		Size: 203.1 MB (203074530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0257263724ed21fbc451a9fc2347154213f01a10a84013f96768c0896a61ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16325941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a4f78e10d73740a4281a968baa9c2f476e5f957ddeeb90a6d587a2314de006`

```dockerfile
```

-	Layers:
	-	`sha256:96b84a8049841659a7c5c2f86801eaa076a2da236eeae1ccb31f9622b0044ad5`  
		Last Modified: Wed, 13 Aug 2025 01:23:03 GMT  
		Size: 16.3 MB (16315788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e5c7c632e52a268580c6ae6323e90b5cf375d8a5643fce0dc79fd5fe0daab6`  
		Last Modified: Wed, 13 Aug 2025 01:23:04 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e92d080516a7d74264b70445193b1e2993f2c4fdbb4b60110596127703d5f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323214493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d476c8a0d61b38e10c8095c84ef27fd9b1c467bd60690128f71f3f158028dfd2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86fe6006038239df0ed2d48c27073d2bc03b5547e42ef3e28ba6ae24c42e7f`  
		Last Modified: Wed, 13 Aug 2025 19:22:34 GMT  
		Size: 67.2 MB (67186448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5200e8b4afc50ea558b5c358e93dd23057fa272ab1fa20e18ab8d8b3af91b104`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 177.9 MB (177930237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bf7543ed2f2be5ee2e9a2d471340fe2165f8b10af73a799f153417bdecd283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc6be1ebcbab7ec27757f0d14c53aa806cece44166a0e8903ea95d266798ba8`

```dockerfile
```

-	Layers:
	-	`sha256:b1bd668dc038ff262a764cc57bb489d410c1884ffd5a858e1c9ff54e9f036acb`  
		Last Modified: Wed, 13 Aug 2025 22:22:03 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8483d6279539c31b712b95308223d9451626f6c7c78becdac0ff0f794ec02fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348425331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14965229893a0c205915170801a2fcadce8f6ece9611b958dd5f78f3c96a676b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca3385b479d65092a57bf9f294af41066b99dc31de27938a478b8d7dae4e82e`  
		Last Modified: Wed, 13 Aug 2025 21:22:30 GMT  
		Size: 73.5 MB (73507342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a33dadb21f3de9afc0a83f58306df9d6910807e3bb2ce9b03400946f47da9`  
		Last Modified: Thu, 14 Aug 2025 04:10:46 GMT  
		Size: 194.7 MB (194700987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d279a4f066a452b27641e1ae83be148a5b8a758bc5497f6273177d0e7909f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16340953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8aee994a2175f4c64dee24bdc66d470ad700bcea066170caf538dbe62441b8`

```dockerfile
```

-	Layers:
	-	`sha256:f7c8d6e272e57b2d8b1ee4f1030256fe910feb742af074a675612fae74a609ad`  
		Last Modified: Thu, 14 Aug 2025 04:21:19 GMT  
		Size: 16.3 MB (16330745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd087ded9930c2c4767ea5826df94400d54d4ddc69d520517694163046cc0ce`  
		Last Modified: Thu, 14 Aug 2025 04:21:20 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:947819fd7bb0f2e26d23be7cf588260e11787f4329b49f4415f3d414fb7adef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.9 MB (408883050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d03007dd08b1b5d8e468d886099d7816d02f0d5aa6e89765dbd45ae113c1ecc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1753056000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6fabf8fb5a31bc932739f876ea8d8586883a5d8fb0ada966a0b25599654a946f`  
		Last Modified: Tue, 22 Jul 2025 00:57:59 GMT  
		Size: 47.8 MB (47772164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78be56cbeb485aa0fbbc0ed604799ac1cda6b118967e824616a611ca0311a9`  
		Last Modified: Tue, 22 Jul 2025 01:27:06 GMT  
		Size: 25.0 MB (24960814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf803e2e42bb82c411aa32368e9fe1faf8739ac51da0f6a5e58a86f806dd32c`  
		Last Modified: Tue, 22 Jul 2025 15:36:08 GMT  
		Size: 67.0 MB (67044438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fedf6d742ad70df181260aa6f60985e35809d711b8c0469f62951cddb0f7a`  
		Last Modified: Tue, 22 Jul 2025 15:36:49 GMT  
		Size: 269.1 MB (269105634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9cdf82b71723124d98c22c08aa0900adaad89561223430b85778c4dbe3e62954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16377641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f294cbede31966715d960ade2f0b6defe6d62749a507bad59a46b93147b28c5`

```dockerfile
```

-	Layers:
	-	`sha256:0abe1c574b4c19bc04a32e066035fe207af6f92b9f5ccecf8a5764866b53ea99`  
		Last Modified: Tue, 22 Jul 2025 04:22:21 GMT  
		Size: 16.4 MB (16367433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d260d017ed59b6bc80ff1155b5aa8b05b226675c2cc882e0f0450ba865e832a9`  
		Last Modified: Tue, 22 Jul 2025 04:22:22 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6dc35a1d8a9f0fffd43e6bca573d20d673dfcd6887f166f667050a56af313259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317880973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b0ab5a283a03d1bdac480d03e1ee5b5ca1ccadb85472cf2f2b6b90ad48201`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4959d43b6e4e3bb883ad4324fbf3d2d46fc88486af520d990c753fc3a7ba0062`  
		Last Modified: Tue, 12 Aug 2025 20:56:23 GMT  
		Size: 49.4 MB (49380676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9f068820d21f743fb7a4899ffdac4cbb3c9018377c7ccd9ea60dfaa661d90`  
		Last Modified: Wed, 13 Aug 2025 11:02:14 GMT  
		Size: 30.0 MB (29993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c726bc62e5513d157547977196ac5e96f4f6b0c75bcf55735caaa59100d378`  
		Last Modified: Wed, 13 Aug 2025 15:08:18 GMT  
		Size: 69.0 MB (69018547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84103ed16a9a275b646f4ea64c94e011b85a3cd1424906ca73b63a9f9bf6e429`  
		Last Modified: Sun, 17 Aug 2025 07:13:22 GMT  
		Size: 169.5 MB (169488435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f915fb56c186390e11dbe030e0d11a4e99b4dac87d542e5f805a8edc82f716c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16133408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77f46e84c1bbbb0f790d270873cc50dede6194ad3410ea9f012f0717b5ee30`

```dockerfile
```

-	Layers:
	-	`sha256:30e5aa21c76971ca0a08c953a147530b760c34be9d2e90a4be32f93e4de056ee`  
		Last Modified: Wed, 13 Aug 2025 19:21:53 GMT  
		Size: 16.1 MB (16123233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a237f60a2c3689e58bfe6ca21b9f40332c3e0195392b3d292546a5c1ec75707c`  
		Last Modified: Wed, 13 Aug 2025 19:21:54 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json
