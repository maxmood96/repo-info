## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:0215e40c5e367aa0c1dc9533e2f14b523f527b3b5dec90ad0c37f3b32ff1e0ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:bc62c9b146672d0f63f0b3a38722acae32e859f635e6f32f0b31afdcb1013c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae0d824f4bc7874b3fd26fc5e61b2fe8c3fc9b58f82f3be24a6010c05ec1c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89cbdbe5025b3c7d2ff8f9f6bfbb7bcd639adb35200de6f0b8b4515488f1b05`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 103.8 KB (103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139dbcb2579cd1e9f78db09fd279e08d323c219a6efcad878b42cd961d24a25`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 958.8 KB (958765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3487c95e4eb9d8fb5506b2cd3406c02c1fba592fbafe1078c141420c22939fc7`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf1d2da7366110dda884212201a67c62fb0f9c921217de86755d35b80fbee9`  
		Last Modified: Mon, 09 Sep 2024 23:04:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:c96c825ac5a6f1db0849694d7878693b7113126e5c85540cdb4e191454d0afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 KB (107135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3dddb2bd6769fc79a77da8e93edcfe6d98d55badebcebbc9faaecb661ad001`

```dockerfile
```

-	Layers:
	-	`sha256:7102ff71a3580f59d96136c579e83bbb7e913951d315d57f5d15541dc8438bdb`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 87.8 KB (87785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e083725668b94672a9a645717ffd665a9f0059d9823eed6b8b1bc89bee285c4e`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:93c51fc832f2fb19b7beb41f69d4824422c541888aec386eef016dbea5bc29ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe802bd19707a473aff06b3aa5c130fb7f731c85d6ffc5b5eb258aa9807c763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 00:54:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_VERSION=1.6.30
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.30.tar.gz
# Fri, 06 Sep 2024 00:54:10 GMT
ENV MEMCACHED_SHA1=6482b69c80132ebcbd91cff63b4bab2a3b2b8f7a
# Fri, 06 Sep 2024 00:54:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 06 Sep 2024 00:54:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Sep 2024 00:54:10 GMT
USER memcache
# Fri, 06 Sep 2024 00:54:10 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 06 Sep 2024 00:54:10 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04310511d0b87f77a431a5f50ac0c3d95896d6a39a16aa043ba443f6b0e0fddd`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b28609c2d169047004bf72890ec5ac9e3a88bd3aa153e465bf17c14f3ebf3b`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 121.0 KB (121024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7575f758dbf5958130651b01d475e5d49b07a3679105685c425eab4bc4f3f70`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 962.7 KB (962688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ed7a67beedd2671827612ff7360a9b468f5013d71480d8556cca7bb87845b0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3269d7f10dce335766e60147c2d559e1a198769982853881ab2a430d71183c`  
		Last Modified: Sat, 07 Sep 2024 05:30:39 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7c7aeced35bc289be819f7a72a8d5a0175761312965dca157890dfc348349e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 KB (107587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a742548ebe52eb525b2c6fc032137414ef7044dd78ea6b3f203de14f67b5501`

```dockerfile
```

-	Layers:
	-	`sha256:622fcaebe9b8cab9d45a5d8414ea364a76a3f136117a1055989a99f4351fdfa0`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 87.9 KB (87889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92279bdcd5d388b338eafe380ceb49218383e5fa9d9af7c26f02edc9fc7a45be`  
		Last Modified: Sat, 07 Sep 2024 05:30:38 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:7228773d86ac6e8955e5d2d7ffefc2ae564b00cadd0c858310dec50e9fad6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4531177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f22aace0957bde9cbc95b95320e1836991afac8a43e215d16ef141508788c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e2704d07ea50e4350fc30a778f91c517bee857b54bcc571b464e2b563744ab`  
		Last Modified: Mon, 09 Sep 2024 23:04:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4ec43894c33c1d68e1fbb24d27f314125a8617ada637af061725989f14953`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce951cfcb336fa2050f3422e487f515d16ddcf2c69c80d29d9f66baa9d16e`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 951.7 KB (951692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfaaa1bc534e7c46c1b3aa67465a41ca91d4ce83071caebc7a11e3ff143be02`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615a81d8e335acdc6d68eefcf35b5d516a3cc0ed68bac6adfd5807799b53f46`  
		Last Modified: Mon, 09 Sep 2024 23:04:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:7940458999ce753465ef3f968a9eabac518a9df3d5d77386552d3526c2b946ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 KB (107035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2e327ed8d984210e8a47612bf76565fb47b80c1d0e63bbc53b45c571fd09f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1c9fcdee5d34fae3276a06573fa1e3d9a3a0b6d532765266d4e86f6be9a695b`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 87.7 KB (87740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c78394468356d9d60cea99380a31c53b12f50a43699c3916eda41ba6ee3470`  
		Last Modified: Mon, 09 Sep 2024 23:04:43 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:517da247dc00201621112cd48487139ce6966636899a4c40fdb02b307f3f1b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb649600a0e4277874d7abade7034b99d425dcb34c55e165f11569d4166b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645d78667a8075f56004a7a283eaeb1a630309a9d950a27de5cc29eb72cec340`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844b90ee5623766614a832d5e5f322566849ed5853adfbe1f63e8d954b540d9`  
		Last Modified: Sat, 07 Sep 2024 07:05:29 GMT  
		Size: 123.0 KB (123003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b715436c927b60842b1c1f98f7cb7c4257838f7b36a5e2334b5f590ca152f6`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 997.4 KB (997389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad232e17fce60e215c458fcac12f4ac1d5bdd60080527a4c28d76c6c831393`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e18c99726667f58640d52458967d66a4da28b7f2eaaac5626723a6691ed45`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e4e8b6df3a60e291797c10897a7779345a41715ab61dfd7f76bccdc42ef8a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469f18677668b4dd9a3de113d4ae3f111f5b89e03f3795cef6eab0e1e3eecbbe`

```dockerfile
```

-	Layers:
	-	`sha256:f7beb1e9f1753005bac3249d305c8567220853e93353216074762ad7f1813c0a`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 85.9 KB (85889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea735dc745320130c1139867abe3e0b71de840a5a8a3170b9191994b69b01b`  
		Last Modified: Tue, 10 Sep 2024 00:55:43 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; riscv64

```console
$ docker pull memcached@sha256:ceffb56b913ca8a62831ef271642b11ddbeea098de65d093af55cbba0f8d56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c258ae7e36ddd3758d8ddff147c4db3f4928f4db92f67bc7b91ffa68c86d4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Sat, 29 Jun 2024 00:54:11 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230af89e5f8d3eec0e6d96c87e99a85b938e0722dacebe0009ad7b8b00ca320b`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75b82861f48f0052a86f16f944c0324ed20af856a4c9d87c147dc645460ee6`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 108.6 KB (108596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d23c6553fa0ff65e57ebc39080a958cc4d1d02587781c94836137d124c47ce`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 947.0 KB (947030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab42ab26d315472c0f9433b5c7f25e0e426c020b3b0e8cc52d1c7d09ca7bf91`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436e8ed56076dff056e7dc989a1944739cb23a96400a543900ab3bd07a77b6`  
		Last Modified: Sun, 28 Jul 2024 15:58:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:fdf92c6c75f08244e376b28b33307c9ea75a07f7523b56b86df44f1be3335f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 KB (105303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc24bdd15449aa6c8213cd2607de7998a598edba9ca2fb7de80b4b761b833a64`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3dc8245856acbf66987c1cd0f4f37d8af7b49bc0c7b8eaacfb02321594ac5`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 85.9 KB (85885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2359a9107230c13ad5d1c580fc348790129c58ea95b407db376ee7eb5a109571`  
		Last Modified: Sun, 28 Jul 2024 15:58:49 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:a6f8155d863aa33eae871b75e7543c04404c30248007928840beeffae2eb5e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4556594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63fcf33c45f689bdee882ed4ad8692b55a55abe13941eb4cc525adeafab650c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_VERSION=1.6.31
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.31.tar.gz
# Sat, 07 Sep 2024 18:54:11 GMT
ENV MEMCACHED_SHA1=85e2cb9520beba71d7fc69f5717208a57facde28
# Sat, 07 Sep 2024 18:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 07 Sep 2024 18:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Sep 2024 18:54:11 GMT
USER memcache
# Sat, 07 Sep 2024 18:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 07 Sep 2024 18:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc58d10317d926d80ab2de5020728ade9434725004663fce6207d95ecc3ba0c`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed425e517c8a02d89379669853a47dbd343281c3fcfc3e37f91b671f0b35ffc`  
		Last Modified: Sat, 07 Sep 2024 02:51:40 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fe29c4e792447391a38d4b9d7aa18f9a51d6f171eb15297a427efb6a33e839`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 980.9 KB (980896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffd060f2e26e85750706fd829abf92d787fdf9321cba829cab93f30845547f`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93825c9e15b3ee5a0f3ebddccf232551b4506353af049da3e37f7ae97e39a384`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:5c62ae13354b08074917592e56f436a96d4ccf47cbf5c4a13231f53d556be814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 KB (105181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0c239bf944625a0bd5aeea27175b74c697a79c4b068f9d8e137b786a2b4a4`

```dockerfile
```

-	Layers:
	-	`sha256:870d5efdd4242eb6cc01519cd2092666c5ab15b546cb69d2711791408721605b`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 85.8 KB (85831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbbbb69edb2b376c21146fd5c88b6254433cc9264976b2868973688bb8a95cf`  
		Last Modified: Tue, 10 Sep 2024 00:00:56 GMT  
		Size: 19.4 KB (19350 bytes)  
		MIME: application/vnd.in-toto+json
