## `redis:7-alpine3.16`

```console
$ docker pull redis@sha256:dc1b954f5a1db78e31b8870966294d2f93fa8a7fba5c1337a1ce4ec55f311bc3
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

### `redis:7-alpine3.16` - linux; amd64

```console
$ docker pull redis@sha256:7c9e7c305125c68354c4902ed09a3c6da96436a5a2929b73f29748d56cf8e3c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11857584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9192ed4e495547641a71f90d7738578d4e9d05212e7d55d02cfc7f0e1198a61e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:51:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 10 Aug 2022 01:51:11 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 10 Aug 2022 01:51:11 GMT
ENV REDIS_VERSION=7.0.4
# Wed, 10 Aug 2022 01:51:11 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Wed, 10 Aug 2022 01:51:11 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Wed, 10 Aug 2022 01:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 10 Aug 2022 01:51:58 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 10 Aug 2022 01:51:59 GMT
VOLUME [/data]
# Wed, 10 Aug 2022 01:51:59 GMT
WORKDIR /data
# Wed, 10 Aug 2022 01:51:59 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 10 Aug 2022 01:51:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 01:51:59 GMT
EXPOSE 6379
# Wed, 10 Aug 2022 01:51:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99be1b28c7fb4cf8f2b54b1bf6d0e4fd6961f76d04af0f24d09c055286057a7`  
		Last Modified: Wed, 10 Aug 2022 01:55:24 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff0bb7e55e3a23d3d0f3dcaaa666d83b6128bfc307c1cb5198fc2112e7b12ce`  
		Last Modified: Wed, 10 Aug 2022 01:55:24 GMT  
		Size: 406.1 KB (406132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80de393db7bb6d3178742ef3dc3e905253dd47165fb9eeb53a50993c699262`  
		Last Modified: Wed, 10 Aug 2022 01:55:25 GMT  
		Size: 8.6 MB (8643419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbffc478db1b3dee9f43a7d5cfc7d94727286fb59cd0adb6902707b7a3c5682`  
		Last Modified: Wed, 10 Aug 2022 01:55:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7402bc4c98a0e78307c5d13c4c87ab3fd18e238b6752181d6b7669855c0845c4`  
		Last Modified: Wed, 10 Aug 2022 01:55:24 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; arm variant v6

```console
$ docker pull redis@sha256:345ff44b6a17671d2d859d1b88b5cdfc7c98c469bd2805932703aa97642ec5a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11787944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ba5811dac2fc5b9d9d2feb89663e8b07745993678548bc681ec216bfed17a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 23:51:54 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 10 Aug 2022 23:51:56 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 10 Aug 2022 23:51:56 GMT
ENV REDIS_VERSION=7.0.4
# Wed, 10 Aug 2022 23:51:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Wed, 10 Aug 2022 23:51:56 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Wed, 10 Aug 2022 23:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 10 Aug 2022 23:53:21 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 10 Aug 2022 23:53:21 GMT
VOLUME [/data]
# Wed, 10 Aug 2022 23:53:21 GMT
WORKDIR /data
# Wed, 10 Aug 2022 23:53:21 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 10 Aug 2022 23:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 23:53:21 GMT
EXPOSE 6379
# Wed, 10 Aug 2022 23:53:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2190a9665fc7451699f15b4a985c24cbbcd235289904fcc91b8ecdc9344ff82`  
		Last Modified: Wed, 10 Aug 2022 23:58:29 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e129985695d6fe04056a90f255b2007d03adaf44706c8bb670439865322a5f`  
		Last Modified: Wed, 10 Aug 2022 23:58:29 GMT  
		Size: 410.4 KB (410373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ab26ff7f5fea5afa195430e04cd72e27ab185e3cbc869a6c0bd9959f0a5a0b`  
		Last Modified: Wed, 10 Aug 2022 23:58:30 GMT  
		Size: 8.8 MB (8761623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac6c6a6d34702e6756093fc2da121f32311021b9be542da256f689786c6c285`  
		Last Modified: Wed, 10 Aug 2022 23:58:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3c4ca656dc23bce3504bcd66d8cc4f86d21ca251eff5d71f4cee2de984b0f8`  
		Last Modified: Wed, 10 Aug 2022 23:58:29 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; arm variant v7

```console
$ docker pull redis@sha256:7859e655c9acc2aed7286b542e4840d2664bd4fd33507744adb14d4ec0d0bf6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11458738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0072c5f4b13959925b66183725d787fe92523669d84bc9ba64f8415fe54516b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 02:34:56 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 11 Aug 2022 02:34:57 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 11 Aug 2022 02:34:57 GMT
ENV REDIS_VERSION=7.0.4
# Thu, 11 Aug 2022 02:34:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Thu, 11 Aug 2022 02:34:57 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Thu, 11 Aug 2022 02:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 11 Aug 2022 02:37:17 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 11 Aug 2022 02:37:17 GMT
VOLUME [/data]
# Thu, 11 Aug 2022 02:37:18 GMT
WORKDIR /data
# Thu, 11 Aug 2022 02:37:18 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 11 Aug 2022 02:37:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 02:37:18 GMT
EXPOSE 6379
# Thu, 11 Aug 2022 02:37:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7cd8b7e74348f54e0e55d7b3644116fb8128620506e79ae7f7776af0ec155`  
		Last Modified: Thu, 11 Aug 2022 02:45:41 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a806cbdb5773ebc7041d3171958c60ca053e52af84169d3eaf1835c629d1d9`  
		Last Modified: Thu, 11 Aug 2022 02:45:41 GMT  
		Size: 404.1 KB (404088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e74f63bedd018d9f3cedeb1ccbe8ea670b1318283a87b328882f90658468193`  
		Last Modified: Thu, 11 Aug 2022 02:45:43 GMT  
		Size: 8.6 MB (8635605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef5acc733d2a8ec01dbafff0b0c6832464b6b09905c71d3dcc839cf4aa224f`  
		Last Modified: Thu, 11 Aug 2022 02:45:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d8852f0e7793786297ea0a6e40304c94a4016f7066d854e267cc2798e327d`  
		Last Modified: Thu, 11 Aug 2022 02:45:41 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2a569eb7e06d7f7ee35d170089f32347e4c00d5713403938864fa42afd52250c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ae745dd6773c1c14d6d67cbb8bdf9118f6261935403c653e212ffbbbd61843`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:31:30 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 10 Aug 2022 05:31:32 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 10 Aug 2022 05:31:32 GMT
ENV REDIS_VERSION=7.0.4
# Wed, 10 Aug 2022 05:31:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Wed, 10 Aug 2022 05:31:34 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Wed, 10 Aug 2022 05:32:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 10 Aug 2022 05:32:24 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 10 Aug 2022 05:32:25 GMT
VOLUME [/data]
# Wed, 10 Aug 2022 05:32:26 GMT
WORKDIR /data
# Wed, 10 Aug 2022 05:32:28 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 10 Aug 2022 05:32:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 05:32:29 GMT
EXPOSE 6379
# Wed, 10 Aug 2022 05:32:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ca35ca74079916662b40ab785f68d98745dad43788d053a68a876f6304071`  
		Last Modified: Wed, 10 Aug 2022 05:37:30 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a29726af503141346c8cd269ed50295ac16434ec77bdc29278b26d551eb51a`  
		Last Modified: Wed, 10 Aug 2022 05:37:31 GMT  
		Size: 407.2 KB (407205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036b6931dcec4fc0711cc1ffb0a7504a639e143241c3109df69e9e421d1c2c39`  
		Last Modified: Wed, 10 Aug 2022 05:37:32 GMT  
		Size: 8.8 MB (8780796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c349d1dacd4078ae28ad37fb31676799c1c11b95c1c17846e79b3ed20da4a92e`  
		Last Modified: Wed, 10 Aug 2022 05:37:30 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bab1e281f255eee9bdee225e13526219cc653de09ac1b1668768f98a0aef9ee`  
		Last Modified: Wed, 10 Aug 2022 05:37:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; 386

```console
$ docker pull redis@sha256:5431332526bc14bcc06445180565b17248025f1e66a4d6fc2367ffbd4602a58a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11502302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31de0456806c5f891886034d53e29ad2920c37f47c755dd3c3d425e37f13e1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 23:25:03 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 09 Aug 2022 23:25:04 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 09 Aug 2022 23:25:05 GMT
ENV REDIS_VERSION=7.0.4
# Tue, 09 Aug 2022 23:25:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Tue, 09 Aug 2022 23:25:07 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Tue, 09 Aug 2022 23:25:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 09 Aug 2022 23:25:58 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 09 Aug 2022 23:25:59 GMT
VOLUME [/data]
# Tue, 09 Aug 2022 23:26:00 GMT
WORKDIR /data
# Tue, 09 Aug 2022 23:26:02 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 09 Aug 2022 23:26:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 23:26:03 GMT
EXPOSE 6379
# Tue, 09 Aug 2022 23:26:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4284cf1d7f09fe6c57c32a44fdc26f6c1cb0db81645601b262f1f9e564ad54`  
		Last Modified: Tue, 09 Aug 2022 23:31:13 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d95c5de7dcd60eed120dda7861878c6aa135c2a598bd412bfc11b80f66b2867`  
		Last Modified: Tue, 09 Aug 2022 23:31:13 GMT  
		Size: 413.6 KB (413592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce333df8a8c6a218ded88abdf85f7b8b15bfec1b79048ec6972834c20e299d03`  
		Last Modified: Tue, 09 Aug 2022 23:31:14 GMT  
		Size: 8.3 MB (8279669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d191b96d0ded45f6d52fac0703eda7aed8ee571a72081f78a2696a8e4c114a31`  
		Last Modified: Tue, 09 Aug 2022 23:31:13 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0822018d0ff418436c37fd0f3025804a73367c1c5cb51778c859e73c05d852a`  
		Last Modified: Tue, 09 Aug 2022 23:31:13 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; ppc64le

```console
$ docker pull redis@sha256:edc7e996bed42b2ed4ca165a6d80ae30e1a2b82f1010e6d770b912efae474d07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12477735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8814a67c3119a47cda011e166e506bc2af1d71db8b70ba5aae500808493127c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:08:55 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 10 Aug 2022 02:08:57 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 10 Aug 2022 02:08:58 GMT
ENV REDIS_VERSION=7.0.4
# Wed, 10 Aug 2022 02:08:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Wed, 10 Aug 2022 02:08:59 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Wed, 10 Aug 2022 02:10:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 10 Aug 2022 02:10:04 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 10 Aug 2022 02:10:05 GMT
VOLUME [/data]
# Wed, 10 Aug 2022 02:10:05 GMT
WORKDIR /data
# Wed, 10 Aug 2022 02:10:06 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 10 Aug 2022 02:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 02:10:06 GMT
EXPOSE 6379
# Wed, 10 Aug 2022 02:10:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4604134df5dec4743b2f2fe72b250a9b4ebcae8203cf89690a5655dae8b481`  
		Last Modified: Wed, 10 Aug 2022 02:16:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ee6a1cbc8818cf13e31dd18d0b21f20159c1ac506f05bc5026da830f8a6e4`  
		Last Modified: Wed, 10 Aug 2022 02:16:04 GMT  
		Size: 413.7 KB (413659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcec776b941706f08e35fe7ac7916b3ec4ff04ab8db93a79541ed5344189c36c`  
		Last Modified: Wed, 10 Aug 2022 02:16:06 GMT  
		Size: 9.3 MB (9258778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dbfe4e593e95e9faf2d38cfdf60215339ab1eb374d1f794a2b1836536e2b3a`  
		Last Modified: Wed, 10 Aug 2022 02:16:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ea0096b5c1dc947db0746d32a864b67466e95ca49abc644ee95f9c32862334`  
		Last Modified: Wed, 10 Aug 2022 02:16:04 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:7-alpine3.16` - linux; s390x

```console
$ docker pull redis@sha256:bdf36fb5e50a3d10c225efda94a431d0bbe7af2d23ba491026d2a853dd0c54e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11911165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba0d83129050a039d777fa44d6c2f40e2fb7f742d094f2f585c2767c00ee2d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:10:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 10 Aug 2022 06:10:09 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 10 Aug 2022 06:10:09 GMT
ENV REDIS_VERSION=7.0.4
# Wed, 10 Aug 2022 06:10:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.4.tar.gz
# Wed, 10 Aug 2022 06:10:10 GMT
ENV REDIS_DOWNLOAD_SHA=f0e65fda74c44a3dd4fa9d512d4d4d833dd0939c934e946a5c622a630d057f2f
# Wed, 10 Aug 2022 06:10:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 10 Aug 2022 06:11:00 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 10 Aug 2022 06:11:00 GMT
VOLUME [/data]
# Wed, 10 Aug 2022 06:11:00 GMT
WORKDIR /data
# Wed, 10 Aug 2022 06:11:00 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Wed, 10 Aug 2022 06:11:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:11:00 GMT
EXPOSE 6379
# Wed, 10 Aug 2022 06:11:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c8b1916163e61b0131e6ea46df548800984d88df181ad702e2b5252b79a93e`  
		Last Modified: Wed, 10 Aug 2022 06:15:55 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b42f963ebec44e3704a0c671c1b4bb6a893aa89d4551baea3b887e6f99eebf0`  
		Last Modified: Wed, 10 Aug 2022 06:15:55 GMT  
		Size: 411.0 KB (410954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655569f1df5739a9527db31b4ebfdd3f4bd692df3d10e494cfc60a0b59569364`  
		Last Modified: Wed, 10 Aug 2022 06:15:55 GMT  
		Size: 8.9 MB (8907633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381793e80b4e3d2b109a5f001f0207255ce664ae89f456beb732bf5eeb796b0`  
		Last Modified: Wed, 10 Aug 2022 06:15:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c51c2eea4a1cedeffc3dd394b129369955092d11fac7b531e21d8ed8aecc00`  
		Last Modified: Wed, 10 Aug 2022 06:15:55 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
