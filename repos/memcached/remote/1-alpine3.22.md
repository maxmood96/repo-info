## `memcached:1-alpine3.22`

```console
$ docker pull memcached@sha256:7b45203a99eb1419c95b875c7e48c5a9eebc0a305eeb09eefc9f3a2cff758a46
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

### `memcached:1-alpine3.22` - linux; amd64

```console
$ docker pull memcached@sha256:e319c3f1f6623fb2caedb14c4a5c8594f88736d90dc89d19f1ec11c8533ee263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70bce40b6c41c7484f47d1d51e8be171c582e0b3e18f2379dd66e49e3178d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c711f2e2fe464121135109729faa513b79413712df200207ef35dfb19e550ca`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0cba00095a1ab15ee2ec0bcefea9c1fe601b9533d47626ab2fb6b74bf8a770`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 104.7 KB (104727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9204d372b3172134a4f3bbcf654ab17d33079a3aff6930e16fa7262df7c9cdbe`  
		Last Modified: Wed, 08 Oct 2025 22:42:05 GMT  
		Size: 2.0 MB (2000281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9dd6a61433e778f70df6cd37bc70c4dcbfa8e0b0e8b1f9a0fc2f993c78685`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5a283c3ec8e0142f3f4b0b17b2901ab6d7dbff9e3f62bf978a03e5d31833f5`  
		Last Modified: Wed, 08 Oct 2025 22:42:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:1cb56f4b692737cc136d1ff3c5dc0ca16e6b7c3be7023b1a9214348578dc4536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 KB (116754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7a80cd482b54ecad43450e81b2d6858d2397277cf2d8358315295ef8152dc5`

```dockerfile
```

-	Layers:
	-	`sha256:659cc6afa1cde9acfc6444a310575d263f25f2f83d4987d4fddf83e5bb0d3082`  
		Last Modified: Thu, 09 Oct 2025 00:34:37 GMT  
		Size: 96.2 KB (96180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43c8201b9a29cba2a3392f6a10e9ee6f0d6295f0248c8d3e9a792871224ec10`  
		Last Modified: Thu, 09 Oct 2025 00:34:38 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull memcached@sha256:43072fb4c4cfd652bf1a32d617dd81060515017e52b14f35faeb2fe26d071dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5557528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87416926a00e28eb0313c62e942bea0ce0517d67c95df6258358f109a49d392c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd90c0f65a0d79d1685d8fefb0f95b02afd962d0b160a1274598cb584ec37d9`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920bb020947e8d1d3b077c6d9861f8953febeb54f94421c689d40240e56b7ff0`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 101.5 KB (101532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc3dc5cf827d37f28e2a9a6758089ff72bc10d1915dbb61cce8f30350de40`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 2.0 MB (1950567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2afb9c93ba0497cadc25e69b15de772b64456929b70dbe23c7ef54faa3815`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88088c7b652b283feabfeb2974fb4bd7140ebf7da94c5d502f22841f26eb4a`  
		Last Modified: Wed, 08 Oct 2025 21:44:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:bd27295997fc0e77ad410a3e638c230d83e3d366906a449f5349d8311d72e657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a474656b8df51a30dcb397a44bcb48c6ba3cb76e49cc3a108a15a662cd64c4b`

```dockerfile
```

-	Layers:
	-	`sha256:9a80e6fbb7fc2254a12359760da6745c28fe1d3fa2367b1137aad71c6732a8bd`  
		Last Modified: Thu, 09 Oct 2025 00:34:41 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull memcached@sha256:2caa01f7607cf1d95b2e261de80716a27de4077bf25b9dc623688091b78bf4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1be64fe03e8832bc6208dfced118762e57dca6b55b4482140c8fc3b06dfb3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a02f5bd6bf63e96f5b45eda4849003b01c41b23425e7ac5a77eb01b5391e0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f277f740301c69a561a94545bc7f140ee2d5f4ea87f88c0c861eb7b4f7983b0`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 91.3 KB (91313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e9ebffe0c4c57cd5b7fd1da1fcc7f14e2e881a81673f81e8bde4bf662a45b3`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 1.9 MB (1909853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46526f6db8416530677567eac97b5cfc18e2b86ec5c930d06de26b62f0c7a5c6`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19627fe74f6edf1d0aa4deb85d035125067fcd28b2ee240aeb110e48330f19`  
		Last Modified: Wed, 08 Oct 2025 21:45:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:09108dd858c6aae1c834fd9c8a7f9f78e552673ee6296d9f5cf2d84c0c26c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 KB (116969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9755e3f89f06272910c7fcbcaf44a3cb373b551f73bc7c9dc6dbffe13aad48`

```dockerfile
```

-	Layers:
	-	`sha256:13ba800aa65c8f207645e4069de55b11ad0a2dc87b951414df4bd35ad3923afd`  
		Last Modified: Thu, 09 Oct 2025 00:34:45 GMT  
		Size: 96.2 KB (96248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636139066de216a683805bafa6cd72b23f1754f8dd2b5854e61578a684260418`  
		Last Modified: Thu, 09 Oct 2025 00:34:46 GMT  
		Size: 20.7 KB (20721 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:03d8054231ea1bb1dbb54d7e8bb32449b95c35475fa280a9b12d78219822fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42028500064e9ca7d32291ca01c636547943d3a6e6f11b80e503166efcfa6149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098f75f9dd9f7dbf0e5993587a5b4de796bc9c01f2e795b325f1e22fe66c6833`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c130fe47b24dbff1989543c440e0d6635524f9bf84473a6dc37472ecacac0`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 120.8 KB (120823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a41614e1c7aff72360936c76c0218330a487dd6ff6779cd243ad1c60ab6634`  
		Last Modified: Wed, 08 Oct 2025 21:31:15 GMT  
		Size: 2.0 MB (1991055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8573d5df234537883a638f95501925286c3367fd1cc40a4c6a80b70ef59ffa16`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6f77485828d14a277cde4d3649153b058047ad8477c919e974016eb3ef6f7`  
		Last Modified: Wed, 08 Oct 2025 21:31:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:b47c7c82754dea9552416b18a213b43d6824105eb9a0318e31789b64ebb4524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 KB (117055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0f98e226622d3dd6ab1b57679deaa27c10decc2a26c0d7c64feeeae3b6e18`

```dockerfile
```

-	Layers:
	-	`sha256:949b28585bcee0143420765476ff3f8231f4f8049c4d0b3136c102cc9a3b272f`  
		Last Modified: Thu, 09 Oct 2025 00:34:49 GMT  
		Size: 96.3 KB (96284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c10e36727f7634ae28cb6de04bff91b38d77420fce24cf9b31503d14aff0636`  
		Last Modified: Thu, 09 Oct 2025 00:34:50 GMT  
		Size: 20.8 KB (20771 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; 386

```console
$ docker pull memcached@sha256:3dbd66df3fa527ea9d5ef8e15484f90fd2bc4445e9d21ad40602c7d954a57c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2b9eb15af4ed95101c0752bbde283e07e28adfed081d3a9a731aa82d1ab68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5efc90d716eb56816bbbf625c914fe13450e5c8059469e05eaef18ddf200fd`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795865ca1e6e3ac4e3ed32dabe363301a453512615868e180c6c23f28f711154`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 109.5 KB (109526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93c274afbe9d7756256b49ac152cdbd8b21b7bf4c0e1a564bf36c6940e986e`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 2.0 MB (1962279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8db2caca7c819c90101fe1d4c62396dd78bf9677be35f005e0026d6b76c095`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53143d130829def781c84b33cfc19fa4ac216deae7acd8c510186dd525afdb`  
		Last Modified: Wed, 08 Oct 2025 21:16:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:c7b1229c17eb2270b6a966423e63e1ad70b16a7c79c87d2ea9df82f9d733d383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 KB (116649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392076445efbd53c3eea2f14c49336ed1c8f521c209369edbb2e7686671c310a`

```dockerfile
```

-	Layers:
	-	`sha256:e91e563cbe752ee16efaa2007b7b0f49392b0f5326018a94f34a2e187c1cb743`  
		Last Modified: Wed, 08 Oct 2025 21:34:33 GMT  
		Size: 96.1 KB (96135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207733714725a312d472d7f8657279033f48a213756c3f87714f3b4bd3e03195`  
		Last Modified: Wed, 08 Oct 2025 21:34:34 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; ppc64le

```console
$ docker pull memcached@sha256:7e2b422eba145439e8c30b7e3191cc1f8498a721f4ca3d90c31fbc5ed80aee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5951257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48257955bab73ec394b46e2350210da8ec488c125ff0c7cb4ce03893fff291d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8caf4ead4d89e7cb932248ec2c3e7ae5ee7efb8989eb2ab51d407f7094fe6bf`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff948909dcd7ac6c4301b934b30465617e899ca99e5cb6ac6e537be4e6f6144`  
		Last Modified: Thu, 09 Oct 2025 01:11:40 GMT  
		Size: 124.3 KB (124318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c3c0f9d01825484f8ddf4ea689855d4c1ed78848558c4c2bf8bf817caed0`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 2.1 MB (2093342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee4b65e8fe80e2ad3919c8c15d8855829430a43445decbd73237095a9771a9`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06240440b6e443402b0a5ca4dc97a2225661f3da03b4c6bc67c2e9443ba95ce4`  
		Last Modified: Thu, 09 Oct 2025 01:11:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:ea61cc67a9e9ffc7a8aaf326e701ea53f5d074dc907d4ad89b4274c4cb8ce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213afd703e8e97590346c2a301a08bd84f590c17e18aefcbcdefc4d93622c57b`

```dockerfile
```

-	Layers:
	-	`sha256:d3b5325b8aa7c43ef1c7b6f6f4a09cbcfd07d64d439c41a950bc41da09e060ff`  
		Last Modified: Thu, 09 Oct 2025 03:34:33 GMT  
		Size: 94.3 KB (94287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd52654f2c500e460030d1f9328acbf6d095a5e2d004a4f6417b79522c7fddf`  
		Last Modified: Thu, 09 Oct 2025 03:34:34 GMT  
		Size: 20.6 KB (20647 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; riscv64

```console
$ docker pull memcached@sha256:588117152fae8688e5cee8aa65963a1adb1e3851845da5da3e18c80099cdb1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5559076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c983e214f48d62c0be8ffbceb2a86b504aa71c02ac195047119fe264f612c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec1911f91425f5b1fc00d35f661d0dcb2691cdbff9a0ea4a65789eb8dd9b89`  
		Last Modified: Thu, 09 Oct 2025 04:54:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577a02d7726836381f3dfcda7cb11472d8e99ef2feb088a9570bc2c0203f15`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 107.9 KB (107909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6a77fdbd897c87616b71f12d107a1db186b3944ccdad6b89e33186d2645bf`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 1.9 MB (1934579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2879148828c59fde0e744fb56e2490c68a2e98902f3c6a0d01bb8381588a58ba`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00990bf09cdd6c9e756438f8b076739cea749be4889b317c88bf5d06c908e9d8`  
		Last Modified: Thu, 09 Oct 2025 04:54:07 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:da1dc0b73e866df98aacb962264ed5b50bf3f61862f76c42828b9a179c32e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 KB (114931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8b102978a5d01b2e4ec0cf55dd00df9776a17f5f31b8bae680908b73d2e1de`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c9249a94130556f0db88a655ed432c15ad40e151579870de604725fbc086`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0262f9b3a73d1455147e4436e4bf7da9aa19a7d385d28a807688e23d6a1f1d05`  
		Last Modified: Thu, 09 Oct 2025 06:34:34 GMT  
		Size: 20.6 KB (20648 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.22` - linux; s390x

```console
$ docker pull memcached@sha256:ed5969236f4728c97696471e08c88864c21019ea227118b3336d6484ed3e5b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c049e21de6c2be2f58a69ee9eb633a51a0491febb4b48fa476556586ac0fbd96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 29 Jul 2025 06:54:12 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN apk add --no-cache libsasl # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_VERSION=1.6.39
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.39.tar.gz
# Tue, 29 Jul 2025 06:54:12 GMT
ENV MEMCACHED_SHA1=132d165af4d032d97081a2ccda645595d6bbb17b
# Tue, 29 Jul 2025 06:54:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	case "$gnuArch" in 		arm-*abihf) export ac_cv_c_alignment=need ;; 	esac; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-proxy 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc" || make test; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 29 Jul 2025 06:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 06:54:12 GMT
USER memcache
# Tue, 29 Jul 2025 06:54:12 GMT
EXPOSE map[11211/tcp:{}]
# Tue, 29 Jul 2025 06:54:12 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d91bfc8fa88993cee87c33ea18494c5e9f0ad8e5b6f644411e9cd648982653`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a682e0d523bab9ef58be0ad290abcee8563e45ceccc9d04fc9b47308aeb709b`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 113.5 KB (113502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fe3585b1938fd376ffbce3ef824ed7bc20ed49039f98e279ff5ab6159b81e`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 2.0 MB (2040430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870bcfd315f7fc77b2fb8e80646695f277bc2e7689cf73b395e230aa6fe327c`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20f8ef4bac131999b759bd8b49d1474c540fb1874c8db4e3f4b21a7262b6903`  
		Last Modified: Thu, 09 Oct 2025 00:47:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.22` - unknown; unknown

```console
$ docker pull memcached@sha256:2d42234a0a18e44870f34c7796f717e9d61b56556ba027f9fae085adfbeeb7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 KB (114803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd89a980babfe6204633d40fbc2b82da6c42a3c42f43f980c4d29d3015fd40b`

```dockerfile
```

-	Layers:
	-	`sha256:70fb18f0cec1c9db308335dffc76a505d0855256e74dd6cd73079481cccac057`  
		Last Modified: Thu, 09 Oct 2025 03:34:39 GMT  
		Size: 94.2 KB (94229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c95a382d7ff8c2fab05ba8609f8b69576ec785d085ed04e606445051336db9`  
		Last Modified: Thu, 09 Oct 2025 03:34:40 GMT  
		Size: 20.6 KB (20574 bytes)  
		MIME: application/vnd.in-toto+json
