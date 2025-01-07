## `spiped:alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json
