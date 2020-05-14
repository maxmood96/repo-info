## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:d2ec6dc9b948de942cfbe763efeea73a4f54ac198828032727be49d195615202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

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

### `buildpack-deps:oldoldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:23a94255414b37736b35846f45973596b3a4fe511ff7030ab2162bae827757e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227140177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a3a8012c88873b01c70cc84f0ab7755bb8235c83b516be2e8ca0e62a0ca78f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:50:39 GMT
ADD file:621441e8cf0bd677ecfb646d7c54417894fedb89b8b03295c25a4ea0ebefbaf3 in / 
# Wed, 13 May 2020 21:50:42 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:37:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:39:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:43:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:535d6dc5159c1d8f20f2d1a86a8433d89941a1933de7a6930246eef7811be611`  
		Last Modified: Wed, 13 May 2020 21:59:45 GMT  
		Size: 52.6 MB (52581076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73189ba1a9ac8eb7f3c4a34630c9eacf6ef34fde77675eed4b21857d50d7a3e`  
		Last Modified: Wed, 13 May 2020 22:56:53 GMT  
		Size: 17.0 MB (17037185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd7802ce38e2c324b7cc2c2773a4bdda1c88367f6d1823d6807df3c2d00a9ce`  
		Last Modified: Wed, 13 May 2020 22:57:15 GMT  
		Size: 41.2 MB (41156562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311a88ec1bec506cd1aaa951469b373c436fd1dc83b93cc211bf502370e27bec`  
		Last Modified: Wed, 13 May 2020 22:57:56 GMT  
		Size: 116.4 MB (116365354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:04fd20dbd3be3e6b715d9b3f6fac812be7123fb6ed749ef495755280b633a9c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221424964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5df97c60d4de7d6f8201d927f88759246d1ce12017981b080d861264995161`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:47 GMT
ADD file:348008ec05929291b5465cf2ea0b89cbd08f4eb55d53f50f37727783e36e439d in / 
# Thu, 23 Apr 2020 01:03:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:18:36 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a08cb6362fece7101fb94628a874d1a40b2ffc270a3fcb4fc3f4ed97228fd505`  
		Last Modified: Thu, 23 Apr 2020 01:11:30 GMT  
		Size: 50.3 MB (50304341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4f5614a4faaa521ea475ca54cf68fd7fe337514cb7551af1c9c7d465f0a424`  
		Last Modified: Thu, 23 Apr 2020 04:31:26 GMT  
		Size: 16.7 MB (16723212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad1ef58b6bdf48fa13b037e301a7ff234155531aa1cad2c0a08b46608bfce02`  
		Last Modified: Thu, 23 Apr 2020 04:31:49 GMT  
		Size: 39.8 MB (39777498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd6cfaf8793ffa4b4cc878a7740301e35b0b453902715ea654ae2fd90cecf5`  
		Last Modified: Thu, 23 Apr 2020 04:32:28 GMT  
		Size: 114.6 MB (114619913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:37e257ad391bfda9e2b9c1cc3ad1de95d10a41710c2d0495574b42e152f0cce4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254319055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571714567abb1ee61c79c068726da5313a58d0717ded6c861e82dd29851c6b29`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:50 GMT
ADD file:5a51343ededbfe4c380e189c99b1136cd1143a41ea66cee7cbdc3b9b523ac86a in / 
# Thu, 23 Apr 2020 00:39:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:46:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:53:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46bce17837ebb6f15aa73ef7b5c4ce1f32c9108c2dc291e4af9944c5bb7130e9`  
		Last Modified: Thu, 23 Apr 2020 00:44:51 GMT  
		Size: 54.6 MB (54607867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a64d5974b96b34da72142a0155b10ccf50819700a2fd7d3faf98329ad3808cf`  
		Last Modified: Thu, 23 Apr 2020 02:01:40 GMT  
		Size: 19.9 MB (19855827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18254c800e99a51f674488ec0f9688b8f952adcf63222e9648847baefaef31cb`  
		Last Modified: Thu, 23 Apr 2020 02:01:59 GMT  
		Size: 44.0 MB (43979929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8304a435121ebd2a484bf824296e9ae9942b34be1e7f2b9308896eb343bd74ec`  
		Last Modified: Thu, 23 Apr 2020 02:02:36 GMT  
		Size: 135.9 MB (135875432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
