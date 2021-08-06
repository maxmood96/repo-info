## `redis:6-alpine`

```console
$ docker pull redis@sha256:3515d585b44fde042e7d13e4095d9da3c706c53089fcf788c791b7fa85744410
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

### `redis:6-alpine` - linux; amd64

```console
$ docker pull redis@sha256:324faae103b6af6dd7085748ca8ea99b9e32785a0f3f80f62ce6f2d5185aeaaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10895186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814803e951a7ff04c8f7dfd366b4cc6de6859ac159e185f9ecbe9db82c9e9388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:07:59 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 06 Aug 2021 22:08:02 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 06 Aug 2021 22:08:02 GMT
ENV REDIS_VERSION=6.2.5
# Fri, 06 Aug 2021 22:08:02 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Fri, 06 Aug 2021 22:08:03 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Fri, 06 Aug 2021 22:10:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 06 Aug 2021 22:10:03 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 06 Aug 2021 22:10:04 GMT
VOLUME [/data]
# Fri, 06 Aug 2021 22:10:04 GMT
WORKDIR /data
# Fri, 06 Aug 2021 22:10:04 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 06 Aug 2021 22:10:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 22:10:05 GMT
EXPOSE 6379
# Fri, 06 Aug 2021 22:10:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bbd9479e910eabc5de34a71d51574b0a02cf7a90456d94377af78b3aa6726d`  
		Last Modified: Fri, 06 Aug 2021 22:14:20 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bb2b90a23b5e3f3871306be4f92344b08c2568b3c4166b61238f576f592cb7`  
		Last Modified: Fri, 06 Aug 2021 22:14:21 GMT  
		Size: 384.5 KB (384463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b05d94792ae5064f3c23625eee73c924c5a37c9d9ef8ce0cde6a7059ea611`  
		Last Modified: Fri, 06 Aug 2021 22:14:22 GMT  
		Size: 7.7 MB (7695902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a615fd1f2fd070050e2a5181c0334d55efdd7e2a85adb7c4bd159838125ade4`  
		Last Modified: Fri, 06 Aug 2021 22:14:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd76b8efa6e93f9e401fa5e2e138617b6f0e13a2d4e81236131c927bb3ab58c3`  
		Last Modified: Fri, 06 Aug 2021 22:14:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:92cc798af34500c0424b795fa89aa0e5fc0d12a32753e8ffbd373f6a391e2e2b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10590628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00352495d7226a8689a1d71775c09c746f9fac3aca2f366921bad8f0b8eed656`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:42 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Fri, 30 Jul 2021 17:49:42 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 07:13:01 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 31 Jul 2021 07:13:05 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 31 Jul 2021 07:13:05 GMT
ENV REDIS_VERSION=6.2.5
# Sat, 31 Jul 2021 07:13:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Sat, 31 Jul 2021 07:13:06 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Sat, 31 Jul 2021 07:14:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 31 Jul 2021 07:14:18 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 31 Jul 2021 07:14:18 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 07:14:19 GMT
WORKDIR /data
# Sat, 31 Jul 2021 07:14:19 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 31 Jul 2021 07:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 07:14:20 GMT
EXPOSE 6379
# Sat, 31 Jul 2021 07:14:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217b0e4ce8f8888b44fe73c67d5c5dc93757b58de867e2de30a8d462e1c1dda9`  
		Last Modified: Sat, 31 Jul 2021 07:19:05 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f787658d48fee032e8935a8ee0f39a35e8115e2cab1cb9d2abf4ac1678c8c7`  
		Last Modified: Sat, 31 Jul 2021 07:19:05 GMT  
		Size: 388.5 KB (388461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597f302f0b42b58e3089b42c2697cf8f9defd0312c0d672c4c977cd4ee0faac3`  
		Last Modified: Sat, 31 Jul 2021 07:19:09 GMT  
		Size: 7.6 MB (7575965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2b4996dad35e4c63b4296df40a77f2d4156073a7e12b5b7661c3e2b2173e55`  
		Last Modified: Sat, 31 Jul 2021 07:19:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05898ef2c0564b54e2dee9fba5b8eee972e51d15ec158b7ea3e90ee2aef21871`  
		Last Modified: Sat, 31 Jul 2021 07:19:05 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1f4a148ac60084274a7f53696d83da935461e2bc917368e0a5e1465acefdbee0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f95d552d342f9a317b159603b709306b7f01a21990ea75af9bc9c897863b15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 09:26:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 31 Jul 2021 09:26:11 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 31 Jul 2021 09:26:11 GMT
ENV REDIS_VERSION=6.2.5
# Sat, 31 Jul 2021 09:26:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Sat, 31 Jul 2021 09:26:12 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Sat, 31 Jul 2021 09:27:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 31 Jul 2021 09:27:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 31 Jul 2021 09:27:23 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 09:27:24 GMT
WORKDIR /data
# Sat, 31 Jul 2021 09:27:24 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 31 Jul 2021 09:27:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 09:27:25 GMT
EXPOSE 6379
# Sat, 31 Jul 2021 09:27:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b8c75604ed788a8333d7f73667be4dcf86aa495075bab0af16f9926b3c3791`  
		Last Modified: Sat, 31 Jul 2021 09:33:45 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fce2682ab9aacd68846f113c55eb67ca4830d931dd999195efe26d784d166d`  
		Last Modified: Sat, 31 Jul 2021 09:33:46 GMT  
		Size: 383.2 KB (383239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f4e34b5607302cd547537ee44a6f1c92c36cf10c5ea64269e415d4fa66a026`  
		Last Modified: Sat, 31 Jul 2021 09:33:50 GMT  
		Size: 7.5 MB (7458642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426eed9181523bbe44b49c8f3275182eb810728f6b78b3b4bddececc4da4c102`  
		Last Modified: Sat, 31 Jul 2021 09:33:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0669dcec5e04bf00da8a31c41f0790351f2d2692e64f891e3b10b6dcca6b9b98`  
		Last Modified: Sat, 31 Jul 2021 09:33:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:bd093dbed98367e3de9cd719819602e578ec303e76f4222bd7ba07844563e81b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10800333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d8f2bc17dddfec0df800fccbcb5b82caa34a835876c4f5d843afc58be062d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Jul 2021 23:19:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 06 Jul 2021 23:19:09 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 23 Jul 2021 03:41:34 GMT
ENV REDIS_VERSION=6.2.5
# Fri, 23 Jul 2021 03:41:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Fri, 23 Jul 2021 03:41:35 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Fri, 23 Jul 2021 03:42:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 23 Jul 2021 03:42:33 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 23 Jul 2021 03:42:33 GMT
VOLUME [/data]
# Fri, 23 Jul 2021 03:42:33 GMT
WORKDIR /data
# Fri, 23 Jul 2021 03:42:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 23 Jul 2021 03:42:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 03:42:34 GMT
EXPOSE 6379
# Fri, 23 Jul 2021 03:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf9b6d29f21b067b79d9c4788fc5f9fce9025ae889259c057d944efb7ff6e2b`  
		Last Modified: Tue, 06 Jul 2021 23:24:05 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb4f37113747531a22d738c7ff07eea3e4a0f3ba83b0c555c96896fb5e41a14`  
		Last Modified: Tue, 06 Jul 2021 23:24:06 GMT  
		Size: 386.2 KB (386199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afabdd7ccaa02185bfb63e6ade2f08af70467337ed4c2237aab88ea5361431ed`  
		Last Modified: Fri, 23 Jul 2021 03:45:01 GMT  
		Size: 7.7 MB (7702690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f863db389051dd15e351e84399b7e213b1ee0a34fa3fc71fa5a6c8f9975b8`  
		Last Modified: Fri, 23 Jul 2021 03:44:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf843fd84703032ac2dfcdbf5bb0e3e5e31e1d464dbc7739b2bcfb2170549a8`  
		Last Modified: Fri, 23 Jul 2021 03:44:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; 386

```console
$ docker pull redis@sha256:0f016f8158ba8ffb1ba126216b545e97e7d2449a8a2e812e0e7d61562c990060
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77d4df2ba186bfc9a819af6855cc41856aa1a692e2657252b8fbf77077b63f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 15 Jun 2021 21:38:30 GMT
ADD file:3b0fe1454491bb05e218b090fd461f2fd39546aa4a53eb3f953ee8eae149ac57 in / 
# Tue, 15 Jun 2021 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 06 Jul 2021 17:58:37 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 06 Jul 2021 17:58:39 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 23 Jul 2021 04:08:59 GMT
ENV REDIS_VERSION=6.2.5
# Fri, 23 Jul 2021 04:08:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Fri, 23 Jul 2021 04:08:59 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Fri, 23 Jul 2021 04:10:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 23 Jul 2021 04:10:15 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 23 Jul 2021 04:10:15 GMT
VOLUME [/data]
# Fri, 23 Jul 2021 04:10:16 GMT
WORKDIR /data
# Fri, 23 Jul 2021 04:10:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 23 Jul 2021 04:10:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:10:17 GMT
EXPOSE 6379
# Fri, 23 Jul 2021 04:10:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:be21df321efb39c5daf3151073ebff7688e15ea6cd5158878bc9559a5db76ac6`  
		Last Modified: Tue, 15 Jun 2021 21:39:16 GMT  
		Size: 2.8 MB (2820718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2551de8396d4fcd47753ef4d9beb999c0b7ea922e5a92009681b6f94f5c0506b`  
		Last Modified: Tue, 06 Jul 2021 18:04:37 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7f9665c61bd95041cf22f6ce770b5e8bbbbbad420a7eb1f7566217c27198d8`  
		Last Modified: Tue, 06 Jul 2021 18:04:37 GMT  
		Size: 390.8 KB (390807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1591e59fe8b648d8754496f4b055880cb77b76436048330260d012aa4882a29`  
		Last Modified: Fri, 23 Jul 2021 04:12:46 GMT  
		Size: 7.3 MB (7342619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445fd76a7d37ef5637c1c2f7f81c6e57ac479641c0617ab844aecb70cdaac7cb`  
		Last Modified: Fri, 23 Jul 2021 04:12:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec598b606cf55cebac367a6d380f2fc94e5f180cab66a02b32e41691f257ee4`  
		Last Modified: Fri, 23 Jul 2021 04:12:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:56ac5d84957539a5fc774100618297e8b84611d5ae81f8885cac6ecdcda4e857
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5325c2096a8dfad065b5061c2c0ec9aba9652d82357d38f04cc07fa4adb5696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:32 GMT
ADD file:0075aad7a94f0496483442bb2d9fdaa13e9c23087b90638d014b4bc263aa3861 in / 
# Fri, 30 Jul 2021 17:24:37 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 08:13:14 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 31 Jul 2021 08:13:25 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 31 Jul 2021 08:13:31 GMT
ENV REDIS_VERSION=6.2.5
# Sat, 31 Jul 2021 08:13:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.5.tar.gz
# Sat, 31 Jul 2021 08:13:38 GMT
ENV REDIS_DOWNLOAD_SHA=4b9a75709a1b74b3785e20a6c158cab94cf52298aa381eea947a678a60d551ae
# Sat, 31 Jul 2021 08:14:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 31 Jul 2021 08:14:54 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 31 Jul 2021 08:14:59 GMT
VOLUME [/data]
# Sat, 31 Jul 2021 08:15:04 GMT
WORKDIR /data
# Sat, 31 Jul 2021 08:15:06 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 31 Jul 2021 08:15:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 08:15:12 GMT
EXPOSE 6379
# Sat, 31 Jul 2021 08:15:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:baf144cfb66ebe9df1969f3b90f1c448beff98edc84de1ccb5d6346195a070d4`  
		Last Modified: Tue, 15 Jun 2021 22:27:38 GMT  
		Size: 2.8 MB (2810478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4893b0ea01414a9215d08788a5907eebecf8c8c5f24b5f43ef160d8b4b77bd`  
		Last Modified: Sat, 31 Jul 2021 08:21:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d548882afb3e3ead2b86d8e2b7de82843f49db25252fce63fd491c751186b806`  
		Last Modified: Sat, 31 Jul 2021 08:21:52 GMT  
		Size: 391.1 KB (391058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc45d2109d7d0d528b6e9f57d02a17344024a66c67fb6e08abe2f5f38c3fe2a`  
		Last Modified: Sat, 31 Jul 2021 08:21:53 GMT  
		Size: 8.2 MB (8206155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44d15c7612f7dec5522a3964d40bc44568a967696c05f701e563710a5bbcae3`  
		Last Modified: Sat, 31 Jul 2021 08:21:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bcad102484a37c3335b0c1dcbc4912e80b4c4f71d9dffe3a33e3dffde29284`  
		Last Modified: Sat, 31 Jul 2021 08:21:51 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:77ae2cb3812e0c6f47591a44ea2cac7e9656acf43ead89f4846930a6a9b124b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11008406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a342ca31ea484b5f34c858d4dd10d4683b21683ccd91cc52bf292f31fb71f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:57:34 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 06:57:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 02 Jun 2021 02:39:10 GMT
ENV REDIS_VERSION=6.2.4
# Wed, 02 Jun 2021 02:39:11 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.4.tar.gz
# Wed, 02 Jun 2021 02:39:12 GMT
ENV REDIS_DOWNLOAD_SHA=ba32c406a10fc2c09426e2be2787d74ff204eb3a2e496d87cff76a476b6ae16e
# Wed, 02 Jun 2021 02:40:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 02 Jun 2021 02:40:10 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 02 Jun 2021 02:40:10 GMT
VOLUME [/data]
# Wed, 02 Jun 2021 02:40:11 GMT
WORKDIR /data
# Wed, 02 Jun 2021 02:40:12 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Wed, 02 Jun 2021 02:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jun 2021 02:40:13 GMT
EXPOSE 6379
# Wed, 02 Jun 2021 02:40:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8301b8855bd6607f74a6f0e494262a313b941546f676be3a98ff67cb3921a975`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e8e413247eebdfc21ae64af7664f78b06ca050ca165a1734e375c5db4ee9fd`  
		Last Modified: Thu, 15 Apr 2021 07:01:07 GMT  
		Size: 388.8 KB (388827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34144f3a758d18e073411db6afbb197f510cbcfcfdb8170c9f5fa58c9711a3aa`  
		Last Modified: Wed, 02 Jun 2021 02:44:05 GMT  
		Size: 8.0 MB (8015120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525025f411a92fb2961c50f0d45297ab2a1c538545f2140f6818cf2ee36be34`  
		Last Modified: Wed, 02 Jun 2021 02:44:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698caf43174210a1022c486a565db272b061521b4ba81b1dc3482fd9cdf22025`  
		Last Modified: Wed, 02 Jun 2021 02:44:04 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
