## `spiped:alpine`

```console
$ docker pull spiped@sha256:e1b7c497848f6c414b718267c003c183a28c1d2d7bafd57382329cf3703f5a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:b30ffb11062d050f5e82aaf7d78c68bfba0145bcaf9d552e60e5d4a1ff989f01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5080918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22627799e7a16dc63c4a87f5a10aab25a0208b38b355991ec5c1746ba6e307f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:22:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 04:22:08 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 04:22:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 04:22:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 04:22:19 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 04:22:19 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 04:22:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 04:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 04:22:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7009e83c06c17eb996625171bf08b8b88dfc800b7110240cee783b8df3bdab`  
		Last Modified: Thu, 15 Jun 2023 04:22:35 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968c07669fd5c8684973e30777b3d7aa561332751af2fbaa4d903a96942787f`  
		Last Modified: Thu, 15 Jun 2023 04:22:36 GMT  
		Size: 1.5 MB (1483166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34038a914a6100cd46d4fc4ba06b2406f05cb528f07affe5cf1d0bcc3f012e`  
		Last Modified: Thu, 15 Jun 2023 04:22:35 GMT  
		Size: 221.3 KB (221304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3bb3dbe0ec4d1442cc10f5a9d0dfc971ced50a1b024748a0441f7717259a62`  
		Last Modified: Thu, 15 Jun 2023 04:22:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865d54f1b59ecbcdd28db4a8ed51db52bced0b9103c08b4e3bd60d9ab5092ea`  
		Last Modified: Thu, 15 Jun 2023 04:22:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:06db8f6e615702076a78b5544ab4972b3d852851a43606bcff093be29bae66a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acff564be060667f5e783e1a68645d35ad3986c948318d77a247b6669f8e22d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:21:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 06:21:34 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 06:21:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 06:21:43 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 06:21:43 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 06:21:43 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 06:21:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 06:21:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:21:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db263a5aca0de0797095f3bd22056067e9842fc931f78f7ae95d38a25236c185`  
		Last Modified: Thu, 15 Jun 2023 06:21:55 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec31a87286e0f4dd73f465a80b19111ac981d83ea1469375bd2531510958a9b9`  
		Last Modified: Thu, 15 Jun 2023 06:21:55 GMT  
		Size: 1.2 MB (1239671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cdb69483917a1a97a1e4517bf749631474cd4947b581bf545fc8ec922d82e3`  
		Last Modified: Thu, 15 Jun 2023 06:21:55 GMT  
		Size: 206.4 KB (206394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ffc82f232844968ce89b84e87c160a076403e5187688166db3012478b0ee8f`  
		Last Modified: Thu, 15 Jun 2023 06:21:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b99c8d7cfe4e601948b514fd305b8847633003b25cef4243a97e5e6349e033c`  
		Last Modified: Thu, 15 Jun 2023 06:21:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:69eaa2a0c21e8170650365f7d40d3a7c233b81d7661ece405dcca3b032e1bb77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7dde6285f1cdcbb4a49836abd7fa495595c255ae308325befc9aaee20f12ce9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:20 GMT
ADD file:5e92075a8d9a5898d661caf9c2be8a83fb25742251b4ebdc0c3d448a6dc58e4a in / 
# Wed, 14 Jun 2023 22:36:20 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:40:23 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 05:40:25 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 05:40:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 05:40:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 05:40:33 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 05:40:33 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 05:40:33 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 05:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 05:40:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f929d112168394cf1fbe294a86fbe5173dd92df4daac8cb09437b17dfc5df802`  
		Last Modified: Wed, 14 Jun 2023 22:37:01 GMT  
		Size: 2.9 MB (2868554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37196072c4a2a985d715b1ad2657cf1978ca9533fc1e523c12b328715e0b45d5`  
		Last Modified: Thu, 15 Jun 2023 05:40:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee5c46b5d561cfca9315d84fc298ad4d230bdc1a7cf8bd49a1249df54078185`  
		Last Modified: Thu, 15 Jun 2023 05:40:45 GMT  
		Size: 1.2 MB (1166836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf9facf339fdeab9ce293f598a0921e55287c3b97644313fe1f8cc691a0eda`  
		Last Modified: Thu, 15 Jun 2023 05:40:45 GMT  
		Size: 200.1 KB (200145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f49e7526be5915de8b82401cadb9a075e97c38dc51550ef1b5d3377544cb685`  
		Last Modified: Thu, 15 Jun 2023 05:40:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c7d118f25d5783b96754c98b6ec37c70b99f774f36ebf6beecdf0db3bfd9e0`  
		Last Modified: Thu, 15 Jun 2023 05:40:45 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:57c39b5750e18a31bff98637650ea090af4ebc2d29f321aeaf965038c4e2a11c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4841122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394fb835324ff4abcf12b18a1d05aa12b83540c07cc3241c429d63e413d753f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 07:08:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 07:08:12 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 07:08:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 07:08:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 07:08:20 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 07:08:20 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 07:08:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 07:08:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 07:08:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6ff8e6bcf8348815f9192563a0933c7bc36aa5d93a52b5258a1a07b53b55f0`  
		Last Modified: Thu, 15 Jun 2023 07:08:31 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f248e544999c4dd4330d208a807fcd37535d8118fd64bcca8b650bd19e40426f`  
		Last Modified: Thu, 15 Jun 2023 07:08:32 GMT  
		Size: 1.4 MB (1362530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b1e61b9ecdab1e8cdd80bf9885ebfaaf129ac359a883b68cf2b4dfb4eeeb56`  
		Last Modified: Thu, 15 Jun 2023 07:08:32 GMT  
		Size: 215.7 KB (215717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa66ada810775bdb91cc1b2e9a36c42109d101de16f2e51bd1cf29a3e818690`  
		Last Modified: Thu, 15 Jun 2023 07:08:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be54027b5c58467b7d758c1d7fc00b3569858d0fa4f8762f9a0097939e0218f1`  
		Last Modified: Thu, 15 Jun 2023 07:08:31 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:a0ef5e3831fe6edff2cbb0e86a938d1221c7cb3722165a2d84a75bb80c331700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bda906f8180f69c7a88e6bb9dd0306173696c2dfdb7ea927ee728006fc8806`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:19:23 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 06:19:25 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 06:19:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 06:19:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 06:19:36 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 06:19:36 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 06:19:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 06:19:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 06:19:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6dc9f335c57afbc7b1e16495708b766aea73dd4a701c48f8224c9969059fe6`  
		Last Modified: Thu, 15 Jun 2023 06:19:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173a46948db93064f235acd48f05a36d8367fddd933d24bd195f318e84c8e88`  
		Last Modified: Thu, 15 Jun 2023 06:19:50 GMT  
		Size: 1.5 MB (1485192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bf49c77ef03f39d9e293ebf197f230f3d09bd0dbcb18574059bfaa8a4e1023`  
		Last Modified: Thu, 15 Jun 2023 06:19:46 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31434ea8ac7b673d5a898062b978fcf0b4eee889fe01aa4cdfc06a430063672d`  
		Last Modified: Thu, 15 Jun 2023 06:19:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bb416f535d69f288a9157a121afd70395a1694248283a278a68424ad083d83`  
		Last Modified: Thu, 15 Jun 2023 06:19:46 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:07ecd79bdc7a73cc105de98257e8352a6bbc78539c96c60e473a591118cdda19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5023242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa10dec34d7740e8f6b2e886e38be9267b07f9095199b6a90e5a3c788b983e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 11:48:23 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 11:48:27 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 11:48:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 11:48:42 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 11:48:43 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 11:48:43 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 11:48:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 11:48:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 11:48:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb229d3396558a9569778f23d7302b803f3a32894ac72bb66aaa18d7763b75`  
		Last Modified: Thu, 15 Jun 2023 11:49:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae1b258a7d74d686736b6459d63f65e7b84802c25eb69c14593c702eeaa36ab`  
		Last Modified: Thu, 15 Jun 2023 11:49:01 GMT  
		Size: 1.4 MB (1411537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427ace77d047161132485d0d1e849e6313bfd3ac5906bdc5c1a14581ec615eef`  
		Last Modified: Thu, 15 Jun 2023 11:49:01 GMT  
		Size: 220.1 KB (220063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2245c7f6798c644fb92a427974afb750eff040bedc67839f23f819021b988e3`  
		Last Modified: Thu, 15 Jun 2023 11:49:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2beec732ed9fea5742f56cb7c9fc3dcf72541cb5df22e9e59570e15f9e953e0`  
		Last Modified: Thu, 15 Jun 2023 11:49:00 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:557bc9f87a1e1bc52642bb8952d0a879ac5593a353c14796cddddb156582cb3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62d68f98632f8097320aac6902f7c602c1dcffd7a6bdae0b0673d9543a6c0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 15 Jun 2023 05:19:50 GMT
ADD file:8ad8a62cf274ba5a6568f68473359114136cb5c7704bfdfce6c38efef3081782 in / 
# Thu, 15 Jun 2023 05:19:51 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 17:34:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 15 Jun 2023 17:34:18 GMT
RUN apk add --no-cache libssl1.1
# Thu, 15 Jun 2023 17:34:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 15 Jun 2023 17:34:24 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 15 Jun 2023 17:34:24 GMT
VOLUME [/spiped]
# Thu, 15 Jun 2023 17:34:24 GMT
WORKDIR /spiped
# Thu, 15 Jun 2023 17:34:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 15 Jun 2023 17:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 17:34:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eb857838eb854a669f87c5df4d936d905fb3129287a93ef485da9454c11d83cd`  
		Last Modified: Thu, 15 Jun 2023 05:30:48 GMT  
		Size: 3.2 MB (3174898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5897952b7e299dca2b896d423bfda7066b1acf478f8cc0e7913cbd37a49389`  
		Last Modified: Thu, 15 Jun 2023 17:40:55 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06405603908eb28e88f899138f60655b0e1f1f3f8e70dbeef03e6548c4a45ddf`  
		Last Modified: Thu, 15 Jun 2023 17:40:55 GMT  
		Size: 1.2 MB (1221484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8625783f9b107b57ae6b8ab2323a93270e807b4525dec5b9f73667ed5b0aa9`  
		Last Modified: Thu, 15 Jun 2023 17:40:55 GMT  
		Size: 208.7 KB (208656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02d5c1789ad20269529284a4f65d9b868bdac4d431802fe12c463e47fb289b7`  
		Last Modified: Thu, 15 Jun 2023 17:40:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebdbe4b7a1197ad5630c73bd6de30fc339c371645e88f9859514654b6dd44ee`  
		Last Modified: Thu, 15 Jun 2023 17:40:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
