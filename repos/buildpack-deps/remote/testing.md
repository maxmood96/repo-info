## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:dd7b5593a575b31a1fe713a7a2a69a3fc5fea479b8e3b80ee6cfa315f7810fbc
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
$ docker pull buildpack-deps@sha256:9e78e9bee7fe04fedb342c27f532b5fab0276f8953a07bac2586a9a55c9a6fe4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350793405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c648904f81d3e17dbd2968542a1bf1c2972db04dc0e6f580e4851d52d259fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:59 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Tue, 02 Jul 2024 01:27:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:55:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f3d296dd0e92cd772395160b84eeaffb55fa2ffce846bc61595e5e164a5e3`  
		Last Modified: Tue, 02 Jul 2024 02:03:19 GMT  
		Size: 19.0 MB (19021831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb04f2f4343d6b362ed3e5d55a9e7736eacbe6aaa43d185b2b3e8af75e33528`  
		Last Modified: Tue, 02 Jul 2024 02:03:35 GMT  
		Size: 66.2 MB (66152359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424e4bce86283b449bbc585417aabf91115bd147aab8e173405d02eceb06319`  
		Last Modified: Tue, 02 Jul 2024 02:04:09 GMT  
		Size: 213.2 MB (213161001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:68f3fe41a177c7d97ccd6eb1e7c57ee751e9f89299e54771d91e9c49c19b69ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321391499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad53c907b537f7330f58bd1a20c181c99ca23b2ff4528324bf05edc9446420`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:52 GMT
ADD file:c318229166795e4eb716c1fa6af23bbb2d4ecba024b60f621a291810a3a401d4 in / 
# Tue, 02 Jul 2024 00:49:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:22:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:000d0bc5723ca659fec8fc6ce252cb52307971eb476903fc3b9275de15df06e8`  
		Last Modified: Tue, 02 Jul 2024 00:54:39 GMT  
		Size: 49.5 MB (49521421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736d7cf5b3e3c6cf6b2dca2768e87625a43b941f89b6406ba80bef82b5dcbee3`  
		Last Modified: Tue, 02 Jul 2024 01:25:57 GMT  
		Size: 18.0 MB (17968957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e085c26efcb68cf6283027c6da91a96cdc6853a2e46a54addc7366a9803c4bc`  
		Last Modified: Tue, 02 Jul 2024 01:26:15 GMT  
		Size: 63.9 MB (63876252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08caa244269058bb3c2c824e11018a2904c25932eb88fcb8bce5115e78eef73c`  
		Last Modified: Tue, 02 Jul 2024 01:26:49 GMT  
		Size: 190.0 MB (190024869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f3d9d9671f8520e82078a95482f478378ef88ea7d93febd46c9d3d6d6f549ef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee546cabe4d9197c4e0511a50def79f36eda07544ad409cb1c90a909f563f7a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:43 GMT
ADD file:527e478975b1f859c9421d232809fcdad4ae845a2591655169c3c0cbd9556cb0 in / 
# Tue, 02 Jul 2024 01:01:43 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:31:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e4626e10f2b2fa1f8bd684a19417be06dce44506821e68c986c039ebcf444ea1`  
		Last Modified: Tue, 02 Jul 2024 01:06:18 GMT  
		Size: 47.0 MB (47028058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdca2198e49697301427c37393c92e7e2c23045ee43c3f521b70811fad9baacd`  
		Last Modified: Tue, 02 Jul 2024 01:42:27 GMT  
		Size: 17.4 MB (17362030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53904b9da40d410bed49b2fce148f70c4bb32e0d641635fda45634ed2b643633`  
		Last Modified: Tue, 02 Jul 2024 01:42:47 GMT  
		Size: 61.3 MB (61281024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dd55dbd8cbe28cb7cf88713cbd8c3a56dc59a8bcd92ca452fe90f4428cc25a`  
		Last Modified: Tue, 02 Jul 2024 01:43:20 GMT  
		Size: 177.8 MB (177827916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6946b524587fdfb8804d74ca8c7297cde64dec1c55682cbfd8654cf38fcf8b26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344812580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c228b9102c2cdaf53fb665c93f639497a8378bcfad99bb19f86a8f245fe6937b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b366a841875c380bfef184d661cc1ce4751b4e07e9e2eaaf6d0c55114a91de`  
		Last Modified: Tue, 02 Jul 2024 04:05:03 GMT  
		Size: 207.0 MB (207001748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1682a8553d0b99f2d1cc34123122ad3c14f34ee44fc11dcf9f0f28e081a1c548
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354149550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ab5b556b33ef94cf3f27b8e044f6db68580e6080fef613793c95f80a867d47`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:52 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Tue, 02 Jul 2024 00:40:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:13:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed3a89daa70bb513739a2ade83fc5f0a43a784f37749e2584d3c335224ae6e7`  
		Last Modified: Tue, 02 Jul 2024 01:17:53 GMT  
		Size: 20.0 MB (20029610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3099c8c1942a3e6f5ac57d77a04b1e727414a9f58f935b9f5458db57884654a`  
		Last Modified: Tue, 02 Jul 2024 01:18:14 GMT  
		Size: 67.9 MB (67907106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135c6148e71db34537498ee0ac5384eed4d28a786611943b8d590ea2e1f95b87`  
		Last Modified: Tue, 02 Jul 2024 01:18:58 GMT  
		Size: 212.9 MB (212879658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8b914d983289052a08a5a50fdeac542b02dacb0645b5e9ea16feee19d1825f91
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329807910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cf9235edc2618a642bd7ef1134449f684ad486b752d02419243f89d56c76ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:15 GMT
ADD file:3db649d00cbcab4f80ae59713bc5516d64748afefc7b50d6ec9b17f007a2d82a in / 
# Tue, 02 Jul 2024 01:25:20 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 02:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 02:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f6c6179e3393971283f4159a87b337ff64cbda1886dbd0e30fe99b15d1f2b7ec`  
		Last Modified: Tue, 02 Jul 2024 01:36:31 GMT  
		Size: 51.3 MB (51311657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8992fbd14e1b9fc5fdb381b9396a2ccb1f18397cae60807f219afbcf1579ac7b`  
		Last Modified: Tue, 02 Jul 2024 02:39:15 GMT  
		Size: 19.5 MB (19507340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f227430dafb09eb295efcfc652188f4b6892b99c5ccb986b8e11138216a465e0`  
		Last Modified: Tue, 02 Jul 2024 02:40:05 GMT  
		Size: 65.2 MB (65189673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22347c1c1b43cffd4a3a8f730a5ef788db0f4097177646daac7e730b37229c1`  
		Last Modified: Tue, 02 Jul 2024 02:42:12 GMT  
		Size: 193.8 MB (193799240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59c73a54b77343a1a5253c674a9d01283574f5233bd6a1a8575dee8b9afec913
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362903676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778f9a301430750ef592d35d58e1ba06e803638ec57634ed414f23973db0de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:54 GMT
ADD file:2befd9889f7183dff7c3af514af787c529a360a9bdb089a9e9db6dafcd6001c6 in / 
# Tue, 02 Jul 2024 01:19:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:53:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:56:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1562048ab74aa86e6df4a38c0c8f568200759fc4f56abccc22d1df342f206dab`  
		Last Modified: Tue, 02 Jul 2024 01:25:27 GMT  
		Size: 56.3 MB (56345204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea8d116669b7a9effcef7da51c6a3adb0b03e6013b8bdbdc06106781c822b6`  
		Last Modified: Tue, 02 Jul 2024 02:08:00 GMT  
		Size: 21.0 MB (20982544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf30d890983307c7c405d9221c5b4107daefd6f37bc649fd38c82720f869cfd8`  
		Last Modified: Tue, 02 Jul 2024 02:08:19 GMT  
		Size: 71.7 MB (71714300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5a7454066f16c1883d12ca24fc1270cfd8fad993e0a8cbf12e16984cbc4b4c`  
		Last Modified: Tue, 02 Jul 2024 02:08:57 GMT  
		Size: 213.9 MB (213861628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c1e5c01986e4b69b8622517db8fa892d22bbcc0101b3c8e25a06dd2f783a2c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329040584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffa4584fd171e896630273d9a66152fe5c66b32d9e4f420aed4474737bc9c9d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:46:19 GMT
ADD file:8bed729fdb05f23c2c9685e4b49aca399cccb129d549ff0cd5178ece57a34073 in / 
# Tue, 02 Jul 2024 00:46:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:38:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:38:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:39:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7663a7e6ec84fcce1d022bfe86b7d77ebcf92e841e95456e76280883841e0985`  
		Last Modified: Tue, 02 Jul 2024 00:51:04 GMT  
		Size: 52.1 MB (52089479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb594591801b3f0f0c97b7761fc4001fd8d788cd8eb1fac03442aa5ccbab471`  
		Last Modified: Tue, 02 Jul 2024 03:47:01 GMT  
		Size: 20.2 MB (20208262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71f5b2f892fbc7bbfbf5e24b35413c82ba30845f64c37d9ec5bd2ca8a5cabfc`  
		Last Modified: Tue, 02 Jul 2024 03:47:15 GMT  
		Size: 67.4 MB (67449508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8b44ae9e710d004d1a439e246bfc60eaf1b97ce6c861ae87e0d55a321872d5`  
		Last Modified: Tue, 02 Jul 2024 03:47:43 GMT  
		Size: 189.3 MB (189293335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
