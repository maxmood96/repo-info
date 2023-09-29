## `redis:6-alpine3.18`

```console
$ docker pull redis@sha256:27cc767b08716abe74d13eac7761204c4eee6a4d0b194c561d80f94546919736
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

### `redis:6-alpine3.18` - linux; amd64

```console
$ docker pull redis@sha256:5352ddb4eaa01b89be2faffa6259beb57a37fb6a6775d5c588b8763c511dee9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548e1b98531df3fdba160d11b93abde06bc50f7350aaf822b263a26491a94554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 03:18:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 03:18:37 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 03:20:39 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 03:20:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 03:20:39 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 03:21:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:21:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:21:17 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:21:17 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:21:17 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:21:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:21:17 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:21:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949aaab26a7c944a85191d1103a3216703895060691f12536b531dcd207938b2`  
		Last Modified: Fri, 29 Sep 2023 03:22:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d25a72f6eb6a7fd188d61aaaffae4cd0b332310ae70d8571a304887bbcaa0b7`  
		Last Modified: Fri, 29 Sep 2023 03:22:33 GMT  
		Size: 347.2 KB (347160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca3eaadf11f41fe7a43690ea7f560a2b69230175ed8e1181e61361f5d176da3`  
		Last Modified: Fri, 29 Sep 2023 03:23:16 GMT  
		Size: 7.5 MB (7528454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe00c8ac61c06221327fefb3dd3c85729f749668e4bf61cf5192adcac962de`  
		Last Modified: Fri, 29 Sep 2023 03:23:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c33e23dc9e79e1fa2d53ae46168403b3860b1fd6f00f0da4925dc886382b`  
		Last Modified: Fri, 29 Sep 2023 03:23:15 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; arm variant v6

```console
$ docker pull redis@sha256:c97d70a63a59c856c4c48643c91d97e5cdb3d1448babfb25adc8762a6cc213a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11070245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f87b9f8cb608da65d9fab99f51d8b790d1f6367afed24425fe4e56b932a7b3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:52:56 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 01:52:58 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 01:54:24 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 01:54:24 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 01:54:24 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 01:54:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 01:54:57 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 01:54:57 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 01:54:57 GMT
WORKDIR /data
# Fri, 29 Sep 2023 01:54:57 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 01:54:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 01:54:58 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 01:54:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6390b8e2cdea8f076be8f32d021526f492cec080a58c72916255ebbdb932b9`  
		Last Modified: Fri, 29 Sep 2023 01:55:59 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eaf6970a5d816d576135effb1f27b281846ec654a4d8426ba0052af3933d04`  
		Last Modified: Fri, 29 Sep 2023 01:55:59 GMT  
		Size: 346.9 KB (346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7e3b190a62be1353b23dfec23453e3854914508b1b724013b1217d6f0e2151`  
		Last Modified: Fri, 29 Sep 2023 01:56:37 GMT  
		Size: 7.6 MB (7576030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4eb01537344bb4f35998c5b71ff7b1608d46cf2a3bbbd18461ffb1e44a3cd0b`  
		Last Modified: Fri, 29 Sep 2023 01:56:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1757474bbd4760fe1432723c05c5ef35529cd3aadc38db87b2cc18e112780451`  
		Last Modified: Fri, 29 Sep 2023 01:56:36 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; arm variant v7

```console
$ docker pull redis@sha256:274a507508495e42698d372e426f542cec3374b2497a6ff647a35920d8f73bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10710706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b767a0c05858a00181e5987d2876c6b7da8650980eae34ed19ba92cb32f2a935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 03:02:55 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 03:02:56 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 03:04:33 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 03:04:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 03:04:33 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 03:05:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:05:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:05:09 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:05:09 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:05:09 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:05:09 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:05:09 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf85d1532bd5b85b54876e254d1a4a5bca21624f573ef0695a51ffd167cd77f`  
		Last Modified: Fri, 29 Sep 2023 03:06:24 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf5468a57e4938c3aee829560cb5f5680b207bf097bd50d014d833a3db79b32`  
		Last Modified: Fri, 29 Sep 2023 03:06:24 GMT  
		Size: 346.8 KB (346771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceebcc3d35418d7e42338fe42832bad92c3bcc241a2a0a55e76ac87f4368620`  
		Last Modified: Fri, 29 Sep 2023 03:07:05 GMT  
		Size: 7.5 MB (7462045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12faac300518bc9f6e946bf60818518fe062f4fa32dc55eeeab861f24644a97b`  
		Last Modified: Fri, 29 Sep 2023 03:07:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f485c3e49bd2d0fbb191c9ecb3e9e3de51be7cb68da78ef3774dc55d42fc517`  
		Last Modified: Fri, 29 Sep 2023 03:07:04 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:96c730f2c9b019f6d071e23d760b57434b29eb31a19f0cafea2d6aaffbe56e44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f2e3913dcbe429fce591ae054ea71e03c678f9860ec61424b89f2d7d44069c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:07:50 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 02:07:52 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 02:09:13 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 02:09:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 02:09:13 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 02:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 02:09:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 02:09:41 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 02:09:41 GMT
WORKDIR /data
# Fri, 29 Sep 2023 02:09:41 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 02:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:09:42 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 02:09:42 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80ec02a1057155272dc0bbf44c62068b20a1ac34681d39bbfccafe042b292b`  
		Last Modified: Fri, 29 Sep 2023 02:10:50 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cd39eabe55b52786e5a80f6219cfd2744f7f4c0fddd76d871b74cf5ce02804`  
		Last Modified: Fri, 29 Sep 2023 02:10:51 GMT  
		Size: 347.4 KB (347410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae0bad28e5019224b98d21798adb53d7a5eb8214553c58d26c99fb4534f55ab`  
		Last Modified: Fri, 29 Sep 2023 02:11:33 GMT  
		Size: 7.6 MB (7597964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f823368717d0a04741fd050c63508da374f18297a224e67d93d6660cba092c`  
		Last Modified: Fri, 29 Sep 2023 02:11:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088cb07f861c611b7c0cdf3f23b73d11516ce150f911a20ef62fde961f789e09`  
		Last Modified: Fri, 29 Sep 2023 02:11:31 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; 386

```console
$ docker pull redis@sha256:5bc22c5e93a01c1bfcdedd99527df108e3636e76f6cfb5e86c117cbfe372b5c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10843972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de06ac6f6cf1d761303baa595b7036ceaf394bd8f98f9f8f7dd766934748a43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 03:29:58 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 03:30:00 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 03:33:17 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 03:33:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 03:33:17 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 03:34:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:34:23 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:34:23 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:34:24 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:34:24 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:34:24 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:34:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bee1919ddfecf06c9540640bb5cfb18a79dde81eec9fdbf67307a88fb6f769c`  
		Last Modified: Fri, 29 Sep 2023 03:36:04 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f628c56adac4ea53efea4ff752c71cec5c790d55f96b1f10ec6af999dd6fdb23`  
		Last Modified: Fri, 29 Sep 2023 03:36:05 GMT  
		Size: 347.2 KB (347168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095b303d3135ab395e76be9787ee7017367223f8caee177b0d6ad855f1f656ce`  
		Last Modified: Fri, 29 Sep 2023 03:36:46 GMT  
		Size: 7.3 MB (7259062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4ab9a3c366c4d3554a4afe96fecbbb98fd9c83ef3381dc6385f5acc2d71e13`  
		Last Modified: Fri, 29 Sep 2023 03:36:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94631d86d758820412b94aa93717082dae3cf71817967095ae8d5a62d1b246a`  
		Last Modified: Fri, 29 Sep 2023 03:36:45 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; ppc64le

```console
$ docker pull redis@sha256:d25b4ee6514b4091ef5f3b0fcfe1af2efd4d88aae40d6e6e1e5ef319a045e2f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11835406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2603e633b898aa755a825b020408a1fd2f4d9e0505d7f30831b0aa87f8e47326`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 04:05:49 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 04:05:52 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 04:08:27 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 04:08:28 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 04:08:28 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 04:09:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 04:09:21 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 04:09:23 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 04:09:25 GMT
WORKDIR /data
# Fri, 29 Sep 2023 04:09:25 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 04:09:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 04:09:26 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 04:09:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0298f37bf824b5c08616ec38d5dffa969d8e9c7a082e5ecf398d88b1ad7d520e`  
		Last Modified: Fri, 29 Sep 2023 04:11:16 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a574d82aba203c3f8a2f3dd483c11d01a1d51246cf7a497a0f4aff9323a91e46`  
		Last Modified: Fri, 29 Sep 2023 04:11:15 GMT  
		Size: 347.5 KB (347458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943f324fe477533d5902a62eb56c93d88a8b3b201401f2c708a95cbd195e5d1f`  
		Last Modified: Fri, 29 Sep 2023 04:12:01 GMT  
		Size: 8.1 MB (8139456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8615a12a76e817f22b2796d1d64e732fabf165cdafe209b12fe1fd5ff95a628f`  
		Last Modified: Fri, 29 Sep 2023 04:11:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6665d2e7240593027a23869a8088b579336435642a04e5a822eb2e39e3dcb7e5`  
		Last Modified: Fri, 29 Sep 2023 04:11:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.18` - linux; s390x

```console
$ docker pull redis@sha256:e8888e7851eff41e9d447965d0662e00c521de4c48baedc3b7f77f7b29d248fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11390435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cc5f7dde9789035119384b6db2f14a6708c4f435b9e838bc85be8ae66687eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:09:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 29 Sep 2023 00:09:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 29 Sep 2023 00:11:51 GMT
ENV REDIS_VERSION=6.2.13
# Fri, 29 Sep 2023 00:11:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.13.tar.gz
# Fri, 29 Sep 2023 00:11:51 GMT
ENV REDIS_DOWNLOAD_SHA=89ff27c80d420456a721ccfb3beb7cc628d883c53059803513749e13214a23d1
# Fri, 29 Sep 2023 00:12:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 00:12:27 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 00:12:27 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 00:12:28 GMT
WORKDIR /data
# Fri, 29 Sep 2023 00:12:28 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 00:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 00:12:28 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 00:12:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd0f793a7b34c1ee0505820f6568cce068201e7c6fa5f94566a04b88b45debb`  
		Last Modified: Fri, 29 Sep 2023 00:14:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a813b472c6527d734d55b55e1a63f985c2ff9528d0d8cdd9b5f1000cbe62c`  
		Last Modified: Fri, 29 Sep 2023 00:14:00 GMT  
		Size: 347.1 KB (347145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb89c9d0eb39f6294c81fcaefc30c3c2de306eeda0139a80ed929b8e055bcd4`  
		Last Modified: Fri, 29 Sep 2023 00:14:31 GMT  
		Size: 7.8 MB (7826207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4dab405240de836afe1ff2a1e67e051a00b7a8086bea5ab366c27f26bb678`  
		Last Modified: Fri, 29 Sep 2023 00:14:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242c2d32815e6f232838fdb39f8cb9807a719f8145dfb21f88209d874dd9a05c`  
		Last Modified: Fri, 29 Sep 2023 00:14:30 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
