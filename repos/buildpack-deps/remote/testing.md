## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:b902087d4e6dc08365debc5c7473cca58b2beeb5b6a02398769cb889dacd7634
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea270324fc89bffc8655b18530eaf16c8be105028b541b14fd8e27c3d8c18509
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406084464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f5e6f7876e6a769bfc4648d373d5b92011e54a6457c200421daccd1e4a0ee0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 06:00:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 06:02:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3989ddeeace463dca551e8958b92088c5e4b3d49b9ba7ca3579c7dbf9cd9af1`  
		Last Modified: Fri, 02 Feb 2024 06:21:45 GMT  
		Size: 24.3 MB (24340256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b2c7ba7e29214031a9c39d6d5b6571c726fcfdab6f617b8aae44203ea601ea`  
		Last Modified: Fri, 02 Feb 2024 06:22:05 GMT  
		Size: 66.4 MB (66423406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0beaa393fc5b0cf30ad7c7983d01a5f0299988e669717a9879a7b05b7a2bd2a`  
		Last Modified: Fri, 02 Feb 2024 06:22:46 GMT  
		Size: 263.0 MB (263037605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e64909db19a56e73d1b3ce133800dd6afdb77355d9e98472b94fa0d463b4c176
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367829572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d6f8248127c2d250742b5da26a3d5cf1fc769ca82bb995894b9c41d3589fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:51:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8e83ce6004aab85ee491973a0f9e3b97cfa5114d4dacf9858519bf7991608f`  
		Last Modified: Fri, 02 Feb 2024 00:52:46 GMT  
		Size: 22.8 MB (22791743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae023c275943af5403b4457371b90865b8075cde3ba18ef56c9dcce109b643a9`  
		Last Modified: Fri, 02 Feb 2024 00:53:11 GMT  
		Size: 64.1 MB (64079789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbc67ab1f5ac10951b154ba7862006f5310f069ce3ec1976ec50d38633bb6a`  
		Last Modified: Fri, 02 Feb 2024 00:54:04 GMT  
		Size: 231.6 MB (231557249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47ee187d76f9489b091eb1b1a77ff83c3ad5323bf58fc6f270a6985bf8f5487a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343879173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bb91b9c52756a00109e626e23382f06182acd4e151d3478584efc666772880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:47:01 GMT
ADD file:313528f956e019639cb41933c0f6d14e7dca01353fe4ca789d7ac69e4c131ccd in / 
# Wed, 31 Jan 2024 22:47:01 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 02:28:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:30dca4c17f72b09129956e26ae0841f8c684bf0810e63983ab453762044c668b`  
		Last Modified: Wed, 31 Jan 2024 22:53:21 GMT  
		Size: 46.9 MB (46892605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6a602f4bf46f38d84ca21598d3b5c8d8cd9291a8b80057f8063d0308237cf9`  
		Last Modified: Fri, 02 Feb 2024 02:29:52 GMT  
		Size: 22.1 MB (22110720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945560866c3256a8a40e1abfb8b34b94c6d6f046db32782069e2544c08c8e2e`  
		Last Modified: Fri, 02 Feb 2024 02:30:14 GMT  
		Size: 61.4 MB (61443263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0cf67d92aae40416c3351a4c43a4cf6213b002911b7d09ee0b4686c20da763`  
		Last Modified: Fri, 02 Feb 2024 02:31:00 GMT  
		Size: 213.4 MB (213432585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:215ae05dd29b76b8e018951df5d2e8de5fb11f7285ee3222cc17e078485b843c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.2 MB (386193256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8209ad79eeeb994c392831c0ee634da34495b938ac1ff448464d6e00e44f982`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:49:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c4512a32748f0e93f76775383772932810e78398b7fc5a25c81e38a202a60f`  
		Last Modified: Fri, 02 Feb 2024 01:06:57 GMT  
		Size: 23.6 MB (23596615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a766100162b3e4745b3fea6e0c168464cca872d32ac0adb8922d33c224aa3a5`  
		Last Modified: Fri, 02 Feb 2024 01:07:14 GMT  
		Size: 66.5 MB (66537471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7c421b734f06c61de04526591b6befd47bc6b071c6e6fe381fdb1ad41eaf7`  
		Last Modified: Fri, 02 Feb 2024 01:07:48 GMT  
		Size: 243.9 MB (243897783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2a3d51d6fa62c5809f71d347a615fc6da91c1ba3fad139aac228bb332f158f0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.1 MB (400115296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540614f2841db8efa796aff98eb4518fbe179cbe1fe49848203f50bb685abd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:38:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 00:41:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d65910f8e6ecd215a4cfaada6490da4c0f4366147a1cc7a5c79cab0ae7f7fd`  
		Last Modified: Fri, 02 Feb 2024 00:41:55 GMT  
		Size: 24.9 MB (24931471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44a5c722cd80db8316b102f28c77833949cff82e03df4affc5a5ff9a7005cfe`  
		Last Modified: Fri, 02 Feb 2024 00:42:21 GMT  
		Size: 68.2 MB (68222097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ace9b60f073f6580a56f02847a10adc40b1fa636a055219897cae655993ee5`  
		Last Modified: Fri, 02 Feb 2024 00:43:20 GMT  
		Size: 253.8 MB (253821689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a9127a52341c87d8ef547fb6ad050d83834d6ce150e345bdb4029d8243c15b4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.7 MB (371712191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24a867a30154297a6b4b4c872d62ecca372a17dbe8bb0c3a64c8bca9bc5ea66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:34:03 GMT
ADD file:534203d126346e48b8c0d0430dcecaa093294a7a3c98d571701aab3e6c36d391 in / 
# Wed, 31 Jan 2024 22:34:09 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:14:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b3d1be35073c977f0bb775d26df73db32aabd06a76b52f045f43c249f737a518`  
		Last Modified: Wed, 31 Jan 2024 22:45:28 GMT  
		Size: 51.4 MB (51373756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66eaa0ef2d3a43d454ccecb5a8fe8fa3b404d14c1ba170162b92b5af9de940`  
		Last Modified: Fri, 02 Feb 2024 01:15:50 GMT  
		Size: 24.2 MB (24238462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3da179896578bdfa4dfee5627d51e3a213d69a2df22deb29cbc53008828a13`  
		Last Modified: Fri, 02 Feb 2024 01:16:41 GMT  
		Size: 65.2 MB (65235503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bedade2ce97660e9257fc41e4cea8f14e47e33edd244328d9198b8d84451afa`  
		Last Modified: Fri, 02 Feb 2024 01:19:11 GMT  
		Size: 230.9 MB (230864470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:66a8c5be286e23f66fb2ed6fab20cdb3dad12ddd90701e1283ea198bc23fcb65
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.6 MB (408582792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097287d3f5cbe01cc504af055be0c654057ef22919b3da1e054a407996162d39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:57:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93e7ca5c80e8f2f02d9ac6b4b4be99c286789f9a34f79d3eda30ad8e96cd16a`  
		Last Modified: Fri, 02 Feb 2024 02:31:59 GMT  
		Size: 254.2 MB (254196302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cba332f9b6a486b056733fba480355cf2ec74e89c99344db631962540078c282
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (373971420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa3ca098cb4eccabb3b3349b1532ed101ec00ffd4fc7395e8ed386548eda31c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:18:29 GMT
ADD file:3b31c2bd33a3d7e6352823413292afa26a09dbcdbc56396202701f16e609204c in / 
# Wed, 31 Jan 2024 23:18:33 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:02:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:651c4bce8b545a7028c9eea81f8b25dae93c9bf0073fff7020f5784448310184`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 51.7 MB (51697772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85ac82864171f5b39a8cef06755753f3688ade2c0de1df1df59738ce25afd0`  
		Last Modified: Fri, 02 Feb 2024 01:32:15 GMT  
		Size: 24.9 MB (24922536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01072c7522404012c43b712d6cf353bb9f279ab8edf997c932c4711b106e26f`  
		Last Modified: Fri, 02 Feb 2024 01:32:32 GMT  
		Size: 67.5 MB (67531843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed432a71247d47fe7a572eeeaa2b8bb341d410ab737f7831698cf32e78d463f1`  
		Last Modified: Fri, 02 Feb 2024 01:33:06 GMT  
		Size: 229.8 MB (229819269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
