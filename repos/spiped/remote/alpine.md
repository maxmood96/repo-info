## `spiped:alpine`

```console
$ docker pull spiped@sha256:817d8a13b805b5e833f639fddfe373137c33047904360cee1d521d4765cc7143
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
$ docker pull spiped@sha256:7b7f7844dc68c4b9728d9185d906025f7565df88ca9612aaaf420ac91523f405
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5080949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b60c5b50be16ba58852d923ea4e7d5224aecb355eb4588ab08b2f70c72ad851`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:36:50 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 30 Mar 2023 02:36:51 GMT
RUN apk add --no-cache libssl1.1
# Thu, 30 Mar 2023 02:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 30 Mar 2023 02:37:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 30 Mar 2023 02:37:01 GMT
VOLUME [/spiped]
# Thu, 30 Mar 2023 02:37:02 GMT
WORKDIR /spiped
# Thu, 30 Mar 2023 02:37:02 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 30 Mar 2023 02:37:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:37:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833c4ea98211ab2b826b6d62f250a61b8c5ae407b5de38776cc5bc31d895d3fa`  
		Last Modified: Thu, 30 Mar 2023 02:37:13 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870359eb3ab308a11eaf9cfc6782cd2bea0c513f3920492180bd5f5cbbea54eb`  
		Last Modified: Thu, 30 Mar 2023 02:37:13 GMT  
		Size: 1.5 MB (1483362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4afeb4ec06ad120774f5e7a75610323bda25b84d5957c8bac3f5c90ea7fdd17`  
		Last Modified: Thu, 30 Mar 2023 02:37:13 GMT  
		Size: 221.3 KB (221284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9641a8793752f42f60dcbb12e857125ba41995c02e48630112ef3f6d5747a28`  
		Last Modified: Thu, 30 Mar 2023 02:37:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb90b001556af3810279377523e96a71161f2dc727b628cb3d284764e5e847fd`  
		Last Modified: Thu, 30 Mar 2023 02:37:13 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:98e69abcdbbbc31f8223857ec6529b855f8e21be02602fe6763b73403a252650
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4871452a88018819e0282cc73c7c17274cbea4b4fd8f73619664078771460b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:22:48 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 30 Mar 2023 00:22:50 GMT
RUN apk add --no-cache libssl1.1
# Thu, 30 Mar 2023 00:22:50 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 30 Mar 2023 00:22:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 30 Mar 2023 00:22:58 GMT
VOLUME [/spiped]
# Thu, 30 Mar 2023 00:22:58 GMT
WORKDIR /spiped
# Thu, 30 Mar 2023 00:22:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:22:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 00:22:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f18e2ef9b0aa3ce161a88dbc21a7f6e04c161889cd2e9a48db6753f539a908`  
		Last Modified: Thu, 30 Mar 2023 00:24:29 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f98080b1dde5f78f59c30b4e0ecd3d8755ce81a51335edb1f928872b6ea2758`  
		Last Modified: Thu, 30 Mar 2023 00:24:29 GMT  
		Size: 1.2 MB (1241151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaabfafc343e9926cb7046e859064ad3777e2fc8cddcb7e477dde08175094e7`  
		Last Modified: Thu, 30 Mar 2023 00:24:29 GMT  
		Size: 206.4 KB (206355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41f7588b8c91b544e8c7d054c90e59b7a9bd11c4e88918abb84a283000e0017`  
		Last Modified: Thu, 30 Mar 2023 00:24:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cd529e07580d9750fa02477c2004129b10b554d974efb4047239df64df3a24`  
		Last Modified: Thu, 30 Mar 2023 00:24:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:361539f7f9277859ba382de7be4afe676210140f53c3c5cd85d5ae3985f905c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e899581be5421f50eb7e6339c7512ab16c114d8213f09e8aca52c68f0bcc311`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:31 GMT
ADD file:143b601fcc6b5d7d95d3e5ccad3fec7081191a47e28d4f9294a7fb2499cab1af in / 
# Fri, 10 Feb 2023 21:51:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Mar 2023 17:00:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 01 Mar 2023 17:00:07 GMT
RUN apk add --no-cache libssl1.1
# Wed, 01 Mar 2023 17:00:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 01 Mar 2023 17:00:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 01 Mar 2023 17:00:14 GMT
VOLUME [/spiped]
# Wed, 01 Mar 2023 17:00:14 GMT
WORKDIR /spiped
# Wed, 01 Mar 2023 17:00:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 01 Mar 2023 17:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 17:00:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6fb81ff47bd6d7db0ed86c9b951ad6417ec73ab60af6d22daa604076a902629c`  
		Last Modified: Fri, 10 Feb 2023 21:52:33 GMT  
		Size: 2.9 MB (2868494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcf9acc5eeca77f6d435380f4f1fea53c3643c4cc9042daf13fdd9b6b72d9f5`  
		Last Modified: Wed, 01 Mar 2023 17:00:57 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34e65da889251051ec9481b5d6cb0d428c45c8861fb2948b0c38c07470bba59`  
		Last Modified: Wed, 01 Mar 2023 17:00:57 GMT  
		Size: 1.2 MB (1167579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0412dc4bafb0f9dabcfd28a3c0b4454de2db5c81112fdbb51bf5c883f4a6925`  
		Last Modified: Wed, 01 Mar 2023 17:00:57 GMT  
		Size: 200.1 KB (200120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70011259fd33df6da621cfb9142329c3c7a89b4bc5bfe91a87f7335995930ff9`  
		Last Modified: Wed, 01 Mar 2023 17:00:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d3fd9f335e89a8501d7008f1bbaf813f4a5b26227452ecfc0001613be1ee7f`  
		Last Modified: Wed, 01 Mar 2023 17:00:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b202c4e5897cb771f303b85871c6b7a1fb5f025c51e651b30a4415f0e2e4973d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3a0f714da4f343e79de4855fa4cdc4a23892d7fe5654dec6710bc79bb2cc2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:39:43 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 11 Feb 2023 06:39:44 GMT
RUN apk add --no-cache libssl1.1
# Sat, 11 Feb 2023 06:39:44 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 11 Feb 2023 06:39:52 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 11 Feb 2023 06:39:52 GMT
VOLUME [/spiped]
# Sat, 11 Feb 2023 06:39:52 GMT
WORKDIR /spiped
# Sat, 11 Feb 2023 06:39:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 11 Feb 2023 06:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 06:39:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e706a54c37c1524628e434965039ac738ff48a6f151dd2ef6da2cb49958cc0`  
		Last Modified: Sat, 11 Feb 2023 06:40:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99781ddd302da37630cc491b5190c39c7867e6bd96556fad9f613e3411bca0d`  
		Last Modified: Sat, 11 Feb 2023 06:40:07 GMT  
		Size: 1.4 MB (1363548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768a1af5c81e5cc877ea8cb330527a3924d5f2b5acfc5dd8239f84fdf091e5ed`  
		Last Modified: Sat, 11 Feb 2023 06:40:07 GMT  
		Size: 215.7 KB (215691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7567bda17775002440a508f6ff25154cb13c9201175281b80186ce38d44e2b7`  
		Last Modified: Sat, 11 Feb 2023 06:40:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba17a7f3c3024db40a3e0b478318d1eb5168af1437c2bd502fb302591b78f95a`  
		Last Modified: Sat, 11 Feb 2023 06:40:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:0e5f49d56599b01f5aa0c4d6ebedb8fe9e52f5d2a66e094700b5f7703cc3f26e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa9e52e3f82d57652b3398c82d896ea0c351c189b78a1daa85740fc04413b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:30 GMT
ADD file:61bc44c9685b610d18bddd05d2ea1e57b4313f5f433a0a0b7e5269ec24f108b0 in / 
# Wed, 29 Mar 2023 17:38:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:33:08 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 30 Mar 2023 01:33:10 GMT
RUN apk add --no-cache libssl1.1
# Thu, 30 Mar 2023 01:33:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 30 Mar 2023 01:33:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 30 Mar 2023 01:33:22 GMT
VOLUME [/spiped]
# Thu, 30 Mar 2023 01:33:22 GMT
WORKDIR /spiped
# Thu, 30 Mar 2023 01:33:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 30 Mar 2023 01:33:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:33:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2b0f0faedf1b87a3c77cf90d027fb7a25aa67f35400244a4655ad5842a757e4`  
		Last Modified: Wed, 29 Mar 2023 17:39:00 GMT  
		Size: 3.4 MB (3412260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a513a8526f3d62fd7ec1e80a76b26d4cf8c8c37ea534b10e2c0060eb3cb6f0`  
		Last Modified: Thu, 30 Mar 2023 01:33:31 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7fa7db70396ccd0f7c43ec98f7831c11a443d8d0f9ae5383bd39a0256cd39d`  
		Last Modified: Thu, 30 Mar 2023 01:33:32 GMT  
		Size: 1.5 MB (1486443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d342e0d74297744901c335be2694a48a287375cc57389ee49fc329b6093f5a`  
		Last Modified: Thu, 30 Mar 2023 01:33:31 GMT  
		Size: 231.6 KB (231615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5bf7a2360503d1b51116e389e689406594d6295129a36524b8e4f7bad02d7`  
		Last Modified: Thu, 30 Mar 2023 01:33:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cb4f4de570095d623ebcde4ca7cf3062c366c24ad3595d5108c7111c29af`  
		Last Modified: Thu, 30 Mar 2023 01:33:31 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:75c7e8ce27d4c68e8862a8e832409e09dbeb2c47fa2163ac0ac7f4e794b6b14c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5025550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cfab6c09a42cd9174ca6dee237febe2f4a72f0c07628ccddab56278968150`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 09:33:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 11 Feb 2023 09:33:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 11 Feb 2023 09:33:50 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 11 Feb 2023 09:34:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 11 Feb 2023 09:34:04 GMT
VOLUME [/spiped]
# Sat, 11 Feb 2023 09:34:05 GMT
WORKDIR /spiped
# Sat, 11 Feb 2023 09:34:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 11 Feb 2023 09:34:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 09:34:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d50df2303841e19f748472d51fac8d0695468f1d50516484905b50450aa48`  
		Last Modified: Sat, 11 Feb 2023 09:34:31 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b54432b9107e6d87810bd116ab5112e27a1f713d4d2c06525f0ed14f102e3c`  
		Last Modified: Sat, 11 Feb 2023 09:34:32 GMT  
		Size: 1.4 MB (1413040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bda8ea646857e9e3d0c92c042261af7dba424338abfc7cc1c58eec7b8985be`  
		Last Modified: Sat, 11 Feb 2023 09:34:32 GMT  
		Size: 220.0 KB (220021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e33bc423b9fd5cc84d66be2c92fc2c78368e9b5553d8c6848fab3570115fb66`  
		Last Modified: Sat, 11 Feb 2023 09:34:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a89c5ec31eae84c318581d292f2fdc24ec49bc7692940d54b3b579b04cd2d6`  
		Last Modified: Sat, 11 Feb 2023 09:34:31 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:604fdf074de91d3fb86a39f54c9e130aeae2855ef71419e51d46b3fdbf10d3de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4608998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a0724e4059c76aefa5294b08af1999e786b6c97b94942a93375b39f74ec82a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:37:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 Mar 2023 22:37:25 GMT
RUN apk add --no-cache libssl1.1
# Wed, 29 Mar 2023 22:37:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 Mar 2023 22:37:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 Mar 2023 22:37:31 GMT
VOLUME [/spiped]
# Wed, 29 Mar 2023 22:37:31 GMT
WORKDIR /spiped
# Wed, 29 Mar 2023 22:37:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 Mar 2023 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:37:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d252736c81578b3badb86bd65e11e8c42a3eced9b84da155c5d277746787398`  
		Last Modified: Wed, 29 Mar 2023 22:37:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4b9cdd39312641949e882585794aca9deab09fa611f8acf8a7b6c157519893`  
		Last Modified: Wed, 29 Mar 2023 22:37:46 GMT  
		Size: 1.2 MB (1223431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4a09ddda6c10edd737c5f0240c12ce3c655fe0cf8717062fdf0ab72f20285`  
		Last Modified: Wed, 29 Mar 2023 22:37:46 GMT  
		Size: 208.6 KB (208640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3df4963fb4aa70acb7774a679b92580dffeb32ff4899e3ec8919a9feff0338`  
		Last Modified: Wed, 29 Mar 2023 22:37:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af10966e7af681719def4af18b191e9fbdc7723fbc3c8f645089965679fe6c7`  
		Last Modified: Wed, 29 Mar 2023 22:37:46 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
