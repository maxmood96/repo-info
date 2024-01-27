## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
