## `redis:alpine3.18`

```console
$ docker pull redis@sha256:9150d86fe2a9d03bbdb15bb9758fa5e3d24632386af8f6eb4d675ee4c976f499
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

### `redis:alpine3.18` - linux; amd64

```console
$ docker pull redis@sha256:2d148c557c85309c7cf1bbf15ebc21d5fc370ab1cb913a6c19b74bd29d10801c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15624397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e69f18a4aed932fcb0c7813c85f37977b8a567a3b6ed0057305c90a1a8645d3`
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
# Fri, 29 Sep 2023 03:18:37 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 03:18:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 03:18:37 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 03:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:19:34 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:19:34 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:19:34 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:19:34 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:19:34 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:19:34 GMT
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
	-	`sha256:324f1acb0a49252dbc76aae5d5a869075cf1d89ef3efd61c44c888cf2d5f5562`  
		Last Modified: Fri, 29 Sep 2023 03:22:35 GMT  
		Size: 11.9 MB (11873287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43b88319d8febd8e8c5568906f59ca28864c8ff03cc14262fd2e3a97a951d95`  
		Last Modified: Fri, 29 Sep 2023 03:22:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b054b71c0540bf9a45d960dac5c556b6d75141fa846a0c970361de10295bd811`  
		Last Modified: Fri, 29 Sep 2023 03:22:33 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; arm variant v6

```console
$ docker pull redis@sha256:218a0c4132094384e4880a94dccf7141f25b5f8b4a880096b95dbfd2c629d0c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15518808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0748a3b09ea59ba6f8311d619d6ccbd9ba6f9263d2ee88450c434cef874a18d8`
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
# Fri, 29 Sep 2023 01:52:58 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 01:52:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 01:52:58 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 01:53:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 01:53:39 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 01:53:40 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 01:53:40 GMT
WORKDIR /data
# Fri, 29 Sep 2023 01:53:40 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 01:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 01:53:40 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 01:53:40 GMT
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
	-	`sha256:1091c082288644cc7495d09e528ceb4db59476f30fe826bd30385f3f0a0fde77`  
		Last Modified: Fri, 29 Sep 2023 01:56:01 GMT  
		Size: 12.0 MB (12024591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fb4fbebb6319a2e5726c584da52421f7a6325e56bf5d2c196dc42794601334`  
		Last Modified: Fri, 29 Sep 2023 01:55:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fca140e8cdef73caf0d21e6159bf4066b9b559bf1e4bad35bddd35376947c8e`  
		Last Modified: Fri, 29 Sep 2023 01:55:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; arm variant v7

```console
$ docker pull redis@sha256:5b640d3278fd9e7df795bf3645f4fd37e6d291d5e1cc0649860c312aa90ced97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15138669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0b026ca60280ea834ece684c6947b9f678155e9b584f183585a4695f6d01d9`
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
# Fri, 29 Sep 2023 03:02:56 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 03:02:56 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 03:02:57 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 03:03:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:03:39 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:03:40 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:03:40 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:03:40 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:03:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:03:40 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:03:40 GMT
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
	-	`sha256:cafcba218d7f24e5cba50ee314902afbea65e887eca38da85a2e7ec87701dac9`  
		Last Modified: Fri, 29 Sep 2023 03:06:26 GMT  
		Size: 11.9 MB (11890003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa14754d8bd02d66b63d02670768747cf18793b4313e2dcaa54e080f8c3ccfd`  
		Last Modified: Fri, 29 Sep 2023 03:06:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b5917f8b758c6b3bb8a4c77a0791f1ee96e1c2acfbbf8960c688119e09d562`  
		Last Modified: Fri, 29 Sep 2023 03:06:24 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:e2a186dae59c9d6621c0dfd604f11dbb400e2a5c33a57b68a8654c8f178c3b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15725527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0507ab9af022bcfe9fa2d961c651cdf9d540aee7e5c775888e0886f1befcc99a`
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
# Fri, 29 Sep 2023 02:07:52 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 02:07:52 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 02:07:52 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 02:08:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 02:08:27 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 02:08:27 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 02:08:27 GMT
WORKDIR /data
# Fri, 29 Sep 2023 02:08:27 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 02:08:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 02:08:27 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 02:08:27 GMT
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
	-	`sha256:6ca6319989770021c876af588aa9dca38eb531dfb2251002fac8d91a5a46a8e1`  
		Last Modified: Fri, 29 Sep 2023 02:10:52 GMT  
		Size: 12.0 MB (12044300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab403bb38357d98bc7a80efb7462a8c45a756b6919683a8a901e81ccaaf8eb9d`  
		Last Modified: Fri, 29 Sep 2023 02:10:50 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e736635b0ef0a7665fb3a0c0a9b0b3797f1a355894e47cb3d18487dc9418613`  
		Last Modified: Fri, 29 Sep 2023 02:10:50 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; 386

```console
$ docker pull redis@sha256:462e118367f426b0655b3ed978684fd4a73f21056709c3c96d537147a3c0ac00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15077413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e074b773e063db46a5b9602b10093c0ccc155d1908a24726d761aaaea34c77c`
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
# Fri, 29 Sep 2023 03:30:00 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 03:30:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 03:30:00 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 03:31:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 03:31:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 03:31:41 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 03:31:41 GMT
WORKDIR /data
# Fri, 29 Sep 2023 03:31:41 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 03:31:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 03:31:41 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 03:31:41 GMT
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
	-	`sha256:74e366f76de08579a0a406b9c9b919226cf8afadca5acf7a3df158f4e697ad39`  
		Last Modified: Fri, 29 Sep 2023 03:36:06 GMT  
		Size: 11.5 MB (11492505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a560f5129fba055166be68a2673501f8a4535522cd9dc6f84c681d774a6b595`  
		Last Modified: Fri, 29 Sep 2023 03:36:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5537ff7d66837b4902dd98f2dd6f4873d1d04af3bec60e524c48f27fda3197b3`  
		Last Modified: Fri, 29 Sep 2023 03:36:04 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; ppc64le

```console
$ docker pull redis@sha256:e5960b65e030c91a5a37e33c032a18c9b24c70cc6743ce1d9d7f8e49e71c0d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b00f2088488f15471d3c0f510227598d654d157ec251974f93cb1b88866dcc`
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
# Fri, 29 Sep 2023 04:05:53 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 04:05:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 04:05:54 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 04:07:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 04:07:03 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 04:07:04 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 04:07:05 GMT
WORKDIR /data
# Fri, 29 Sep 2023 04:07:05 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 04:07:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 04:07:08 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 04:07:08 GMT
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
	-	`sha256:e12e169e416e4f0b790da5375fcce04975e87b217b7ff3c8d29699047073989e`  
		Last Modified: Fri, 29 Sep 2023 04:11:18 GMT  
		Size: 12.7 MB (12745575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5e6dc24f77524e8a10525d14a2b22b08af298b22f63e15ecccc2e707a965b0`  
		Last Modified: Fri, 29 Sep 2023 04:11:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6e175160e2556aeb421a1a2fbfdab223065e4e722707feb15f987a111aa9f`  
		Last Modified: Fri, 29 Sep 2023 04:11:15 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; s390x

```console
$ docker pull redis@sha256:773b0d549fd5d7fd53859bad784f9e15c7e6a8d3de647da7741d1f0a3bac336e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15806127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192f3df7e93108343d56031a88424c10c2d496d5bb17e6c1dbcae14cbf85d357`
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
# Fri, 29 Sep 2023 00:09:38 GMT
ENV REDIS_VERSION=7.2.1
# Fri, 29 Sep 2023 00:09:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Fri, 29 Sep 2023 00:09:38 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Fri, 29 Sep 2023 00:10:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 29 Sep 2023 00:10:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 29 Sep 2023 00:10:31 GMT
VOLUME [/data]
# Fri, 29 Sep 2023 00:10:31 GMT
WORKDIR /data
# Fri, 29 Sep 2023 00:10:31 GMT
COPY file:a9e7249f657e2eec627bb4be492ad18aae3e5e1f0e47d22644eaf1ef2138c0ce in /usr/local/bin/ 
# Fri, 29 Sep 2023 00:10:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 00:10:31 GMT
EXPOSE 6379
# Fri, 29 Sep 2023 00:10:31 GMT
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
	-	`sha256:f131b96779127061517297ab04eb050db51cda49c83f9439087a2948f6514932`  
		Last Modified: Fri, 29 Sep 2023 00:14:02 GMT  
		Size: 12.2 MB (12241898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a7cc5a30da091c010c57a2a8af7d98cd82e9ebde375245a181d6d4efec5470`  
		Last Modified: Fri, 29 Sep 2023 00:14:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da074b4cfe4c0023bf10d556d49fdbd4dde6049ad95937c072fc2deeb9ef6367`  
		Last Modified: Fri, 29 Sep 2023 00:14:00 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
