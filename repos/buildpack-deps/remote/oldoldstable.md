## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:fe9b9f579e29902a32ece1614ef54f0efe5118b49d8393f5cd92e079621bbcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a7ecd23fa1383a83fd76bf8a48eed664276277fa069c0585b15833f4ddfe2ca8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247182634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d4bfde0862ea4a7190825a330ada775fe009f40966b7f2ee7581388dbaed6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:57 GMT
ADD file:c7289562291bdeb61e0423cc6f7c93e71f1db0631093278de35bccc99ac0137d in / 
# Wed, 22 Jul 2020 02:03:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:09:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e58952790bdd9e11086d30293a8de4ff1b9960b3ef414cfb7cfe6283010d156c`  
		Last Modified: Wed, 22 Jul 2020 02:10:14 GMT  
		Size: 54.4 MB (54388443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2ff14f8a79fc9f0751ebbf0b42f16b01a3167518a5c32a36f03e616a037af0`  
		Last Modified: Wed, 22 Jul 2020 03:17:30 GMT  
		Size: 17.5 MB (17545946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c48eb095f4e23bc343acb9f93e42c07047a4cd3b842658d4d0ca5bd0c1c4d9`  
		Last Modified: Wed, 22 Jul 2020 03:17:50 GMT  
		Size: 43.3 MB (43334743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3fddfd374f576d2b7b6b91b648ecfa877d13a91cde02479305bdf424c2d64d`  
		Last Modified: Wed, 22 Jul 2020 03:18:18 GMT  
		Size: 131.9 MB (131913502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a624959cc52ae2eb4fe4805e4cd8bc3040d635746ba67f37fde50a515bce39bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227152675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab5a85563d9aff42c6a37a9e2363235345c3411b298bfe75bf01ef202d05317`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:26 GMT
ADD file:fc4891c90bebbee0aba9f67d9b8de47f8693ed50bef201731e9894f6297b31d5 in / 
# Wed, 22 Jul 2020 00:51:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:38:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:39:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:41:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:45:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:739cbc68f8a36404ed5c151d6fe7ca27af395e77aba90dda62da8da449501169`  
		Last Modified: Wed, 22 Jul 2020 00:59:18 GMT  
		Size: 52.6 MB (52582500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e34a1145258f8f0479492b494469d6e62e97a0c95c4c5f071a1080a195d541d`  
		Last Modified: Wed, 22 Jul 2020 02:05:03 GMT  
		Size: 17.0 MB (17037398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad717891ba03cf69d6968c2c424c6d36a6584d6864f20ee1add1e2ca1e9027e`  
		Last Modified: Wed, 22 Jul 2020 02:05:26 GMT  
		Size: 41.2 MB (41155622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09ca5b1405767096dfdaa11b47d37ab199aa7dc600b5756e439315816a4a305`  
		Last Modified: Wed, 22 Jul 2020 02:06:07 GMT  
		Size: 116.4 MB (116377155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e37784d9f93c127385b5af7e4cff01eb72b16fd0080488882f8c0ae981ee32da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221441303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4ab712c900fd80b109ba26807e787d870e698c68a589d98020a112f0af7885`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:20:52 GMT
ADD file:fc97a5157392072f2e584533bc20a7c8565d3ab25811c37aa8b0be0d2772d001 in / 
# Wed, 22 Jul 2020 01:21:05 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:34:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:36:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:42:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23856a2fcb20620043f7afa719e5733743f2f68b019438dea4617813e12db79c`  
		Last Modified: Wed, 22 Jul 2020 01:40:57 GMT  
		Size: 50.3 MB (50305246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71e2d521b630caaa42f6e89b0fcbe65a9c6841a05078ba147410ee43faf4e9a`  
		Last Modified: Wed, 22 Jul 2020 06:03:43 GMT  
		Size: 16.7 MB (16723465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431287079b9de87676113f46b63c388b0863d730e7c35fb4947ce0fe35e26392`  
		Last Modified: Wed, 22 Jul 2020 06:04:06 GMT  
		Size: 39.8 MB (39779419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1272fbe8554eb128718785fd264cb6831a2792db00334eaa790f87706cd8b547`  
		Last Modified: Wed, 22 Jul 2020 06:04:44 GMT  
		Size: 114.6 MB (114633173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3415dca64dff8fe9d00005626ca09e47f88339f06960d11d8c8de621d3fa5509
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254341870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c3a99380d99a5cb1b21a2ed3fc71327dcbbb4a1e60c74240d5ac2dc0c0d7d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:09:33 GMT
ADD file:7daf3f651c76cffc9df8609ab9c201a868bb0b25716eb7d7cf929b036d05b8a6 in / 
# Wed, 22 Jul 2020 02:09:34 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:24:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:24:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:32:05 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00b5abd6cd880905c210361dac76afbea3e74aef0d203bba4e663196cdbb89e0`  
		Last Modified: Wed, 22 Jul 2020 02:16:06 GMT  
		Size: 54.6 MB (54608798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336722d46e9c737ab1215cf606a080c9c4c07c1c16635127f97d8d3b2f534dfa`  
		Last Modified: Wed, 22 Jul 2020 03:41:55 GMT  
		Size: 19.9 MB (19855800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf8f09aad23c87f45388cc1b2f254074664c3aff8780c5bd8d558ef63a8ff54`  
		Last Modified: Wed, 22 Jul 2020 03:42:22 GMT  
		Size: 44.0 MB (43990549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010215baa526af940842025e0c883e5b17ae670a9bad1b519c07fb07de96aa6a`  
		Last Modified: Wed, 22 Jul 2020 03:43:21 GMT  
		Size: 135.9 MB (135886723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
