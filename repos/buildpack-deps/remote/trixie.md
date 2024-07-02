## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:5a785de576c9bfae82a0fb1caa031478b27128d01a877bc65501969405461529
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

### `buildpack-deps:trixie` - linux; amd64

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

### `buildpack-deps:trixie` - linux; arm variant v5

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

### `buildpack-deps:trixie` - linux; arm variant v7

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

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:74e90493e4b88de1d5f4bdab997cf68cff1a4a90235f148c421d9bd75ef85c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369961938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e7bbe62b186251ff6708bbd2dcc44927924de7a0dafbe9acc2dc7efd9d7cc9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:41:36 GMT
ADD file:c7b7f4f414b176b634ecfd58cd24ff7ad3d2b36f1fefaf2139e52ba8948ce751 in / 
# Thu, 13 Jun 2024 00:41:36 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:29:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f5ff74329e5ae53cf8fd13f7790e7a8ad37f71aeaaf9d356f6e2d2b40673d16d`  
		Last Modified: Thu, 13 Jun 2024 00:47:05 GMT  
		Size: 52.5 MB (52514381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8683c80540c7eb50048b740b87fd2cb2b3cbaf60c92b8018d677d09081ecb3`  
		Last Modified: Thu, 13 Jun 2024 01:33:47 GMT  
		Size: 18.8 MB (18770350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03862673682b3f6fb031c4a5c8074c6d011c221416b657d74c8a1da0e35fa431`  
		Last Modified: Thu, 13 Jun 2024 01:34:02 GMT  
		Size: 66.4 MB (66358070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb32f6cc55be585ddde214c0068112a7e2fe0d22795409319c853d4d70757db7`  
		Last Modified: Thu, 13 Jun 2024 01:34:32 GMT  
		Size: 232.3 MB (232319137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

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

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ad1aac1cfe1f223c2faaade63b2d13203e0094ad84931139844a1b5761ad7aca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353544284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20abe834cbfaa60b725d7a3cf66eb712c8c9ed2087e5423a91d24950cc254634`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:26 GMT
ADD file:4f8e64cb73f0bac5394470bb779521bb9b544dd7513205d8a870b13ebce84cf0 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:35:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:82cf140ea060591c60ad59c1c2af2452121c8cf77b184829ed04be1d69b176dd`  
		Last Modified: Thu, 13 Jun 2024 01:29:05 GMT  
		Size: 51.1 MB (51137261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0995f3325cb4fe9538ff2c2cb740572ccf176df40429dcb0b8a22aed9a06214`  
		Last Modified: Thu, 13 Jun 2024 02:46:15 GMT  
		Size: 19.5 MB (19512135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a3cfbc2aeda20ac68a789ca74022fd826e3d1aa98a47c8a0e8597cce2c4e5`  
		Last Modified: Thu, 13 Jun 2024 02:47:06 GMT  
		Size: 65.2 MB (65188152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b4072bf49c5b9814c922ee070e031a3ef3c9b5842f65aa5bd6914e09da72ec`  
		Last Modified: Thu, 13 Jun 2024 02:49:34 GMT  
		Size: 217.7 MB (217706736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

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

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:be3e38956ab5909eae6afd978da0988f62765a6774b8ed0e206a6f79070129b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357992815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bed386af366f018a203bc9e95f65c1c7f097c4f0c5019a5f396d4c1d20661e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:45:25 GMT
ADD file:1021b70eed1c798afb52193fbb22f6cde06dc4de4ba0e601974f25a3ba8db833 in / 
# Thu, 13 Jun 2024 00:45:27 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 05:27:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 05:28:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9bf5f2c747732ad70198f12b8184edafc2dc0d62b3b69d1720a7860e85d2991a`  
		Last Modified: Thu, 13 Jun 2024 00:50:09 GMT  
		Size: 51.9 MB (51895333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881a757b7d6a45c462757e1a28c908e081a0ab80818b81e12a39358e339d17ea`  
		Last Modified: Thu, 13 Jun 2024 05:33:28 GMT  
		Size: 20.2 MB (20215017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b18e0e4b6525d38f743d2ece4445392df8a961ad26cf263c160a824dbc13aa`  
		Last Modified: Thu, 13 Jun 2024 05:33:42 GMT  
		Size: 67.4 MB (67443422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb5b7c634f7b817cf0d2e6b3e8a2d153ad7b4df4aaa0d2ff2b72c69d1a3b71`  
		Last Modified: Thu, 13 Jun 2024 05:34:13 GMT  
		Size: 218.4 MB (218439043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
