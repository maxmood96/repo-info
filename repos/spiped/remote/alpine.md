## `spiped:alpine`

```console
$ docker pull spiped@sha256:82dced4a656b2d513450d2342ecddc3f9244f04c9c07a8565d1e90dd24b83259
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
$ docker pull spiped@sha256:88600bfd34359fe38ba773717d293fc4d6095338551ab0b9c98ced2944029635
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef58a68bf7b0e4e343f1c174cd34a75b21f0714a3fe9e5e50df70c1cb3313a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:31:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:31:10 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:31:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:31:21 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:31:21 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:31:21 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:31:21 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:31:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba143d89ef43493de610789b011ec6f78fd98311801bd1b895263425d2b80f9`  
		Last Modified: Sat, 12 Nov 2022 08:31:36 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3bf49195ff499a5b7913c2890b39e1ca85bd2ba2fc46bdf7967974cdaa578`  
		Last Modified: Sat, 12 Nov 2022 08:31:36 GMT  
		Size: 7.8 KB (7762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6bcd4c1d546b37c09f8d577cb9065b685c82b401a5f2271774cdf3a57f325e`  
		Last Modified: Sat, 12 Nov 2022 08:31:36 GMT  
		Size: 221.2 KB (221203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e9846fbf23dbba2f28e731ca1a2b68957835ecbfe09de8fcecd43f01ce7312`  
		Last Modified: Sat, 12 Nov 2022 08:31:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1bbea7f748e9071525f54078c4c1afed13fcad17509d2a56a430c21b8b56d5`  
		Last Modified: Sat, 12 Nov 2022 08:31:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:4a97e4614d77053ba39fa5c745d6105a7715cb2a1339a25d4fa13a27d0d5b071
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef16808dbefc833d0994260a2717a0477aecef28d949a2bd4c8da571b5627b51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:28:16 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:28:17 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:28:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:28:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:28:26 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:28:26 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:28:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:28:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:28:26 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8ad9b8c9f0b2df322f6b1cabda5e7ca816a4a3d899eb140b118c2827fddfe2`  
		Last Modified: Sat, 12 Nov 2022 08:28:46 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2057d8252d211e7c1c7a5a22ff586d7ad6fb222a67ddc10c861346d2f5de70d7`  
		Last Modified: Sat, 12 Nov 2022 08:28:46 GMT  
		Size: 7.8 KB (7761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036cdcac704f3ec530ed23d018a37fa64b0d4e1ec8c26bd0388a1a2d99220d7`  
		Last Modified: Sat, 12 Nov 2022 08:28:46 GMT  
		Size: 205.9 KB (205882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d603c20f7582181b49742ecc7a817667c6067b1e3ee6ec3e64ecbe1bf10206d0`  
		Last Modified: Sat, 12 Nov 2022 08:28:46 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2d6b98135a7de547f76953f15d873bc47703d65c6f2c87b0a719561fb1066f`  
		Last Modified: Sat, 12 Nov 2022 08:28:46 GMT  
		Size: 338.0 B  
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
$ docker pull spiped@sha256:cc37e731d1198e448359b790e73b2016b757e9d1a05425fa0a2df9fc6fe0cc9b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1152848438c5b85156eb4f564f5a436e27d69210842e300de2be7c0bdf598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:52:50 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 09:52:51 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 09:52:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 09:52:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 09:52:59 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 09:52:59 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 09:52:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 09:52:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 09:52:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a33d40b7aea60d797950562e12532c05e2bec1dfb8dc5431f8c871028f801d`  
		Last Modified: Sat, 12 Nov 2022 09:53:16 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046893368895bc36323127bb34d70394b9e08715b8cd3609c1396fd7dcc7baad`  
		Last Modified: Sat, 12 Nov 2022 09:53:16 GMT  
		Size: 7.8 KB (7771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5d84e6ac65d4649eecb08b3cb834f0b6205a88df39adc3099e196a2e03d066`  
		Last Modified: Sat, 12 Nov 2022 09:53:16 GMT  
		Size: 214.6 KB (214567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7ee94c43226ce1cbb59b1a15b651a023be893f860642d7af91e0dbf49b0bdf`  
		Last Modified: Sat, 12 Nov 2022 09:53:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053b7b3dc658bda7a53962394fac910f8408b95bc4066c9342ad508eb98fb56e`  
		Last Modified: Sat, 12 Nov 2022 09:53:16 GMT  
		Size: 341.0 B  
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
$ docker pull spiped@sha256:9a5fa9635e3b3150a7fb86be203bd9ac800242a8715366e1ebf80137524c1d49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3422852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac8ab48bba973ccd96958d6b1a6ead1c79dc7016524a07dc87240ccf918e9f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 13:39:51 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 13:39:53 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 13:39:54 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 13:40:08 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 13:40:08 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 13:40:09 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 13:40:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 13:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 13:40:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194afa072d947a442ef104e10d9216659dfc8a0d66a1aa9d83dc2daa6d3cb60`  
		Last Modified: Sat, 12 Nov 2022 13:40:42 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3636e065dbfa3ffe9e220f75a2656046c6e68daa308f669c824c33129da33d8e`  
		Last Modified: Sat, 12 Nov 2022 13:40:42 GMT  
		Size: 7.8 KB (7776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f6a06d391f6599e576cc221ab33e97777c1a2d34912c03b26bb42f42ba72ca`  
		Last Modified: Sat, 12 Nov 2022 13:40:42 GMT  
		Size: 611.8 KB (611788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0000fde7d027d5e5be6d184daac6a936d889c009e92180fc9992b2e1b4385cc`  
		Last Modified: Sat, 12 Nov 2022 13:40:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385151a4c23844070ef5830264bf1ee9abeb01f86bbb0c5dba45868ea8324f3c`  
		Last Modified: Sat, 12 Nov 2022 13:40:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:47e6ca3b66046e043d8efb1996b3f02334b21d52d0378b9e70a9eee14bc8ba05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2809081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb44b07872890902f462d8051264598233b2791b8d17ac8d1e9650682147605`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:49:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 12 Nov 2022 08:49:59 GMT
RUN apk add --no-cache libssl1.1
# Sat, 12 Nov 2022 08:49:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 12 Nov 2022 08:50:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 12 Nov 2022 08:50:06 GMT
VOLUME [/spiped]
# Sat, 12 Nov 2022 08:50:06 GMT
WORKDIR /spiped
# Sat, 12 Nov 2022 08:50:07 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 12 Nov 2022 08:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 08:50:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c21b0fe0ff4f5675555696be2fdd46dbd120c67b2a2a82d2f9358d673a2fddc`  
		Last Modified: Sat, 12 Nov 2022 08:50:37 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faafadd95cb1b92a7217a5e1a180e88ffd0de612088f75c144bbf3d501585ff`  
		Last Modified: Sat, 12 Nov 2022 08:50:37 GMT  
		Size: 7.8 KB (7770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157d141feb67cd00e910527177fb9131596a73032d3f627e9160255a17512dc6`  
		Last Modified: Sat, 12 Nov 2022 08:50:37 GMT  
		Size: 208.4 KB (208447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd5180ea5424d8443b199fbe5a892596a2c6d2f9fff62a8e41bcc2a68035514`  
		Last Modified: Sat, 12 Nov 2022 08:50:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda12945c53bd011c9f75619e916738acd26381a21194ab28a173176009878b0`  
		Last Modified: Sat, 12 Nov 2022 08:50:37 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
