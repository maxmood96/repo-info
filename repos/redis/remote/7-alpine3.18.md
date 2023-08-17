## `redis:7-alpine3.18`

```console
$ docker pull redis@sha256:74eedd2ac6be8f535024b8d581b4b2c6d862d8f322e3621dddee3269fe90313d
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

### `redis:7-alpine3.18` - linux; amd64

```console
$ docker pull redis@sha256:336ff85d67e89689913130cd7334d5eb67783d0e94362c6ce76314161aa1f0fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12432323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c09b0364aa894b3f107b077db815da21e9a96d4fed7b517899e7c3b29c036bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:31:40 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 09 Aug 2023 03:31:41 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 09 Aug 2023 03:32:40 GMT
ENV REDIS_VERSION=7.0.12
# Wed, 09 Aug 2023 03:32:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.12.tar.gz
# Wed, 09 Aug 2023 03:32:40 GMT
ENV REDIS_DOWNLOAD_SHA=9dd83d5b278bb2bf0e39bfeb75c3e8170024edbaf11ba13b7037b2945cf48ab7
# Wed, 09 Aug 2023 03:33:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 09 Aug 2023 03:33:20 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 09 Aug 2023 03:33:20 GMT
VOLUME [/data]
# Wed, 09 Aug 2023 03:33:20 GMT
WORKDIR /data
# Wed, 09 Aug 2023 03:33:20 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 09 Aug 2023 03:33:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 03:33:20 GMT
EXPOSE 6379
# Wed, 09 Aug 2023 03:33:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28817da73beeabdf8ec3919ae9b26efeba0ab2eab533cd6c6e9a125cceb3f97`  
		Last Modified: Wed, 09 Aug 2023 03:35:24 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536ccaebaffb687f1a27e3b61a5eea07a0281df81eb8392bdbab9d045643cd9d`  
		Last Modified: Wed, 09 Aug 2023 03:35:24 GMT  
		Size: 347.2 KB (347162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81efa230a080986de141495fb7dd135310b0343a6d2d8c5a8282750547cecc1b`  
		Last Modified: Wed, 09 Aug 2023 03:35:42 GMT  
		Size: 8.7 MB (8681565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a325b46fd79589c9e8cc490314a2a644081c9b530f049597762e003b471861e2`  
		Last Modified: Wed, 09 Aug 2023 03:35:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7e435438caabd43efafa261ac0b46867b35ad4bfed4b3e915f5b97a3ddb87a`  
		Last Modified: Wed, 09 Aug 2023 03:35:41 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; arm variant v6

```console
$ docker pull redis@sha256:2160f3820e0dbb184db95d8654428b95e1467277eacb561b20efa3dc4806f040
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15518243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcb61a1e8a6982091fb1024021af9aa1e52f3fd0394c3975d57594fc5ead476`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:07:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 08 Aug 2023 23:07:33 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 17 Aug 2023 00:00:19 GMT
ENV REDIS_VERSION=7.2.0
# Thu, 17 Aug 2023 00:00:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.0.tar.gz
# Thu, 17 Aug 2023 00:00:19 GMT
ENV REDIS_DOWNLOAD_SHA=8b12e242647635b419a0e1833eda02b65bf64e39eb9e509d9db4888fb3124943
# Thu, 17 Aug 2023 00:01:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 17 Aug 2023 00:01:13 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 17 Aug 2023 00:01:13 GMT
VOLUME [/data]
# Thu, 17 Aug 2023 00:01:13 GMT
WORKDIR /data
# Thu, 17 Aug 2023 00:01:13 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 17 Aug 2023 00:01:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Aug 2023 00:01:14 GMT
EXPOSE 6379
# Thu, 17 Aug 2023 00:01:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12c77a3e53b4d4d92239da6e7f9f51be8e4d864b6034be8c0fab1adfbc60f84`  
		Last Modified: Tue, 08 Aug 2023 23:10:54 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7ba0b7e01a1cf4af8082d01f8d4e55b166351603ab6ab4303b1c38f32b551c`  
		Last Modified: Tue, 08 Aug 2023 23:10:54 GMT  
		Size: 346.9 KB (346941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9458baab06525f443ed9e1b4b25e49ba836615f0e004005cedeb456cdbeced`  
		Last Modified: Thu, 17 Aug 2023 00:01:41 GMT  
		Size: 12.0 MB (12024512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e6bf7de9ee79fde9f2b6b4bbcd145757bcd39bf044f14bc0ee73be0d9400ac`  
		Last Modified: Thu, 17 Aug 2023 00:01:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcf6fca3c37f4173694830bb951d739158974c924c9fa2eede9cdf1b44f7ec`  
		Last Modified: Thu, 17 Aug 2023 00:01:39 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; arm variant v7

```console
$ docker pull redis@sha256:aac0f7a8f042cabb3b6201ad02d8e61e720db3c7a90d9cf2c3486e617beb45f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11890486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d164381f10c006c1dde9747c551633e97daaa46abd8846887cbe2bcedd1dee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:11:52 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 08 Aug 2023 21:11:54 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 08 Aug 2023 21:13:46 GMT
ENV REDIS_VERSION=7.0.12
# Tue, 08 Aug 2023 21:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.12.tar.gz
# Tue, 08 Aug 2023 21:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9dd83d5b278bb2bf0e39bfeb75c3e8170024edbaf11ba13b7037b2945cf48ab7
# Tue, 08 Aug 2023 21:15:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 08 Aug 2023 21:15:03 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 08 Aug 2023 21:15:03 GMT
VOLUME [/data]
# Tue, 08 Aug 2023 21:15:03 GMT
WORKDIR /data
# Tue, 08 Aug 2023 21:15:03 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:15:04 GMT
EXPOSE 6379
# Tue, 08 Aug 2023 21:15:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f61e7688a65385d2fc7a6e60773b0d912f03a495a7c7c8b7bce21af36e0d91c`  
		Last Modified: Tue, 08 Aug 2023 21:18:18 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba711c78f5c39444e4c00f78a5e520ecdb2a31ce75bcc2f73bc2cb940ffbd6`  
		Last Modified: Tue, 08 Aug 2023 21:18:19 GMT  
		Size: 346.7 KB (346743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6e4b39fd81b2924315c897b7406edc8eb8429090600c37895d355bea39a62f`  
		Last Modified: Tue, 08 Aug 2023 21:18:41 GMT  
		Size: 8.6 MB (8642283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee8b7f56fea20a04154acc17ec369dda8d2ecdddca55f2a116d991d02c1ef89`  
		Last Modified: Tue, 08 Aug 2023 21:18:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1a513c2e4bfce032fe5f65dfc74ea565b584caac61423aeeb414fb3aea8748`  
		Last Modified: Tue, 08 Aug 2023 21:18:39 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:c22fd995c357fe52cef720675ccf0fe95efc0ef291c27b9e7d6a3ebaa9f6f836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12459098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea69a3fa8c0b9c8ef742866fd94b8e456ae9b1a6b8029d4c48b44627548e3e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:58:59 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 09 Aug 2023 03:59:00 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 09 Aug 2023 03:59:40 GMT
ENV REDIS_VERSION=7.0.12
# Wed, 09 Aug 2023 03:59:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.12.tar.gz
# Wed, 09 Aug 2023 03:59:41 GMT
ENV REDIS_DOWNLOAD_SHA=9dd83d5b278bb2bf0e39bfeb75c3e8170024edbaf11ba13b7037b2945cf48ab7
# Wed, 09 Aug 2023 04:00:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 09 Aug 2023 04:00:11 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 09 Aug 2023 04:00:11 GMT
VOLUME [/data]
# Wed, 09 Aug 2023 04:00:11 GMT
WORKDIR /data
# Wed, 09 Aug 2023 04:00:11 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 09 Aug 2023 04:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:00:11 GMT
EXPOSE 6379
# Wed, 09 Aug 2023 04:00:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808541ccd6854e4e93ed54aa9c6671d15164f7fbec805e132d3aefe5e62ca22`  
		Last Modified: Wed, 09 Aug 2023 04:01:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6a7a1ce6c85723273d61f7e9bf53458e79c1aea22fd3122b8a6b05e5c6cb70`  
		Last Modified: Wed, 09 Aug 2023 04:01:47 GMT  
		Size: 347.4 KB (347393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c703b0ef599c53c4b1da77c8652f8766f0da72f1285c47fd28d970642f50ce`  
		Last Modified: Wed, 09 Aug 2023 04:02:04 GMT  
		Size: 8.8 MB (8778959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be89014096973044285cfec118606493226225ee7fdd4e4bd0d36ef2ab05ff28`  
		Last Modified: Wed, 09 Aug 2023 04:02:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5db9f8b916c7922d3a7612c54d09580aa81b95c356f5f3fae2eeb04a15fa16b`  
		Last Modified: Wed, 09 Aug 2023 04:02:03 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; 386

```console
$ docker pull redis@sha256:ba8bbb79ebf0d42b688c820308fd464090ddbf35dd4d5e491ca3a915327cd867
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11904576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36451760f968b20505f0d970b7c033353f10784322798c3814167139da95a5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:45:41 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 08 Aug 2023 21:45:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 08 Aug 2023 21:47:35 GMT
ENV REDIS_VERSION=7.0.12
# Tue, 08 Aug 2023 21:47:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.12.tar.gz
# Tue, 08 Aug 2023 21:47:35 GMT
ENV REDIS_DOWNLOAD_SHA=9dd83d5b278bb2bf0e39bfeb75c3e8170024edbaf11ba13b7037b2945cf48ab7
# Tue, 08 Aug 2023 21:48:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 08 Aug 2023 21:48:47 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 08 Aug 2023 21:48:47 GMT
VOLUME [/data]
# Tue, 08 Aug 2023 21:48:47 GMT
WORKDIR /data
# Tue, 08 Aug 2023 21:48:48 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 08 Aug 2023 21:48:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:48:48 GMT
EXPOSE 6379
# Tue, 08 Aug 2023 21:48:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39173ad50c8b2bade620367f8a2824a9bb28697fd3eea181d4f3fcda4dd6509f`  
		Last Modified: Tue, 08 Aug 2023 21:51:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ff06a0a1f18bec9ab6d2e5360b1f22f83835341adc4b96e367d250d20f089`  
		Last Modified: Tue, 08 Aug 2023 21:51:45 GMT  
		Size: 347.2 KB (347162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c78055564ebd502061749bc9a7f2e5d2312ed4bf00643130f408e0ed174d7c`  
		Last Modified: Tue, 08 Aug 2023 21:52:04 GMT  
		Size: 8.3 MB (8320289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3abfc559011941eb74b4ac9eac43fc9cddaa433576ec658a6b71540ce8f23e7`  
		Last Modified: Tue, 08 Aug 2023 21:52:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a907309d4b3561420c4db4169d3eaa802799b33bd66d7f80f4ed955eacd2155`  
		Last Modified: Tue, 08 Aug 2023 21:52:02 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; ppc64le

```console
$ docker pull redis@sha256:12cc5a368845ef98e4c72a7b19f96e67dbaf79f4a7518683bc85aa4d4b50b1be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12967458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab348bfe00f99eb14f2ccc38d93054b95ca0b4d9fab8f93d8ee273e1a28d857`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:04:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 08 Aug 2023 23:04:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 08 Aug 2023 23:05:56 GMT
ENV REDIS_VERSION=7.0.12
# Tue, 08 Aug 2023 23:05:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.12.tar.gz
# Tue, 08 Aug 2023 23:05:57 GMT
ENV REDIS_DOWNLOAD_SHA=9dd83d5b278bb2bf0e39bfeb75c3e8170024edbaf11ba13b7037b2945cf48ab7
# Tue, 08 Aug 2023 23:06:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 08 Aug 2023 23:06:53 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 08 Aug 2023 23:06:54 GMT
VOLUME [/data]
# Tue, 08 Aug 2023 23:06:54 GMT
WORKDIR /data
# Tue, 08 Aug 2023 23:06:55 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:06:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:06:56 GMT
EXPOSE 6379
# Tue, 08 Aug 2023 23:06:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc576c087212d0f5e94f42408a0e3807586d64d2e3b12ffe41e0a67cc18f5d3`  
		Last Modified: Tue, 08 Aug 2023 23:09:49 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25fa0c025300c123bcb002c2eaf6df282d3655bf277633cc59142b7df50b65`  
		Last Modified: Tue, 08 Aug 2023 23:09:49 GMT  
		Size: 347.4 KB (347441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6ef31779d51bfba4b7c9ba5ef866bdb213cf0bc14c4b2ba6d304f1d029c5a6`  
		Last Modified: Tue, 08 Aug 2023 23:10:18 GMT  
		Size: 9.3 MB (9271783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe3bfbeeb6c06304e53c019b459c7ba1ff84d0f586aec564b8aa015e9130e9`  
		Last Modified: Tue, 08 Aug 2023 23:10:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bb07d1c42585da4d0ae2cc62a5e04e69f4d9ea338ae9941afd1213e1b0031d`  
		Last Modified: Tue, 08 Aug 2023 23:10:15 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.18` - linux; s390x

```console
$ docker pull redis@sha256:2663dadc6b4317d661ce0bcb1e927738a941283fc4fa98b7b9ba52f65b0a4c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15803563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8632a3e93fb10f510e5fa34d453da2dc3ae6a7a6f47d57acf85e3437f28f3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 03:46:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 09 Aug 2023 03:46:10 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 16 Aug 2023 23:51:46 GMT
ENV REDIS_VERSION=7.2.0
# Wed, 16 Aug 2023 23:51:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.0.tar.gz
# Wed, 16 Aug 2023 23:51:47 GMT
ENV REDIS_DOWNLOAD_SHA=8b12e242647635b419a0e1833eda02b65bf64e39eb9e509d9db4888fb3124943
# Wed, 16 Aug 2023 23:52:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 16 Aug 2023 23:52:36 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 16 Aug 2023 23:52:37 GMT
VOLUME [/data]
# Wed, 16 Aug 2023 23:52:37 GMT
WORKDIR /data
# Wed, 16 Aug 2023 23:52:37 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 16 Aug 2023 23:52:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 23:52:37 GMT
EXPOSE 6379
# Wed, 16 Aug 2023 23:52:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d0bbca871d4a4c479bdf5487901063c88d57814a69a2a45551109c31ef85e9`  
		Last Modified: Wed, 09 Aug 2023 03:50:40 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04249ebe58273831e95cd29d4c0c1039ebb2eb45ac592ce3a784bb79e7dbe0a4`  
		Last Modified: Wed, 09 Aug 2023 03:50:40 GMT  
		Size: 347.1 KB (347124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722762b961e7dfa4b3d58f92ae1c7a60277a7c6bf1029d22aca8c917bfc14222`  
		Last Modified: Wed, 16 Aug 2023 23:54:03 GMT  
		Size: 12.2 MB (12240266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd828e145f9f14e32e0733dd215ccda8c7143a265727b0ffe0c3bba58003b0c`  
		Last Modified: Wed, 16 Aug 2023 23:54:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa11580089d58d398c82779eebcef6512bff648b662608d966fffe964f6bc424`  
		Last Modified: Wed, 16 Aug 2023 23:54:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
