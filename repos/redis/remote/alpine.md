## `redis:alpine`

```console
$ docker pull redis@sha256:dbd779a0cd0f3e0336d38963d0cd4e278f4e36236c0e8b86acea75c79d03e5b2
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
$ docker pull redis@sha256:8158082a62d4dc96ce7492026bb0e0de012bee04a0a50a97a93244112611c60c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12389276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53278c28ec70ea2ea7e28a7e6955416f89201a159389bbdeb9d16a4123385ee5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 20:04:34 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 09 Jan 2023 20:04:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 17 Jan 2023 21:14:12 GMT
ENV REDIS_VERSION=7.0.8
# Tue, 17 Jan 2023 21:14:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Tue, 17 Jan 2023 21:14:12 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Tue, 17 Jan 2023 21:14:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 17 Jan 2023 21:14:54 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 17 Jan 2023 21:14:54 GMT
VOLUME [/data]
# Tue, 17 Jan 2023 21:14:54 GMT
WORKDIR /data
# Tue, 17 Jan 2023 21:14:54 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:14:54 GMT
EXPOSE 6379
# Tue, 17 Jan 2023 21:14:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0152d355cb21f10a6599c8f7b6423492c2afa3ecfb516b49e649ad2b0aa1`  
		Last Modified: Mon, 09 Jan 2023 20:07:37 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402c460b24b7cb3db325fd375d404548e0faf1b2115355f3bad7182317090eeb`  
		Last Modified: Mon, 09 Jan 2023 20:07:38 GMT  
		Size: 347.7 KB (347680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a51e6c2ffd95266a6b6af492970474916260dbb2c22ada9e976e862be383af5`  
		Last Modified: Tue, 17 Jan 2023 21:18:58 GMT  
		Size: 8.7 MB (8668991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ff5e2bc6cce4bcc87d00abffd5f9b60eb258c598311cdfeb6a23349d4d17af`  
		Last Modified: Tue, 17 Jan 2023 21:18:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976b5457593c4a7795e86d2c6799e69973e9bb4c83ac8b7d717fe456177191a9`  
		Last Modified: Tue, 17 Jan 2023 21:18:56 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4486f9e5d18cdcaa54067ad365213169bb3c6a43dc68a1166c095fdffc1cee8c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12207847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6df938e17fda66f8e91dfb417a51fd0f9aa2dc9111abbac49f50cdab8e26fa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:54 GMT
ADD file:b15fd8e9f996815394e25f20c8459bfb4c2a8c4074592d6f4c75f4fe79ce537e in / 
# Mon, 09 Jan 2023 17:04:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 23:17:28 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 09 Jan 2023 23:17:30 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 17 Jan 2023 21:08:14 GMT
ENV REDIS_VERSION=7.0.8
# Tue, 17 Jan 2023 21:08:14 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Tue, 17 Jan 2023 21:08:14 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Tue, 17 Jan 2023 21:09:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 17 Jan 2023 21:09:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 17 Jan 2023 21:09:00 GMT
VOLUME [/data]
# Tue, 17 Jan 2023 21:09:01 GMT
WORKDIR /data
# Tue, 17 Jan 2023 21:09:01 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:09:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:09:01 GMT
EXPOSE 6379
# Tue, 17 Jan 2023 21:09:01 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0269c10e600f3a375f36ddabdbd264ce9503a455f0d0969ce8a00f24eaecc032`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.1 MB (3107243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb45892966a7bb0d81a41a80c90cf0ba34cbe07e607bb75c3f3de92f3b95ae6f`  
		Last Modified: Mon, 09 Jan 2023 23:20:35 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a6415e47d37e04c10fc4845e0d3fbe817dcc865c911cad2879e47548867105`  
		Last Modified: Mon, 09 Jan 2023 23:20:35 GMT  
		Size: 347.8 KB (347792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e39b0403a2fe737df89a31f13a22563a2f7ffed8976d3145ee3beae5508b4`  
		Last Modified: Tue, 17 Jan 2023 21:11:31 GMT  
		Size: 8.8 MB (8750895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d7960ad274ec9b1bc47fd91ba8fd4ed251c6f149d47d1d9f37e8e5a330ca34`  
		Last Modified: Tue, 17 Jan 2023 21:11:30 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5669225e9d87777ec8181b8663087663192aafc354bc8fd1b7b1da4d693dc0`  
		Last Modified: Tue, 17 Jan 2023 21:11:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:47ff4dc2e0dc2452369808eff3a1e8d5c19e5d6011d65cc5562ce1e401552ea9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11841097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3f069ddad5f9425dc7aa0d640258109daab471084925926bc1626f7982c57a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 09 Jan 2023 17:06:27 GMT
ADD file:4696f25d0f019b27457c55b3b128b70bf153f38e3e4eb5bdfc21058543313e94 in / 
# Mon, 09 Jan 2023 17:06:27 GMT
CMD ["/bin/sh"]
# Tue, 10 Jan 2023 00:56:59 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 10 Jan 2023 00:57:00 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 17 Jan 2023 21:34:36 GMT
ENV REDIS_VERSION=7.0.8
# Tue, 17 Jan 2023 21:34:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Tue, 17 Jan 2023 21:34:37 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Tue, 17 Jan 2023 21:35:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 17 Jan 2023 21:35:17 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 17 Jan 2023 21:35:17 GMT
VOLUME [/data]
# Tue, 17 Jan 2023 21:35:17 GMT
WORKDIR /data
# Tue, 17 Jan 2023 21:35:18 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:35:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:35:18 GMT
EXPOSE 6379
# Tue, 17 Jan 2023 21:35:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c527615e4ffa2d5b9b777fd469b3b5ba7c1b1e9201c065be2c43569de48a3754`  
		Last Modified: Mon, 09 Jan 2023 17:07:17 GMT  
		Size: 2.9 MB (2865208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1540f52dcc833026e08c308d3f44486acd419e502f224ed054cf218e5871ded`  
		Last Modified: Tue, 10 Jan 2023 01:01:14 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3458b1b0e2c8efadb573231f958a9ecc4d0c9ccb5c8fb4a8be98befc6fd9eac9`  
		Last Modified: Tue, 10 Jan 2023 01:01:14 GMT  
		Size: 347.6 KB (347576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbffef4f4f136213508c23f10d4090e275dcc2a4141c64e37344999b61ac447`  
		Last Modified: Tue, 17 Jan 2023 21:40:52 GMT  
		Size: 8.6 MB (8626397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd55395dc461fe70f051d7a6734af9904a48ff5375e1697f50cd293ab58864`  
		Last Modified: Tue, 17 Jan 2023 21:40:50 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32034abc83069e7e00e727ccc1a7d7cdfa9c39308dea8a68afb625f7a2505109`  
		Last Modified: Tue, 17 Jan 2023 21:40:50 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:17154907d4697ecfe19cd503913104cc1b27f7cf3149b6863dce6acd4e572ae8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12372876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28189db829c1d24e2bf92a8ce1b6f5cb31e872ce462d9303b67f3efbbd809ecc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:18:20 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 11 Feb 2023 05:18:22 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 11 Feb 2023 05:18:22 GMT
ENV REDIS_VERSION=7.0.8
# Sat, 11 Feb 2023 05:18:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Sat, 11 Feb 2023 05:18:22 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Sat, 11 Feb 2023 05:18:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 11 Feb 2023 05:18:53 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 11 Feb 2023 05:18:53 GMT
VOLUME [/data]
# Sat, 11 Feb 2023 05:18:53 GMT
WORKDIR /data
# Sat, 11 Feb 2023 05:18:53 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Sat, 11 Feb 2023 05:18:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:18:53 GMT
EXPOSE 6379
# Sat, 11 Feb 2023 05:18:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5015c79ed515bf1c31986bf0c02f0058deb7f938811749567bfb8d1263a5e8d2`  
		Last Modified: Sat, 11 Feb 2023 05:20:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca28624189f688cb7e78c078bfbc4a0ebf1688dddf9fcf0a2ac7754818decf6`  
		Last Modified: Sat, 11 Feb 2023 05:20:47 GMT  
		Size: 347.9 KB (347907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f37260edce46cf8228b5215b5e9018678965ad04492c283c3552ce560d81d6`  
		Last Modified: Sat, 11 Feb 2023 05:20:48 GMT  
		Size: 8.8 MB (8761032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310621b348ca364b62830ce80eaae1b7196836d6bff783352493d0a966a946c2`  
		Last Modified: Sat, 11 Feb 2023 05:20:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f813dc3ebdfb44db361d1de58f00aad577a24ba8012ab27814ea49349c6d5d0`  
		Last Modified: Sat, 11 Feb 2023 05:20:47 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:bd98c35010af8c6351b8087c12c90f02930ed37bb12c8fbffff3fbdb677de6f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12066249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63af131febecb643c6d391e909bc54e3593587ccd5a43e8a2a1539e75574ba11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:23 GMT
ADD file:125f3514520a5cd29df2830a409aa026a2bc06a77a7a5d150133436404b33d41 in / 
# Fri, 10 Feb 2023 21:24:24 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:42:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 11 Feb 2023 02:42:15 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 11 Feb 2023 02:42:16 GMT
ENV REDIS_VERSION=7.0.8
# Sat, 11 Feb 2023 02:42:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Sat, 11 Feb 2023 02:42:18 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Sat, 11 Feb 2023 02:42:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 11 Feb 2023 02:43:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 11 Feb 2023 02:43:01 GMT
VOLUME [/data]
# Sat, 11 Feb 2023 02:43:02 GMT
WORKDIR /data
# Sat, 11 Feb 2023 02:43:04 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Sat, 11 Feb 2023 02:43:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 02:43:05 GMT
EXPOSE 6379
# Sat, 11 Feb 2023 02:43:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b3e346c15c2377ec0e75cc9efa98baecd58b0e9bb92f0ec07eeda0bcc7e67fc7`  
		Last Modified: Fri, 10 Feb 2023 21:25:13 GMT  
		Size: 3.4 MB (3412353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed33790235ed12bfc39c6015e39ac603eef3c97869474228fd55cd8884d39408`  
		Last Modified: Sat, 11 Feb 2023 02:46:17 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cdd52ff76f5b537420062fd9a7c0315832fd0ef807068e828af1f6d63ed35d`  
		Last Modified: Sat, 11 Feb 2023 02:46:17 GMT  
		Size: 347.6 KB (347596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b6b4089070543ba72ef962ccd629dbebe821fef3476f1b08c71e1e3ca171b`  
		Last Modified: Sat, 11 Feb 2023 02:46:18 GMT  
		Size: 8.3 MB (8304384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b612df02d78c6b3c2f2c59745fd1c69e3cd1bb095ccdfbfc0a2b98ac597fb5`  
		Last Modified: Sat, 11 Feb 2023 02:46:17 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d5b5ad554640dbc546b99305edd3fbc13856a8f410f912e2e64d45d592e2ab`  
		Last Modified: Sat, 11 Feb 2023 02:46:17 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:f27c48543ee9f0b7a6c8bafad0ec45037da41e71b63ce520bc475f7f908cb23b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12996443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac91c280e177fed109fdba6843a9e2a88e98de30587916672bc030c5a1acdafc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 00:35:51 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 11 Feb 2023 00:35:56 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 11 Feb 2023 00:35:56 GMT
ENV REDIS_VERSION=7.0.8
# Sat, 11 Feb 2023 00:35:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Sat, 11 Feb 2023 00:35:57 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Sat, 11 Feb 2023 00:36:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 11 Feb 2023 00:36:56 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 11 Feb 2023 00:36:57 GMT
VOLUME [/data]
# Sat, 11 Feb 2023 00:36:58 GMT
WORKDIR /data
# Sat, 11 Feb 2023 00:36:59 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Sat, 11 Feb 2023 00:36:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 00:37:00 GMT
EXPOSE 6379
# Sat, 11 Feb 2023 00:37:01 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984eda205048e12763406d5bba006c9cdd29c0a96716b8eb19b6341ea87a136`  
		Last Modified: Sat, 11 Feb 2023 00:40:55 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1596dbb042b71d9d2f99fa35647d78556855f99b031224641dcc4e3921c6ab46`  
		Last Modified: Sat, 11 Feb 2023 00:40:56 GMT  
		Size: 347.9 KB (347920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6b0debc2efa83beb0b05ead599c90ce956e98bfb924022a91e6f919789cd32`  
		Last Modified: Sat, 11 Feb 2023 00:40:58 GMT  
		Size: 9.3 MB (9255791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc2c8c1290d68503b670537a017b47260ff6bd1705ca6f795ae4526600d84d4`  
		Last Modified: Sat, 11 Feb 2023 00:40:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de678dfb8ed2af179a43aa48c12ea3402437b0d8847b6f2e0f2dd60ed284d595`  
		Last Modified: Sat, 11 Feb 2023 00:40:55 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:bbe398614e8282cf561f98728ff610c012dd25a3bc580984026f3c22bde485fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12406580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1645c66b94f679d036f8851f437cbb5f6306c6a4e88b16ec3cbde44ca540e19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:14:39 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Sat, 11 Feb 2023 05:14:40 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 11 Feb 2023 05:14:41 GMT
ENV REDIS_VERSION=7.0.8
# Sat, 11 Feb 2023 05:14:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.8.tar.gz
# Sat, 11 Feb 2023 05:14:41 GMT
ENV REDIS_DOWNLOAD_SHA=06a339e491306783dcf55b97f15a5dbcbdc01ccbde6dc23027c475cab735e914
# Sat, 11 Feb 2023 05:15:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 11 Feb 2023 05:15:25 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 11 Feb 2023 05:15:26 GMT
VOLUME [/data]
# Sat, 11 Feb 2023 05:15:26 GMT
WORKDIR /data
# Sat, 11 Feb 2023 05:15:26 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Sat, 11 Feb 2023 05:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:15:26 GMT
EXPOSE 6379
# Sat, 11 Feb 2023 05:15:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498875fea887faca6923f24eb01071d9726f31e2190602d0d5f4a95460615a66`  
		Last Modified: Sat, 11 Feb 2023 05:18:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701202efffcf5330e98381a4555776e1d78fb6ef4cd5eaa611ea7870d1554420`  
		Last Modified: Sat, 11 Feb 2023 05:18:35 GMT  
		Size: 347.6 KB (347644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6324251cd98c933392d762e8262ac0d06a67f8f05107773efca459f64e54325`  
		Last Modified: Sat, 11 Feb 2023 05:18:36 GMT  
		Size: 8.9 MB (8881839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7b90ec2a8642b2bf8ad52f9a0991865ef91f744b1e6a3ee093a255a7fdeb5`  
		Last Modified: Sat, 11 Feb 2023 05:18:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486cd5cb8c79a2663b8adbd8775b7751807319b55a31edee3f11da1e2415b87`  
		Last Modified: Sat, 11 Feb 2023 05:18:35 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
