## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:b07f4ec6f8fb732de8e1a6794a925ac6079421f30c49568ffbdbfa5cfcf9b148
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
$ docker pull buildpack-deps@sha256:a60d63d456d4a37cd7c583875120f83c8d9865b9e1fd9a07bdf913fe0fea59ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 MB (378144406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d06640b2398cceb5499da6e689b2d90d3ca992dcaa49286c473ebdd4ddc79ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Tue, 03 Jun 2025 13:35:19 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d3fae0f8d1c689d461da616de1a85e5ade1f7c61c5496c0c3b6b1bf6e722d`  
		Last Modified: Tue, 03 Jun 2025 14:37:41 GMT  
		Size: 67.6 MB (67637573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c053c3fe409c6202007ee9fe27860b42e831015c1fa52afc3a49e5110c1c`  
		Last Modified: Tue, 03 Jun 2025 14:37:55 GMT  
		Size: 235.7 MB (235676174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:216742157fff3aa4b4fed0aee18a72806f6b0e7be312c33840482c7f21ababbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16925615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74914abd44a5b9fbccafe6c6046b4504c53c7215caafefd55e6ac400a9a6d32`

```dockerfile
```

-	Layers:
	-	`sha256:d9e74b77f930f3277ffe9ddd8fd1304238528c723b8ee3ff1b7dbdda98bf029e`  
		Last Modified: Thu, 22 May 2025 00:13:00 GMT  
		Size: 16.9 MB (16915422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6762793613d242035ac02a2fa94e1858932d8357ab659647dd883dcabe9582c8`  
		Last Modified: Thu, 22 May 2025 00:12:59 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:773d41abff076f587187ac21ef333ad611e9fcde632a7f2ff6e1c296e41b2527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345390194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3ca8dc5e22becf3743931c195587df8badaf0036247845f6f1cd558f4cb3ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9616f5c2624aa57711d4d3a917ef21ea33c33b9e29ed21732abc6456aa133801`  
		Last Modified: Tue, 03 Jun 2025 21:52:52 GMT  
		Size: 47.4 MB (47438143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fced245b3861daa32a8eb96fca42f40c6b8763a3cff659d7638f85cead39fe0`  
		Last Modified: Thu, 22 May 2025 01:15:18 GMT  
		Size: 24.3 MB (24327560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbae712d6151507af038108c551389130a66d8e4e0824e97fb8a78ba564685d`  
		Last Modified: Thu, 22 May 2025 04:46:33 GMT  
		Size: 65.4 MB (65354830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9260b6f4a9e190cb6cb4926f1fab0dd9546aa5f5ba1f420a3817e41b7284e`  
		Last Modified: Thu, 22 May 2025 06:41:23 GMT  
		Size: 208.3 MB (208269661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b9fd795928d47223fc23866abd0e6046ffdffadb7538f4190f2fa88c3027e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16694230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20af0ffe5dc7b4bfc7a2ff586abac1c9379a27e1669c767613c58a2ea72b33e1`

```dockerfile
```

-	Layers:
	-	`sha256:5338a1817eaae96ebfdb51313c5d8f779e1aee06d81eff6b7544ad3dd8c17640`  
		Last Modified: Thu, 22 May 2025 06:41:18 GMT  
		Size: 16.7 MB (16683977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3cbcedf417bec90f28e639d382bd02df1b0a293b2bf7b86ac00aeca33f15b97`  
		Last Modified: Thu, 22 May 2025 06:41:17 GMT  
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
		Last Modified: Wed, 21 May 2025 22:32:07 GMT  
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
		Last Modified: Thu, 22 May 2025 15:38:51 GMT  
		Size: 16.7 MB (16683381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9f9485bba875bbabd96bb2c574b8e53dc349e1d1cf364e59a2530b8284d762`  
		Last Modified: Thu, 22 May 2025 15:38:50 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98a488780cb3dd53e3b4ddbc63a334089b10fd3d79ab806beb55e33cdbc703aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371633465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5569cf57b1c1812bec348449885c2d970fbcb671b79f8b0e2ca22c2f357009b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925a0b1aba64c2f9934b5b752199fa927f08300fc82c456fa922c4303a06f43`  
		Last Modified: Thu, 22 May 2025 02:48:53 GMT  
		Size: 25.0 MB (24981840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546584c670303be4513862213cb042edd5a8f7eec9db9d6e8c5844665b49b26c`  
		Last Modified: Thu, 22 May 2025 09:20:02 GMT  
		Size: 67.6 MB (67605213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c6be8c6dd5bd91c6ce2428d6b5468fb72cb93a15464af537aed1a93d8c7d9e`  
		Last Modified: Thu, 22 May 2025 12:31:45 GMT  
		Size: 229.4 MB (229428118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:462d85b74a1f2646bf6d4a690fe2c6a9e0bc71378262edbbd3d757d5b96fe557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17009970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9432186dba6e08ef9a90e7e9d7d7324cfd919eec1c13b80f4dccb33a6e43388d`

```dockerfile
```

-	Layers:
	-	`sha256:7965bee69bdc753cc1bfe63eecfd994228b5b43c7c772a34acc0a450e551006d`  
		Last Modified: Thu, 22 May 2025 12:31:39 GMT  
		Size: 17.0 MB (16999697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a3b7dc49134acecaf0edf42ccb2fef62fc53c00b18f1e286eadbbd5823010`  
		Last Modified: Thu, 22 May 2025 12:31:39 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:81ac221c0018e9238ccc7dd0053c5bfa0b810ba6b31430a0c28c3d2d6d0f0872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b0b1273ff285e91764a99f0768eb52cce21267283a7d102d493cc48da7ab8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Tue, 03 Jun 2025 14:04:15 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53475a03e00d0d9a396cb70f6edb89c6daaba7c95e28d935ced8a0100b7b7bc9`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 69.7 MB (69655812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dd214bed674db855a1bb7bd96a9a5f465ab885f73c5b07af7d81223142c462`  
		Last Modified: Thu, 22 May 2025 00:13:25 GMT  
		Size: 239.8 MB (239782595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c63bb64e4cb115b6c93c841f6f1a835e5d506e96e81f03f9ecd17c1711d164ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45019c9c9fa7ddf7c74e5e147c643464a872778e09a3b28c1c6ae7476ae5ba73`

```dockerfile
```

-	Layers:
	-	`sha256:14698a6f978b4bcb513060673fef5af05c56c3ebd430451f51cba68f47e98f49`  
		Last Modified: Thu, 22 May 2025 00:13:20 GMT  
		Size: 16.9 MB (16885037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ae96c519f9eb947e3ae21c04dd12295f80d2daeafc1441676cdb266f98fbbd`  
		Last Modified: Thu, 22 May 2025 00:13:19 GMT  
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
		Last Modified: Thu, 22 May 2025 16:59:05 GMT  
		Size: 16.9 MB (16907296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7a6bcc752e90092cb345242ceb9e8e373f5e1ed434c87cb57380a196d8bb46`  
		Last Modified: Thu, 22 May 2025 16:59:04 GMT  
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
		Last Modified: Thu, 22 May 2025 02:50:15 GMT  
		Size: 17.0 MB (16971541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4362dd8ef686114ddc1bb8934e492e76e4ed0c42c774ee6be458005a2ee32558`  
		Last Modified: Thu, 22 May 2025 02:50:12 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377319b6be2c65712dcf26256e5181a1f772a032ed728796e4c7afb9d17b8fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354195049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd8719f45947ed8cfb058ee2d9d81dbbfac8080102b74e1fdcb5acdcf8dea40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645228c4b06e89bef4ee7caae64a6417dc0f102985c8d7902876a160465531e`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 26.8 MB (26757774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925cb7f6baca00c5ff3348d92eef6b2e3dd349323f30f9ed50efa944600d250f`  
		Last Modified: Thu, 22 May 2025 04:39:04 GMT  
		Size: 68.7 MB (68653716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebac43471b53ab79ddabf4d6fdc081af87cc53f59821c86f41dedabfb749e22`  
		Last Modified: Thu, 22 May 2025 06:44:10 GMT  
		Size: 209.5 MB (209461332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7f8532abd32bfe49d974721688685b0cbfd7ac254ecfd328f683b68489b79c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16709227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ace3b5427d8fb5ed8b45893624d02dd088427569f3e157855349ca57a1cc38`

```dockerfile
```

-	Layers:
	-	`sha256:8e400582cc5fae937168748a119f9b3eac1e8f003692e02cf4426d957e9050bb`  
		Last Modified: Thu, 22 May 2025 06:44:07 GMT  
		Size: 16.7 MB (16699034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59fc1d8c0b9c57f70f26027925e5168286ebf7290f795b16e3aaecb646b4abf`  
		Last Modified: Thu, 22 May 2025 06:44:07 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
