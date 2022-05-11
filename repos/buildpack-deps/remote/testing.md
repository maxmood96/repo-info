## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ad7be54e991389c376775939553430927effbe8adad52c17b82b4e3cfccbd5df
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
$ docker pull buildpack-deps@sha256:2da4302f8e87179eaf4f830f5f504a0c25d0a7eca6f9ac8cd2ece53d4a7d19c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335695675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2427f7ff88724fe25ab3304a10a6c209684e3468b0e52881ca68fe0ef38a84d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:19:44 GMT
ADD file:daaac4875b34dee73ff062c17a4763b2cf5726753df4e9700bbcefa0f88153e6 in / 
# Wed, 11 May 2022 01:19:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:47:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:48:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d68396ae84f0ca729923a79943893f43492725d77e7b329170777a2bdbb6752b`  
		Last Modified: Wed, 11 May 2022 01:24:08 GMT  
		Size: 52.9 MB (52944400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f77feabfdca5ac1aeded64e65a1943aee6d39af1ab6f3081de4bdd78eb986f`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 8.0 MB (7999176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ce0f5a715fdcaa40b523d43006725581030728153a1a16199ef5a3097bd43`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 11.3 MB (11264369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834bb0724f857ac407fe281ac6fe1866c2b96d1b631ba15110494e2454e36422`  
		Last Modified: Wed, 11 May 2022 01:56:32 GMT  
		Size: 57.6 MB (57584781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c3c68642aa6787b3219af0b670d32ef9707903308a6f6dcaac8e68374bb515`  
		Last Modified: Wed, 11 May 2022 01:57:06 GMT  
		Size: 205.9 MB (205902949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6e739743d1a206b4ed39725e6aa9067c5b6c2b271e9974ae55fd40a7dd1cc968
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306599333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942f65374532665d4f801d762521f85ed12fe95379b553724d6d131622d08d27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:01:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:05:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cacfec2c73325f6ee9727f3ee99a764a10620c61e467c786773e82fac2589`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 7.5 MB (7536108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a878bece2839158834198a327d030c397685382713b32bee43b9de34889dc`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 10.9 MB (10927476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222936f7ad04c2a63502712adf47f0d5e8415536d3b0815b84016fc8a214d3bc`  
		Last Modified: Wed, 11 May 2022 02:27:43 GMT  
		Size: 55.2 MB (55173746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e6bfd8430c731df5f5e74b96e86f72bed8ce3f757d400f59154c64d456507f`  
		Last Modified: Wed, 11 May 2022 02:29:46 GMT  
		Size: 182.2 MB (182224566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a344cdde065ae2aa0c12074e8c2d7c3a7ee9be98e4392bb33d901311f0e86e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293974582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9665e902c9e1f81bf9cc68189d21f382108b9199fe532b11eb3b7cedd032f17e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:47:29 GMT
ADD file:ae0b1a579333a3c7912430243fe91f71f32d0e234d52667dd937f7cd23a8d3d2 in / 
# Wed, 11 May 2022 01:47:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:18:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:19:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1fdc9e441250146f7b7c78b0264138dc69a0b46d264373157ac1c2cdba7a552d`  
		Last Modified: Wed, 11 May 2022 02:02:37 GMT  
		Size: 48.5 MB (48475916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8d2e8ff6478f1fc3388064baa5d6e059276c7a093a627bc6dc36d79ed4107`  
		Last Modified: Wed, 11 May 2022 03:43:50 GMT  
		Size: 7.3 MB (7269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864281f702c002b286df6a1ef302fe0c7cde6323a4e78ec43b18718d930be2b8`  
		Last Modified: Wed, 11 May 2022 03:43:51 GMT  
		Size: 10.9 MB (10933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f541bea22fba3f321a2207e36d3b3f6d26f89a61dabbd9a1305ed9b9938b15f`  
		Last Modified: Wed, 11 May 2022 03:44:37 GMT  
		Size: 53.2 MB (53179745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f3636c3b2d37b4f8c5433d7bb4f6c441925e423935c03e91cc58399d6b5d0`  
		Last Modified: Wed, 11 May 2022 03:46:25 GMT  
		Size: 174.1 MB (174116001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f7d38375ad352e7f068fb2169e2264bd2d7f8ab47725e0f72dc88f6eaad33666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328408240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bdac2a6d8bcc3f2ba59b99497c5fe61ad61fff418f77cca86775d9e0d8c6da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5de1fe22d36e48b637912dbd432cf236f1d956231296b275af61bc5cc951b1a`  
		Last Modified: Wed, 11 May 2022 01:34:36 GMT  
		Size: 7.9 MB (7853647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f57f959274f20ecbbfac9d0dd7e9dcbbc904e7eaf49a4ff37e3149afcbb2247`  
		Last Modified: Wed, 11 May 2022 01:34:37 GMT  
		Size: 11.0 MB (11041680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ec64d54ab363857036338cc3377146eb8961f5b02e14d7ea1b925353b370d6`  
		Last Modified: Wed, 11 May 2022 01:34:57 GMT  
		Size: 57.6 MB (57605368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b6ae33da6dcd4875f53044d0e67087c5b8c8780fbda31415e9aa49ae4ef707`  
		Last Modified: Wed, 11 May 2022 01:35:33 GMT  
		Size: 199.9 MB (199866202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28fddefa08e0ff60f67e7797ce8c5f7867f97d1e4f86987d5e0a218a04ba45d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338847869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6373d977e35cd78e527accbba2ae9302d024d63c9f9647aff5c0c748bff55ec0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:38:30 GMT
ADD file:ba0a6f659c101ad7b3c77be40e790f4ec4576f59a39c794974d82b28b115788d in / 
# Wed, 11 May 2022 01:38:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca5b88a4b2f0398218cdfea0aee4d6b7cd7ae535feeb27719eb9603a02ef7752`  
		Last Modified: Wed, 11 May 2022 01:45:11 GMT  
		Size: 53.9 MB (53944746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8f042cf42269dcb19e8d0bd96f00d64f1515c06c0da6b2f1a0038169d0b453`  
		Last Modified: Wed, 11 May 2022 02:20:32 GMT  
		Size: 8.2 MB (8177691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fbb27fa740e35a981b580f8380ae286a64f2544917232dc1ff6abfccce82f6`  
		Last Modified: Wed, 11 May 2022 02:20:33 GMT  
		Size: 11.5 MB (11464314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47059d7a37d27a501ce3009fd0ce0c77b5b64735265702aaeb59335caa402c22`  
		Last Modified: Wed, 11 May 2022 02:20:55 GMT  
		Size: 59.0 MB (58990642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c02e9bbf771696ab6adb07d8530728551ef86c3160c71b3fea33525455629b4`  
		Last Modified: Wed, 11 May 2022 02:21:30 GMT  
		Size: 206.3 MB (206270476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7ba443454a045816d97f920cb8d87884b6208cddbec925869db530cd5feaed5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316230340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5355444ef1714761cf9155ae5cc31dd7a6a1df9671fb56de23e8cd9a4a47eda`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:21:42 GMT
ADD file:023ba5f785e781bda7875c3b4c2f163666fe7b1a6a0fde74103b7799380a55c3 in / 
# Wed, 11 May 2022 02:21:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:01:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:07:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1315838dc3fae911b53ad8b9fdb88cdc4a2988e4a4924922837b71b52b18d1fa`  
		Last Modified: Wed, 11 May 2022 02:31:44 GMT  
		Size: 52.1 MB (52066926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2722654f4b60f68f8cf6d835f62f8bbadd36e2eae5b31ec1b4cd273785fa9368`  
		Last Modified: Wed, 11 May 2022 03:34:01 GMT  
		Size: 7.5 MB (7508574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4489d5ecab6698b42b344d5e72df6f74ea21c3b4a125cdee3c103f8e742b642`  
		Last Modified: Wed, 11 May 2022 03:34:02 GMT  
		Size: 11.2 MB (11158255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91735533194b8e27b334d10d7d19e1b7008ace8c9d32869cdf24a530fcd6226`  
		Last Modified: Wed, 11 May 2022 03:34:50 GMT  
		Size: 56.3 MB (56312831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6cbb89a89dfb1e54a0b235527af48ad008828a8fc4aa744e4e43e66682a5dd`  
		Last Modified: Wed, 11 May 2022 03:36:58 GMT  
		Size: 189.2 MB (189183754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6599608ef6e2e32b7ec9910c96d3bbc69ead68cbf9a0f3a35510da1cc55024b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (345974647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16074f3e37a74863a4a40f9cd66a029aafda44a143159d7681b2dd657c456c8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:11:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:27:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac162b59dc7eb516878ceab4828d006f42ec802f1755cbd5bc3126bf8d03c9e`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 8.5 MB (8496430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4172550a38e5e5676e20f279186dcd1ebf123a9b2693d032e98814590d62a`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 12.1 MB (12065559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b1c75bb53e1b4ca0c91d2d1a0d8344e323b723c6a10f2b51bb99bb0cd6f948`  
		Last Modified: Wed, 11 May 2022 03:46:59 GMT  
		Size: 62.3 MB (62308040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65815a6849cdba46fa1750a43dbdaabab9f89a778d6499516a1645b7bd9838f8`  
		Last Modified: Wed, 11 May 2022 03:47:47 GMT  
		Size: 206.0 MB (205954177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60cc21c2fd32bf95ee5051d92eba65ad817a56076f35ec06e69201a0ff6d40ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307699325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc4bc15eed8928c98394c35f3b4eb4bacd40f57e62cf4e7bdb1ebb50704aff8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:43:27 GMT
ADD file:d38e77e014746a6349342f7d1cb5eada86f6e06423bf095efa6f182b4d038b77 in / 
# Wed, 11 May 2022 00:43:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:13:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:13:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3467d807091357239fe13d54d3572c25afe85ac06c182eba9268af6bac8f48a`  
		Last Modified: Wed, 11 May 2022 00:49:13 GMT  
		Size: 51.5 MB (51483972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100136ea0fb238c9c9013ef4e514f31fc2bf960000bae26e543ca80d01ae2e12`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 7.7 MB (7662307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d34880cfc5b88a3b84c6d27165e8e6e19b4a2668efdb3f9e2b27a5422d12f2`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 11.2 MB (11157530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841cf490c32295ead18a8dee0de5c5b2a8c16ae6170f41a3f6b9686186269c5b`  
		Last Modified: Wed, 11 May 2022 01:24:06 GMT  
		Size: 56.9 MB (56890853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84f8d60216724ddfcd9a8b6600febaf9e245fe4fb5b95eb4c8b096f66f7da34`  
		Last Modified: Wed, 11 May 2022 01:24:34 GMT  
		Size: 180.5 MB (180504663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
