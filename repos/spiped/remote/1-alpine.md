## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:d11c78fbbafe1ed8de8217225ff80e2cdda887e450a129532e09ec4056d62039
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
$ docker pull spiped@sha256:198d81fba38183034cc0e9b15527f23513584b0a742930e2dbe38248d73821d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ab67e1be9e9e103fe4b4ff8ecec3151a98ae24dbb1948de904781cbf3a19e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:03:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 09:03:27 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 09:03:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 09:03:37 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 09:03:37 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 09:03:37 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 09:03:37 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 09:03:37 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ee39bff1ab9c448949e88b9ace60f4f38323ff95d41e9bc7a07b13bb942576`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee961c77ceca0ebaa1deb9e6aa7fefc1704c7caf2702d8db3ca9c3d75b463db`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 1.4 MB (1432999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf8d6612d20129d3e748da7a51e08c7efd8f498f596c040f4811b72e3bbef3`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 221.3 KB (221271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968283c56820f977959aea83a4de20638951e0a9f01df763de8edcb66537caf7`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eafdca9b52817340f4be3919e3542b3f07d6519b869febaee3a3a73467f3704`  
		Last Modified: Sat, 16 Mar 2024 09:03:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4adf9877b944a5f4a7be52a9998ed7bb2d3a58f52f9baeb55832d4201f64f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177bbeea849b5f63f35c023cd2f81e190e3ddde2d4a8b46aeec6657aecd925ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:35:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 06:35:28 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 06:35:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 06:35:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 06:35:35 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 06:35:35 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 06:35:36 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:35:36 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532923c8d05020af62be9a0dac000f433af0ff15afeb378712d39a3bcf18bf17`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cb4e9d15c5093396bb29d21821482be1684dac442ec148da29dfa5ad7127f1`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 1.2 MB (1236772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0d07e0c0ea44033ff193a368045c0499d5f5e7bcaf8da069ba1f2e896d920`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 205.9 KB (205861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccddf6cba8181efbb10afc23488311fdf05aefae103ca830386a8cf00629f48b`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d7429e3758e302d5edec1472feaf9a843efd77d244bb67c3390cf6aa50b139`  
		Last Modified: Sat, 16 Mar 2024 06:35:44 GMT  
		Size: 340.0 B  
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
$ docker pull spiped@sha256:eb278f1652564d9df4afdf05a9b3667bca71c0929ded40f773ecb5efa36372dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728919f6d4dbc8da19537551d6e16da4c85844c592f515aee2a7a66623074116`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:15:21 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:15:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:15:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:15:29 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:15:29 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:15:29 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:15:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03910404e6281e9ad56565c58c5baaa4998bba46773bf799a0181741bdd214e`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04373310480ac3f90e857e67a93fa8b705a4937d0666b55f22351cfd6f0e6b2`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 1.4 MB (1362703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e8ff14ad9843af323d419f40faa502ce4009765fec582f9a5451aba4030f06`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 215.7 KB (215680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb9061eb845a247cc9bbc3f12f506eb82eac0025d6c95019a3e1adf38a939c`  
		Last Modified: Sat, 16 Mar 2024 05:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c5992824b3088c29a31312ebb8cbabe9bf6a9ff2b9e1a832332346c67c69e`  
		Last Modified: Sat, 16 Mar 2024 05:15:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:ac9655daf19c8c0147be28fd461895ef3a1c79db08b596ed2d588b6a3c816504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ddadfdc5396a002ff71f7430163abb731e6890e7a49c16d77c5649e58dba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:07:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 05:08:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 05:08:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 05:08:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 05:08:13 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 05:08:13 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 05:08:13 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:08:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508806baeb68406329423224090a40940d296f944edc857b31946a1e0b2eb94`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20d8676a55b9005ca166d422eafb181f4e0dd038fe4912102eb35278224336b`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 1.4 MB (1353903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a80dfc8677984adef1a26dd3a1761ea6cb42ae6b57a49cdf27458771baa848`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 231.6 KB (231638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b2b104abfcd98f8e2aaab8be718007a2219883fc986e109873f9e777847b30`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae79c3a2a70ad960e3ab773fce80eea1b3cda5966da88a81b40895af47cda41`  
		Last Modified: Sat, 16 Mar 2024 05:08:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:91493c946db15eba4386b0b2a820f943dc3d29f55a1de28e4591c91dd27ac7d6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4db55030112f4e2638c067c584a4edcb1f7199152e94e0a613f5f39364da85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:12:03 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 16 Mar 2024 07:12:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 16 Mar 2024 07:12:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 16 Mar 2024 07:12:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 16 Mar 2024 07:12:16 GMT
VOLUME [/spiped]
# Sat, 16 Mar 2024 07:12:16 GMT
WORKDIR /spiped
# Sat, 16 Mar 2024 07:12:17 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 16 Mar 2024 07:12:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 07:12:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d463955fc02ba4f84639b3d043165a5c28c566c0a20033980b4f4c3faf760`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d878c69e3e371c35fe73ad27732a539ee52fe55145d7de6488abe3925845`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 1.4 MB (1361743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a363ee7e9be874a2cc0b6e345b8cc3922279c96fb5b46f586c41a80116c97`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 220.0 KB (220020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a490aa09932ee227df910f1be26cc62c155abd010823121b17001e617c2d652`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a702b0f7fce70e7a512f362b2fb211b08209ee54a29ed22266c16335f6d579b`  
		Last Modified: Sat, 16 Mar 2024 07:12:32 GMT  
		Size: 339.0 B  
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
