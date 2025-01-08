## `memcached:1-alpine3.21`

```console
$ docker pull memcached@sha256:03cea0adcd7595491cba44399087f6f401c8c94ae884c6f1d5f00f04a9f7f31e
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

### `memcached:1-alpine3.21` - linux; amd64

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
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
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

### `memcached:1-alpine3.21` - unknown; unknown

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
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 93.6 KB (93627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d335515fbde650b85378200ced749c54054a662b77a34ed8ed62500990e9b`  
		Last Modified: Wed, 08 Jan 2025 18:03:20 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:a2a51385054ca1194537458beda60209c8a5adf44c8eb0f24a276beb861c05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a3563f06e0e3578e09ffbfa95a5a4474085d9ff6e4ded4751c2811e01f640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754dc9937c8a1b6d9c8ceb98f89650cf15eedc5166771088d7ced55a6c922473`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda0e670d0bb60513dcc44b5011ae0fd97f2534d44ab71d774013e4dd17ceaa`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 120.8 KB (120776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a27373c912c1e33268baa8727eeb07f0dc36bb279e793e7de2909aa4928ff`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 961.2 KB (961250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd3bf8e4bf24607b0e8f2c2d9d3bfe17f4171e3b73d39f59135eb971d0e9903`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bddb8bb13a1313700cfb399b6a9d14778290b7da0bac513ea07d6293c428cdb`  
		Last Modified: Tue, 07 Jan 2025 04:20:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:a10eb73fdf98a5556238c57963229be67ccaa3780702e2062b7157db710e0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 KB (113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88433a59ed21e86f6d6cae38ec2c910034cf5f45c627d8a72efbf3f6f1e3df9b`

```dockerfile
```

-	Layers:
	-	`sha256:a983a114b2609c5d8a45cf94d45671051f9e6c4feefce5006e96aba713d8a094`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 93.7 KB (93731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:149ad9f7c01212b10522e1368bb782a41dc7358e4b842e0d232726b562392777`  
		Last Modified: Tue, 07 Jan 2025 04:20:02 GMT  
		Size: 19.8 KB (19768 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; 386

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
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1247b601c3e53be28d705421dcfa8334d532711cf382269d8f21563b07fab56`  
		Last Modified: Wed, 08 Jan 2025 18:02:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

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
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0f4870afe3634547a0ab0797766bec959c50766406f8127643b52bef01290b`  
		Last Modified: Wed, 08 Jan 2025 18:02:33 GMT  
		Size: 19.5 KB (19513 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; ppc64le

```console
$ docker pull memcached@sha256:14b386859e4c095e65ad6d31b763bf0a424849e45f246a67d5b15c686a15bcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd011e3b55f70a0a8feecd23e228fdb888799664aee64e94f3eb6ede02bbdd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290886131baa908c93701fedb00593a3479cfcbeeccc86f0e0c874247822b91f`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cf0939cd518c7bf0f259452ecc1e1e78500e007525a133c1f53d58f1cd331e`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 124.3 KB (124274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0aa50af8dbd0f30a1199a5350608d6814ca1d7dff1c0992d68b298529d9bc9`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 1000.9 KB (1000854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87355cb483c63a6ce0108fdb11ce9681ba00060582c73038061cea4fcce645`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400cd49b1cf1452efcf83a0ab27f1302f2b88dd0648867a74131cadd045d3f`  
		Last Modified: Tue, 07 Jan 2025 03:50:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:ce62b9a413aa6bd377420c8dc9c4f9a9cb494c341eda0b997aa88efbd55bfe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 KB (111380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a92f0fe14f77bc6e10338b31e7974d2995ca4596e7c0bfc3eff3b6bf4d3e53`

```dockerfile
```

-	Layers:
	-	`sha256:4369d0a37135f9171dc5b01f0b70f1fd517e76a9e6db86a161177f3ddaaa4080`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 91.7 KB (91734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0061e2ab574d9bc797f5f58ae906d5d2b3863d2cab983647bf4c60f14a978f65`  
		Last Modified: Tue, 07 Jan 2025 03:50:13 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.21` - linux; s390x

```console
$ docker pull memcached@sha256:c232a990ac4a91a70e3f45322d7336dbcc74b6662949b6e15a945b16defad2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4558078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf6733ae3feb8513d691d46447c8fe9e1d456ad8a9d1ae3c0c0b9999671b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 23 Dec 2024 07:54:13 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113f2215779e43664b85ce27026aaedde13356649afeaa43e6de581f176cca8e`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bedf907f7d4d338a818bdff540814f4223df95b6e8c894db38013d84bd06825`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 113.4 KB (113447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187bdc90e65d14ce49260a440eabe253202e8009c82822d2a2ae87435661984`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61020e84997e1c9f362fb276118354556bbac4992e21dc07e677ce8a2008f`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbab7a81d32530b6a5b22e33596ca2f37a778aeb7b931fc6786dfb6c8e77cee`  
		Last Modified: Tue, 07 Jan 2025 03:45:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.21` - unknown; unknown

```console
$ docker pull memcached@sha256:b663774aabd2e319d65c058727ffa7df05477e1639132fb27aac9bc902b97b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 KB (111247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396afc78bfad1b4e0eb6724c8d6ec202b4009bb26ecbb3f36198c656ea0ecad`

```dockerfile
```

-	Layers:
	-	`sha256:b3261506c2a4652d70dd2350cde0b5eb34d5c5630540ae9aa9f64712854829cf`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 91.7 KB (91676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91089a30c3ef17d24955d64bad919e17251e313870e4c73e2dba517025a86927`  
		Last Modified: Tue, 07 Jan 2025 03:45:22 GMT  
		Size: 19.6 KB (19571 bytes)  
		MIME: application/vnd.in-toto+json
