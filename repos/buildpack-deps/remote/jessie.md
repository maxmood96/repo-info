## `buildpack-deps:jessie`

```console
$ docker pull buildpack-deps@sha256:7c9576044137de4017466860f8b545099d93aa95961f9f233670e5d08a712f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5b3206d7dd29c7f8e9991a0b7ae570799da9638565860944bd277efc94afad2c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247166903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96f285a599fc0b6e4ff2ec21dc5dfc6b08a462239f5265714e489dc83032020`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:54 GMT
ADD file:63fdbdcc45a46a993700d252a6f9652db8ab25688daa8bbceaed90b73b2654cf in / 
# Wed, 13 May 2020 21:20:55 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:31:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:34:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bc53e9ecf017dd9c8c8ba0c497d08e2d7c04f4a57dfce491d755cb37613f58a`  
		Last Modified: Wed, 13 May 2020 21:26:59 GMT  
		Size: 54.4 MB (54390659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf82ca715cf8b41a88bfb26ad7225ae77537b5999a2f9a3ed1c430b19bc98d`  
		Last Modified: Wed, 13 May 2020 22:46:29 GMT  
		Size: 17.5 MB (17546015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb3decbe8c76a4818f476de7732333bc00cdb7c3a75887374dd6d6450202e76`  
		Last Modified: Wed, 13 May 2020 22:46:46 GMT  
		Size: 43.3 MB (43334784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2417d595dacc6492feeb4ed843e3148b8eba618781c085dd45c08428b541fe15`  
		Last Modified: Wed, 13 May 2020 22:47:22 GMT  
		Size: 131.9 MB (131895445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c0f0783c755f67ab3aac74f2055ed4c70fb6ced04a7ebe18237617c6e04b783e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227141419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb89db68526c4eccc4f802df0482a450d63deeba918b51a43b7abc851f14e24`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 22:38:25 GMT
ADD file:63b1bfb335518fc40ecfe92c179a8d32d00b3dee86ccf70751c74ed2ca14cd28 in / 
# Thu, 14 May 2020 22:38:30 GMT
CMD ["bash"]
# Fri, 15 May 2020 03:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 03:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 03:48:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 03:51:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ef4eb1ad38349445de10c8a3682121a581770f589f1a35b7cb327b49bb1797d`  
		Last Modified: Thu, 14 May 2020 22:47:16 GMT  
		Size: 52.6 MB (52582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f3d44466578cfe6461e4b482b19224356c7b6537b39780b2e75a727ff8ed7`  
		Last Modified: Fri, 15 May 2020 04:03:29 GMT  
		Size: 17.0 MB (17037233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90476d81b98379937371481027b6bee589dad9dbda48c9b553b41f039ff3dc2b`  
		Last Modified: Fri, 15 May 2020 04:03:50 GMT  
		Size: 41.2 MB (41156510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a687230ff4ed813d6d7dc69cecd5f7ef195919f636b5e1743ef98eb069a89d08`  
		Last Modified: Fri, 15 May 2020 04:04:33 GMT  
		Size: 116.4 MB (116365594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2426b548d8e595475a5137a1937279dbcb46313468af8ca8bde6cc034403bcbb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221426769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f09c5b45e5890212ac7c88289eedae93ec9efe3377e2363c6214a9e904f23f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 01:00:40 GMT
ADD file:a56bb3e7bad583ad3aa641fc5aa4f91db9848e13388179a63b14ab0aa7fe06dc in / 
# Fri, 15 May 2020 01:00:50 GMT
CMD ["bash"]
# Fri, 15 May 2020 10:38:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 10:38:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 10:41:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 10:44:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2cbbcc58403b5ede472aaa750e8ded783a6a7d6c87b217ae8713700515dfd33`  
		Last Modified: Fri, 15 May 2020 01:11:43 GMT  
		Size: 50.3 MB (50304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f880f61061969936f29c8cc4a0b12ac569f2e4d7946b61d7f077d65f13e5c4`  
		Last Modified: Fri, 15 May 2020 10:58:53 GMT  
		Size: 16.7 MB (16723381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6e728b8f32c320336b080a08a6d8fa094c7bf4064a84ebaf331da1fcad49e6`  
		Last Modified: Fri, 15 May 2020 10:59:15 GMT  
		Size: 39.8 MB (39778662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9488e21781d3b3a431127e3e2765ce20365ef80704e63d1a595d34d4bef426a9`  
		Last Modified: Fri, 15 May 2020 10:59:49 GMT  
		Size: 114.6 MB (114619745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:dd280effa6cfa57a21bf405519a58f234bcf761768cce179585c76caa8ee98a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254331320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d980db8dffbb3c054e37c9e2f8d55fa8468b579f0aa9fdc9d22067f9b494102`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 07:08:25 GMT
ADD file:4f7aa7ecb1a9f0f641f4c7dfe0e5360a0705c5e0eb159391b79bec0e4442bc34 in / 
# Fri, 15 May 2020 07:08:26 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:11:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:11:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 17:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:19:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6277e17fa0a21fe6d4617d7259f00c2649972514e9940fbd56cb6d7b75e60de5`  
		Last Modified: Fri, 15 May 2020 07:18:45 GMT  
		Size: 54.6 MB (54608707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5e945f79d261702a2e4dcb64d114abca64e1b6503a3b336cc15a1c68960260`  
		Last Modified: Fri, 15 May 2020 17:27:52 GMT  
		Size: 19.9 MB (19855851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94aa3afebb13160d1fffafda1bc7af540c974a11c0cbc7377a05755342a11ea`  
		Last Modified: Fri, 15 May 2020 17:28:11 GMT  
		Size: 44.0 MB (43991263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82c9338ebc67d958077b5a25e9e7c74a525b8304496f172b786b02333e355ad`  
		Last Modified: Fri, 15 May 2020 17:28:54 GMT  
		Size: 135.9 MB (135875499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
