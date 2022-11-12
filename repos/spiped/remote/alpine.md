## `spiped:alpine`

```console
$ docker pull spiped@sha256:9fb1b03f0a8a685b4498c68cd5015cf4a09bb8ab67f00b497978bdc360ea54bb
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0efc6c3831eb2faf7335225ec92ce9fb02a206c4365a071f17e1b74788758614
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868463e78de77da4bef4772aa7cc6a7d28464ef542579c0261c09e2c8c781f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:27 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Thu, 10 Nov 2022 20:49:27 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 11:57:34 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 11:57:35 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 11:57:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 11:57:44 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 11:57:44 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 11:57:44 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 11:57:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 11:57:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 11:57:44 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc27c5af139465b6aa05baab3c0d20030b5e8a48f4d493905c4a04c47f2cceb`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9cf0a5a0c3c72f63de85ff87dbfbcd89f59cd361ccef40daf03a79b48f956e`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f75d111fa4b0724c680dd28515c34016f39b3a3e985eef7a39b7fb09035b8`  
		Last Modified: Fri, 11 Nov 2022 11:58:06 GMT  
		Size: 1.8 MB (1833585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d265756106316b71be7bb36cc32aad20cd231c0ad2f1c3a3a4cf12025d427294`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90a6706272ed824e7db29975247f2a56a7e5a468b56a15e8f2f93b203d036b2`  
		Last Modified: Fri, 11 Nov 2022 11:58:05 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:da26d167b81e6942d2bf840b15ff59a945c83bcb6c34968a2cb76d61b48368d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335ebf8c2444c91778b85ac23284d5a8bb8a0564755cb6ea06160705fc72ebfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:09:59 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:10:00 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:10:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:10:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:10:09 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:10:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:10:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:10:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:10:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeca438422069f0b2d529c93aa015b2d66ff14e7f811a2db7155b3780f3f17`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a307f22f7b61faf288c16b2e278af2069d3f0f1d7ccb5de2669081f800b82595`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 7.8 KB (7766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ada82ce81437697e7bbaef8a8df96fe30079d2b62708af97071da84c0be91f`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 199.6 KB (199550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650ecac6d83dd8ac1473ff90545abe2e47ad63985de2031e7fb65a25c99847b2`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304511b2e0cd4c9408aace74412dcce1dcbb72f7cc52fa88e57892bfe2beae31`  
		Last Modified: Sat, 12 Nov 2022 08:10:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd655cf784128209a6ce84327a6d97766bea83bac20745aeb465d4053cd4f105
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86d0ae659c9b8298694e19a19e61e1096d1ea1af24b229862d9c37f6deb1b68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Thu, 10 Nov 2022 20:39:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Nov 2022 05:24:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 11 Nov 2022 05:24:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 11 Nov 2022 05:24:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 11 Nov 2022 05:24:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 11 Nov 2022 05:24:55 GMT
VOLUME [/spiped]
# Fri, 11 Nov 2022 05:24:55 GMT
WORKDIR /spiped
# Fri, 11 Nov 2022 05:24:55 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 11 Nov 2022 05:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 05:24:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc0fd009f6ccc62d80c4b480c66a29b1585894ea074dbe47eb333980bf9bd6`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236aea0d806ec2bb4e08480c6db584b2e726baae7d26439a2bc394b4c5fc88a`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 7.7 KB (7739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28c32b7753ad7c53a2bf64f16493bc5a3032cd1a4043d9bf7bd38c3b1d1640`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 2.0 MB (1971114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6352383f529cef4add4006f77dbfaf604b1e246e11a14b8d50a03e50998a361e`  
		Last Modified: Fri, 11 Nov 2022 05:25:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ba1f3cf56eca1bd4f9b02d4fd58f55791f2463be1bc0d0f049c817423dc30d`  
		Last Modified: Fri, 11 Nov 2022 05:25:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:843ee0a06fce410e9185f279bedec495552d30a9b235351c9e52bd669095b6a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9c942ec6bc7f10412698170c354b1c1e3784c5293bb45763683f9fae4ff45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:29:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 07:29:08 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 07:29:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 07:29:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 07:29:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 07:29:22 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 07:29:24 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 07:29:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 07:29:25 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d809fb6be6b6c5126ea93c77f723eabd38a79da96195f2112d4ba37475d11cec`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4111161b7b7d291c73883105977d83b95161ff3092cb8c51baa969a0f4f40`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefd93dcc118fc9b6c2575a0e2e6442cf1941ad36cd7c23a11ff37f954d72696`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 231.4 KB (231353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12465fe04c57bef25da7dd19448585a8f389a2be5002904390928db02803c463`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f19ff97a8609ea6c7b399819d80dd69016ccd3db9c032fb36c9caaec3462cde`  
		Last Modified: Sat, 12 Nov 2022 07:29:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
