## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:0445de954a95927d59beb4134f3fc4f04d0e0eef4b74a6d4c38c920424c4642e
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
$ docker pull buildpack-deps@sha256:d0934181581b9a094793bd17a6b4b06e090d24813ac527c53e833cf3f9830235
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396653217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc2dcc11b1161cbc1d6d1e0ebae8fb4c5b756563d6b20780795c5464a44ce22`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:38 GMT
ADD file:221c5996f1ff4dd71764ca719f363e27bb329a807e397f6654cbb3c478c54c9e in / 
# Thu, 11 Jan 2024 02:40:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:43:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5c06b5f92f5d425b6a1eca65d06813d5da1bf325255b6cdab64db03a7ee0d47`  
		Last Modified: Thu, 11 Jan 2024 02:47:11 GMT  
		Size: 49.6 MB (49562052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b14ab6cee5b8a008ac52067ba895976219bd813b8d4aa739a74ba5ce9121594`  
		Last Modified: Thu, 11 Jan 2024 04:48:48 GMT  
		Size: 26.5 MB (26464231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e1dd418040b8206f8c9d1069566b49a386b6b9fc3cd2fa8612d76819d240e3`  
		Last Modified: Thu, 11 Jan 2024 04:49:06 GMT  
		Size: 66.0 MB (66044625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b49e735ead2509afab7209dd5ee7e829c85fc2018f59c91c8cc8350f683469`  
		Last Modified: Thu, 11 Jan 2024 04:49:47 GMT  
		Size: 254.6 MB (254582309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d803c828fa78e4048b6dd9f0819767f330151ea595818e1febed9c5afd3cb1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364689828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733f23a4295ce61add3f84746d870e37e455f2f81532ea3486e741341710334`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:30:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0751a1e8acd62fd190d7c3bec2800497b26033c33f78f5fb4ac87c59dc9eff`  
		Last Modified: Tue, 19 Dec 2023 05:36:11 GMT  
		Size: 228.9 MB (228855857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a28dc7425b6455351a0fe2edaf8ff20876a43473dddeab567c4a60a1fc557efa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340919831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaa22e2af095fd362f6d4d9b0ecafecd609dfbd356c30ecd45f2d14984008fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:43 GMT
ADD file:2578bbd6242f569b630ed2a8dbbe60a6317a1fd910aebe4814313b4c0eb7a482 in / 
# Thu, 11 Jan 2024 02:45:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:25:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:27:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d77eb11f48fd53e8f4a4cad655e31f2fb5f91177fb35abe347a055a3352eff1b`  
		Last Modified: Thu, 11 Jan 2024 02:53:33 GMT  
		Size: 45.1 MB (45063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37916331c99d3b698aae6553fb6c2a2c76d2cdb8dea2d3cc6e825c690f03420`  
		Last Modified: Thu, 11 Jan 2024 03:34:33 GMT  
		Size: 24.1 MB (24103233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb41fed208e1ec1bace230d40b75cf9e9012e2296ace322150b1ff2f121346`  
		Last Modified: Thu, 11 Jan 2024 03:34:58 GMT  
		Size: 61.1 MB (61056442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cf87bcc0604ea18dc3f3462bd14ddec58f15bec062d30cde5c2fd0ec1f5941`  
		Last Modified: Thu, 11 Jan 2024 03:35:52 GMT  
		Size: 210.7 MB (210696708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb68cb18300df68a560fc268f70c78ca7c055d4b8cddec272bb844e177b2418d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382964950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f4c85dcef57c264951aaaa9a7eefd7ffa3daeb32b9bd17cac512192065788d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:55 GMT
ADD file:3a7cff48546e976afb3192375ccd816fa228a2a86ca359ad2d25968d89736a30 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:41:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54db10be8b28565099ed8931d6e2048335ac2a2e8633f5ee9961d35950099935`  
		Last Modified: Tue, 19 Dec 2023 01:48:52 GMT  
		Size: 49.6 MB (49615103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3258514d2e2ba8de515d7376cc008e3df15536a3972bbc964930061817df14e1`  
		Last Modified: Tue, 19 Dec 2023 11:45:54 GMT  
		Size: 26.0 MB (25951112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f1ab7417116c7641a520689c7837277c5b5d78343f1e4e4a42effbae89c744`  
		Last Modified: Tue, 19 Dec 2023 11:46:10 GMT  
		Size: 66.2 MB (66172700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ebe0a39eeac98f80c2f1e2d2f0049d2a796beff951e570d79a775e3e220ac2`  
		Last Modified: Tue, 19 Dec 2023 11:46:41 GMT  
		Size: 241.2 MB (241226035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1d3b7fb70dd9091805853c552b492613186ae6d4f59f342281969f98b61b5cf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397354045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d936e608e9d19d2fe6aa7fda314f87f00158bbd0a1aef4cd9be0db95c64cf2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:24 GMT
ADD file:5564e4ab4c2aca360aa2b99bcb8c9c77e6d97554833ae3cc9bb2f49ed35e25b2 in / 
# Thu, 11 Jan 2024 02:41:24 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:40:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a827afb392949e39b5beea804bcbbd7be98a07848f45ead6a59e020bce5836dc`  
		Last Modified: Thu, 11 Jan 2024 02:48:52 GMT  
		Size: 50.5 MB (50527068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181d3088fd6488ff4296a6d76024c5ceabebb089069d60b6dcbf62cc62624985`  
		Last Modified: Thu, 11 Jan 2024 04:47:28 GMT  
		Size: 27.5 MB (27453882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427ac95ec51ede300e74262c9ded6e199d3947a3341d21a1dc672fb66a3c458`  
		Last Modified: Thu, 11 Jan 2024 04:47:52 GMT  
		Size: 67.8 MB (67814735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19358c3fb602d5cb0e86c288e8b2372695d18a6ef62fde0675d82e0f9a6428`  
		Last Modified: Thu, 11 Jan 2024 04:48:49 GMT  
		Size: 251.6 MB (251558360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:378613bf30a508e408e6d84edd41692f2fa846a5cca4bbc39432ccdcdaf9acc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369056382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd09b1e449db678be0cf02fe117387b89f07b699757dd3ac58b201e6ebbfb3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:18:24 GMT
ADD file:f8968c17bd3825e4f058fd68c683a3c699e06368b69577a14d575a0c3ac70e6c in / 
# Thu, 11 Jan 2024 02:18:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:17:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5cc64b8a2f7c7d0c78917ac707955e566c39f9c62003870eb7cd32f7b23a5f`  
		Last Modified: Thu, 11 Jan 2024 02:30:01 GMT  
		Size: 49.3 MB (49333270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a6eeb1b81bae44e0e846833442693a689a375fce576961be0a2c167f5f861`  
		Last Modified: Thu, 11 Jan 2024 03:34:44 GMT  
		Size: 26.2 MB (26204931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb2f97a9c0cb49fd93afb006f99f7d60718b4032952d234bb51636d62c2ba0`  
		Last Modified: Thu, 11 Jan 2024 03:35:36 GMT  
		Size: 64.9 MB (64922447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb23dffca74e914c9a2e767ff13a3cb320f1cc8c196042a06e4e5a1aa141dc`  
		Last Modified: Thu, 11 Jan 2024 03:38:10 GMT  
		Size: 228.6 MB (228595734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b45bc504ee4fda550cb99b9bb73dc89e0f0326fd347493a93457e2364575265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 MB (406135677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ec76a98fe283c076d6398adcfb0665dd8a9cdec4a43ee1da1c11f0a9c6377`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:24:15 GMT
ADD file:0c76fa40c0d4d6eec23b49588ff6dbe4b5563f6db327a13831ab7eb6e3f30743 in / 
# Tue, 19 Dec 2023 01:24:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:21:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9aa21f27abca3b3157546abcfde68519068ba019777333f48885704721c81290`  
		Last Modified: Tue, 19 Dec 2023 01:30:10 GMT  
		Size: 53.5 MB (53476480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4bac2e5e84f15314991062e11b3bcdec79ce34bab827dc518eb86ed33d8593`  
		Last Modified: Tue, 19 Dec 2023 12:26:37 GMT  
		Size: 28.9 MB (28929833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e9e5a914f7e92834cc5f6c63a7bcf55219a7fde6114e91ad54a5cf55e99362`  
		Last Modified: Tue, 19 Dec 2023 12:26:57 GMT  
		Size: 71.6 MB (71599173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf858753babf0e4ab185c8a2da4d466a6b6231570bb5f2ce34c9ec6332d4b1`  
		Last Modified: Tue, 19 Dec 2023 12:27:44 GMT  
		Size: 252.1 MB (252130191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c2a878a7c03349c52aee0fc9b529075acaadac507951f38f5fb7b0fcba8c3259
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.0 MB (371014955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7c3e030ea21d6eeed017a8fbcd2ac6cbb93f398baee7c459119c721bd4320b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 02:18:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47161a7187326816c278e7d750ac894a70682803dc239b5d8c20d926e36e792`  
		Last Modified: Thu, 11 Jan 2024 02:24:08 GMT  
		Size: 67.1 MB (67130864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce18ce061b7b10504caa95c78ffefd4c54eba93d2b4f83ecf1e907ba6e3dd60`  
		Last Modified: Thu, 11 Jan 2024 02:24:43 GMT  
		Size: 227.6 MB (227592411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
