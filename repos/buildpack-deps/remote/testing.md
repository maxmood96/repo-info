## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:21284940c2374059cb30efa7b4197d3f4db6cd7325d66d4f5ea1ba2460906fb2
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
$ docker pull buildpack-deps@sha256:2e0df549474cde4893562be6627df41a95fd13695938a1305036a9e592080402
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365317086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99399255020f608381fbb243b8de7cc3f3d6f522ffab1eeb144a4afc3acb4205`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:32:39 GMT
ADD file:ed4581bde732d71193f12e8501c7543059ca0c0c5f15f40c1028474d77fb7400 in / 
# Wed, 04 Sep 2024 22:32:39 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:59:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:00:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2896aaf66dc1af0c9c081d65bb8e63535523af07f049f294d89f549ce0b8febd`  
		Last Modified: Wed, 04 Sep 2024 22:37:07 GMT  
		Size: 53.2 MB (53152948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255717a28b33d59d6a3dede8a111d2d33c43202f627134e76b25cfadeb555a5`  
		Last Modified: Wed, 04 Sep 2024 23:04:13 GMT  
		Size: 20.5 MB (20489923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da4176ccfc0b61583df03b9466a003ee06066c08fa17db7930744efc514570`  
		Last Modified: Wed, 04 Sep 2024 23:04:30 GMT  
		Size: 66.2 MB (66217850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22db95340ceebc1ccc73cd678fb695dbe369c7b73e767635573b134360781e5`  
		Last Modified: Wed, 04 Sep 2024 23:05:04 GMT  
		Size: 225.5 MB (225456365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:372f3e5f923b3c9277d390fe4e250d110f3b11b156b8f867e26a53b8d16e22b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328384281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945d8c80524783749b323d4b3de423ca771a4cbf28f1bd12015f8d25a9c128fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:29:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e1ca7e0ec63179505bc4d7b369ec98cb8968fcebcdb5cc723a2d9011e899`  
		Last Modified: Tue, 13 Aug 2024 01:33:03 GMT  
		Size: 19.4 MB (19440857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24383425ce336421fbfcfd0e62dfaba17636c030330599590ab7b5d8e4e149af`  
		Last Modified: Tue, 13 Aug 2024 01:33:22 GMT  
		Size: 63.0 MB (63001460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f582246bcb8be76eb91cfe4ce1a465ccf5994c61db67417139e45c601e3c77`  
		Last Modified: Tue, 13 Aug 2024 01:33:56 GMT  
		Size: 196.1 MB (196070350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d3d119cda38974d83c93ecf47180a360ff6120909f8405cfe2a0cbadc2d35e85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315485099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c7471066cf547315214b5bf0bb4212a6b639793d45c16dbccc66cd51c85ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:58 GMT
ADD file:09cac9d3912a7a93696c655d21effc386d2cb7ff21832c28ce416cd006e647f3 in / 
# Wed, 04 Sep 2024 21:59:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:35:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b4fae8e82872ebbe80a6660f7c8967b490f12720a699b611d1fc451d460e9c10`  
		Last Modified: Wed, 04 Sep 2024 22:04:53 GMT  
		Size: 47.6 MB (47600373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b91a055644a3da6d54b9d0ed225b45a08441e0d542e888bf06f6da6a265c059`  
		Last Modified: Wed, 04 Sep 2024 22:39:19 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1cd9b83eb6a11fc2bfd0f145ae9fc8ee9f0d5564e3b28a008f43b172b63a83`  
		Last Modified: Wed, 04 Sep 2024 22:39:38 GMT  
		Size: 61.2 MB (61150667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017488a8ae5b0d46810348f43cbf30520604b3a267121b90af6e524919714e05`  
		Last Modified: Wed, 04 Sep 2024 22:40:10 GMT  
		Size: 187.9 MB (187900232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c99ec2fa97aa47a20c15cf639b779ebb08cb6e5f056db4b4276cac8a1db4f39b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359147411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61207ab7b0b70524f64b4fbb024945fb60a7cb06b97c05fc54b41b863a36a30b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:41:11 GMT
ADD file:0d3579de5c93cf19bff9f7634a0a159ccc6f879b5b3b127688adfdb71440fc3a in / 
# Wed, 04 Sep 2024 21:41:12 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:07:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6df7e1b9cec91c022805e35821c4d6cf9ec8f98fd36df834cd2b60410faffd11`  
		Last Modified: Wed, 04 Sep 2024 21:45:14 GMT  
		Size: 53.6 MB (53594338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3d236efb8ab77adb7cfeaa0b050d56eeb60763492d44b452ca5124c4dc3e14`  
		Last Modified: Wed, 04 Sep 2024 22:10:41 GMT  
		Size: 20.2 MB (20234813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65145a9285af4b5bbebcc4c38c65635bf19540a153981b2e047fbfcce92216d`  
		Last Modified: Wed, 04 Sep 2024 22:10:56 GMT  
		Size: 66.2 MB (66237440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0622095ce10919ff1fbf55116995eedcefb2cf63a53958394e3cbff13298e3df`  
		Last Modified: Wed, 04 Sep 2024 22:11:23 GMT  
		Size: 219.1 MB (219080820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb8bff1d818def7a2f22ea0f49a8685fa94b9917603df0642628116b1a30c508
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363874327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70deb4dfacb021a563799df9a83678c946ed3a56efb8cb6244b5b2d6af11605e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee207a11e4a6de69d2bf4707298d7d6291e3b054d299d2964e51c9aef6ee01e`  
		Last Modified: Tue, 13 Aug 2024 01:18:43 GMT  
		Size: 221.5 MB (221526932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dd86ea6c1ac9d97509fc8c6cef961e973a70cf96f7c6565f728f0ea3a5a6ef38
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336783254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aaaba46df956f56bf02443e502c95ff15056e15d393234240249863a0a8fcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:30:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc5979bb9a19cf877f4c704e0c836440a8fb779e7dc36bf701723c94696438e`  
		Last Modified: Tue, 13 Aug 2024 01:41:12 GMT  
		Size: 20.7 MB (20734134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdca8b68360b0ebfce94a5c7ac25e6db987b2b2549ef1754ae12e7585a9c801`  
		Last Modified: Tue, 13 Aug 2024 01:42:04 GMT  
		Size: 64.2 MB (64197669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c951d6341f7b059bae3179565d39537533ee9d1986dfece9e6cb00b078c7baf`  
		Last Modified: Tue, 13 Aug 2024 01:44:19 GMT  
		Size: 200.1 MB (200133839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4aca54aec2a39581f95720c64add62fc87f05385a0f0d8289d642c7dca305951
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369591381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34508033db8d878c42ea36ae34d2f22f18d7f9d8695b72677885ce12e9a19cdb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:33:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beceed51fa25589c06ddeea2d1cf90183fe7061b5f0c746fde5c8782f8e623c`  
		Last Modified: Tue, 13 Aug 2024 01:38:19 GMT  
		Size: 23.1 MB (23082335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29987d85cabed87e33bd1473f10a5dec4eb0ac635560351ca53022c9a377d1b8`  
		Last Modified: Tue, 13 Aug 2024 01:38:38 GMT  
		Size: 70.7 MB (70650978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76965f731d3de981bcbaeb56b632d6f3eb13dd717e940d77f4cb915c60811d`  
		Last Modified: Tue, 13 Aug 2024 01:39:17 GMT  
		Size: 219.1 MB (219082484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ea10cfbc99a625868cf640c06034bf2c011a3e5265f907af2a182e868de2286
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334655383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96cc6e5e18b227d264f00ed7829ee6a12fe76afdbcee2660ab8338bfcf3e309`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef15ecd64bb80ffd29cdce30241b3a9b2dda360fd5c66fc2caee9b085278bea5`  
		Last Modified: Tue, 13 Aug 2024 01:27:05 GMT  
		Size: 21.5 MB (21533227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826f762934c1c39d2dca0d862589e99bc991c7536f69a6e4b21f744a0b7f131e`  
		Last Modified: Tue, 13 Aug 2024 01:27:20 GMT  
		Size: 66.4 MB (66449875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918a9be05d4e4860cc8177bb1e67262cc77b9ba0bc6a1bebfca990da01c64d5`  
		Last Modified: Tue, 13 Aug 2024 01:27:47 GMT  
		Size: 194.2 MB (194191367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
