## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:3fb78d6765f70cec3901b69c7768dcb09e6b03c243f627f6280d454d7bebd8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9fc82c3730d2e3d1ae162100e70b883c5392f02f73f5b6c60253a844bba4c18b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d7e352c300d9a25741a6756a3cbadbe4e64857252bca581142bd1bfd0f89ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:22:09 GMT
ADD file:ba5db69738244d00088ef591ca43fa8b3189e78fba56bc69b70a232e6f04c7e4 in / 
# Sat, 28 May 2022 01:22:10 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:45:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:46:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3d4e1d44a24e0c5abd41b803d14f211ba153bc7963871713cba8ee5fc687888`  
		Last Modified: Sat, 28 May 2022 01:28:41 GMT  
		Size: 45.4 MB (45429730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec8bceb2e238bbbbec9e458cf83c1342015ed1b717be0f88b50d267c52437d`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 11.3 MB (11302994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2aa521faedb4a16c079e9574f537b51a05c2ad4fbabd16f83d9bd58c365bac`  
		Last Modified: Sat, 28 May 2022 02:52:34 GMT  
		Size: 4.3 MB (4342992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20527d0d718ee46b5f18a310324e3d635eeb75021e2b9d9ec450ea75755ddcfa`  
		Last Modified: Sat, 28 May 2022 02:52:51 GMT  
		Size: 49.8 MB (49765581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4ef7fa62d9393e18cbdc052a0c4215c7d3bee0182aa064cc0212d08f91ec26`  
		Last Modified: Sat, 28 May 2022 02:53:28 GMT  
		Size: 214.5 MB (214488851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7251838197e01781afa788e234bb0fc8196df80f1d338b5159ca663bd5ac0d11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309228173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba453629467df5621ab06ddce3b3bc5945e97011a54a95e29c1367b2364a02cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:08:22 GMT
ADD file:ca5505d9f3e1ac4f55a706fa62d334e14d6bb1ed90bc9b5e693cdbd51baa5450 in / 
# Sat, 28 May 2022 02:08:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:20:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:24:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5450f0cf6abbf9c0e24877d991f23d0bb00a7ad2be57f32f1d9a95d1db4d3a6b`  
		Last Modified: Sat, 28 May 2022 02:25:24 GMT  
		Size: 44.1 MB (44124502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47eb48bf728f24b8e81217db5c19aaf41c16e66134d55e1969f52ac53d3e113`  
		Last Modified: Sat, 28 May 2022 03:39:42 GMT  
		Size: 10.4 MB (10352917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18968c0654885075bb50183fe3816b09108c576346ea3b35afdc47af2884a86`  
		Last Modified: Sat, 28 May 2022 03:39:37 GMT  
		Size: 4.2 MB (4162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8578e6677af75baf5ff701cd0098aab65ae8bdfd4f7c74984ea653a2bceb086b`  
		Last Modified: Sat, 28 May 2022 03:40:28 GMT  
		Size: 48.0 MB (47988481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9f58bf4c33d96a0aab5c5784b8270db8deade469b172f8489968774082e66f`  
		Last Modified: Sat, 28 May 2022 03:42:40 GMT  
		Size: 202.6 MB (202600201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5cb65b6681bb0a10428c73f18132dc391fa011827e6867b55dc1e21faf211d34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297229300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399f9af40b7ee06f115c713e9e99f42b3beadd729ecdbdeb962cf13cfd6924a7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:05:16 GMT
ADD file:f859825c79355490a08b5fd55799cc3eb1643e21abfeebe59a3a4b08e54e3f7f in / 
# Sat, 28 May 2022 01:05:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:54:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:54:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:58:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae3d55ab33f9bf9aa2c47629e66da1c4e679da10d83c29941f39b04140996e4b`  
		Last Modified: Sat, 28 May 2022 01:21:38 GMT  
		Size: 42.2 MB (42150781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277a5551d8d3385d5cf64c67234fe8db9bad96903365595e8c6c61146e48d2b`  
		Last Modified: Sat, 28 May 2022 03:17:39 GMT  
		Size: 10.0 MB (9957035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2055cd14260ece06830786d784271b3008f3ce2ea3279123620a6d78a2afecfa`  
		Last Modified: Sat, 28 May 2022 03:17:36 GMT  
		Size: 3.9 MB (3921757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7574dbdaaad44c5640ade0f5aba1843344998699356f46c27a9d56220564c345`  
		Last Modified: Sat, 28 May 2022 03:18:23 GMT  
		Size: 46.1 MB (46127871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782235e3a688ec663d99170e2f7d041c60be70184f79e1e0c1469563275858ad`  
		Last Modified: Sat, 28 May 2022 03:20:26 GMT  
		Size: 195.1 MB (195071856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d1afbdf5c0581e8ec21cfa0d1ea6a9d4504e4ade6d762031d2af6f544fc48642
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306837578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be430c10a25c8dcc78b7405e13f1b7156e73d919472bb6fcf8ff73c22a7e044`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:08 GMT
ADD file:8949016fba61b18207f5a2309fc974562080c5cc80d1eb82adb35c4fa03f6f05 in / 
# Wed, 11 May 2022 00:49:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:29:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:30:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:31:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:139065d8f4553df403babda56f830c32aa1f3e57f18d2145a3179468921a4bb8`  
		Last Modified: Wed, 11 May 2022 00:57:26 GMT  
		Size: 43.2 MB (43212478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0acfd1725613d968a54b7fbfe1f70f24b8a0dad792ad3cb28349035f7736fe`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 10.2 MB (10217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c314192ef0350d2ac1d1e49b4fddbc49dbcdc609e56e0e2567ee2dd37f0bc`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 3.9 MB (3874525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a0592b38ee1d873cc3681a7998f4ccbb2745e34ddf1d93c35a1d299949facb`  
		Last Modified: Wed, 11 May 2022 01:39:44 GMT  
		Size: 47.7 MB (47735546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b2158b1273a74152e77de956cc46e488bac0aa69b766d08ae8319d4a66c91f`  
		Last Modified: Wed, 11 May 2022 01:40:23 GMT  
		Size: 201.8 MB (201797253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:62851063ced20e5d6984ed5c1a0a0bb2fb1cf04791961eb30ca94b67f34dc3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332630034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628eaa5f6a553054c719cfb1c74ee1f3512f4f239fd87cd1fcda6c76bd58ef6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:50 GMT
ADD file:1a448f874e606582cb67d9369c97c83c78f2327fde8089b8cb6aaf476dc51935 in / 
# Sat, 28 May 2022 00:41:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:16:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:18:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99b3b0cea6c21e2e36bc4c198a72e5aa3b3ab76d26c2c63d9b0c2b0add554135`  
		Last Modified: Sat, 28 May 2022 00:50:28 GMT  
		Size: 46.2 MB (46150199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cca76d5e15edabc23b8e1a62888ca87b80e71009098aab933b555891ba8af`  
		Last Modified: Sat, 28 May 2022 01:25:03 GMT  
		Size: 11.4 MB (11358709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a795692955c7b33f32b3c1a422a6d1bf8d2d10eea37afa9f414b5ccad00ad0`  
		Last Modified: Sat, 28 May 2022 01:25:00 GMT  
		Size: 4.3 MB (4342253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4d58f49c17116aca3a038f7654a0f4635eef2069cd5a06232723448d9f23a`  
		Last Modified: Sat, 28 May 2022 01:25:21 GMT  
		Size: 51.3 MB (51268924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b9d996444e63be6314cbe9630f4f60049a922e39a97dbdbe20c549b8443c70`  
		Last Modified: Sat, 28 May 2022 01:25:59 GMT  
		Size: 219.5 MB (219509949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
