## `buildpack-deps:stretch`

```console
$ docker pull buildpack-deps@sha256:13c01d41bd120ee6643d8c00f3c140881fc809db3048ca3f132de323842ec109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d674ce1fe7dce418d8594379fbe9b3b6ee528406c390a05d9c50a87d6ab948c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324892936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26adf75c8dfac192f51e567266ad6d2d162ece817e169f55d78ba8511b3b8c43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:43 GMT
ADD file:c3a852d22b3aac160ba028af69d56b491a2a9419f32a459c4b9b2cbd9129c004 in / 
# Fri, 11 Dec 2020 02:08:43 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:40:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:40:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 20:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:42:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22f9b9782fc328ea8192a309b7517c33b1c786697804153ed52a03005919f659`  
		Last Modified: Fri, 11 Dec 2020 02:15:19 GMT  
		Size: 45.4 MB (45377606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75c9e56a8a6e63c485833c91ac3df1d2a9ef0e467971466d7bec9cf88990c8`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 10.8 MB (10752431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d19b99daaa41c283a63436fb7d49eeb1ee5d47314d9786274bf93edb95050`  
		Last Modified: Fri, 11 Dec 2020 20:47:03 GMT  
		Size: 4.3 MB (4340681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e000cbf49b08c6f2538b371f5343011525002d32fd2fe3de07162fab67d59389`  
		Last Modified: Fri, 11 Dec 2020 20:47:22 GMT  
		Size: 50.1 MB (50111650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892def1a6f88c9c733b6d55d7f8980ca9e8ac0438a10a7219462b92fb6a7f673`  
		Last Modified: Fri, 11 Dec 2020 20:48:25 GMT  
		Size: 214.3 MB (214310568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:dcfd26b66c58ac30312bbf39642b15bda20c09d4cc29613853ca8f16fffe4a34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308859407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde1a02e998866c2ab8d8911a149dd56bce3aabdca1923af93aa7084daa115b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:23 GMT
ADD file:ecf2c81fa53759cae3e17b1b743a884b747d5d2b2676bb7f14bdb4fb1a5cb38c in / 
# Fri, 11 Dec 2020 02:09:35 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 02:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:04:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 02:05:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:09:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74944684cd609943dde5912069d99b50bdb10f0cbca3bc5f96b0b17fc41f8c18`  
		Last Modified: Fri, 11 Dec 2020 02:18:35 GMT  
		Size: 44.1 MB (44089598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf108950f8cc0ac18c401de2c89700c6c85e5dbc0c26c5ce342f6c95ff25836`  
		Last Modified: Thu, 17 Dec 2020 02:19:47 GMT  
		Size: 9.8 MB (9826001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a99d9fc9fe43ac9269dfdead78116e5999565777dfdb0b7b81c65e41a9099`  
		Last Modified: Thu, 17 Dec 2020 02:19:45 GMT  
		Size: 4.2 MB (4160232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d74acb84f3335fb8c0613cfd426165e4a3a73cb6caed85e9b501dc02f762a`  
		Last Modified: Thu, 17 Dec 2020 02:20:21 GMT  
		Size: 48.3 MB (48302433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258f54e91e691245b73fb3527c8931ea0e757d1f0b518d1e24e7e8454f338469`  
		Last Modified: Thu, 17 Dec 2020 02:21:50 GMT  
		Size: 202.5 MB (202481143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cb8da4c6edd0cb069cd077789a56c585ff8bdd755ee0ec0f37197b5a5ba9e7a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296882426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa569da3ede16c46afa9453ab4963c890526d8186c14f53450153ad902f5026d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:06 GMT
ADD file:e74dce76704e3faa6198db5cf4192fd431f5addf55f658277eb5b60d254fee8e in / 
# Fri, 11 Dec 2020 02:28:09 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:24:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:25:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:28:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:062f5403576d7e3aca1c92115ff0a9ea110b270cb0b61013efa86744515666fb`  
		Last Modified: Fri, 11 Dec 2020 02:36:48 GMT  
		Size: 42.1 MB (42117949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913e3a9a9e04d7e4fdefdcc5847233d712c26520bf9484ed8e890f521f2bbf41`  
		Last Modified: Thu, 17 Dec 2020 08:56:01 GMT  
		Size: 9.4 MB (9445217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d26373a692630f7276d1b4be2fc66079b5d68123d5ddc98490cc9a4d0775a31`  
		Last Modified: Thu, 17 Dec 2020 08:56:00 GMT  
		Size: 3.9 MB (3919961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba1289ccfa23ce645ca9f7bef0aac996b4b533a1000c91c4381b871283895cf`  
		Last Modified: Thu, 17 Dec 2020 08:56:26 GMT  
		Size: 46.4 MB (46412967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96e9970b264894dad36f964f11861bc65febcb7ac6b1886134441118d6eabc3`  
		Last Modified: Thu, 17 Dec 2020 08:57:25 GMT  
		Size: 195.0 MB (194986332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:957b59da53d81108025a4a2b63e9a986efcc74f6ed0fdae1cc27b08977f54c1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306694156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0597b284601f123aa1088c08b4e861fc6facbe571bd11bbb6ae4ddaf47d85c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:16 GMT
ADD file:48e44714f486662ed380343e556f0f7411bd6600d916440063753c55d1f94b45 in / 
# Fri, 11 Dec 2020 02:48:17 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:00:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:00:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 11 Dec 2020 19:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:03:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ecefb91918e846819df74a1beb8e41f454bef156738373818c20656a3a46d5f7`  
		Last Modified: Fri, 11 Dec 2020 02:55:36 GMT  
		Size: 43.2 MB (43175941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc4aa0f5cdb9142c6a132303c43a6ac4227b4756b3f431c9e48499eb9a2904`  
		Last Modified: Fri, 11 Dec 2020 19:11:05 GMT  
		Size: 9.7 MB (9702496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8454d6fa6606ece6f85f95e9fbe351549d84085e6084902e37c0514065cead`  
		Last Modified: Fri, 11 Dec 2020 19:11:03 GMT  
		Size: 4.1 MB (4095435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebe590c369a1a395ba51ee706dfa93cc52ade1aa7b62748986b1fc94d080bec`  
		Last Modified: Fri, 11 Dec 2020 19:11:26 GMT  
		Size: 48.0 MB (48042787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a402bd8b8d9544c8078e7139afcfc063ffe4162ac0a6b94ccfba7ea1fdc23b`  
		Last Modified: Fri, 11 Dec 2020 19:12:24 GMT  
		Size: 201.7 MB (201677497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8bb80aeee1cd853f8e61927260cdd058d86fb014fd5ffe702d1eddeeb7584a7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332422539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a83e4efa81a4846c41f0941996fcee9c4f417555b953bbcd566bb54b538ed1f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:38 GMT
ADD file:65da710638e196cb40b07b1d2461114bb3c8b34d69693449a905397c192f1ac0 in / 
# Fri, 11 Dec 2020 02:05:38 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:12:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:14:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c6c30bba175680710c6b02f65235cc2a0b8adf1ec4be1e440e260afda9487b37`  
		Last Modified: Fri, 11 Dec 2020 02:13:22 GMT  
		Size: 46.1 MB (46095117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc0247c6906d18f48f42d4ecdf060009453e884a50dba3d3b52166e5bd61ded`  
		Last Modified: Thu, 17 Dec 2020 08:29:18 GMT  
		Size: 10.8 MB (10774964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bcca64ffc98da2fb811c456d5ab074caf61174cb723eb8429a5e4ade473a4`  
		Last Modified: Thu, 17 Dec 2020 08:29:15 GMT  
		Size: 4.6 MB (4563306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2949e32cf476c215c8b8ec60ce8dfdf335001f253da3619f69e3bbc6566ade`  
		Last Modified: Thu, 17 Dec 2020 08:29:43 GMT  
		Size: 51.6 MB (51627576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7463ee01b6607324ef2227af6392ae45c0aa41cc1c6a67e9d2f18a78e29916e0`  
		Last Modified: Thu, 17 Dec 2020 08:30:49 GMT  
		Size: 219.4 MB (219361576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
