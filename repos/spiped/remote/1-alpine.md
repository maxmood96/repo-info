## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:a82fe533bbfcb11434959e2a42e40d2ccee910137bbe78798a87d135ecad4eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:11414532f1ec8fd6497b16fa18f9b80023e7cc0db3822c0fac04d8d285697298
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b87e76d8bfd9ef6c6e408cd1211a5849a15b86a68e249464dcf8369259ac6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:26:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 21 Jun 2024 02:26:07 GMT
RUN apk add --no-cache libssl3
# Fri, 21 Jun 2024 02:26:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 21 Jun 2024 02:26:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 21 Jun 2024 02:26:19 GMT
VOLUME [/spiped]
# Fri, 21 Jun 2024 02:26:19 GMT
WORKDIR /spiped
# Fri, 21 Jun 2024 02:26:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 21 Jun 2024 02:26:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:26:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28011ab10e256cef38b7a12c637e0cd897ccdf80cdcb31cadb392c6f61bc695a`  
		Last Modified: Fri, 21 Jun 2024 02:26:31 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1aa97b3ec31b62bf5215e0ac4ac626dc2cac458b4cd743b80fe7c35340a857`  
		Last Modified: Fri, 21 Jun 2024 02:26:31 GMT  
		Size: 7.6 KB (7582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc05ed83f8ac7ffa7c35b2b28b7e6fbfa04b56d0a60223eff9f9ecc02ae43a9`  
		Last Modified: Fri, 21 Jun 2024 02:26:31 GMT  
		Size: 224.3 KB (224268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ebd5f8e4130ef120cc9338b53f1b1cdfed27184147f39ba01a2f1cca2a5b1f`  
		Last Modified: Fri, 21 Jun 2024 02:26:31 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabca1a56b9d7d172809133328a7b5c6fa90523b749c7a8b21014d30595acf4c`  
		Last Modified: Fri, 21 Jun 2024 02:26:31 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3ed90db5d6eab20406150e0758792245f8e65569326b4f0a7674419ceabb424c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5411d76f0d76beb4631046f7f8f54db02664294d64da29f9bb3638c1fa71334d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:59:13 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 21 Jun 2024 01:59:14 GMT
RUN apk add --no-cache libssl3
# Fri, 21 Jun 2024 01:59:14 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 21 Jun 2024 01:59:23 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 21 Jun 2024 01:59:23 GMT
VOLUME [/spiped]
# Fri, 21 Jun 2024 01:59:23 GMT
WORKDIR /spiped
# Fri, 21 Jun 2024 01:59:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 21 Jun 2024 01:59:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 01:59:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d5816075f3a21cc71c749e7cdb10fbb5fef7a8b8dd3501b9e39c4c16c01e9`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb1dec5190ed67e438f01c8bdae60a9e72733f9e11b7feb1db5ac568c98c4d`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f84c2c1ddc190a0a2ea82d2fb262f8cc6ac315355176e9ff6475174126cf8c1`  
		Last Modified: Fri, 21 Jun 2024 01:59:32 GMT  
		Size: 209.0 KB (208955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787cff256cc70ae8fa4e53a36e497e9d00650437491c303598ca31bbac882d86`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d2ad3a347111ab93c30958ceeb4c6e22bbbfd527183bb20e152db5e16c1ce9`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:332f7cbde4e40656c467864ffbbb5e11f782dedf12b63cf8997a3aeef8483d5e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec8d91ed902939340f52d2252bf72e59143e66290fb6451cb60d162cd3d5758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:24:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 21 Jun 2024 00:24:07 GMT
RUN apk add --no-cache libssl3
# Fri, 21 Jun 2024 00:24:07 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 21 Jun 2024 00:24:14 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 21 Jun 2024 00:24:15 GMT
VOLUME [/spiped]
# Fri, 21 Jun 2024 00:24:15 GMT
WORKDIR /spiped
# Fri, 21 Jun 2024 00:24:15 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 21 Jun 2024 00:24:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:24:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3971930614c9155581e6b78ece59a716555e53d9976b81dd4ff57aea5b55a65`  
		Last Modified: Fri, 21 Jun 2024 00:26:26 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a8d171c50b0030711a829589a6bed457964e2c0020d5a98ee665c4b67c926`  
		Last Modified: Fri, 21 Jun 2024 00:26:25 GMT  
		Size: 7.6 KB (7592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e233b4b8fa9b02d614f8cce0ecdbb7006d7e1e479b9b24cae4d7ed2fd90a2513`  
		Last Modified: Fri, 21 Jun 2024 00:26:26 GMT  
		Size: 202.6 KB (202567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a0954116b93cfaaac729b85f30aedc12fe0c32e3c834a79fb8b64a9d562a6`  
		Last Modified: Fri, 21 Jun 2024 00:26:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9213c0650e5c776fb32eae98074c6e837e0702cc68669db89ceeb852ba56e`  
		Last Modified: Fri, 21 Jun 2024 00:26:26 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e2ff742e02eafce18cbb0d4a8495c5d201da0a9ce4352ee3021a26626f547c1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b02c56cc5999482ef520910535958e10a336067d0f56806bda5bb4f9740364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:24:00 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 21 Jun 2024 00:24:01 GMT
RUN apk add --no-cache libssl3
# Fri, 21 Jun 2024 00:24:01 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 21 Jun 2024 00:24:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 21 Jun 2024 00:24:10 GMT
VOLUME [/spiped]
# Fri, 21 Jun 2024 00:24:10 GMT
WORKDIR /spiped
# Fri, 21 Jun 2024 00:24:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 21 Jun 2024 00:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jun 2024 00:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41353419dfd6ca69ceb8ba4accb3776510b80c753191309af3f8a3f59e7c39c8`  
		Last Modified: Fri, 21 Jun 2024 00:28:34 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1889cf02ef445250f94a97b8530e5ba2287ad3e13e15d373ad3619d6d59b9d9`  
		Last Modified: Fri, 21 Jun 2024 00:28:34 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771d7907432031636eb79dc80b8bd457afb826005b305924f082979bf004176c`  
		Last Modified: Fri, 21 Jun 2024 00:28:34 GMT  
		Size: 218.9 KB (218932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195930be2b080954056ca0112d59b3753e9f6891a26bfd8d43b966b3a0ae678f`  
		Last Modified: Fri, 21 Jun 2024 00:28:33 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efe793d250740d87fe312c1687d034f0849847db39d282325d8bd2d1f7b0368`  
		Last Modified: Fri, 21 Jun 2024 00:28:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:dcebe7990820984458295f3502ff84eb51d95fd85f9658a68ee9e91615e42278
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48057bb08853cbdb14147937647660de3533b4a5bed019e3b3b6714da09d17db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:15:56 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 20 Jun 2024 23:15:58 GMT
RUN apk add --no-cache libssl3
# Thu, 20 Jun 2024 23:15:58 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 20 Jun 2024 23:16:10 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 20 Jun 2024 23:16:10 GMT
VOLUME [/spiped]
# Thu, 20 Jun 2024 23:16:10 GMT
WORKDIR /spiped
# Thu, 20 Jun 2024 23:16:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 20 Jun 2024 23:16:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:16:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec317a5ea96eae256bdb39e720f5810ebbc81dcdd11df024d8d54bc961ac41f`  
		Last Modified: Thu, 20 Jun 2024 23:16:24 GMT  
		Size: 963.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0dbfd22a6ed87a5ef2a1b675d63694e19b75d158f1ed56c80d547bad5af42d`  
		Last Modified: Thu, 20 Jun 2024 23:16:24 GMT  
		Size: 7.6 KB (7590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0398943dac3f3dbeb6b76e9faf94146110afa42ceb48f1dc33113b44f58f7bbe`  
		Last Modified: Thu, 20 Jun 2024 23:16:25 GMT  
		Size: 234.9 KB (234874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8784adb0bf87c085b1dcee98da4e719f52a6520f7382442c30ce0216e7be6b89`  
		Last Modified: Thu, 20 Jun 2024 23:16:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af68aad8c86b75a72d7a2e300ebb10eee29c57440130518b7e89a61252721cf7`  
		Last Modified: Thu, 20 Jun 2024 23:16:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:ff73f9ff4534662723ff09b9ddb548319460571f7b3c18403e32299897a1b0f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0979c2ba1d403ef846aed708cbd21a4e99b62869211895f79bc4b3d91e1f3798`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:23:29 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 20 Jun 2024 23:23:31 GMT
RUN apk add --no-cache libssl3
# Thu, 20 Jun 2024 23:23:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 20 Jun 2024 23:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 20 Jun 2024 23:23:41 GMT
VOLUME [/spiped]
# Thu, 20 Jun 2024 23:23:41 GMT
WORKDIR /spiped
# Thu, 20 Jun 2024 23:23:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 20 Jun 2024 23:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:23:42 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba2f986428a32552ad234cae876a790e7493582050c3c8c6a468228024ded7b`  
		Last Modified: Thu, 20 Jun 2024 23:23:54 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19b49ba3e0f4c291b4466f94b0df7743f3943a8ad76730eb6ffd76c0ace492`  
		Last Modified: Thu, 20 Jun 2024 23:23:54 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281373237728c8661b2379afc6598a91eea24faf6e8735be55480468cb82184c`  
		Last Modified: Thu, 20 Jun 2024 23:23:54 GMT  
		Size: 222.9 KB (222918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e58176c8871663ff25d9233f511076d05fcb8b56cb3156ac3dee8c9dc49496e`  
		Last Modified: Thu, 20 Jun 2024 23:23:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc155b7c734c584418110561a0f683109d7fb97d65b735fb583a2cd19d1f0ed`  
		Last Modified: Thu, 20 Jun 2024 23:23:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:cd5a4621afff483f36101ea9ebae88f7dcf25f86c2309d723bbd483be19ceafe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e812e801b6ae16522a84a7ab6f7556c16c0a15341d272fce6510208bf865f58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 04:22:05 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Wed, 29 May 2024 04:22:11 GMT
RUN apk add --no-cache libssl3
# Wed, 29 May 2024 04:22:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 29 May 2024 04:23:18 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Wed, 29 May 2024 04:23:18 GMT
VOLUME [/spiped]
# Wed, 29 May 2024 04:23:19 GMT
WORKDIR /spiped
# Wed, 29 May 2024 04:23:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 29 May 2024 04:23:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 04:23:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c0c4f99ba3a3946abd6a4741459ac597ecf8393da29611c0c72c127c3c8fc6`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5b031480a0383a5f02d1f22612813b1ffa3cfb8ac50bda5bca486fdbf7499`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1e17de0f3b7417191ea5c8f7779379c7965a389e87d7fddba3c8d28d6f854c`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 215.3 KB (215290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f7d27f6c07e7feb513acf854ddaee65e51ce92daf7c3918f1625aaec5fa14b`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e20db4a7ebcccd41cb86827aeddf9cb92dfc787970bf9623b4779f5bf8559`  
		Last Modified: Wed, 29 May 2024 04:23:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8dec41cbe81f417096082fdaa31bb95bdd7e36dfec4cc462a7e9462205ed2402
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee6531c62c7ffe07b640d5ab5b763be7303e38a61c81bb6524855dec0ca243`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 24 May 2024 00:57:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 24 May 2024 00:57:59 GMT
RUN apk add --no-cache libssl3
# Fri, 24 May 2024 00:57:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 24 May 2024 00:58:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 24 May 2024 00:58:05 GMT
VOLUME [/spiped]
# Fri, 24 May 2024 00:58:05 GMT
WORKDIR /spiped
# Fri, 24 May 2024 00:58:05 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 24 May 2024 00:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 May 2024 00:58:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7d2acf9b7465edffd5a10fedbf230b30c81cb8b13eb3c7d97b4ba3dc542d17`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 987.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbc970af29f74dd00097324a2d43d0cd4ea77aee3bf1217ffe3b76397a889`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec7c94b7827b61d57438499589e4d6f5b1320a6bd0eee1a2226d3f8d22d81aa`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 211.7 KB (211719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad9a1996f006554091faad0788cedfe9c37ce442aefa430c0d7b7a7eb402280`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531998ea71dc30b5a286d51c478a1a6f9ff8db7afc074c302dfe6bef2f5da69d`  
		Last Modified: Fri, 24 May 2024 00:58:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
