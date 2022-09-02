## `buildpack-deps:kinetic`

```console
$ docker pull buildpack-deps@sha256:c24817e44bda6ad8cc19783d2b65814fce5afa3a1b83857359d0e0d22c849e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3c95ad74f79e8e0d742dbf0b70cabffb0135dfa4a377b9191bc38aa416ba6e48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6d2926c4684f01fa0103bb24bdb1b2a93bec0dca4b41885fc0ca5e11f05fd3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:43 GMT
ADD file:d5de90ac61ee7027aa0900efb669efa73f611463cf73ab2cfdacadf5ab9fee19 in / 
# Thu, 01 Sep 2022 23:46:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:32:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:35:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b78030514e08aad79cb596ba84b18b9579e90eac0b8e0c2dec483c3da8dbee8`  
		Last Modified: Thu, 01 Sep 2022 23:48:15 GMT  
		Size: 27.4 MB (27428015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71363ea1301988ddf4ef6039b34a05a19b44a70e1ba2764e95fa0f47b3585c12`  
		Last Modified: Fri, 02 Sep 2022 02:39:23 GMT  
		Size: 6.8 MB (6779788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261ea038a7743d40031459e01e57001571ca5986a617d9e2d3174c66d98187a`  
		Last Modified: Fri, 02 Sep 2022 02:39:23 GMT  
		Size: 3.6 MB (3633660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dee5c450c1549fab83f54e9138820f82132ebf0b50a52e7ffb97b6074e98c1b`  
		Last Modified: Fri, 02 Sep 2022 02:39:39 GMT  
		Size: 39.7 MB (39729510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8f5804b753a7685df0f765050b72cb63d67092265ce7d2dacd3391cfa09ace`  
		Last Modified: Fri, 02 Sep 2022 02:40:13 GMT  
		Size: 181.8 MB (181779687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f6c70d3da9e107526ed57d9da0674e7e3bdcd2c3656609d1763abad413898dd8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222315041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76db4726c51f452cfcf90471617a6293cfa2ed57469fa660aa52c3fad7b47eca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:44 GMT
ADD file:6fea481ddc80754c10680e7c291055af82ef815eb0fdaf745c49c4f4cdf2afa1 in / 
# Fri, 02 Sep 2022 06:08:44 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 09:35:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:35:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 09:36:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:36:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f63be4c3b8fca43746377bd8a99dd9b04acdd942d8464feaae1671e6363d920`  
		Last Modified: Fri, 02 Sep 2022 06:10:58 GMT  
		Size: 25.8 MB (25845683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c94aedbe9250aab4e90e8e88c1f2af520548789812f567b90a81f67dc9145e`  
		Last Modified: Fri, 02 Sep 2022 09:43:15 GMT  
		Size: 5.9 MB (5948408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78166495a53038ebe64fd164f5d7e26607173735e8a0e096424b99f947d93cb`  
		Last Modified: Fri, 02 Sep 2022 09:43:14 GMT  
		Size: 3.8 MB (3801422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28471ad57cdb7e9e4d1bd803eae0208867737111fd76d4143f4b6120903361b7`  
		Last Modified: Fri, 02 Sep 2022 09:43:34 GMT  
		Size: 42.6 MB (42593085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd81b6de6e71e74e98034d486ef79416eeab04372473695ef4a57a2dc8dab6b4`  
		Last Modified: Fri, 02 Sep 2022 09:44:07 GMT  
		Size: 144.1 MB (144126443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bcffca5d2875c3c5e9e2ebbae1682df46d1a2202cc72f8d63670b9e3d68e3503
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246828390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c63411acefb29eac5a58855779b5ce4e65910ca3242fa4cd116d30e28860fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:58:02 GMT
ADD file:1b9e898b22915c14e3d83959e989e2a653148ff82c8e2a1b3dfa8035256219aa in / 
# Fri, 02 Sep 2022 00:58:02 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 04:42:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c0b344a74c2d365a9a57a618f4a544c4e8e70f341f67973d3a22aee52a267b9`  
		Last Modified: Fri, 02 Sep 2022 01:00:04 GMT  
		Size: 26.7 MB (26663798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ff0107faab8a809cab0821df6c069bdc690f3cda610960915bb07f0c47780`  
		Last Modified: Fri, 02 Sep 2022 04:48:55 GMT  
		Size: 6.6 MB (6603091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62edf58fe3260c89e551263ca83a26aead51b89196e35322ead3ba9023c23aed`  
		Last Modified: Fri, 02 Sep 2022 04:48:55 GMT  
		Size: 3.4 MB (3390812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df24de8e3685677e98d7d3aea7263fa8e11665eb30549c733d0760b8bdd6a28`  
		Last Modified: Fri, 02 Sep 2022 04:49:12 GMT  
		Size: 39.5 MB (39516416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a7dab39ac145cb27e46bda054f99ccfa338d3b9d323b4053bc8b9bacd5e88c`  
		Last Modified: Fri, 02 Sep 2022 04:49:47 GMT  
		Size: 170.7 MB (170654273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aacd2841a1e442fc1a51300cf1624bb6f38dffcdff3c27fa7a1e7f942d4a3ebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282251775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015622ad1f917fcedd420ed628aa2356b7b6306b47a5885e9a81b47e602f7868`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:50:26 GMT
ADD file:79183abf8a1f4a6d4d04d73bcbe47e66f08bea9796acebd37d515855a459d132 in / 
# Thu, 01 Sep 2022 23:50:28 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 03:48:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:51:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff717d18c49d9ec97ec3efef7dd73fe40829e1902f57d95a91516a42f69a091a`  
		Last Modified: Thu, 01 Sep 2022 23:53:03 GMT  
		Size: 32.1 MB (32082633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c734e70f580a1e1db27a87020a89cba5ca648c7e9c85068bd42b1e3126ebe`  
		Last Modified: Fri, 02 Sep 2022 03:58:49 GMT  
		Size: 7.8 MB (7750570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09098d7e8658181028c27fff2df2b67293550987d175c5fab78075ddec7dd8ac`  
		Last Modified: Fri, 02 Sep 2022 03:58:48 GMT  
		Size: 4.4 MB (4361359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc897ebe25a803a066f6b1910e20dec6fc0162253745894a729850d1d32c57c8`  
		Last Modified: Fri, 02 Sep 2022 03:59:13 GMT  
		Size: 44.2 MB (44161167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b502c070e035bff4190a1869e54d6a3382719ec5513be9900a64d748b181aaad`  
		Last Modified: Fri, 02 Sep 2022 04:00:12 GMT  
		Size: 193.9 MB (193896046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:73bf7abfabd3ce3f80d631c8b4246bfb77cc7865a6ea4a088e1f1bcd8e898b00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280785501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d3e3d306e8b6f9c7a24e537c8ca6080ef2a051ad1d85eeb998da9e2c4ff0b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:14:23 GMT
ADD file:7c2ab85ecb4dc221c58ed92c05acad8d0b2ad90e46ec34c0a45fd5a5c3a9f7e2 in / 
# Fri, 02 Sep 2022 00:14:25 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 01:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:17:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:27:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:26010bd634bfca42373b6c36c189031dcce89570ea1226e9462a48d7a684240c`  
		Last Modified: Fri, 02 Sep 2022 00:32:57 GMT  
		Size: 25.6 MB (25594334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826196a5d14cf0f019090771814dce885e1420c992b36ab31bfed7b28d86cf5`  
		Last Modified: Fri, 02 Sep 2022 02:00:23 GMT  
		Size: 5.9 MB (5930253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add19389e79fd75d5e3421d12568767855677a99cc4cfe5d50d5590034851237`  
		Last Modified: Fri, 02 Sep 2022 02:00:18 GMT  
		Size: 3.9 MB (3881273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f04e7e633bdcb9ab785ebbaa03714ef1fb30b6e9341369572e7eb655916151`  
		Last Modified: Fri, 02 Sep 2022 02:02:44 GMT  
		Size: 42.9 MB (42853430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67eaacb0aa78a362fe9ee225ee0e3ca057354904b8418793e4b7a1511e7aab3`  
		Last Modified: Fri, 02 Sep 2022 02:09:59 GMT  
		Size: 202.5 MB (202526211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a565fb5e9470fccd7e7164a3c87a5b2433fa673dc08c7e1a760184769385eb1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228802204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa992f61c6a6e4dbc5ee3ffe027303904613e78c952d7f7192bf0e5b84ed6b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:38 GMT
ADD file:61a0b983796cf76453cbc73a44968b8cefb9f90cc922075728432bdbdaaeb854 in / 
# Fri, 02 Sep 2022 01:03:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:10:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:12:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a51274124ed15147344e4d31d9378a33521faff1de175e551081c34c14db1b9f`  
		Last Modified: Fri, 02 Sep 2022 01:05:17 GMT  
		Size: 26.0 MB (25995506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9727cdfe9e4d0ad02573de5f42a04ee40c70d014fcdffb4b684522e06d667`  
		Last Modified: Fri, 02 Sep 2022 02:17:04 GMT  
		Size: 6.5 MB (6470487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd626668509bf2d37bfd328fa211e8e7ad57c719072d9c7f1fc379bc2c187745`  
		Last Modified: Fri, 02 Sep 2022 02:17:04 GMT  
		Size: 3.6 MB (3625387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1947234f2c6685065fd711d09a80a70640e7a9c3b7521b8bbdd0c52afb85d8b5`  
		Last Modified: Fri, 02 Sep 2022 02:17:16 GMT  
		Size: 39.6 MB (39561768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74547493d0510538ad41fae3cfd6a5789215a1d753d5ea8509671d8f743cb2cf`  
		Last Modified: Fri, 02 Sep 2022 02:17:40 GMT  
		Size: 153.1 MB (153149056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
