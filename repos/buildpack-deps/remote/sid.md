## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:a8435c9f398bc9f8e69164a4bff2ab8ab79a07ff149628d000b28b021f534f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42a21e26a4e695f00b57656041ed5d941ec2eb44220d203990da6a85a318d463
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323256574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f39f9d2fade10fb18bc173eaef31360fcaaa2b946a3b57b535978920fb95be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:21:58 GMT
ADD file:5d2d72d29ae1c01dc7f5bf337c78d40925a9843052910f79f066f681a2ec43e6 in / 
# Thu, 23 Apr 2020 00:21:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:58:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:58:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:58:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:59:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2bbc6b8c460d7ed40af9e8f69693608780022541107dbb47c4a717e0a15e84f4`  
		Last Modified: Thu, 23 Apr 2020 00:26:48 GMT  
		Size: 52.0 MB (51979787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af86ee5a9d864ef79346df3bd57faa5631e1b16cc83353b543768d6d306d88f3`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 7.9 MB (7934538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4c0ecf8059fde4ddfb61bd7bca435c46f56832aba0b7726caffbe9f0eb90c`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 10.3 MB (10297783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab49313f0d6d21322b207f20dcc4226bec4418a685bbed264ea4a288a05ad50`  
		Last Modified: Thu, 23 Apr 2020 01:04:49 GMT  
		Size: 55.7 MB (55656164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468df7e5a902bd3f99b4fb866e53e2eb5e2efcd5a50584e3d51d905cb09a2b8d`  
		Last Modified: Thu, 23 Apr 2020 01:05:41 GMT  
		Size: 197.4 MB (197388302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:73d81bff35a8820f4fbae2ed87e5dcfe362886a68d21d01ef5b48e0092189474
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294711159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7dc482b934edf9911c000439b99ac8ebab4c883dee43be267e35967f8aafea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:30 GMT
ADD file:a75ce77565b83a916eece2d56e963b63f9ee7367ef197d8c290ff79a800514a6 in / 
# Thu, 23 Apr 2020 00:54:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:36:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:37:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:38:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:40:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e7313629a61ef455f6387257ffb8f19dafc5546554a81db1483683758531fe25`  
		Last Modified: Thu, 23 Apr 2020 01:02:16 GMT  
		Size: 49.9 MB (49937767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c899094d7c95a1d63461502d6a6462086ecd6082030f55fd59fefae8e1088d`  
		Last Modified: Thu, 23 Apr 2020 01:51:55 GMT  
		Size: 7.5 MB (7515305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19b16385622348c287bab3a3358b580809022125ad4d1aca43b5c38cdfcf2e`  
		Last Modified: Thu, 23 Apr 2020 01:51:55 GMT  
		Size: 10.0 MB (10008578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d28a5518079a2ea55f8d7914040ed566f0aeaf677bcab2bccae6721ddb28f3`  
		Last Modified: Thu, 23 Apr 2020 01:52:25 GMT  
		Size: 53.3 MB (53295899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2b49e5645b8569be020c1dc9305c75f8ac834a6108f13c1497e1d37fd2efa2`  
		Last Modified: Thu, 23 Apr 2020 01:53:22 GMT  
		Size: 174.0 MB (173953610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4d075ca0b825dbe9af3ac123cc4f5d91c2d214d386381bceda9f1e49aa43351c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289084510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52936e37461d71fec90993cca439fdabcacf07bedaaec7aa712480719b8cdcac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:05:52 GMT
ADD file:465fed22a1d7f049dd801ccbefcbf7935f5c5f16afe77b6b85ec70d29f68c29a in / 
# Thu, 23 Apr 2020 01:05:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:19:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:22:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb14aff5b9321076d299a3cbc700d0f2230140c74e6d1556733e1f8a03e877e`  
		Last Modified: Thu, 23 Apr 2020 01:13:09 GMT  
		Size: 47.7 MB (47659080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435f19640aaff696311982d6c431b3aaf1673d5f2f94be3106dc7fed67539b3`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 7.3 MB (7257375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27313d2b2136e2d0cc017a27c4974044c01dbfdfd2f863ba921839d87686147e`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 9.7 MB (9672965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1d15e346be4952d2bfeeaa0a5c2b14e01c0f703d6ca46ef995a185e3465efc`  
		Last Modified: Thu, 23 Apr 2020 04:33:06 GMT  
		Size: 51.1 MB (51081545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525fad786105ed6c0292f48b2edf6e912171baa433992054ae3239b0d6bc1b61`  
		Last Modified: Thu, 23 Apr 2020 04:33:59 GMT  
		Size: 173.4 MB (173413545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a2e90405a92b101e95e1f510e6f2b3a39da2736edf626d7002bd350567ab17af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315179161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13cff082563c9a1897f55a6a236da082365b0379b7c51522ab309124aa5c75e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:31 GMT
ADD file:b2be126f717b29a49979e4124d91ab7eaeaa56922ce97a6c9756f621c8481f0e in / 
# Thu, 23 Apr 2020 00:56:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:42:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:42:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 03:43:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:45:16 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03219b383ad9717495dade4e3f10c420901a34fda6c7c20c16cb0b59ba8b1abe`  
		Last Modified: Thu, 23 Apr 2020 01:04:22 GMT  
		Size: 50.9 MB (50909142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9efc7b20fb46ef0217bcfb108d32e426ae9b0759b2456f2dbdcf1d56f70d2c`  
		Last Modified: Thu, 23 Apr 2020 03:53:37 GMT  
		Size: 7.8 MB (7810063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6298cade50a2eb79805724b15c129c5cc4dbd0a1e8d2621695dc69a47c1bd878`  
		Last Modified: Thu, 23 Apr 2020 03:53:20 GMT  
		Size: 10.3 MB (10294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b162a6e57fcc6e342cb664a55902f8a75714fddff53df9d8a834aef9412e59f4`  
		Last Modified: Thu, 23 Apr 2020 03:54:04 GMT  
		Size: 55.8 MB (55803462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3fb865673f72b06a56c55c15f4caff6d0bd415fa16cf65ce7fc4e71a7e5a27`  
		Last Modified: Thu, 23 Apr 2020 03:55:03 GMT  
		Size: 190.4 MB (190362084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd200a5ac6e7a292ec2336b7af6651915b191db1e98b6f7b36f8167ee5bc75c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333047571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc67c1b4f3ebab30b8b4d12454aff8138075e033fe6d3444ff0e13b205c42bf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:06 GMT
ADD file:5651707cdeb4825b44f6e8cca314dc9b453dbc8c9eb87d4235235b6f6065edd9 in / 
# Thu, 23 Apr 2020 00:41:07 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:53:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:53:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:54:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:55:35 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6b90db2302f3b878a7e51a668d323ec00b33326362c4983e10df2b689e081dcc`  
		Last Modified: Thu, 23 Apr 2020 00:46:19 GMT  
		Size: 53.1 MB (53123711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce77e9469d5af64bf3279f4b449bc6a887436148b9e1690295858e67ff72aaa`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 8.1 MB (8112210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea37667c03d37033a105606940d504f39ee410a6c8103822b0079326b905c448`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 10.7 MB (10657220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c990c61d17e4dd94174396267f80a8189c9884fbbc6d7385359954821f14a9c5`  
		Last Modified: Thu, 23 Apr 2020 02:03:06 GMT  
		Size: 57.5 MB (57518480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1df106935fdca673ec5881b5f778998747b460de5e579e937e32d3491fe0d5`  
		Last Modified: Thu, 23 Apr 2020 02:04:03 GMT  
		Size: 203.6 MB (203635950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:423b90971d5764b51c9fe636decb269c2e45e874714d82f7433c4a91cddea2ca
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305442293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac80f327c412886cdab94a82797ab749cd9fb7b464f8ec07af22f338ba4d01a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:00 GMT
ADD file:66d4b8806942796ca49e31a046824a633333dba393126281f5c12e26efea8e7f in / 
# Thu, 23 Apr 2020 00:11:01 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:56:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:56:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:57:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:59:54 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e50f308fab9e31aebf27548f07771af5a99a609ac88a60bbf74cd4f85125c24f`  
		Last Modified: Thu, 23 Apr 2020 00:19:59 GMT  
		Size: 50.7 MB (50696153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81374d42ab3f43b1e9a01bc0af60264f1036fe997a6abb2a98e309bef8774229`  
		Last Modified: Thu, 23 Apr 2020 01:13:33 GMT  
		Size: 7.5 MB (7461350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f82f88069fa53135d2819a8aa2d5e279767bf7aaf186c38c0b84e09717b63d7`  
		Last Modified: Thu, 23 Apr 2020 01:13:34 GMT  
		Size: 10.3 MB (10324460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0a1c2f8318544a7575e0094d5dceea034ae91f430e4404b8d5eec3a37b90`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 54.6 MB (54597573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb19a30e54d6bb44b5f32b5c7fafb5003d9d8c5c53a87c810f9ecccfa4fcead`  
		Last Modified: Thu, 23 Apr 2020 01:16:55 GMT  
		Size: 182.4 MB (182362757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:22ade3070dc18d169774c9a6069282c1fc1a72c6e8e800d19ed8f81d8b0ef947
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342609468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabba05b322d4b7e3cb1d19d359cb775fddcb0018ac738b393d263200a4540fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:45 GMT
ADD file:d55bd2bc22fb060f41d4316af4a741b519580bd2eaf76cbbbf9e3b88355447eb in / 
# Thu, 23 Apr 2020 00:38:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:00:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 02:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:09:54 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1757960a31f3d7e8a61f52b30d276d1605aa71eec0c10f82c131db13d7402512`  
		Last Modified: Thu, 23 Apr 2020 00:52:17 GMT  
		Size: 55.9 MB (55855455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563142de6e877d15e44abd8c25bfd401d3b30ad60789123881110c1b09c3973`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 8.4 MB (8357037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8308c7f5986dc304d470a4bb73bbf6316be522707269361fee59307548cc763`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 11.0 MB (10975930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548c6fd949381bbdfaf54bfbac4ddccdce7a765b0656dee4776b58726b776cc`  
		Last Modified: Thu, 23 Apr 2020 02:26:43 GMT  
		Size: 61.0 MB (61049666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d1d4aae0414120cee0086d5259749f5264fa212ff0a4452bb96693afc134e8`  
		Last Modified: Thu, 23 Apr 2020 02:27:59 GMT  
		Size: 206.4 MB (206371380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:55be1789702e574bea59657db7cc39b450ed431af362f5d5979207d41817b338
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304014053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebc3aa1b0dbbeb98131219c6d3945c1b61979de74967cb85f8e8b526bd44a90`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:32 GMT
ADD file:8af210766ac887956b2d532d05d6f2685732ae449b64cc451bb1892dd0d39fc8 in / 
# Thu, 23 Apr 2020 00:52:35 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:01:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cfdfbea2787f2ac0078069f7f5d3094e3b61cefcec7239ac77ce892b23d101ba`  
		Last Modified: Thu, 23 Apr 2020 00:56:39 GMT  
		Size: 50.6 MB (50581330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13e3ca73b27934f52752169891ab565d3136558697ae5958bb58e05acdcc84`  
		Last Modified: Thu, 23 Apr 2020 02:08:41 GMT  
		Size: 7.6 MB (7601311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf12399d434a43c9b18e6f51ac8d33334d68063a5e80a24b4db1e4a3c589fbe`  
		Last Modified: Thu, 23 Apr 2020 02:08:40 GMT  
		Size: 10.2 MB (10183921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8e5e512c3996df54edcff78ec858912c1ee2a69734a97f7856f6d851b39e1`  
		Last Modified: Thu, 23 Apr 2020 02:08:55 GMT  
		Size: 54.9 MB (54900285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2212bcc29042d1642ff4c7b87ca12e05c3a2887f29f0f4bc915310ca957367`  
		Last Modified: Thu, 23 Apr 2020 02:09:32 GMT  
		Size: 180.7 MB (180747206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
