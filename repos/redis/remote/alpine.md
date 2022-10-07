## `redis:alpine`

```console
$ docker pull redis@sha256:6de23471560f18e3144056596b75db76bd27875f2759979ad6da947020684e16
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

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:a9cc5c331a573b4e073cee01a100327800c11f111c8fff5a8209dea2d854768e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11860905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0139e7020436555eb895d12404fa296beb1f579796eb25ad116cfd56d1b68bad`
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
# Thu, 22 Sep 2022 17:21:32 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 17:21:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 17:21:33 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 17:22:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 17:22:19 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 17:22:19 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 17:22:19 GMT
WORKDIR /data
# Thu, 22 Sep 2022 17:22:20 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 17:22:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 17:22:20 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 17:22:20 GMT
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
	-	`sha256:dedc3f029c28d0e374ad28a88b5aaa497257cb7ca62c15f8e45cc9f711fefbb8`  
		Last Modified: Thu, 22 Sep 2022 17:24:02 GMT  
		Size: 8.6 MB (8646736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820ef2f65f1b1c6394081a2bd4560a5441f17cc0f029e61bd146e803c4615348`  
		Last Modified: Thu, 22 Sep 2022 17:24:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117f9ecd7959d23c5f7a90cfe5a68e520fbc85dd317b65aa32387358add0d13`  
		Last Modified: Thu, 22 Sep 2022 17:24:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:5548087d3e7536f9799aa2f125f3b51bb521cb178a2f414594f0d1d4fc216283
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11788953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ce0e603f416556e354a86e248943c8f3d4b74c87d66a9f75ae3a58cdfaed39`
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
# Thu, 22 Sep 2022 17:49:29 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 17:49:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 17:49:29 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 17:51:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 17:51:41 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 17:51:41 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 17:51:41 GMT
WORKDIR /data
# Thu, 22 Sep 2022 17:51:41 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 17:51:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 17:51:41 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 17:51:41 GMT
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
	-	`sha256:fdbd3adae954d4c66b419d1e3964ad70c83bd2370db52c96c2c9a583b6d5e455`  
		Last Modified: Thu, 22 Sep 2022 17:53:10 GMT  
		Size: 8.8 MB (8762630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c004675f774a32d47572dcfee5aa0e5d64b1b22d8d792293b94ed17e03e4b0`  
		Last Modified: Thu, 22 Sep 2022 17:53:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c24776b6f218594c58ca171028dfad534a44adf994b2016cc3b8a0ce6531b66`  
		Last Modified: Thu, 22 Sep 2022 17:53:08 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:5fb6b0bc62d67f3d36954750463699878228f4d26dac82caa5b3696282366520
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11463604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc47ef1aed583c78ac06a8d56313f211cc44d1d1b9ef0f0e2fc55a3bbf3fe845`
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
# Thu, 22 Sep 2022 18:00:05 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 18:00:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 18:00:05 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 18:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 18:01:54 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 18:01:54 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 18:01:54 GMT
WORKDIR /data
# Thu, 22 Sep 2022 18:01:54 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 18:01:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 18:01:54 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 18:01:54 GMT
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
	-	`sha256:0a6141183b044ba36ba54520491a42e4523954c64c84b33f21cf70824c93225b`  
		Last Modified: Thu, 22 Sep 2022 18:05:02 GMT  
		Size: 8.6 MB (8640469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dcdad708ca10d113daa52ccd64654343e9ea8672497e2e4bca1b5ee7fda31f`  
		Last Modified: Thu, 22 Sep 2022 18:05:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1f9001081d95bef22cad2b35cc2003d161bd2fdb345a143d627b80c28daa09`  
		Last Modified: Thu, 22 Sep 2022 18:05:01 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:59c2b7a26804b4c6042f6fa435b57afbe7b78ca67c341ff0f4127228aef7c201
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11898958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7405bffacd00a8ebed5b27d5fb73d235c3dcdd394a1e563d045803c94842af14`
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
# Thu, 22 Sep 2022 17:48:03 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 17:48:04 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 17:48:05 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 17:48:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 17:48:55 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 17:48:56 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 17:48:57 GMT
WORKDIR /data
# Thu, 22 Sep 2022 17:48:59 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 17:48:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 17:49:00 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 17:49:01 GMT
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
	-	`sha256:70d0210cfe508a72886d2bc8c5890920d1f71de8d3a75be5b254cd7a056be154`  
		Last Modified: Thu, 22 Sep 2022 17:51:43 GMT  
		Size: 8.8 MB (8782170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a132f3e88f2d82478724f35e104a31d3442bc52a3aee514e527d75b2b5f3f81`  
		Last Modified: Thu, 22 Sep 2022 17:51:42 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8241e65d9ff527211026c18132e6d23986f6676d1bdfd8795d6aa54a4b5c7bd`  
		Last Modified: Thu, 22 Sep 2022 17:51:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:6af92c911d79fa329b550c37ae94bd937940a12b42f2b6a44a23982cdfea7c52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11493922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21148e102efc9ca50215a9a05fe6c8d4dc45d34d36c3ec029325a842530bc22f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 01:29:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 07 Oct 2022 01:29:10 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 07 Oct 2022 01:29:11 GMT
ENV REDIS_VERSION=7.0.5
# Fri, 07 Oct 2022 01:29:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Fri, 07 Oct 2022 01:29:13 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Fri, 07 Oct 2022 01:30:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 07 Oct 2022 01:30:05 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 07 Oct 2022 01:30:06 GMT
VOLUME [/data]
# Fri, 07 Oct 2022 01:30:07 GMT
WORKDIR /data
# Fri, 07 Oct 2022 01:30:09 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 07 Oct 2022 01:30:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 01:30:10 GMT
EXPOSE 6379
# Fri, 07 Oct 2022 01:30:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d753ce7cb7a86176e409fbfed496fbb078d63cd34a5a2c43d5b99a516a11a2c`  
		Last Modified: Fri, 07 Oct 2022 01:35:18 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0890d9a205e664751060d4f2103b2213496b1be5f109712b8a91a7c9b9c5641`  
		Last Modified: Fri, 07 Oct 2022 01:35:19 GMT  
		Size: 405.3 KB (405262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9cfb2dce18ae2e7c2ca7e98936bb98de15016324f772fea1297d3f19b46962`  
		Last Modified: Fri, 07 Oct 2022 01:35:19 GMT  
		Size: 8.3 MB (8279615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efa1599faac16aef38914cde734aa6548d9e628d335a66c43f8412c21f0f2aa`  
		Last Modified: Fri, 07 Oct 2022 01:35:18 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7ba9878e263c279778f9a557265e8720e488f2715ecd95b2bf4fbc82eb78d`  
		Last Modified: Fri, 07 Oct 2022 01:35:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:0c7d0db5237b323d1681e01f03d8e6cc6db0e569bc5c82c56962a54db84f0cd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12480128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa895d01bb0433ac1b81b8322c8f9bc5c604bdd4566e90f0f7c54cdde9ea607`
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
# Thu, 22 Sep 2022 17:18:28 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 17:18:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 17:18:29 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 17:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 17:19:34 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 17:19:34 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 17:19:35 GMT
WORKDIR /data
# Thu, 22 Sep 2022 17:19:35 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 17:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 17:19:36 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 17:19:36 GMT
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
	-	`sha256:c8285e01fa4771339368401825814744dedbe3212f800c5e0580d3081fef8e84`  
		Last Modified: Thu, 22 Sep 2022 17:22:34 GMT  
		Size: 9.3 MB (9261168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39211f0ffc709a7823cd18b1e64806f5043f2fa2833f96c9611352f4f5bc49dd`  
		Last Modified: Thu, 22 Sep 2022 17:22:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f90bc47012d622180af83decefbe39ca3e5371e34245faee781188290096b1e`  
		Last Modified: Thu, 22 Sep 2022 17:22:31 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:4cb1c11368ea8eeb59b4dd1ba222338af05cd3c3c2eeff83cf66434792ae45e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11914001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06de2d2fc2173d93a49ff77e11bc5cbcb37de8fd5a8bae67950623428d67ad2a`
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
# Thu, 22 Sep 2022 17:43:23 GMT
ENV REDIS_VERSION=7.0.5
# Thu, 22 Sep 2022 17:43:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.5.tar.gz
# Thu, 22 Sep 2022 17:43:23 GMT
ENV REDIS_DOWNLOAD_SHA=67054cc37b58c125df93bd78000261ec0ef4436a26b40f38262c780e56315cc3
# Thu, 22 Sep 2022 17:44:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 22 Sep 2022 17:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 22 Sep 2022 17:44:09 GMT
VOLUME [/data]
# Thu, 22 Sep 2022 17:44:09 GMT
WORKDIR /data
# Thu, 22 Sep 2022 17:44:09 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Thu, 22 Sep 2022 17:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Sep 2022 17:44:09 GMT
EXPOSE 6379
# Thu, 22 Sep 2022 17:44:09 GMT
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
	-	`sha256:3ebaeb88737ee02c7a0ca219a848ad452684c5c095df8fd51218234aeff364f3`  
		Last Modified: Thu, 22 Sep 2022 17:51:12 GMT  
		Size: 8.9 MB (8910468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd98ffbe325d913e2079f1f7764cf8e14f9d9f93db58fe797134b5ada77e0b`  
		Last Modified: Thu, 22 Sep 2022 17:51:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d6c39b7515c0553e0c783c565f7771cbc57fce8905eda4e1d128240a234d6`  
		Last Modified: Thu, 22 Sep 2022 17:51:12 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
