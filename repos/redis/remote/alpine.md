## `redis:alpine`

```console
$ docker pull redis@sha256:9696ac9bf341f88955258df426dd51240f21d74a63bd192ed67cb13ee6c711c5
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
$ docker pull redis@sha256:d937dcf39e204d8c1d148544d94cb542a60bac0dfddb83b62939f7ec1ae9a865
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12387370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f27449bcb80865d48c2189284e3134c0d21b035bba4eac3244a962519dac6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Fri, 02 Dec 2022 00:29:41 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 02 Dec 2022 00:29:42 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 12 Dec 2022 21:07:11 GMT
ENV REDIS_VERSION=7.0.6
# Mon, 12 Dec 2022 21:07:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.6.tar.gz
# Mon, 12 Dec 2022 21:07:12 GMT
ENV REDIS_DOWNLOAD_SHA=7b33a7e890d13e27af1f246acb16312669ad8a1d56ce8f807dfbcd3c09aa7bb3
# Mon, 12 Dec 2022 21:07:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 12 Dec 2022 21:07:54 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 12 Dec 2022 21:07:54 GMT
VOLUME [/data]
# Mon, 12 Dec 2022 21:07:54 GMT
WORKDIR /data
# Mon, 12 Dec 2022 21:07:54 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Mon, 12 Dec 2022 21:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Dec 2022 21:07:55 GMT
EXPOSE 6379
# Mon, 12 Dec 2022 21:07:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a990ecc86f092d159c35dbd34b9495256da8d34d3b30f4a2cae249c4d148139`  
		Last Modified: Fri, 02 Dec 2022 00:32:28 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2520a938316fcd3430657090cec57e14416dafca8e96c09a25e885dcfadc8da`  
		Last Modified: Fri, 02 Dec 2022 00:32:29 GMT  
		Size: 347.7 KB (347684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358511a055269d4c487475e9f4c999683d45ab19d9e5c133b8989bf79aacc96f`  
		Last Modified: Mon, 12 Dec 2022 21:10:33 GMT  
		Size: 8.7 MB (8666998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c098870afba4a3e66e507edf38c26df54397435047be596dd80ade1e5fd42d9`  
		Last Modified: Mon, 12 Dec 2022 21:10:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cf08ccc0abb328e0a22392d69a6a5fd487008208bc543a4688324b2e86231f`  
		Last Modified: Mon, 12 Dec 2022 21:10:31 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:ba1822fc334736c2f9db2894ff22dca6173469c4d84b6d37ea5dda21a4b25f18
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12206274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd02209639c412a44b8d0b996c998d38cea54bd44fbd9f2de3cc36599d54a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 23:51:31 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 01 Dec 2022 23:51:33 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 12 Dec 2022 23:22:07 GMT
ENV REDIS_VERSION=7.0.6
# Mon, 12 Dec 2022 23:22:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.6.tar.gz
# Mon, 12 Dec 2022 23:22:08 GMT
ENV REDIS_DOWNLOAD_SHA=7b33a7e890d13e27af1f246acb16312669ad8a1d56ce8f807dfbcd3c09aa7bb3
# Mon, 12 Dec 2022 23:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 12 Dec 2022 23:22:52 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 12 Dec 2022 23:22:53 GMT
VOLUME [/data]
# Mon, 12 Dec 2022 23:22:53 GMT
WORKDIR /data
# Mon, 12 Dec 2022 23:22:53 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Mon, 12 Dec 2022 23:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Dec 2022 23:22:53 GMT
EXPOSE 6379
# Mon, 12 Dec 2022 23:22:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91688d0a8d4b6e99c48c41f5fe1a16e0f9b3f2aa685d708c6193c02690525bc`  
		Last Modified: Thu, 01 Dec 2022 23:54:44 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c2c061cfa4c7fd9f8755ec721a5fa2fda537b2d82bba53ef33835f5cc28d2`  
		Last Modified: Thu, 01 Dec 2022 23:54:44 GMT  
		Size: 347.8 KB (347780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8598f527249991730106b4d76d3f973e4b24ef06c3be61889459ce00e1b7837`  
		Last Modified: Mon, 12 Dec 2022 23:25:01 GMT  
		Size: 8.7 MB (8749439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6a5405e52d2d6d998ab5a010d3354004d159768e39895efecf249ac26246b`  
		Last Modified: Mon, 12 Dec 2022 23:24:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a824e2c4ded02d9ef906b6914d07db8da9c152568c530dbec98b5b07ede2c4f0`  
		Last Modified: Mon, 12 Dec 2022 23:24:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1267a071f923a44756b6bf5187784a578dceab89ba6fd9daa4f312fafcb9c65a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11840684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a34c8d9636befed62795b7a64ee070440e93c32189d4a278d69aaf1bb9d4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Fri, 02 Dec 2022 00:01:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 02 Dec 2022 00:01:15 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 12 Dec 2022 23:56:35 GMT
ENV REDIS_VERSION=7.0.6
# Mon, 12 Dec 2022 23:56:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.6.tar.gz
# Mon, 12 Dec 2022 23:56:36 GMT
ENV REDIS_DOWNLOAD_SHA=7b33a7e890d13e27af1f246acb16312669ad8a1d56ce8f807dfbcd3c09aa7bb3
# Mon, 12 Dec 2022 23:57:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 12 Dec 2022 23:57:17 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 12 Dec 2022 23:57:17 GMT
VOLUME [/data]
# Mon, 12 Dec 2022 23:57:17 GMT
WORKDIR /data
# Mon, 12 Dec 2022 23:57:17 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Mon, 12 Dec 2022 23:57:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Dec 2022 23:57:17 GMT
EXPOSE 6379
# Mon, 12 Dec 2022 23:57:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2eb8d5aa57e030bf1ddee4aa613ecca25cd292516e78214cf4bc28434cd74`  
		Last Modified: Fri, 02 Dec 2022 00:05:28 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959709b3ec332ce2d9e6b098114c0624343032d61ecee79a38f70c4a951db9d7`  
		Last Modified: Fri, 02 Dec 2022 00:05:29 GMT  
		Size: 347.6 KB (347604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5ce30ac70ce7353dde4e4dc67cb4666f9e86c939944b0ede1bdabbb74a5b5e`  
		Last Modified: Tue, 13 Dec 2022 00:01:26 GMT  
		Size: 8.6 MB (8625811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f019bdae13bd8d6e818924f18c46f28ab9d0efcf115c73ddc7351ab3df3a12f2`  
		Last Modified: Tue, 13 Dec 2022 00:01:24 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e1cab11da9c458034c5364239d8b83ef0dcbfb789c74bcadd5715b1202e4e4`  
		Last Modified: Tue, 13 Dec 2022 00:01:24 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2531ab66a8e7d1ee63c500366947640035fca3849e2c0ed5ace7551a64c89a4f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12369676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03be620fd3be11d3da8eb80526cfa37ae63c562f480af01723f2732f45d4626`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 23:59:13 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 01 Dec 2022 23:59:14 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 16 Dec 2022 23:01:37 GMT
ENV REDIS_VERSION=7.0.7
# Fri, 16 Dec 2022 23:01:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.7.tar.gz
# Fri, 16 Dec 2022 23:01:37 GMT
ENV REDIS_DOWNLOAD_SHA=8d327d7e887d1bb308fc37aaf717a0bf79f58129e3739069aaeeae88955ac586
# Fri, 16 Dec 2022 23:02:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 16 Dec 2022 23:02:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Dec 2022 23:02:09 GMT
VOLUME [/data]
# Fri, 16 Dec 2022 23:02:09 GMT
WORKDIR /data
# Fri, 16 Dec 2022 23:02:09 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 16 Dec 2022 23:02:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Dec 2022 23:02:09 GMT
EXPOSE 6379
# Fri, 16 Dec 2022 23:02:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8fc6a3465ef1129a850e221e8e43c4b8381cccc6c4fa4e930cc23a4524796d`  
		Last Modified: Fri, 02 Dec 2022 00:01:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9545f2103602ed70183810dd35d0e551444688abbc0b13f83d45635978e07c`  
		Last Modified: Fri, 02 Dec 2022 00:01:43 GMT  
		Size: 347.9 KB (347902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2491a2e1fd67a1258830ed4ca412de5d49da05edd8c3c32b56dfc36166c84f`  
		Last Modified: Fri, 16 Dec 2022 23:04:08 GMT  
		Size: 8.8 MB (8760608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da7b5bc298119eb9d3a62717ab733d009b1d3a261dd7502771c6a3ebd27e38a`  
		Last Modified: Fri, 16 Dec 2022 23:04:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd92ccede6a3a25f015152d5ff278163c59f1a1ccc398e8ad3f386750262445`  
		Last Modified: Fri, 16 Dec 2022 23:04:07 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:488aca5b94aa5e7770843639571d50e5adc9864b7959629d10d3656c6e4b0fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12061238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ea8cc63218abdf358d6a2f2d3d23b67c9ce737b685e21fe41177e9de550946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:38:24 GMT
ADD file:f2fbc3153694110f7004f005c4e18435b171ed44a3b35498a1b4916ef1e9af43 in / 
# Tue, 22 Nov 2022 22:38:25 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 23:41:23 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 01 Dec 2022 23:41:25 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 12 Dec 2022 20:39:56 GMT
ENV REDIS_VERSION=7.0.6
# Mon, 12 Dec 2022 20:39:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.6.tar.gz
# Mon, 12 Dec 2022 20:39:58 GMT
ENV REDIS_DOWNLOAD_SHA=7b33a7e890d13e27af1f246acb16312669ad8a1d56ce8f807dfbcd3c09aa7bb3
# Mon, 12 Dec 2022 20:40:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 12 Dec 2022 20:40:40 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 12 Dec 2022 20:40:41 GMT
VOLUME [/data]
# Mon, 12 Dec 2022 20:40:42 GMT
WORKDIR /data
# Mon, 12 Dec 2022 20:40:44 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Mon, 12 Dec 2022 20:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Dec 2022 20:40:45 GMT
EXPOSE 6379
# Mon, 12 Dec 2022 20:40:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cc7ae06783159e8c992cfb745833f904e836c74a7704b7a90b4b45a598f878c`  
		Last Modified: Tue, 22 Nov 2022 22:39:08 GMT  
		Size: 3.4 MB (3408493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d61dea6f00f2844356f7ee0cc0eca021e7053fa5d26798b08183a14cb48c41`  
		Last Modified: Thu, 01 Dec 2022 23:45:36 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc9b5b1115874977c1fa433d9911d52b88445b267222a2685f9628a90e15a92`  
		Last Modified: Thu, 01 Dec 2022 23:45:36 GMT  
		Size: 347.6 KB (347603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4836a86b4a50e68f94c09b5eb8f3559c97b318fc85a37ec8909173f48b807d7`  
		Last Modified: Mon, 12 Dec 2022 20:44:39 GMT  
		Size: 8.3 MB (8303228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24e265541853b08282ab9ca97ff09f0b92b74cbaacbf3c1781e4337005c5116`  
		Last Modified: Mon, 12 Dec 2022 20:44:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad85e0acd03a51713f5568e168765f4b99033abad442d1805af57a58898d820`  
		Last Modified: Mon, 12 Dec 2022 20:44:38 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:57fdbdf796008ffacfb734c11290adfdd8c329ac9c666c0ee76265fcf5202019
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12989222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ab4387208ef0ae8f54ff62929567da5a79ff720242d4e22125fe30f1f51996`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 23 Nov 2022 00:18:18 GMT
ADD file:a8e68f93c597f70ce637ef578c72c9b41b4b8d80b552b8e5570d4efcc1d02ff5 in / 
# Wed, 23 Nov 2022 00:18:18 GMT
CMD ["/bin/sh"]
# Fri, 02 Dec 2022 00:19:09 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 02 Dec 2022 00:19:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 12 Dec 2022 22:09:59 GMT
ENV REDIS_VERSION=7.0.6
# Mon, 12 Dec 2022 22:09:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.6.tar.gz
# Mon, 12 Dec 2022 22:09:59 GMT
ENV REDIS_DOWNLOAD_SHA=7b33a7e890d13e27af1f246acb16312669ad8a1d56ce8f807dfbcd3c09aa7bb3
# Mon, 12 Dec 2022 22:10:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 12 Dec 2022 22:10:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 12 Dec 2022 22:10:57 GMT
VOLUME [/data]
# Mon, 12 Dec 2022 22:10:57 GMT
WORKDIR /data
# Mon, 12 Dec 2022 22:10:58 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Mon, 12 Dec 2022 22:10:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Dec 2022 22:10:58 GMT
EXPOSE 6379
# Mon, 12 Dec 2022 22:10:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:69314845b945e4b33e4ee552d0e4156645f71c81b6cb71108c1e32e139aec052`  
		Last Modified: Wed, 23 Nov 2022 00:19:02 GMT  
		Size: 3.4 MB (3384500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cfdac3009c2f827e7dc6432edc1f3726b1ba8a8f35b7ff173284e78a7516ed`  
		Last Modified: Fri, 02 Dec 2022 00:23:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3786223a169388cd0603f29896b77f4deff5978199f9db1783b026551007d3`  
		Last Modified: Fri, 02 Dec 2022 00:23:50 GMT  
		Size: 347.9 KB (347932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64197a4d41e5861bcbc00a9b324ca26c2754de1aea0e88d72185e4be8ac8b258`  
		Last Modified: Mon, 12 Dec 2022 22:15:35 GMT  
		Size: 9.3 MB (9254806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2959ed807c21bf08ee1c807dc86e6878d2621809f2f79e3ce6073abe6af3fc0`  
		Last Modified: Mon, 12 Dec 2022 22:15:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d71b759acc5946c5042f89bfb847de975164534fbda1b443b29ea2bac9584a9`  
		Last Modified: Mon, 12 Dec 2022 22:15:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:656d6d81e183f8643b10a33c5614716cc3dd92657f10e8428389ef63d553960c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88861feed5d5aa4e67511f2c2f8b5a4f5bdd3440fcb56c1dac1d85ec0a8a558`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 22 Nov 2022 22:47:02 GMT
ADD file:d8cbd162b64e4b7a8b83086be37ef5ee69e955ac955ebbe59e70c6be2a2d1a9f in / 
# Tue, 22 Nov 2022 22:47:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Dec 2022 23:46:57 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 01 Dec 2022 23:46:58 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 16 Dec 2022 22:44:37 GMT
ENV REDIS_VERSION=7.0.7
# Fri, 16 Dec 2022 22:44:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.7.tar.gz
# Fri, 16 Dec 2022 22:44:38 GMT
ENV REDIS_DOWNLOAD_SHA=8d327d7e887d1bb308fc37aaf717a0bf79f58129e3739069aaeeae88955ac586
# Fri, 16 Dec 2022 22:45:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 16 Dec 2022 22:45:35 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Dec 2022 22:45:36 GMT
VOLUME [/data]
# Fri, 16 Dec 2022 22:45:36 GMT
WORKDIR /data
# Fri, 16 Dec 2022 22:45:37 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 16 Dec 2022 22:45:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Dec 2022 22:45:38 GMT
EXPOSE 6379
# Fri, 16 Dec 2022 22:45:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:844b8973ca9523380e35625da9a5fd2d50338c403129146541e13d0722c056f7`  
		Last Modified: Tue, 22 Nov 2022 22:47:59 GMT  
		Size: 3.2 MB (3170814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1be814075d1274a0e9bcb59929c7021970d8964094b5e2ad21d1d9d97776bb`  
		Last Modified: Thu, 01 Dec 2022 23:51:08 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c07df67a06c981699be9f591dda0031fe1c1680c39d733f9f4b22de636d128`  
		Last Modified: Thu, 01 Dec 2022 23:51:08 GMT  
		Size: 347.7 KB (347658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b86ebd6b0f5502c95e685f4c04d25656bfb9b68eb927db679ba614838154272`  
		Last Modified: Fri, 16 Dec 2022 22:47:55 GMT  
		Size: 8.9 MB (8879321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65831bdd78d8134c7f2373283f487c9b771f41b7c097df20447f264fb2f8b94a`  
		Last Modified: Fri, 16 Dec 2022 22:47:54 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0895361c3c159162694999fe989091d74463de10d21739e84fbac90552a607f`  
		Last Modified: Fri, 16 Dec 2022 22:47:54 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
