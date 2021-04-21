## `redis:6-alpine3.13`

```console
$ docker pull redis@sha256:f9577ac6e68c70b518e691406f2bebee49d8db22118fc87bad3b39c16a1cb46e
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

### `redis:6-alpine3.13` - linux; amd64

```console
$ docker pull redis@sha256:1e194b7298d21bcbb4531af65db5fcb830b487da8d595610bad3fb05f3e67c62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10885806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554d20f2036575e9d396d422c1569277738aa170aefcf88febbf08442cee0a08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:38:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 02:38:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 20 Apr 2021 23:46:11 GMT
ENV REDIS_VERSION=6.2.2
# Tue, 20 Apr 2021 23:46:11 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Tue, 20 Apr 2021 23:46:11 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Tue, 20 Apr 2021 23:47:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 20 Apr 2021 23:47:19 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 20 Apr 2021 23:47:19 GMT
VOLUME [/data]
# Tue, 20 Apr 2021 23:47:19 GMT
WORKDIR /data
# Tue, 20 Apr 2021 23:47:20 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 20 Apr 2021 23:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Apr 2021 23:47:20 GMT
EXPOSE 6379
# Tue, 20 Apr 2021 23:47:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29712d301e8c43bcd4a36da8a8297d5ff7f68c3d4c3f7113244ff03675fa5e9c`  
		Last Modified: Thu, 15 Apr 2021 02:45:21 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8173c12df40f1578a7b2dfbbc0034a4fbc8ec7c870fd32b9236c2e5e1936616a`  
		Last Modified: Thu, 15 Apr 2021 02:45:22 GMT  
		Size: 384.2 KB (384200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be901b3c77d96f837d4b901b8a1e609118d563ee2d5544c6a2422811e2a10fa`  
		Last Modified: Tue, 20 Apr 2021 23:49:05 GMT  
		Size: 7.7 MB (7687828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33773bf45b44757ab6cb162ea1b1e2f117c9219c9518110e997a8d2abb13fe5`  
		Last Modified: Tue, 20 Apr 2021 23:49:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeb0c30f7e7320e3b209a5f0d7769557abdf11c58dbd9717bccd08e670bc25b`  
		Last Modified: Tue, 20 Apr 2021 23:49:03 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; arm variant v6

```console
$ docker pull redis@sha256:de38e5279c9782376ebcb9b1746b05322606f4137bc1010a95466bd988432dfc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10583851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac16686e09156077b848685289864e5672f294c7dc86acc1b0ca8af48fcbcb50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:28:37 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 05:28:41 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 21 Apr 2021 00:05:58 GMT
ENV REDIS_VERSION=6.2.2
# Wed, 21 Apr 2021 00:05:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Wed, 21 Apr 2021 00:06:01 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Wed, 21 Apr 2021 00:07:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 21 Apr 2021 00:07:05 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Apr 2021 00:07:05 GMT
VOLUME [/data]
# Wed, 21 Apr 2021 00:07:06 GMT
WORKDIR /data
# Wed, 21 Apr 2021 00:07:08 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Wed, 21 Apr 2021 00:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 00:07:09 GMT
EXPOSE 6379
# Wed, 21 Apr 2021 00:07:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccbbd4db84f7364693883d286974083c7239fac9aa12c281ffdb491b7804485`  
		Last Modified: Thu, 15 Apr 2021 05:32:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa1f16547fbe49258acf8ba93c392680545e5ae9dd673fae6f3d31dea09017`  
		Last Modified: Thu, 15 Apr 2021 05:32:26 GMT  
		Size: 388.2 KB (388162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef4a39c6cae5878119c0e2cba284a28e6993e457d8e868e1ce3de00642d3785`  
		Last Modified: Wed, 21 Apr 2021 00:07:58 GMT  
		Size: 7.6 MB (7571752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf321769c2717d541dbe100467414adfc9db83f96ef2473e192d67aed7556cf`  
		Last Modified: Wed, 21 Apr 2021 00:07:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089393b1f8745e78b9b73fbee010fc5148fc9d7a14fdc1c7cfb14cf9ba192cd`  
		Last Modified: Wed, 21 Apr 2021 00:07:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; arm variant v7

```console
$ docker pull redis@sha256:2bc046811059be94270732e1c7ae5ea71164cbe14a6d0c2ca4814bada8f6da79
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10259904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42b6ab9ec9c7b4968bfb629d97df4cf592a272f52a089130c00b3b49ae3aacc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:53:00 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 05:53:04 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 20 Apr 2021 23:40:48 GMT
ENV REDIS_VERSION=6.2.2
# Tue, 20 Apr 2021 23:40:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Tue, 20 Apr 2021 23:40:49 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Tue, 20 Apr 2021 23:41:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 20 Apr 2021 23:41:43 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 20 Apr 2021 23:41:44 GMT
VOLUME [/data]
# Tue, 20 Apr 2021 23:41:44 GMT
WORKDIR /data
# Tue, 20 Apr 2021 23:41:45 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 20 Apr 2021 23:41:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Apr 2021 23:41:47 GMT
EXPOSE 6379
# Tue, 20 Apr 2021 23:41:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20589517e54a354da5d6cb4ea2d35203508b772c35d104b5003a9dd0f2a017`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8858422eeb975991be458833e2120b9fadbfacfb3530991f0e972c3370bb2`  
		Last Modified: Thu, 15 Apr 2021 05:57:37 GMT  
		Size: 383.0 KB (383040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baff8f0847b616609852153c9d5c2244ea0592bd16e6dd7790d404157b9e07bf`  
		Last Modified: Tue, 20 Apr 2021 23:43:00 GMT  
		Size: 7.5 MB (7450912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28bc06215aae56146be91f68e868f4bbc9804460e4ceffa8510fa4eaa8c28e5`  
		Last Modified: Tue, 20 Apr 2021 23:42:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138aa2ebb088c94f185286a9c6b45f7f5e827c513e5fe307db3a4a84b203e11`  
		Last Modified: Tue, 20 Apr 2021 23:42:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:cf65572a0f7319be55980ec5adfdd429e5b55254c8327d36bece7ba1b2e43d9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10791480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14dfbb8ba97f656d922f1f27613858c2e5359521a28f6c8f36f19b45ffc2f27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:14:24 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 07:14:28 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Wed, 21 Apr 2021 00:06:29 GMT
ENV REDIS_VERSION=6.2.2
# Wed, 21 Apr 2021 00:06:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Wed, 21 Apr 2021 00:06:30 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Wed, 21 Apr 2021 00:07:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Wed, 21 Apr 2021 00:07:31 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Apr 2021 00:07:33 GMT
VOLUME [/data]
# Wed, 21 Apr 2021 00:07:35 GMT
WORKDIR /data
# Wed, 21 Apr 2021 00:07:36 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Wed, 21 Apr 2021 00:07:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 00:07:38 GMT
EXPOSE 6379
# Wed, 21 Apr 2021 00:07:39 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f009ede80a4dfb2942ae27d15f3cd96afc249851ba83171edb51346d9e3d975`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea11b4c6f734c1273155ea086da36c719ee65817775dd2a2d3c57cbd531da18`  
		Last Modified: Thu, 15 Apr 2021 07:19:25 GMT  
		Size: 386.0 KB (386003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d4cfb4843a691a31532f48da96d899d4618fc1459b92b8ab235f790c2f6f5a`  
		Last Modified: Wed, 21 Apr 2021 00:08:56 GMT  
		Size: 7.7 MB (7691642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b13d94d21dfbe8f3a9c08ddabf3db55a910910cd5108eaa2f83305c29b7f929`  
		Last Modified: Wed, 21 Apr 2021 00:08:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059d9b30eaac97e5b13484ab545f905ce13ed3691d6117604ab5cb55d52963c8`  
		Last Modified: Wed, 21 Apr 2021 00:08:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; 386

```console
$ docker pull redis@sha256:dff3f2eaf33178881faf20ecb602e82e88bb0c63789e6286ce0cfdf77b1cdfc3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc763f98f8fae440d2ecb1d1c11186b7e85d60e4f70ba56ab04f89d4c628a08d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:39:44 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 06:39:46 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 20 Apr 2021 23:44:14 GMT
ENV REDIS_VERSION=6.2.2
# Tue, 20 Apr 2021 23:44:15 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Tue, 20 Apr 2021 23:44:15 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Tue, 20 Apr 2021 23:45:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 20 Apr 2021 23:45:42 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 20 Apr 2021 23:45:43 GMT
VOLUME [/data]
# Tue, 20 Apr 2021 23:45:43 GMT
WORKDIR /data
# Tue, 20 Apr 2021 23:45:44 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 20 Apr 2021 23:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Apr 2021 23:45:44 GMT
EXPOSE 6379
# Tue, 20 Apr 2021 23:45:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583b1dfa7a770c1329627c5050294279e947bfeba04c300716518c315d1080eb`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e736134af79a478b22deba2ad536f80ae78c0cb383a88d66c2c1c5460fcc1a`  
		Last Modified: Thu, 15 Apr 2021 06:45:05 GMT  
		Size: 390.6 KB (390571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29003783c6621016fca4eab610705fab993a11adf4d7c0b1cbf40c88a65ed10c`  
		Last Modified: Tue, 20 Apr 2021 23:48:43 GMT  
		Size: 7.3 MB (7340283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a094511b139fee2e5cc25d73893866d8f1f3620fecd1ac96b2633785e07c6bf`  
		Last Modified: Tue, 20 Apr 2021 23:48:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbcbf53fcddca3af2bff62a1ebabdac212e44aa9f376888e77e9207d1064897`  
		Last Modified: Tue, 20 Apr 2021 23:48:39 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; ppc64le

```console
$ docker pull redis@sha256:78eb5cc931adbfaf119a9ebe66331a570b742df6fc4d1cab49e0793b0eb0a012
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11409744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870b6ef502ad21b72cabb32d51e1e242d336b037fb4487a51ef5a1e390fbf1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:55:53 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 15 Apr 2021 07:56:17 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 20 Apr 2021 23:32:47 GMT
ENV REDIS_VERSION=6.2.2
# Tue, 20 Apr 2021 23:32:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Tue, 20 Apr 2021 23:32:59 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Tue, 20 Apr 2021 23:34:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 20 Apr 2021 23:34:19 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 20 Apr 2021 23:34:26 GMT
VOLUME [/data]
# Tue, 20 Apr 2021 23:34:34 GMT
WORKDIR /data
# Tue, 20 Apr 2021 23:34:38 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 20 Apr 2021 23:34:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Apr 2021 23:34:55 GMT
EXPOSE 6379
# Tue, 20 Apr 2021 23:35:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846316a488fa621585c7f8607349cf8717e3025cda80dff5a9d73b1761f4c808`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963ad60821f381aebcf57e783a69acea22d4bd86e88ebed8b3ce177afe64012f`  
		Last Modified: Thu, 15 Apr 2021 08:05:10 GMT  
		Size: 390.7 KB (390721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8108583ce09061e9df1c73ccc49a005c8ff635f26ab48a2f3ced158e18fb5d3b`  
		Last Modified: Tue, 20 Apr 2021 23:37:01 GMT  
		Size: 8.2 MB (8204063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec95641f9224faa5282599ffebf493f05b4b24d0419384bb2680c42100ea407`  
		Last Modified: Tue, 20 Apr 2021 23:36:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0b0abac4a933176094a9509811df53118b18ff1236b4269625af234ed76617`  
		Last Modified: Tue, 20 Apr 2021 23:36:58 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.13` - linux; s390x

```console
$ docker pull redis@sha256:78cfb2ad3f5919254d6d89b8dc686d010b49b4787053f719ccf96c588588d52d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11005262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02720a94c4d1e9bc251a40ef5457e037179591680c17bd4a8600a9c90c867f98`
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
# Tue, 20 Apr 2021 23:50:17 GMT
ENV REDIS_VERSION=6.2.2
# Tue, 20 Apr 2021 23:50:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.2.tar.gz
# Tue, 20 Apr 2021 23:50:18 GMT
ENV REDIS_DOWNLOAD_SHA=7a260bb74860f1b88c3d5942bf8ba60ca59f121c6dce42d3017bed6add0b9535
# Tue, 20 Apr 2021 23:51:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 20 Apr 2021 23:51:54 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 20 Apr 2021 23:51:55 GMT
VOLUME [/data]
# Tue, 20 Apr 2021 23:51:55 GMT
WORKDIR /data
# Tue, 20 Apr 2021 23:51:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 20 Apr 2021 23:51:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Apr 2021 23:51:57 GMT
EXPOSE 6379
# Tue, 20 Apr 2021 23:51:58 GMT
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
	-	`sha256:bfe8dc3a84d0e2ac53465ad8767d1df80379476a8e15425786e5dea101e51675`  
		Last Modified: Tue, 20 Apr 2021 23:53:19 GMT  
		Size: 8.0 MB (8011975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337af15f23c0a1e4ae5aa64135af6045b04f7d3094989f0e3284b8efb19cdbe3`  
		Last Modified: Tue, 20 Apr 2021 23:53:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854494d576d750f097696703b5cdf384f053d97b5a4927eccc8c8c558a72ade0`  
		Last Modified: Tue, 20 Apr 2021 23:53:18 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
