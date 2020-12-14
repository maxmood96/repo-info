## `redis:rc-alpine`

```console
$ docker pull redis@sha256:74bc361c2b73c1faaf581b2ab5dad110136bdb822d8e6161fe58356fc5d103ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:rc-alpine` - linux; amd64

```console
$ docker pull redis@sha256:1ca70961589a5527b99981140fce9a61a045957dcf1b9470897571ba5d892f05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12358421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4877d3424361c2e849ceffe4b90ce358882d0f6176edecdd5b0246416ab94e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 16:25:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 16:25:18 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 22:28:00 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 22:28:00 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 22:28:00 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 22:28:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 22:29:00 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 22:29:01 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 22:29:01 GMT
WORKDIR /data
# Mon, 14 Dec 2020 22:29:01 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 22:29:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 22:29:02 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 22:29:02 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c9d57a1c7f4bb594339d259d1485b48bd5b81e9e6f662b4791b1dadc5d4daf`  
		Last Modified: Fri, 11 Dec 2020 16:30:52 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd033d7ec061821df52b64df5078b36d1f755a2f02e4b6b578e3ebd739313dd`  
		Last Modified: Fri, 11 Dec 2020 16:30:53 GMT  
		Size: 381.5 KB (381504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a6b24fcc2ec9fdfa23e8b12adf7d32514fc2b42fb691494f12940322105378`  
		Last Modified: Mon, 14 Dec 2020 22:30:23 GMT  
		Size: 9.2 MB (9178230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5584e6d996ed40d9e3b5aaa5c7758f25f2585a8764f0654560058c4d16308855`  
		Last Modified: Mon, 14 Dec 2020 22:30:21 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080da35320037765d985a24868c779f02a2fb998a3097a51a34925fa2e38c3ef`  
		Last Modified: Mon, 14 Dec 2020 22:30:21 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:c333d2da2d948e0a04e363d787e8d5b4120fc0cd26e6cc68af87e8668d13eef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9dc854437b67712795f955b5c086170cbd3e8b3f68207779da077ea574532e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:10:34 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 05:10:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:54:54 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:54:55 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:54:56 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:55:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:55:50 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:55:51 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:55:52 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:55:52 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:55:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:55:53 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:55:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447a76a74c6810b07663d685dcd2f99da1fc67cf7824495b6f04910e7723f678`  
		Last Modified: Fri, 11 Dec 2020 05:13:24 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f37f74eda655a638a407067de4a279a1536b0fa95d392a642008f7ca9504c`  
		Last Modified: Fri, 11 Dec 2020 05:13:24 GMT  
		Size: 384.9 KB (384903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8674de8b67b3f82ff8d2120ff362f91b14961e5c1fb6569f33a525ee5e8715bf`  
		Last Modified: Mon, 14 Dec 2020 21:56:34 GMT  
		Size: 8.8 MB (8801812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e3fa79db841c90d87d0cbcfa85212dbf107792fb2ff1f03788f883f05dd496`  
		Last Modified: Mon, 14 Dec 2020 21:56:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5fc7263af02fc3dea7b8a7108077485b59a8c141c620390489ed946b9cf582`  
		Last Modified: Mon, 14 Dec 2020 21:56:31 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:5babfde90584b720664b56b2ddecd3e625df4d473baa2fd8f7f0f5553d1ed03a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11376319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cbe7ce1f83969e0c345107b876226fed137ef17840dcca7d78e45bb17447ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 15:47:37 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 15:47:41 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 22:17:14 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 22:17:15 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 22:17:15 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 22:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 22:18:14 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 22:18:15 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 22:18:16 GMT
WORKDIR /data
# Mon, 14 Dec 2020 22:18:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 22:18:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 22:18:18 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 22:18:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdac81f68b558d3a5d368f3b955dc55a67a9c6cfb03221be0d3dfaee25d087e`  
		Last Modified: Fri, 11 Dec 2020 15:53:27 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce249ae19ee7cfd52424c42faa2e50309438aebacb9a43947eb1fdec74bf031`  
		Last Modified: Fri, 11 Dec 2020 15:53:26 GMT  
		Size: 378.5 KB (378477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9550ff27a752a72c54a3ac335d8712bec6a8e4364eb2b00631a6e2dd635594bc`  
		Last Modified: Mon, 14 Dec 2020 22:19:44 GMT  
		Size: 8.6 MB (8590346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e567144cd1f0dfe40ddeedab9ecc9cd6a64a91d5b4d00602d6ca6a8a9c5db13`  
		Last Modified: Mon, 14 Dec 2020 22:19:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b09b3789dd267e8dd15eb8b342a189c53b16b8e509e97f99a100657cd8ee6c`  
		Last Modified: Mon, 14 Dec 2020 22:19:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:47a3549b6823c0b66ea6b92373e178c0cf23d806d4b96c6660d2781fd2e0f17c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12165447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c542843cc364d1fe22a1dfd5eb0886b127699aa72b0cc4ca88eed5fc01a39d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 15:02:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 15:02:27 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:57:28 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:57:28 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:57:29 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:58:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:58:22 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:58:23 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:58:25 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:58:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:58:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:58:28 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:58:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644769aa9380d3217180aef39343466a8888ab65d032d49b2e0d076e1ae64439`  
		Last Modified: Fri, 11 Dec 2020 15:08:09 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d71757449c7064c22fec07fcdc49bb7e35eb87d73ea3bf8c27d1a905d48919d`  
		Last Modified: Fri, 11 Dec 2020 15:08:09 GMT  
		Size: 383.9 KB (383919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1679d88505042e576c9b4dd8413aba2e508da88db303e7b289039ab3864c172b`  
		Last Modified: Mon, 14 Dec 2020 21:59:50 GMT  
		Size: 9.1 MB (9073100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b67d9d7332e51fe9aadc85f2620bd856cf9859d1294c2fb9d69511a6197b3`  
		Last Modified: Mon, 14 Dec 2020 21:59:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9da9d4a93c1ceffa9510d7f6c9406213701b241c98eb145f30f38a2fdc81344`  
		Last Modified: Mon, 14 Dec 2020 21:59:47 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; 386

```console
$ docker pull redis@sha256:01c88cd085ce96a8c0a0c9a35717df5483294d14c87c7320bdb2072c8e0e7385
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12019731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52edf933d4fdeb62bb4b3edbc9e2e4d2664e0658f368134367e23172e5286480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:01:14 GMT
ADD file:8812e502f26af2dc4efdfb7387f8bf99f2a098b6c95b9f6abf900df2ce74e3da in / 
# Fri, 11 Dec 2020 02:01:14 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 21:36:53 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 21:36:54 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:41:03 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:41:04 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:41:04 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:42:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:42:18 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:42:18 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:42:19 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:42:19 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:42:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:42:19 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:42:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b62269920a7a62a905817c7c1b33f33b6e658121e9a054715ff052a23f7de3a0`  
		Last Modified: Fri, 11 Dec 2020 02:01:43 GMT  
		Size: 2.8 MB (2791504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c7c02d89eb295e848e91a38659a947216b36c0341aaca883e067f6bb4e65a0`  
		Last Modified: Fri, 11 Dec 2020 21:42:12 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04935f19e0740c2dc4402dc74f1bec97b3192ebb3cfe86024468916307be56a3`  
		Last Modified: Fri, 11 Dec 2020 21:42:13 GMT  
		Size: 387.0 KB (386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd2480b1faed5e5088097c898c0bcd9ef784935845053d2f3bb2ede68abc2f`  
		Last Modified: Mon, 14 Dec 2020 21:43:34 GMT  
		Size: 8.8 MB (8839527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e83082361a721a6c2386aafdaff184b588cccae95fcddcce97b74b359a663d`  
		Last Modified: Mon, 14 Dec 2020 21:43:32 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec81850553a4ea0b17f004854eb85fd24a1fc6dc489975de45fb9e4348cd950f`  
		Last Modified: Mon, 14 Dec 2020 21:43:31 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:c3094182e1b93387c15d739833142242565dea5cbc018909275d758b22ab99d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12816585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f782b84b4355f78e5fd7c271f1ec4218e4e0a48fe9d12ef4c308ee9c1b8e10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 03:30:29 GMT
ADD file:9b4b44ee9eaddedc13f114bb55c9abeabceff6abd47f4a660734e431d22fcdce in / 
# Fri, 11 Dec 2020 03:30:32 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 17:48:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 17:48:31 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 22:26:10 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 22:26:17 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 22:26:21 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 22:27:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 22:27:54 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 22:27:59 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 22:28:04 GMT
WORKDIR /data
# Mon, 14 Dec 2020 22:28:07 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 22:28:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 22:28:22 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 22:28:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ed596bc4dd0a0c7ff1952005f6cae53a061e1c7998282289586bbfc17a2fd6db`  
		Last Modified: Fri, 11 Dec 2020 03:31:06 GMT  
		Size: 2.8 MB (2803424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1360c5767fd6468cd7bde79f7d4a72eee531ebc516a67dd0f8aaabc3eaef0558`  
		Last Modified: Fri, 11 Dec 2020 18:02:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc1612b5ffd271d6ac2f385981665129c3a9cbb9e5d5f1fb0f0ad460146699c`  
		Last Modified: Fri, 11 Dec 2020 18:02:17 GMT  
		Size: 388.4 KB (388376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f32bfa77321989f52e33b86350ed002224cdc6c7843768d68d64d4a1c17f3f`  
		Last Modified: Mon, 14 Dec 2020 22:30:09 GMT  
		Size: 9.6 MB (9622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b751560440852933b6124528311c0c5f129c2b1376e85d9e825429dae92521`  
		Last Modified: Mon, 14 Dec 2020 22:30:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7695b06be88254f8da42e2adac3c87f6e46950f805031b00396c3c5ce3e4032`  
		Last Modified: Mon, 14 Dec 2020 22:30:08 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:rc-alpine` - linux; s390x

```console
$ docker pull redis@sha256:ec1aabc6050e9b68f81bda9ff8ecdb07e1aa6b9f88f5fe7214465d9ec854c37b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12146474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecdeaac97b32776cffedbdd78522b7c8c6612f3f83bad3aa98b9c8494219e80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 13:58:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 11 Dec 2020 13:58:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 14 Dec 2020 21:45:55 GMT
ENV REDIS_VERSION=6.2-rc1
# Mon, 14 Dec 2020 21:45:55 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/6.2-rc1.tar.gz
# Mon, 14 Dec 2020 21:45:56 GMT
ENV REDIS_DOWNLOAD_SHA=bb7b18aaed17d70efce77ae56d2f7211dd077bcd0e2b94897188eed3e2484c78
# Mon, 14 Dec 2020 21:46:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 14 Dec 2020 21:46:37 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 14 Dec 2020 21:46:37 GMT
VOLUME [/data]
# Mon, 14 Dec 2020 21:46:37 GMT
WORKDIR /data
# Mon, 14 Dec 2020 21:46:38 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 14 Dec 2020 21:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Dec 2020 21:46:38 GMT
EXPOSE 6379
# Mon, 14 Dec 2020 21:46:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9fd6145aff29902d4fd018025ad260fe864cbe9f06627b6964ba58e33a2aa7`  
		Last Modified: Fri, 11 Dec 2020 14:04:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732b2116381efd347a216d9f6b13848bbe0ece877b2e04b99db18bb895ef06b`  
		Last Modified: Fri, 11 Dec 2020 14:04:21 GMT  
		Size: 386.4 KB (386378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0941270b2a08de0fd0e889a435cd15e8385d77c9c309741d921fb5574cccc814`  
		Last Modified: Mon, 14 Dec 2020 21:47:54 GMT  
		Size: 9.2 MB (9192303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327e812487ec9f968b57efa27cba3049dc846ee4b0215262e3b9ee46f5916a98`  
		Last Modified: Mon, 14 Dec 2020 21:47:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f057f0e58900d2bff4800535692e9cb55ec157b4d4d6347eecdb32b6df30fbf`  
		Last Modified: Mon, 14 Dec 2020 21:47:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
