## `memcached:alpine3.21`

```console
$ docker pull memcached@sha256:a3014143bcf49e7ed690e3f769cdce74a28c37bc87af95fea519bb5b66d155ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:alpine3.21` - linux; amd64

```console
$ docker pull memcached@sha256:8fb252ec18664ddaad51976221b8166cebe856372b49ff4284c266806eee0a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f0f9f9e16eb8387a228496c5f1b9a391292399a7d47612cf27d8ec56dd7170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c9e7be82bedd08632d8a6e1ed6660e20b40d99a8351d1d0efd137a217f33e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb36d3941d5ec767386d4c07126459d3d6437a2f4e2eb313d3e5ab88ba1e86`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 104.7 KB (104691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd02828bf8a356f22e0d2c06f65cb46edcd9fb9a1859618687becf629ffb349e`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 969.5 KB (969496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51c3fd5e82d06672d91425a9ed3476bd895ab3ad3a90986f725607bf8db92c`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef552d6262d9489e6a2527088507a296c2b2c0a63cf8533704ac17e50a71e536`  
		Last Modified: Wed, 08 Jan 2025 18:03:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ef791a5ccb3a3dff208178acc0ca05896c5d2d4fa998d3e1996615ae6c005df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 KB (113198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ab962c574455ccd95672e81e19c81342f4056e6685f30c44404ea454fb2c9`

```dockerfile
```

-	Layers:
	-	`sha256:b4db51081b32b07070120e23fd4c606319ee1fb94b91c365793ce500418fc4f7`  
		Last Modified: Wed, 15 Jan 2025 00:31:22 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 15 Jan 2025 00:31:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:ed88720dfc7bcd7321f8c3799fa42f2477b5bd338c879d14c3f04db976723cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84541804beee41a1060c7486f9f048cc8fedc60c13d45d8093b6643907372bf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0979e295332f75d4524814a95c369dc55735c1485c8bd3ac5e63c3142a7de`  
		Last Modified: Tue, 14 Jan 2025 20:43:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ec0507e3a730e450610222231a332075d9b4cd0e904bf08795482c91bbe18b`  
		Last Modified: Wed, 08 Jan 2025 18:42:52 GMT  
		Size: 120.8 KB (120777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b374bb3d403b6e3fc4c1817a3eead8f8e8b8eb9795ee387bf7b2110786baf94`  
		Last Modified: Wed, 08 Jan 2025 18:42:52 GMT  
		Size: 968.8 KB (968832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c570c4ad692cdc30c2cf9277eaa2d6bbe4d35677f6b7e8180ecebd73026236f`  
		Last Modified: Wed, 08 Jan 2025 18:42:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f34a74e4b9d18b3636ff74a2e35a7be0dbbe3c711c79a050024bea4a48e91d3`  
		Last Modified: Wed, 08 Jan 2025 18:42:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:aaa8223d819e7f22f78f73d18ea8bb43fe9e7471bc3ea37bbc5d9d93da3d4965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8447e85b001e22fcdcff2106989a0e9ae350987409c7bf4d6bc65d104918cd0d`

```dockerfile
```

-	Layers:
	-	`sha256:21c3e00b70d1a7bf2e41f6278deafc130e637256453b8c15dbf726cac1fdb9c3`  
		Last Modified: Wed, 15 Jan 2025 00:31:31 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27176949f194c885ef6cd3bffd0dc11b2229c357e2d38105d4fd8b247b2828ba`  
		Last Modified: Wed, 08 Jan 2025 18:42:52 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; 386

```console
$ docker pull memcached@sha256:cef4f93c2a81b86dc5462b7f91311db290538001c94a65b0dff5dab45f50e782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4534771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee808b088b36b9870bc92f45ca1c470f4c3d7dc1f7fbbbe0154c30866306c9f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24637716b10258cffb7d459f9d7262325c4accd3344feea8a4bd6dcd34ad7c60`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1259373c849bb86038f1ac6c56d1aec51ff1d297cd0afde4d4b8c8b38b73fb`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 109.5 KB (109460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378a5315a9e5b732a5a5ecfedcbf394a983658bd81796b66914fc2d2832cc37`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbacb441ce2c644387c07f55a12156015ce19630d3056fdd0b258aeedf90429`  
		Last Modified: Wed, 15 Jan 2025 00:42:03 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 15 Jan 2025 00:51:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:e38f012378e29603b0d51ba1dff93559d223c23ba06b4d2722f6a8ef71cefaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 KB (113095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63001940ccaa994c0076c95a57363dc099712fa449e51c4ac8de153eb188f8e6`

```dockerfile
```

-	Layers:
	-	`sha256:548acc4f8ff40befc83e2f02157d505cc08fa1b5b32dedc992b449d64d22043b`  
		Last Modified: Wed, 15 Jan 2025 00:31:39 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:be23d79f25177667b0f529ba7196a76a700f095540eb33521d75d2f346eaf2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4706820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0498596fc296c753a5883cb35ed1b0dcc77d876f44aad78899e24dca39d55966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bfdcdae57fa9f3dd749ec7b7deab98ef83a687e717521bc47d688144027396`  
		Last Modified: Wed, 08 Jan 2025 18:28:23 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854529e5135c8c9117ff96b77014248d3dc971e0e38b95457860f5a9c2ee0135`  
		Last Modified: Wed, 08 Jan 2025 18:28:23 GMT  
		Size: 124.3 KB (124275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261aa117be614f2ab408e95cb070b13fbb637af8c21cb2c76a2605f40f3ede42`  
		Last Modified: Wed, 08 Jan 2025 18:28:23 GMT  
		Size: 1.0 MB (1007580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c681516ed62caa5d535e19972b8d1d5b4ab3b07cf6b81b12666f1b13fe79d248`  
		Last Modified: Wed, 08 Jan 2025 18:28:23 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0760d117f22bb132cae5e0a4264a09d8b2cb07798e800ad0fb6bae0a8b654331`  
		Last Modified: Wed, 15 Jan 2025 00:31:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:93a3b049d0441fc2e93d63c277825b03061e71c25ee11bd897fe84f5758f86fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653e6a160c6b3ebbb30710a873a0210f76838be37d50738df20fe9bb48c868db`

```dockerfile
```

-	Layers:
	-	`sha256:7b7a2d3a1a81083abb9192c2a9b0cf1ca1356cfb8f7ad52de7776258b73ccec3`  
		Last Modified: Wed, 15 Jan 2025 00:31:47 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac478c67f81e0a63d2cffacd12b23bda095a8d49295f7e366490352a425168a6`  
		Last Modified: Wed, 15 Jan 2025 00:31:47 GMT  
		Size: 19.6 KB (19647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:b7c4a3dcf862532d6ab0024fe4a8a3e2844297f57faa0f319c7302ead5e12b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4570777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52d12733e634ae53e5a1bc598c9a031f0e5f66d8f5ad86cd4a77455230c5f6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_VERSION=1.6.34
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.34.tar.gz
# Mon, 23 Dec 2024 07:54:13 GMT
ENV MEMCACHED_SHA1=d2a0a65b3c69147e1a4fe0b3c20308c40cc0027e
# Mon, 23 Dec 2024 07:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 23 Dec 2024 07:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2024 07:54:13 GMT
USER memcache
# Mon, 23 Dec 2024 07:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Mon, 23 Dec 2024 07:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc90fef26d878964da86f96abbb82676582e0b86b5bde8a281dd1c3df00b2d6`  
		Last Modified: Wed, 08 Jan 2025 18:30:27 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2308982d7b97360240e8bebafb115672c957337c6fc93b7c619e78cec4b92`  
		Last Modified: Wed, 08 Jan 2025 18:30:27 GMT  
		Size: 113.4 KB (113449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1784b2dc13eeb5d3dbe0a4705777d912b8797d9045bd6274949eb6a57d78aa`  
		Last Modified: Wed, 08 Jan 2025 18:30:27 GMT  
		Size: 989.1 KB (989100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba685c27753e036bff467ca3a5ee4f465cf29b50504091a5c0376651946a1cf`  
		Last Modified: Wed, 08 Jan 2025 18:30:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1386869afc050f9f4a8d0bf3448f67a486f6b331978eb7a5e631b20cfc685f2`  
		Last Modified: Wed, 15 Jan 2025 00:42:15 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:9686d95e10e5d05a9617e23877e42d2e196c5f9b3ac3e557a197a182798da80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3541032f653ff34a096e6c2cb91d0beaa02f44caebb6fae02c9c318b3a3a8c39`

```dockerfile
```

-	Layers:
	-	`sha256:9d3d55e53baf105c2e2bf7aba112242e6cdbee25e77a234a036bf0b0682677db`  
		Last Modified: Wed, 15 Jan 2025 00:51:56 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7383562a3e9d74cdd0ea7de194c29a28900601377f71e013fd1ffb3c215ab8c`  
		Last Modified: Wed, 08 Jan 2025 18:30:27 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json
