## `redis:5-alpine3.13`

```console
$ docker pull redis@sha256:6151b520d9ac29c1524d9637e0b3dc69cba7dbef27a427d6dba355652fff8306
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

### `redis:5-alpine3.13` - linux; amd64

```console
$ docker pull redis@sha256:65876c19c93936db82f9df7186e6bc3dafe32920a33716230b7214ee08bc0fad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b24aafdf93a05581fac6db4430badb2024b27c7d6c29eb3144b01828ac5a07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 06:23:21 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 06:23:23 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 23:31:07 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 23:31:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 23:31:07 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 23:32:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:32:12 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:32:12 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:32:12 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:32:13 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:32:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:32:13 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:32:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f47664a3e948aa9846e699a789835d5cebd6d4b08c971e117ab4af508997975`  
		Last Modified: Thu, 18 Feb 2021 06:28:32 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c47feea59c197f5ea8be15d8e7cd92517f8fdabb3cd8a134f8cf130ca3ecdf`  
		Last Modified: Thu, 18 Feb 2021 06:28:32 GMT  
		Size: 384.2 KB (384160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046c586f8a26e7a5aebca620214c625950fc12c3092f9a0021d6547cf86fc98e`  
		Last Modified: Tue, 02 Mar 2021 23:33:58 GMT  
		Size: 6.6 MB (6642166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229d76d9343849038878e96047f7c986b298eedec6d5f3644b4e3ca50170ea57`  
		Last Modified: Tue, 02 Mar 2021 23:33:56 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a45c3ab8b0d89eca903e4253bae613307b5da7451c2fd11788fe43db1a725ed`  
		Last Modified: Tue, 02 Mar 2021 23:33:56 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; arm variant v6

```console
$ docker pull redis@sha256:44d2e0f871f20a8c0f8cf57de6c0f0d1c9359ab15373c9c41ace02fe83198a58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9580427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc58d7f5eab2b09832550dd932e01aa25449c59f97cb180e88c6354ee990e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:03:51 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 01:03:54 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 23:12:31 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 23:12:32 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 23:12:33 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 23:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:13:22 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:13:22 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:13:23 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:13:24 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:13:27 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:13:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88a7bbd2619cadecb386208833a873a1f9de5cdee06b9d84c3dc85bf5e65087`  
		Last Modified: Thu, 18 Feb 2021 01:07:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f54785cfc942f98829baaec59c9cd1d970bef0aba7fc1479e88bff347e0e6a`  
		Last Modified: Thu, 18 Feb 2021 01:07:54 GMT  
		Size: 388.2 KB (388166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712e4c8cc657a4a63458b5cf8bf31b40e63c8407d867aad12b7d9ee086569601`  
		Last Modified: Tue, 02 Mar 2021 23:14:23 GMT  
		Size: 6.6 MB (6568416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178bfeb017a24500bbeee2c593ef4b3a8d2c6943ae73083f75504c79a0784479`  
		Last Modified: Tue, 02 Mar 2021 23:14:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427041b95ce5b24f7ddd258a295c53c3cc5179eeb55b5408d5280bf3f75eb389`  
		Last Modified: Tue, 02 Mar 2021 23:14:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; arm variant v7

```console
$ docker pull redis@sha256:2877f3824090d23aa88792cbac932b85895b15f83da3017516ae72ef9dd6f398
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9273190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9c8d54434724d29ec9d9e125c526de20820b20d0c60c2e236bc1d9f4b97998`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:06:07 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 01:06:11 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 23:11:29 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 23:11:30 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 23:11:31 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 23:12:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:12:23 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:12:23 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:12:24 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:12:25 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:12:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:12:27 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:12:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e119cde15afedf20aa9ae8db6c014e2c0eac0884024f9d685e1c5dddd2a41d4`  
		Last Modified: Thu, 18 Feb 2021 01:10:25 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3b45341af7a86b79d558357e3b4cf489df45cfce40d52ee26fc4b57eaf8d95`  
		Last Modified: Thu, 18 Feb 2021 01:10:25 GMT  
		Size: 383.1 KB (383051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6316d403305581e170e716c11f436e2434a1c690855810d405b8a7ecb51e95`  
		Last Modified: Tue, 02 Mar 2021 23:14:19 GMT  
		Size: 6.5 MB (6464440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aab4a7f35cfb0418a4732730d7172324b610fd4cf182cea2cdf7a462fd51717`  
		Last Modified: Tue, 02 Mar 2021 23:14:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a07a1b49cf01c2a0780bd3a5bca24fe4325ad401f7a8d9637caa607830a06fc`  
		Last Modified: Tue, 02 Mar 2021 23:14:16 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:ffc3863c63983732b7019a88de9b2a3276109201ba3cf43ff17bda4cd0d5ee0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9762313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80aac1746ec9c7607e74dcc7fcbfa1845dddacc8d4aa3154ba3404099a34cb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:37:00 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 01:37:03 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 22:56:00 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 22:56:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 22:56:01 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 22:56:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:56:54 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:56:55 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:56:56 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:56:57 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:56:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:56:58 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:56:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d54d284a9344f4164841804b15309e454bbb02de1f717cd8f60062f8cbf29b9`  
		Last Modified: Thu, 18 Feb 2021 01:42:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c12e0e8854e7f214974b4d2386f0311360923f59a111788b15e5caed495126`  
		Last Modified: Thu, 18 Feb 2021 01:42:06 GMT  
		Size: 386.0 KB (385990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31654a959c009c06343e5cbbcc2f13522a7424902eb59ceda631ede7ce7055`  
		Last Modified: Tue, 02 Mar 2021 22:58:56 GMT  
		Size: 6.7 MB (6662945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0119680dc6eb73390ee5623ecca1146e1c630bfae797bcbeb6c663349dd624a6`  
		Last Modified: Tue, 02 Mar 2021 22:58:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d452947f15b7bcff64247a49777869c8f3ea3bb5a907fd43dc6f7bcd7a72d2`  
		Last Modified: Tue, 02 Mar 2021 22:58:54 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; 386

```console
$ docker pull redis@sha256:b0864c0bfe2773c6711d26d7fd9357229c0e4019a304743a95ee228c2b77c781
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3519758c374fe37e1a5ecd248b1482ec6ba6a52f39f3aa21eeed7dd498ca152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 03:28:26 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 03:28:27 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 22:51:53 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 22:51:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 22:51:54 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 22:53:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:53:10 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:53:10 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:53:10 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:53:11 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:53:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:53:11 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:53:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9037c55177b1b9742841f0c1fdb3fb5c3b0a033042904aa04b5dc34e9cf1870f`  
		Last Modified: Thu, 18 Feb 2021 03:33:51 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0e78b81f6edd6dd809bef662a469950726a13924438af5b25a4bf42398d17f`  
		Last Modified: Thu, 18 Feb 2021 03:33:51 GMT  
		Size: 390.5 KB (390493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3201b07bcf0b9c88e3d4b2d2def71c4b21a318a9b8a0f918626b52797e9ebccf`  
		Last Modified: Tue, 02 Mar 2021 22:54:45 GMT  
		Size: 6.4 MB (6360264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d75e0579615113109a2d0fb112dca4877f816c04589ba1a53461a2260a00f77`  
		Last Modified: Tue, 02 Mar 2021 22:54:43 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f3e33d14b2eaee61b40df300cff952c0dd8dd8c376e6d6924e43d5df164cc6`  
		Last Modified: Tue, 02 Mar 2021 22:54:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; ppc64le

```console
$ docker pull redis@sha256:f749f780486f995cd63363d07f57c7b45491a45c1341f2af431477b34447fbff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9919aa52ff84ef55b6a6564a2828f1587b1d7a2c2ed08f7aaf9c717bb10d4c0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 02:34:58 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 18 Feb 2021 02:35:15 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 23:53:46 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 23:53:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 23:54:00 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 23:55:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:55:42 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:55:51 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:56:02 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:56:09 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:56:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:56:26 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:56:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17164c68edce423072b60089b125907467e703dabccb685d5b56f2bcff005ab0`  
		Last Modified: Thu, 18 Feb 2021 02:44:22 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e142e72e4c6be27360fb4974b5857bc2d4b917fed1813c8815f5cc3ab7f414aa`  
		Last Modified: Thu, 18 Feb 2021 02:44:22 GMT  
		Size: 390.7 KB (390726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b625636151e2bcae98f23255694c886f074c5a77b938fee756ade0700e2a9e`  
		Last Modified: Tue, 02 Mar 2021 23:59:33 GMT  
		Size: 7.1 MB (7119435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59850a37c61bf5aa6edb0a55b7594dc719d0224b7aaea96d2cc4405f50523ed3`  
		Last Modified: Tue, 02 Mar 2021 23:59:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eae1b9ac52791a39b9be0e941c4c053eae55e8a8094d6e660c0d0bb8e5f71df`  
		Last Modified: Tue, 02 Mar 2021 23:59:30 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.13` - linux; s390x

```console
$ docker pull redis@sha256:4930eeea7cbd1efe6d82cc724120e135ea1bf2ab32b48367e300c632a52ddd3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9933841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0792480907ad40653330680f7a693baae907217a1e3273133044b19c10155ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 20:59:08 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Wed, 17 Feb 2021 20:59:10 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Mar 2021 22:51:12 GMT
ENV REDIS_VERSION=5.0.12
# Tue, 02 Mar 2021 22:51:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.12.tar.gz
# Tue, 02 Mar 2021 22:51:12 GMT
ENV REDIS_DOWNLOAD_SHA=7040eba5910f7c3d38f05ea5a1d88b480488215bdbd2e10ec70d18380108e31e
# Tue, 02 Mar 2021 22:51:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:51:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:51:48 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:51:49 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:51:49 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:51:49 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:51:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52cdba8701bf2035629eec9432c85eb50d11b5cff757a53af04f290dd661`  
		Last Modified: Wed, 17 Feb 2021 21:03:54 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0dc8e09542f93dedd884e3d85de46dcb37d11b8b4f697bdd4dfa2171bd8f86`  
		Last Modified: Wed, 17 Feb 2021 21:03:54 GMT  
		Size: 388.8 KB (388816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c03ba0b663584c19ce2924446cc03112982624c8dba01bd598e27fd1fbf40e`  
		Last Modified: Tue, 02 Mar 2021 22:53:30 GMT  
		Size: 6.9 MB (6940837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bcb60b2e675cdd657a138af08745e787c5ef3a22a0041f206c621b0a1caf1e`  
		Last Modified: Tue, 02 Mar 2021 22:53:29 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affa442e1124900713d391609fedddbc5aba2ffc318e54d559c1adf90e638edf`  
		Last Modified: Tue, 02 Mar 2021 22:53:29 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
