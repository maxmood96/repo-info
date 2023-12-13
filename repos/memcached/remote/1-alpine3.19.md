## `memcached:1-alpine3.19`

```console
$ docker pull memcached@sha256:2e2ee96bd8dcf7191ea7c157b57ef44f3b64650a4b993cfe77012d153c328c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-alpine3.19` - linux; amd64

```console
$ docker pull memcached@sha256:04d0d1df8b87df09639e1e9995971ad2ad8fe66c2d02e4987076a370a271a956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4462859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3012cf09bdc9226b392bd2af8f268f16f77c6fe65b3f72f558668e15047b8807`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca103d2276212cc687cf236216a50e9bf98e0d696a8a63a573990e5b75e2a7e0`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbbbad4976dcd0f62489adc6ade439608ccbc5c8d64aa96df8578451559665`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 104.2 KB (104203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f63893492c8f6b29d157137f9062d5cc26157a9f530a15dbeed5864492734c`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 948.5 KB (948535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe795c6bddfd42e13ac78f0081231f8e0e2ec695f3dfa99a77a26473eb160fc0`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f873f0cd6918fb2224432d83c505b44e00227672661a3915574dd956e8194e`  
		Last Modified: Tue, 12 Dec 2023 20:52:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:179681d2f3efc2f6d2f58a2255a3ee29c6bf92a37220b1d41ba0b8c80ade0b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 KB (98070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3277e2ef6023c2abffb46b0362f3b8d7d758fe8b2c1216806c2b190517c70e9b`

```dockerfile
```

-	Layers:
	-	`sha256:9d49890946d1c8bd1ae77de744b5717210d885a7c59e657249b28c3f974e4c10`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 78.6 KB (78603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bff411886bbd4cfaeb87f474853596227a084233568074067a24f2e2b7bcf48`  
		Last Modified: Tue, 12 Dec 2023 20:52:46 GMT  
		Size: 19.5 KB (19467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; ppc64le

```console
$ docker pull memcached@sha256:06711fbe2ddda329f14ab4a0825494b32336140e6a0e3b6c4d879adc475857c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b1d12275d18bb3dac772e05585652308aa081f1aeae540381aea1c9ed321bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add73e7dbebd6c86078686bb046ef57017b090fe917f656feb83ec0ef971b5f3`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64bed657a7e728633e13f2021b35954e98be9ecae77096d30cdaa1d9260d61e`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 123.4 KB (123403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7a39c0f73f39f740b607f200570edf13046db40879e4aebbdca9e2fd273b0f`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 985.1 KB (985092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6306836cf70172b90d6b82bffc8546c005c16cda9b7d58dc5dbd386b7ee7d8`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3eb1fb10d08825521650c7c7ddedf3cfce2f976e93c18ab11aace23c38be5`  
		Last Modified: Tue, 12 Dec 2023 23:20:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:65ba466bf93c49f07fd340ced359d51a13a74b069cca4de2d034d12f42b92ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e68093b9e036b2a9ff696038b0fd906f66504c0a0cd70dda18954ebb93d4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:b64631288cf2d05d3a1d99eb8cb41f077724b027aaf136bb327f88055e4ceaf4`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 77.0 KB (77025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac9ea640f8ca624c147fd0dcc40f859a6284e5f50c4396e0b1e962a4b732813`  
		Last Modified: Tue, 12 Dec 2023 23:20:17 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.19` - linux; s390x

```console
$ docker pull memcached@sha256:53d0bdb491815057b9014ab30e95c68146d83accdc9d8d690e308e67e7f4eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b078f3aede6257187e9488318eac328332ace90ac171c8a99d0ca495e1e9ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_VERSION=1.6.22
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.22.tar.gz
# Sat, 09 Dec 2023 01:54:10 GMT
ENV MEMCACHED_SHA1=7a691f390d59616dbebfc9e2e4942d499c39a338
# Sat, 09 Dec 2023 01:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 09 Dec 2023 01:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Dec 2023 01:54:10 GMT
USER memcache
# Sat, 09 Dec 2023 01:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 09 Dec 2023 01:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff601679be7ba19260a77b326cf587dcc37315b02c2e0b0effc7084da4684bd7`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2401b35befb0832d96cebfdee6215736b27c0e3d064d67da9917deca4c14c`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 113.1 KB (113142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b1e1447b7739e5338731014a96bea369258cbf54b2d152ef50bb06e308bad`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 969.5 KB (969547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c62bb151b09d73f2bc083bb91abedfb6660c5045d34f7d576415190ae4e09f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf7e6dbf7fbf661d0b3f6f5d38fbd888ab6707a76919a5f4a633194e895a2f`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.19` - unknown; unknown

```console
$ docker pull memcached@sha256:1c2ba4c72ac494072ca8249e1368c9974cec5e63ff363b9da79930b7a8fbb5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 KB (96269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c33c986fa5bcf287e1c7594cc4bc4b13289d51ef15c3db591e513fcb7b653ce`

```dockerfile
```

-	Layers:
	-	`sha256:358b294b5bd4c90ab3ded38657baddb4cf8a5d594c5ea9c5683191efc2c70e05`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 77.0 KB (76967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708c671c1199a85cfb58a91ad4f1c34c29d381f2905468f64a42c8fbb6341e30`  
		Last Modified: Wed, 13 Dec 2023 00:39:43 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json
