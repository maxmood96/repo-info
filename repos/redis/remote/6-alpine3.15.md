## `redis:6-alpine3.15`

```console
$ docker pull redis@sha256:4a7ca0b26140a779529e58391b79d66b275d5631a7663a054b19ff3ca9c0a8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; 386

### `redis:6-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:6d8f06cfacafc0c6eff32b2f49a137cf6f358e8878944f68edce50269f5f215f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d44f444e409727b3ebaaceed9372619170545063ad6779705631faddea2f92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Mon, 29 Nov 2021 23:48:22 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 29 Nov 2021 23:48:24 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 29 Nov 2021 23:48:25 GMT
ENV REDIS_VERSION=6.2.6
# Mon, 29 Nov 2021 23:48:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.6.tar.gz
# Mon, 29 Nov 2021 23:48:27 GMT
ENV REDIS_DOWNLOAD_SHA=5b2b8b7a50111ef395bf1c1d5be11e6e167ac018125055daa8b5c2317ae131ab
# Mon, 29 Nov 2021 23:49:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 29 Nov 2021 23:49:07 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 29 Nov 2021 23:49:08 GMT
VOLUME [/data]
# Mon, 29 Nov 2021 23:49:09 GMT
WORKDIR /data
# Mon, 29 Nov 2021 23:49:11 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 29 Nov 2021 23:49:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Nov 2021 23:49:12 GMT
EXPOSE 6379
# Mon, 29 Nov 2021 23:49:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db32390bbc16543d05f686f36c491baece0c1407efa765e5db511efeac8ec546`  
		Last Modified: Mon, 29 Nov 2021 23:52:37 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c030453dedfde348ec68dfb3cba10f71738309cae943b342132300e64f74da3`  
		Last Modified: Mon, 29 Nov 2021 23:52:37 GMT  
		Size: 407.1 KB (407110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11b379f42a3d7987e4051f5e596cfbda59590373b942fc5a78bfe5fe23e2573`  
		Last Modified: Mon, 29 Nov 2021 23:52:38 GMT  
		Size: 7.7 MB (7709629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dc3ae61738141b3bb670f49e624de1d39fdee29e63c4df5ee33a83462689f3`  
		Last Modified: Mon, 29 Nov 2021 23:52:38 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa03246c608c7cbd68f358619dbd08a83f3fc791aa62e4c0fbf6b2fdc72a58d`  
		Last Modified: Mon, 29 Nov 2021 23:52:37 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.15` - linux; 386

```console
$ docker pull redis@sha256:fbaa099fb78776ad4b4c87f93ba43f4eba04c1e7268339c3550cd144ad014db0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10597134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a77a28f19b46c8e0158d71e6bee5d207ab86ce94e034c35e40e83462818a578`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Mon, 29 Nov 2021 23:47:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 29 Nov 2021 23:47:12 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 29 Nov 2021 23:47:12 GMT
ENV REDIS_VERSION=6.2.6
# Mon, 29 Nov 2021 23:47:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.6.tar.gz
# Mon, 29 Nov 2021 23:47:12 GMT
ENV REDIS_DOWNLOAD_SHA=5b2b8b7a50111ef395bf1c1d5be11e6e167ac018125055daa8b5c2317ae131ab
# Mon, 29 Nov 2021 23:48:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 29 Nov 2021 23:48:24 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 29 Nov 2021 23:48:24 GMT
VOLUME [/data]
# Mon, 29 Nov 2021 23:48:24 GMT
WORKDIR /data
# Mon, 29 Nov 2021 23:48:24 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 29 Nov 2021 23:48:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Nov 2021 23:48:25 GMT
EXPOSE 6379
# Mon, 29 Nov 2021 23:48:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e3f9be63f9fd461492801006e23ba1908aef1323ee5735bdc50d06c5deb33`  
		Last Modified: Mon, 29 Nov 2021 23:52:42 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e650f0327bde358acf887bcb562c61283965e8b8fd0f6d84bc2ad70241d77a`  
		Last Modified: Mon, 29 Nov 2021 23:52:42 GMT  
		Size: 412.7 KB (412651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf00273a4c2b95bb95ecc7578f74ae3d43f6e645b83410c3ea8c6f8c060ccac`  
		Last Modified: Mon, 29 Nov 2021 23:52:44 GMT  
		Size: 7.4 MB (7355554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a109e092ca9844a99700274bf71e14f17ed2cf9100e36adce39f8298de74f2`  
		Last Modified: Mon, 29 Nov 2021 23:52:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97691f33b156a440de0846ea94dd70ce4723904836a7f7e36b371d5e52c89ee1`  
		Last Modified: Mon, 29 Nov 2021 23:52:42 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
