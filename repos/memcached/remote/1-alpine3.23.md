## `memcached:1-alpine3.23`

```console
$ docker pull memcached@sha256:27f8b7d01391f6d3c95d1dc1ce18a0071925340eb50a9181036870b3c9fa2546
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

### `memcached:1-alpine3.23` - linux; amd64

```console
$ docker pull memcached@sha256:947366d40559340a4385b3e05f92186b9546e7feb59ef280e243ec8bf34f01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5958530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977390ffe9a7f3b6d3c5840f262b8058ca015d7daf5237e480d3f51a29e0b6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:28 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:29 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:21:03 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:21:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:03 GMT
USER memcache
# Wed, 28 Jan 2026 02:21:03 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:21:03 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0ee508166c94a4f9ca8c32f743bd3733afb7660800042c7da03c2ea1da6b4`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bf9562ecbc21cc4f52d1a4d33eb5eec98aa63c36c59f018b55071b8dd9f05f`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 106.1 KB (106059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c6974a0da2f6cdd2022450be6195683245ba21f601d207ad14566c653ddea`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 2.0 MB (1989295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a859de0eb0253d066d7de73c90f4ebdc8b737fddab90420fd0ba6bd1c74669`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7be89a9ef60cc91d2346c9bc9a975138908bbc03aa40c948ab5e7336aa8e8b`  
		Last Modified: Wed, 28 Jan 2026 02:21:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7579a20056cd9531e754a57f957da811356775f676bfa6cd6e86b95f6de172d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 KB (115404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8408948e08375e96299e735072f97a85aca5d58f65fc7cca125dfe5389160cb`

```dockerfile
```

-	Layers:
	-	`sha256:533c466de2027803aea398674e5a5ffd7d67b9e1eddc4228741a130ff830b02a`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 94.9 KB (94873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c54b10e342535e2af7655af306fbf617d3dbf0922a7dd440f8ed4ea3e1fd5c`  
		Last Modified: Wed, 28 Jan 2026 02:21:08 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull memcached@sha256:3a1e785feba037614143f75204bac3225d838127c68805b29ff23df9d8638070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c891a4120404380161eeeddd4e7c7cb748eb55193453c6e9090a59909bf1969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:07:09 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 06:07:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 06:19:29 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 06:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 06:19:29 GMT
USER memcache
# Wed, 28 Jan 2026 06:19:29 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 06:19:29 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dfe3bd7930f213b1f0f6c2854f26637f5a52c7cd4796e9eb59071fe2ff4b2f`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707447698613ddcfad121290546b5d9e04e2c3194b8f59394a272fe30f42dba1`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 102.6 KB (102646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d366a66d67c4233b2ac1bc38363cb9881e63ca3af7f82ebbffbfb76942e1a34`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 1.9 MB (1939230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5326e5c6353c918ea1ac99aedfb19f688830f93037e66268b39c31f670e01`  
		Last Modified: Wed, 28 Jan 2026 06:19:33 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ead2e4800bd6e32bbdb6225ecb70b554d33b3c17f3e8b973890f3b3c532da`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:fd7fcbdf0e7f96a083f3d6aec29c9d21ac4b768be5949f68958c25756c153f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07888c8ad7065e17bfea11af8f4f20b5f956ab1b553160f5ea4a484c4e437674`

```dockerfile
```

-	Layers:
	-	`sha256:aed006a02d773c56c072711ddc729af9ce5001ab757071fc3abdc5094822e7c7`  
		Last Modified: Wed, 28 Jan 2026 06:19:34 GMT  
		Size: 20.5 KB (20467 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull memcached@sha256:f08c7e3ff92e718b22bc7b21385421ebcf4bf6f542b797690d6547506821ab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fc0ce35a3d59414018d4d8fe69929016a9e8dc7dc27daaafc617e3a7165d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:45 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:22:46 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:25:41 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:25:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:25:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:25:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:25:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61af882efa215dd577f7a17129442647756c535df9c13e821da864cddcf0e6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b88f23b7692bcb2301e4e0a862af10c70c6ec663fca9e0a3389a74a3ba0520e`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 92.4 KB (92374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549b4be8a16d49c33d6adaf28e4f8f7acbdea009dec2daed172741f7540ce5a`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 1.9 MB (1897188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6760f49ea55e45e14e26aaaf690948c109a5d85256175c84bbd06beccc8cd1`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fca934ad2088c9a34e9f20e65d902054dfb9accdb4c6865924dd1fa88685b`  
		Last Modified: Wed, 28 Jan 2026 02:25:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b5c2e8ac0b1fd0bd9c534bf163bad10efc0dc2c3afdfb66e3eb1a827d7bbfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 KB (114969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd20e2507c3ff3732182e3d2d44e5f7bc9b449bb172d5c7895b2fcc2dd423c6`

```dockerfile
```

-	Layers:
	-	`sha256:36627c0161ebd5c055e99a596a600017e5608e5895d1f95159116ff2df2eb3a6`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 94.3 KB (94291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5914862f1fb65973ac0def541c9da056e1a5ef0bb26623a5bbad81803a4383`  
		Last Modified: Wed, 28 Jan 2026 02:25:46 GMT  
		Size: 20.7 KB (20678 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:1a4aa193f53b5a4e2d82f6c67c23e87ef5d3d1cd1ddf96e0aabe73d49e537c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6286893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f275b1c508af04216ccc891e9de0d7cbb35441f4eb424197e529ddbfb1d1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:18:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:18:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:20:58 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:20:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:20:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:20:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42047232a88cba1fc4d173d71bdf04395f6e4b83472de9f225ae2dd70ce14bc`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b625b9113e283efad9a0ee8e305f08edfd38a6c015224459a1ec0f2f49a0b915`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 121.8 KB (121845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf057b1d31677325905e009d68a97c3741028480d8b254105b145f39d157f2a`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 2.0 MB (1966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db407fe2bd85342d8cb160bd73b5efe730723df2d20f2f6021eef8ad2d8f16eb`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfefb839a309e8b3df7a659236c09776f4eff9f8a47d9b331f131d9ad4c5d6b`  
		Last Modified: Wed, 28 Jan 2026 02:21:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:28b857747dd2742dbf00b9c1fc07265248073390d37bacf6cf8bfd313cf52a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 KB (115055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34aaccc9ca109270d86cdb6e46e56b207775ad700dadb1604f0a56b3ed4536e`

```dockerfile
```

-	Layers:
	-	`sha256:53b8cb56ae6a2b4c94fae4924dc03d881acba2e6c746fdb05808f3a86186ceff`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 94.3 KB (94327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03361fd0b86b6e905c14afa88e91f00f54a7e68e1d12d191b3d65c41986adc2e`  
		Last Modified: Wed, 28 Jan 2026 02:21:03 GMT  
		Size: 20.7 KB (20728 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; 386

```console
$ docker pull memcached@sha256:8c10f776d94f57c5e0a4807247add0a2f3638eaafc3f6571b66ac325cc251866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2329492e766d962366bfa352f931d82d7cd74d9e771ae6db7d44c1345197b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:16:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:18:59 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:18:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:18:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:18:59 GMT
USER memcache
# Wed, 28 Jan 2026 02:18:59 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:18:59 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb7a800485646296958fbca0c9cfdd5c397a0dbc2e33f1bc0c55dfca3c47a6`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651295f62c54da7297c4ef646e146ef0acac3f551fb8a3dccc49190efced234`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 110.7 KB (110722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87d7b2cf89ac568b76f6e27208734340c49f4d7b0fedb8e5ae16f54a0cadc43`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 1.9 MB (1942772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f82eada80af7ef4ec5dfcb36c5a93fa36157801318f374c5ab0d0987cd352`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61a034237824e579d4d24c5ec4b58ee8c400255488e658c36064d43c0001301`  
		Last Modified: Wed, 28 Jan 2026 02:19:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:118dd83c690f154abc02b708a01a0a0a48519b7faa920e5540ebf81c8e626429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 KB (115301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7e54c817c006a1a17af2f06a4b3e4d1816cb0051c626c3f5e18a5012224b2`

```dockerfile
```

-	Layers:
	-	`sha256:11c94853238efef3a0c48e7cc56222e34874215e568475cfb20d3f2394aad42e`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 94.8 KB (94828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c97d62051151c9b1528a1b64a558c48025170f167ba863808d5fb67d4c59006`  
		Last Modified: Wed, 28 Jan 2026 02:19:04 GMT  
		Size: 20.5 KB (20473 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; ppc64le

```console
$ docker pull memcached@sha256:3a553e0d4ee19ee930775d8f8848969c6ff96b11e6b20f159ad754d11f5a8f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcda9c1811a9129ce53ed17b8ca116ffbaeebc21da0604c23b90e0dd042b0aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:33:21 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:33:22 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:35:40 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:35:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:35:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:35:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:41 GMT
USER memcache
# Wed, 28 Jan 2026 02:35:41 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:35:41 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c501a178d8bd3c1966eb75a7610efc35f292a3662f9fa7ca0d0089f54f723ce9`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac221803a5094f2d41563eece02e2e93293557ecb1eb5b7b646bcf143abcb82`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 126.3 KB (126255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af754023c45f69e3c70d3b4bfad1459328a7922268883ea41f2089ffe32ac`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 2.1 MB (2076366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5df498426baf66bbc7701a67818ff6903c4420dc16591e79270ea8799caa35`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a9c7624c2d00490e93ff507b003a4b495513fa6ec61b766c50bf5ccb8e23f`  
		Last Modified: Wed, 28 Jan 2026 02:35:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:238c5819c270bbc55c4140407b62939bf6ca158cb58cdbda8098f069301739a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f43e248be2e248fe895fc3beccdf145fb06637800c6b89c19bf606d7c22975`

```dockerfile
```

-	Layers:
	-	`sha256:88da11471f4f95fd0f4679af21785a14ccb57b8bbd7fb96e4c42e1c49c333c33`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 94.3 KB (94280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1fb2f254a022e51ca3dae9140daca46922a20d56b46607f22f1eef757d2fbb`  
		Last Modified: Wed, 28 Jan 2026 02:35:54 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; riscv64

```console
$ docker pull memcached@sha256:9023f4a863c531a74c6ff8cc3b49c3be80ad1db07cc93fdcbf87c5d8e4cccc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2159b7b74e5ffe77e6304def07dec2cfc2bdead26c3012e1e4d39bcd267adfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:39:34 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Thu, 18 Dec 2025 06:39:38 GMT
RUN apk add --no-cache libsasl # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_VERSION=1.6.40
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Thu, 18 Dec 2025 06:52:53 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Thu, 18 Dec 2025 06:52:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Dec 2025 06:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 06:52:53 GMT
USER memcache
# Thu, 18 Dec 2025 06:52:53 GMT
EXPOSE map[11211/tcp:{}]
# Thu, 18 Dec 2025 06:52:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc016d1883c21894ae540944be0270a95cb663037e8592a944bac62e0cc39e7`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c580cd51da178bea3e44467f8b445f50ec9272e42e0254d269a9e38204b12dc`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 108.9 KB (108898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11881c79ebc6a05357f0e2095f00d6d5a8a58bd9f11efeefc80b616d0230ff9`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 2.1 MB (2074429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfa953d895df9672fe0b34207075bd7e686f71104973ad4e02d89db8719a9`  
		Last Modified: Thu, 18 Dec 2025 06:53:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8c865432ff9b07178ba7cb96426e0515b00cc91866fb4dfb8c243e4187172`  
		Last Modified: Thu, 18 Dec 2025 06:53:18 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:7cd6a8f4c278ff9062def241e6cdb501032ed72b091608a6da35812eece0954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b0c310a1ad4186c4beae0e268b71f1a80ed998cd80ceb81095aa9da7e6b02e`

```dockerfile
```

-	Layers:
	-	`sha256:88642ee1ee3c124ff8f2f640525172206ce9483620a70142ca673e0eca181c4d`  
		Last Modified: Thu, 18 Dec 2025 06:53:16 GMT  
		Size: 94.3 KB (94276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:441bda294fdd657b4574cd5337193125e3d0565433a700136501a858fce53d46`  
		Last Modified: Thu, 18 Dec 2025 06:53:16 GMT  
		Size: 20.6 KB (20605 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.23` - linux; s390x

```console
$ docker pull memcached@sha256:f52690bd1266bfbe887fa9c03fc963f0277f331a85d8e81f4f134076c6d899f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7903f118ee1fcea4632b09ffbabd30b82ef4aa3b68dd3570b1173f263cacc343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:21:01 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Wed, 28 Jan 2026 02:21:01 GMT
RUN apk add --no-cache libsasl # buildkit
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_VERSION=1.6.40
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.40.tar.gz
# Wed, 28 Jan 2026 02:24:07 GMT
ENV MEMCACHED_SHA1=f2513db7079ee4c6558eb11fabb55e1adf1fdf38
# Wed, 28 Jan 2026 02:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Jan 2026 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:24:08 GMT
USER memcache
# Wed, 28 Jan 2026 02:24:08 GMT
EXPOSE map[11211/tcp:{}]
# Wed, 28 Jan 2026 02:24:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f843902eb7c01da3de08b6efb672d46d4f41e9e298640c66daabea5d901ef`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100608bf5f6494395c46670a28e6df9d705e08dc9129c1fb36b8f265fa52c22b`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 114.3 KB (114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706c73349baf76aabbef50d7dba3c89b85ffc84ad0aca5c544b1fe047706785`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 2.0 MB (2017124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce545f5bb33e4374e2e0bb9b11e751c89272699812f06c49e8e6a2e5ac3d524`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac2e9e98ac3e799be9d54501be2f2304ef93065d34bef18f002ea38838ea24`  
		Last Modified: Wed, 28 Jan 2026 02:24:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.23` - unknown; unknown

```console
$ docker pull memcached@sha256:b4850489cf16ad5f72674b698ab0c2d16d95c6cc43e1b3f611f9fa67adcf4962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79deed0597f9356a7dd99d34cb933d7634c520350fcabb9da14b254006070d0`

```dockerfile
```

-	Layers:
	-	`sha256:00a586e58a4b437f0260b3197ecff606cb3380869c6861c89d769a99132c10e9`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 94.2 KB (94222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8caeef6fbf9d37a3d092d84298ef02b53e2efff54347431fcc362c14dcdb9eb5`  
		Last Modified: Wed, 28 Jan 2026 02:24:16 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json
