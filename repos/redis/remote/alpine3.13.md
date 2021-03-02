## `redis:alpine3.13`

```console
$ docker pull redis@sha256:9ee44881d515d88352989d1aedbaa333d34f4fcb6d2639c4a40525e7d6bff125
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

### `redis:alpine3.13` - linux; amd64

```console
$ docker pull redis@sha256:a5648ca40eea560d07e4ac51c0eb9beffca933aef99c083b8f6b236f8197f9e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10871411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb69be5871bf83a0e89b4e9d4a9ef5a9eca690b24a58797b023d21a12d67301`
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
# Tue, 02 Mar 2021 23:24:41 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 23:24:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 23:24:42 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 23:25:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:25:53 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:25:54 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:25:54 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:25:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:25:54 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:25:55 GMT
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
	-	`sha256:272e3afc50bf509587f04173e1c75af77e97e9f1e2dce462b300d746e8187135`  
		Last Modified: Tue, 02 Mar 2021 23:33:14 GMT  
		Size: 7.7 MB (7673852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805d349697328b8c3878b45c30a4c5b64c4ef91b44027815e9c881d6a832a632`  
		Last Modified: Tue, 02 Mar 2021 23:33:12 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f0fe75cbce344389f07443cfd84884eea5625feb0dca3ac2dffdd2cef5bab4`  
		Last Modified: Tue, 02 Mar 2021 23:33:12 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; arm variant v6

```console
$ docker pull redis@sha256:a010ec592517cb57d3218bf3020f0a44ae8155fdb899a64255a093d8b405eeb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10567665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f53bdf0e26e8d25a77b71d294c344f7f0dd5ec21572eadc028f256d0b160695`
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
# Tue, 02 Mar 2021 23:09:51 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 23:09:52 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 23:09:53 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 23:10:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:10:51 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:10:52 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:10:53 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:10:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:10:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:10:56 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:10:57 GMT
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
	-	`sha256:860a6cea4a25d49b3e039e4b35923678ada39133aa917344793f8ec0922102dc`  
		Last Modified: Tue, 02 Mar 2021 23:13:56 GMT  
		Size: 7.6 MB (7555654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402f3f077957730dd6c0c3998cf187bf7ae3583ff047b5371eb4526961c1c2e`  
		Last Modified: Tue, 02 Mar 2021 23:13:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f4f3116db614e0e04d59bd9d3eecd4a721bf1ca0b453f05144830ac6cc250`  
		Last Modified: Tue, 02 Mar 2021 23:13:54 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; arm variant v7

```console
$ docker pull redis@sha256:076205e15445b510a790a9391f32475726309bfd8a0ae54ea881e7f6deeb987e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10245009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c220d4986ea6474516aa41f0190be6fb26d5842658936ceea97e7e50083f5115`
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
# Tue, 02 Mar 2021 23:06:07 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 23:06:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 23:06:09 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 23:07:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 23:07:04 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 23:07:05 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 23:07:05 GMT
WORKDIR /data
# Tue, 02 Mar 2021 23:07:06 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 23:07:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:07:07 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 23:07:08 GMT
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
	-	`sha256:a0533af9d6677bcc735b215851e04bf6c2325424f43e70d119a6c0db72451228`  
		Last Modified: Tue, 02 Mar 2021 23:13:22 GMT  
		Size: 7.4 MB (7436259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a87aa9bd44644f47a60eb452df3cb6e54d335d031fdde43d8486d17fcd9fb`  
		Last Modified: Tue, 02 Mar 2021 23:13:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b076e986305c7cbb66bf09def8864e38a114c4a9fe3264c6170f28aa60bf6e90`  
		Last Modified: Tue, 02 Mar 2021 23:13:19 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:e0a7a40c4e6e010549a627b0354575056006e89f6ca8f198917f6967b6e8b794
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c8a7651f2f2d9c561ffb27ac614eae9c6b923bf74fc4e147bec7c5c071b08`
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
# Tue, 02 Mar 2021 22:50:14 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 22:50:15 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 22:50:15 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 22:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:51:17 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:51:18 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:51:20 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:51:21 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:51:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:51:22 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:51:23 GMT
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
	-	`sha256:7cef5af366412fec97d9b6b923f4827083b88cda71ecdbcd669f6f0bf70166e8`  
		Last Modified: Tue, 02 Mar 2021 22:58:01 GMT  
		Size: 7.7 MB (7679142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283842abaafca041a2d1402d68201a71661c7263b90f53e2b8ef3544997e7832`  
		Last Modified: Tue, 02 Mar 2021 22:57:59 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43bafde07cc7d4f3be5a0a8e9b9c558d776373cf9e0e8e44613b61c03426c17`  
		Last Modified: Tue, 02 Mar 2021 22:57:59 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; 386

```console
$ docker pull redis@sha256:123dbfb68e0c53a77d3bf49e0a56ecc15185c945c867447419ec4463e0b06ac5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10535144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75f0b80b3c3efb3ed1d776fa6239f6207289dd55f903f2819a264352bed28de`
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
# Tue, 02 Mar 2021 22:46:05 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 22:46:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 22:46:05 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 22:47:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:47:30 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:47:30 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:47:30 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:47:30 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:47:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:47:31 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:47:31 GMT
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
	-	`sha256:20f0031ba098d7a958ad6ea36256d20bc59c67212b4eff31aa8bcce3be06f044`  
		Last Modified: Tue, 02 Mar 2021 22:54:06 GMT  
		Size: 7.3 MB (7324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c9c50c1397d9a6c34ff930c4389e38c9849b8c2bcb1ddcda790f57b9e0d255`  
		Last Modified: Tue, 02 Mar 2021 22:54:04 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85fc3aa7ce52646a826d5a82470f25ff016d2f9ab3bc81de99bec8df044c3cf`  
		Last Modified: Tue, 02 Mar 2021 22:54:04 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; ppc64le

```console
$ docker pull redis@sha256:08e39c204bb671b43bb68ff15740d6bfc6a7246f6f5b032d4f94b26a58ccb079
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11386725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08da6b23484c3cea8ee8b7b8e7907ac72aaa6bab159a88541696bd755f114b48`
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
# Tue, 23 Feb 2021 00:45:55 GMT
ENV REDIS_VERSION=6.2.0
# Tue, 23 Feb 2021 00:45:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.0.tar.gz
# Tue, 23 Feb 2021 00:46:05 GMT
ENV REDIS_DOWNLOAD_SHA=67d624c25d962bd68aff8812a135df85bad07556b8825f3bcd5b522a9932dbca
# Tue, 23 Feb 2021 00:47:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 23 Feb 2021 00:47:41 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 23 Feb 2021 00:47:48 GMT
VOLUME [/data]
# Tue, 23 Feb 2021 00:47:57 GMT
WORKDIR /data
# Tue, 23 Feb 2021 00:48:00 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 23 Feb 2021 00:48:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Feb 2021 00:48:14 GMT
EXPOSE 6379
# Tue, 23 Feb 2021 00:48:17 GMT
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
	-	`sha256:188859fc0b7d47c65108e13f339e9031622f82836da357c2cc5b8ba192e483c7`  
		Last Modified: Tue, 23 Feb 2021 01:04:23 GMT  
		Size: 8.2 MB (8181113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c499a2d23c02bb67a1a4ec11bfc15a50d913c65d386bfb4bf6e950de01cc952f`  
		Last Modified: Tue, 23 Feb 2021 01:04:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa81ca98255392aca1e830f1f09353abc07def5f77c58f7d4e8515d7f64ea50a`  
		Last Modified: Tue, 23 Feb 2021 01:04:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.13` - linux; s390x

```console
$ docker pull redis@sha256:65cdee78a0dde850f16ea6c66ee28105012aa54906408ebd01278a85cd537015
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10984755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72afae9628b149261b81298a19f91c432ee4d7374d655f0d307925cc6c5d7ea4`
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
# Tue, 02 Mar 2021 22:48:13 GMT
ENV REDIS_VERSION=6.2.1
# Tue, 02 Mar 2021 22:48:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.1.tar.gz
# Tue, 02 Mar 2021 22:48:13 GMT
ENV REDIS_DOWNLOAD_SHA=cd222505012cce20b25682fca931ec93bd21ae92cb4abfe742cf7b76aa907520
# Tue, 02 Mar 2021 22:48:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Mar 2021 22:48:54 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Mar 2021 22:48:54 GMT
VOLUME [/data]
# Tue, 02 Mar 2021 22:48:54 GMT
WORKDIR /data
# Tue, 02 Mar 2021 22:48:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Mar 2021 22:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 22:48:55 GMT
EXPOSE 6379
# Tue, 02 Mar 2021 22:48:55 GMT
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
	-	`sha256:98e553c04dd356361f1616cd3403d36256c564e5886033162971e7063d92d179`  
		Last Modified: Tue, 02 Mar 2021 22:52:42 GMT  
		Size: 8.0 MB (7991754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28756d2d966278e27597a5347803a9b1873edcf0495feaf20c2e6ef0b904afd`  
		Last Modified: Tue, 02 Mar 2021 22:52:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c76f98065b7074aa279e721bbf6727ccea87cdf4e463ddfc7b10853dddb75`  
		Last Modified: Tue, 02 Mar 2021 22:52:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
