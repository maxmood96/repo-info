## `redis:6-alpine3.21`

```console
$ docker pull redis@sha256:ee7c17e5888bab9fa51465342aacbb28bba5c171f432831514fb9527808779a2
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

### `redis:6-alpine3.21` - linux; amd64

```console
$ docker pull redis@sha256:e8773aa976bf0e4ca3e7707b759110c893be504da1f25a61bb4000d1d56b7bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11444448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0f16ceecd18a5e956b58a0b240f8ffb3fcad767eca2b14b90650dbc6543a6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:34:05 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:34:05 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:36:32 GMT
ENV REDIS_VERSION=6.2.22
# Thu, 07 May 2026 17:36:32 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Thu, 07 May 2026 17:36:32 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Thu, 07 May 2026 17:36:32 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:36:32 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:36:32 GMT
VOLUME [/data]
# Thu, 07 May 2026 17:36:32 GMT
WORKDIR /data
# Thu, 07 May 2026 17:36:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:36:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:36:32 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:36:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14c7509f545010819719d4269d58b1358ff935984497f11d6067bdda0ee9261`  
		Last Modified: Thu, 07 May 2026 17:34:55 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f546396032e0b456fe98a8cc057041605fe93a1199309d197f8d4d2a980c1251`  
		Last Modified: Thu, 07 May 2026 17:34:55 GMT  
		Size: 194.9 KB (194939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c6e1388666cbd0c6c0540724fd18d774ee1065c1c14780b374451cf264d91`  
		Last Modified: Thu, 07 May 2026 17:36:38 GMT  
		Size: 7.6 MB (7600952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07708ca400dfc42f609b151138825d61e61aa0b24f28c4f7271acb06bf2598`  
		Last Modified: Thu, 07 May 2026 17:36:38 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902184b21654d047c1a6a0fa8436a5b921edc64e85ca1440e20f9c981d7dd610`  
		Last Modified: Thu, 07 May 2026 17:36:38 GMT  
		Size: 603.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:b0687c30322da6e152c589403426005ea641fbc2e888b17b73104b9628f3e830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.3 KB (487280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95080cdae0d6bb5998057f632a4db3bdf90201fe87e847b6698ddaf8d4ca327d`

```dockerfile
```

-	Layers:
	-	`sha256:82ea1be5f1fe87d1dd770e365b03f5197ef51860087d8e8a14417d13da59e563`  
		Last Modified: Thu, 07 May 2026 17:36:38 GMT  
		Size: 462.6 KB (462597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92163f903b601618d284c19de81e2bf189fdde00275fa78827dff95d265326db`  
		Last Modified: Thu, 07 May 2026 17:36:38 GMT  
		Size: 24.7 KB (24683 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:518cb364201e4eca043d57995bed0cc3e38dae7d4a8222b01dde8dffa71db44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11201952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc350cffb9f16a1389f35626cd2da64124a42bd5b4d56def4b34b82d6a2b1d03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:55:34 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:55:34 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 17:56:09 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 05 May 2026 17:56:09 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 05 May 2026 17:56:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:56:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:56:09 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:56:09 GMT
WORKDIR /data
# Tue, 05 May 2026 17:56:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:56:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:56:09 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:56:09 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e7f9d54c6e53c7a647780e116784d0931148a9c4d7537eb6b73edddd623ab1`  
		Last Modified: Tue, 05 May 2026 17:56:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e1a9ecb99f6b69bf28ea0d5142f8121bf22ed386222d4911757bd7c142842e`  
		Last Modified: Tue, 05 May 2026 17:56:13 GMT  
		Size: 195.5 KB (195453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3920a4409108e0dbed284cf539bb80cbd20595f3d196a1055cf15580a64ddf8f`  
		Last Modified: Tue, 05 May 2026 17:56:14 GMT  
		Size: 7.6 MB (7635739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdf80d35c4dc27b529a7bee65762e72c461fb9fd676ec55aa5ccbadf9918a8a`  
		Last Modified: Tue, 05 May 2026 17:56:13 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d087f8ece704b749d5ff49eff6f579feb4b25e2f9a831a8ab2ab210ad5ca1fcb`  
		Last Modified: Tue, 05 May 2026 17:56:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:d431bc7f101b0b8aa614f186ff6c656e86b7c60317e22b899f8a39830b7a84a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fe830790c3d134709729ff975eb9adccf688b090c3b08d7815b78601f1f418`

```dockerfile
```

-	Layers:
	-	`sha256:b2301fe697c9f09595365eb6a80f13166b7f1561b4f4f108ec7b8916564610c4`  
		Last Modified: Tue, 05 May 2026 17:56:13 GMT  
		Size: 24.5 KB (24528 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:de402b2dea2b0c65dc081abf3c9fe92dcca4f8bb779d4e92f7458a51b9e3ef1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10815892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4538728b9719f6228363d545546a34828a7b5052a0ea02aa23076dfc046560e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:13 GMT
ADD alpine-minirootfs-3.21.7-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:13 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:56:32 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:56:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 17:57:08 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 05 May 2026 17:57:08 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 05 May 2026 17:57:08 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:57:08 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:57:08 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:57:08 GMT
WORKDIR /data
# Tue, 05 May 2026 17:57:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:57:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:57:08 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:57:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7957b137a4005e85cd17d3e5e1bbc7099f5f082aa28f72387126a1c8449672d7`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.1 MB (3101912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9791b0cbfa4047b8d4103059cb17d4dbd791108eb0a811853a354af488085076`  
		Last Modified: Tue, 05 May 2026 17:57:14 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdd4ed8b6b6adb25722499732a6d5a4a1bb1093a7438fa47d5849a630d99ba`  
		Last Modified: Tue, 05 May 2026 17:57:14 GMT  
		Size: 193.8 KB (193754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f175c4c88cc6423ecb7f512007015ba2b8f752f1372cb4b90ca91fcccdecd6d`  
		Last Modified: Tue, 05 May 2026 17:57:15 GMT  
		Size: 7.5 MB (7518523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6669214f1e1f8da96fbd594e6b986c6d3dc733baf46ff32bc3c560cab10f11`  
		Last Modified: Tue, 05 May 2026 17:57:14 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae1230262958611daabc5dfad4bbee6729f3c27ea4375bb74c45f52227f783`  
		Last Modified: Tue, 05 May 2026 17:57:15 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:54395d9b1abe624518cfe4934c335ba9b68d305bc3d182a9f017e403bcf42f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.4 KB (490382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce452afbcd5e06fde824acc6830ab6fac944d87f5f50264ca95e506b41409c`

```dockerfile
```

-	Layers:
	-	`sha256:ceb8172c68589fa6ef8ed2eb5f4cab1496f02cacd15b39a3739a0a520cc2a72b`  
		Last Modified: Tue, 05 May 2026 17:57:14 GMT  
		Size: 465.6 KB (465639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fc3ccd84073bc11898d899c718e5323c3a4b7d1cda233e1ffbc2b4933f14d4`  
		Last Modified: Tue, 05 May 2026 17:57:14 GMT  
		Size: 24.7 KB (24743 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b6368277cf32a754a9250b408f3ef8c152ab1669a8116095cc492385fd71f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11853721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb4a863fae9724940f392c5d79b07a2bc718e3eaef5754d3655e63299d998a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:40:13 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:40:13 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:41:45 GMT
ENV REDIS_VERSION=6.2.22
# Thu, 07 May 2026 17:41:45 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Thu, 07 May 2026 17:41:45 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Thu, 07 May 2026 17:41:45 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:41:45 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:41:45 GMT
VOLUME [/data]
# Thu, 07 May 2026 17:41:45 GMT
WORKDIR /data
# Thu, 07 May 2026 17:41:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:41:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:41:45 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:41:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c77134f8e8625ee728f947b94a94061e9d82b0f836f6496e294eaa0f8c557f`  
		Last Modified: Thu, 07 May 2026 17:41:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6db3587c2a444f65ef481347cc84ba7ef9f03ee60725a9039bee59d2b76f0d`  
		Last Modified: Thu, 07 May 2026 17:41:03 GMT  
		Size: 197.8 KB (197803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a42d54aefece8f63e6fca00389c12fb5348a12afca73b22a69b5d308e390b`  
		Last Modified: Thu, 07 May 2026 17:41:52 GMT  
		Size: 7.7 MB (7659768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15b0504d6aec34877015b58c8416522eb27d6d7e8756bcb5d6633fc43720643`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbec94c594133003ba52ac31be3c87399552c855f918027a46f7dfcd2daadcb`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 603.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:a6a6b45e76d81c579731ba0429c7a7d56272131200b30dfee761d74788cd810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.5 KB (487536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e3e303ff92b393046cc67369c3314caa56df09018dc7e4cbaa416ee944a5d7`

```dockerfile
```

-	Layers:
	-	`sha256:e3b5befec3013d2a531adbe61830a2be96d33e8c3adb6a74e889293c4a16b2a8`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 462.7 KB (462677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04f440c97b4768b9698d9d681c2a697fd45746f233dbb6538fe2b95341605a1`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 24.9 KB (24859 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:41a00a67ca645f13e249bdfca5b99afdb56c60e2f866b91b2713e5b3413b1572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11005010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc291a3aed91cdf580f1874a66df61966d94b934b084468d1e086913d40234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:35 GMT
ADD alpine-minirootfs-3.21.7-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:35 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:37:47 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:38:20 GMT
ENV REDIS_VERSION=6.2.22
# Thu, 07 May 2026 17:38:20 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Thu, 07 May 2026 17:38:20 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Thu, 07 May 2026 17:38:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:38:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:38:20 GMT
VOLUME [/data]
# Thu, 07 May 2026 17:38:20 GMT
WORKDIR /data
# Thu, 07 May 2026 17:38:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:38:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:38:21 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:38:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f6078c6ba1ececd5b6486ae9f846f15a21622e1b802bfd96f0334235ac0b75e0`  
		Last Modified: Fri, 17 Apr 2026 02:42:40 GMT  
		Size: 3.5 MB (3468819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52907c612afe6cd6b306580d888d114cce2b0e8781578c53ead0dcf330a03ef`  
		Last Modified: Thu, 07 May 2026 17:38:26 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66753a1bce3ab2ea7c0b77a3f3a45eca5c4caf248ca4620c8e25ce0bc053079b`  
		Last Modified: Thu, 07 May 2026 17:38:26 GMT  
		Size: 195.0 KB (195022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccaa6ab4787081ab391c8cd3a9af03469c700620261e50cc8fef7e6caea3ff3`  
		Last Modified: Thu, 07 May 2026 17:38:27 GMT  
		Size: 7.3 MB (7339486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c30eaacef20d2cd923b60ec2943d6b100c486853c348c9d8ad2e6d31ff3d2e`  
		Last Modified: Thu, 07 May 2026 17:38:26 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d333e8f19054cbd43fcb9bc9c6c8899597041fc5b3e1840f23f807e60b585e`  
		Last Modified: Thu, 07 May 2026 17:38:28 GMT  
		Size: 603.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:a7e5f8d9e359f0ff7c47f035064614ed606cfbf9b1fe756d71547529cc44e5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.2 KB (487197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb4565613092ad1d35c03fe6935b67810f1848d661db26963ac1b3f84290b9c`

```dockerfile
```

-	Layers:
	-	`sha256:c5c95bcf17308358eeb7c793e91d23ba459f69b0937cf15c2618b51410b17c72`  
		Last Modified: Thu, 07 May 2026 17:38:26 GMT  
		Size: 462.6 KB (462562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a6ed5dee82a01068183bb5aa9e5bd5a5f28038a4bb3f2895663b176353a99c`  
		Last Modified: Thu, 07 May 2026 17:38:26 GMT  
		Size: 24.6 KB (24635 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:a4b4d9ac9e06c8f5853ed65e522bb7baadc5c98617b48e141e8b885429c5511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11974479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4e836b7dbe3ef52da77a7ff1b962a0b7b14782d61aab27484f9cd7b63a7c3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:31 GMT
ADD alpine-minirootfs-3.21.7-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:31 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:57:28 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:57:30 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 18:02:09 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 05 May 2026 18:02:09 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 05 May 2026 18:02:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:02:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:02:09 GMT
VOLUME [/data]
# Tue, 05 May 2026 18:02:10 GMT
WORKDIR /data
# Tue, 05 May 2026 18:02:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:02:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:02:11 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:02:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fe51ead1f71865857c2c015e74518a0be9e72c6a70a845d843f7dd0cd2ee6e2e`  
		Last Modified: Fri, 17 Apr 2026 00:00:41 GMT  
		Size: 3.6 MB (3578920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5cfc15caa31689a25b8c064c6f30c5067346bf1b0869903568f4348b5eda18`  
		Last Modified: Tue, 05 May 2026 17:58:50 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d0af283319fab5670464843b62f03621a5570992d83c878c879b26a2d82ba`  
		Last Modified: Tue, 05 May 2026 17:58:51 GMT  
		Size: 198.8 KB (198804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f7c9f6a47da5d7655ecd4f11859b21882d74b5e143014068631098374013b9`  
		Last Modified: Tue, 05 May 2026 18:02:29 GMT  
		Size: 8.2 MB (8195049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8087fd20a00b3ef8c4715fe0da87ff7609a33b1f37948f95dd955f1d08ecb`  
		Last Modified: Tue, 05 May 2026 18:02:28 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745913ac139aeb6d67985e22a5d36c286335b6d4a38747023adbdfd4b6530e62`  
		Last Modified: Tue, 05 May 2026 18:02:28 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:b408c60a412fcdd2188b9d09af251b5408fa2d207d86cfd38b60356f87a92670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.4 KB (485359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c20c6ff63de39bfc5501ae8bdda3259672ac7ca2ba7e4cef6d44fa786ef557`

```dockerfile
```

-	Layers:
	-	`sha256:8e6eca3bf07cb85c727ccdd8a25e6ba0d77a4d82bc4cad23bb56f07efaa075d8`  
		Last Modified: Tue, 05 May 2026 18:02:28 GMT  
		Size: 460.7 KB (460692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2a0844e8174ef0c5e192c8fbc2cc7146ca271c3b324c2828a713b2a56bc594`  
		Last Modified: Tue, 05 May 2026 18:02:28 GMT  
		Size: 24.7 KB (24667 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:b80d12742ce25180ba42f69bcfde8b216d42caf653c25818b2e1e0f24fcc3fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10926121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b51b8b02730557a298de2bcf6109fd98ca2533c2ac6d606f841d5b3df1e234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 17 Apr 2026 07:19:47 GMT
ADD alpine-minirootfs-3.21.7-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:19:47 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 19:46:20 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 19:46:25 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 20:26:51 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 05 May 2026 20:26:51 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 05 May 2026 20:26:51 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 20:26:51 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 20:26:51 GMT
VOLUME [/data]
# Tue, 05 May 2026 20:26:51 GMT
WORKDIR /data
# Tue, 05 May 2026 20:26:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 20:26:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 20:26:51 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 20:26:51 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c65425fd624c96c0b8c08c71eb68976602b1f3437dea06eb8cd01687585fbf87`  
		Last Modified: Fri, 17 Apr 2026 07:20:11 GMT  
		Size: 3.4 MB (3354662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e7d5de057dc8c6164c47f23bb0c1f1306c530bf19cdea75c5edd69b6d188bb`  
		Last Modified: Tue, 05 May 2026 20:01:25 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005c9eb07b83b7a88218f0df843f750945f736315800a03976d6087ffe339fb`  
		Last Modified: Tue, 05 May 2026 20:01:25 GMT  
		Size: 194.8 KB (194796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccf92db8aeb38a5df560556dd5141ee7837b2f961f9d7a609de43f029fe42ae`  
		Last Modified: Tue, 05 May 2026 20:27:28 GMT  
		Size: 7.4 MB (7374958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d40319eef31ea4991e37f5770c5e2f6fd2dafc78d7bec9fca281da964762f2`  
		Last Modified: Tue, 05 May 2026 20:27:27 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0117d79d0443e8b768ca8ca9582749a5f87e2117d2b9ffe461cde11f71a49`  
		Last Modified: Tue, 05 May 2026 20:27:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:0747f899490c359969cce867bca745f138640ae13c1100eee10daf3c8090e764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.4 KB (485358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f311a9627dff57e49bf7e6f9839133a86184a4fa8afd28203af6c24c959634`

```dockerfile
```

-	Layers:
	-	`sha256:317d9358472da1a50453eadf3fa6d2c32b2515071a30d611a6a538eebb8dd0ae`  
		Last Modified: Tue, 05 May 2026 20:27:27 GMT  
		Size: 460.7 KB (460688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbc40207f5ba7da5f03ee9775af5e56744dcf6a12263b2715f1e69dc2d8bb70`  
		Last Modified: Tue, 05 May 2026 20:27:27 GMT  
		Size: 24.7 KB (24670 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:7ba6a5b1323b1ad0fe51dda2825d029ba1736f055ad5e4440fd9974bed11830b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11648069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a363f402a4cd0d75ddce018d6222322441aca1677a3bcdf6939aeef4102b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:58 GMT
ADD alpine-minirootfs-3.21.7-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:58 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 18:13:05 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 18:13:13 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 18:24:38 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 05 May 2026 18:24:38 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 05 May 2026 18:24:38 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:24:42 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:24:42 GMT
VOLUME [/data]
# Tue, 05 May 2026 18:24:45 GMT
WORKDIR /data
# Tue, 05 May 2026 18:24:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:24:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:24:48 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:24:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4dde3be1ef4aac98984d14e789ca07a8f41fc8984a89741b58981521dba1d412`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.5 MB (3469813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135352b4605929ac8d7b9e4d8ad709a48729740ea39d43233d023a89d5f2cac9`  
		Last Modified: Tue, 05 May 2026 18:17:30 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fc3060fcd33c3eef1a2d85fb32a3668a06a16c6b208e8c2ca64ee9b4a42f2`  
		Last Modified: Tue, 05 May 2026 18:17:30 GMT  
		Size: 197.5 KB (197514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ba74f3fe1ee53b82c96592430b428678787308d101407b8b6a0199e464f05`  
		Last Modified: Tue, 05 May 2026 18:26:00 GMT  
		Size: 8.0 MB (7979031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da9f877e4227b96be1008a2ed703778aa49d64466f0cb1f8d310c5bf70d0242`  
		Last Modified: Tue, 05 May 2026 18:25:55 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa4c4aad28ac1948db6fdabe8e0a58aa266904ad4a1d5dc11e87468b36f5a8b`  
		Last Modified: Tue, 05 May 2026 18:25:55 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:fc1f9221fc580266589c8456f9f2a77b5031c75586da11ba60bbc8849124a1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.3 KB (485253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dcee2d9eede8510cef9ec01db4acf7b9cc3607ca747519e7479128f44a2abc`

```dockerfile
```

-	Layers:
	-	`sha256:e8f3763b62970a45d04b2c7bf5e1b6e2750c642f6b3a66450d1b18a2293eb6a1`  
		Last Modified: Tue, 05 May 2026 18:25:54 GMT  
		Size: 460.6 KB (460646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87269d0cee5db7390cc93d09b703d9db4a3dc1356300bd3cc6a8652987924d5`  
		Last Modified: Tue, 05 May 2026 18:25:55 GMT  
		Size: 24.6 KB (24607 bytes)  
		MIME: application/vnd.in-toto+json
