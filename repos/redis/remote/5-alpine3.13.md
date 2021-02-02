## `redis:5-alpine3.13`

```console
$ docker pull redis@sha256:65df4def537309695ffa9c8a7df7492c7cd2ac2fe16df9766627a0f9251e1477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v7

### `redis:5-alpine3.13` - linux; arm variant v7

```console
$ docker pull redis@sha256:d9da4845c1ec9538bd7c7a3716034d302caa329807f27ca88a2b5af4abe27343
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd84bb141c9b238fa398ef930bf2eb738c433bd5d63ca4bab4557a697875727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 28 Jan 2021 23:58:03 GMT
ADD file:98a89b90a8b442eed5301790dd2bd3a27391c5e4426126eed9d1cf44e70f8857 in / 
# Thu, 28 Jan 2021 23:58:04 GMT
CMD ["/bin/sh"]
# Tue, 02 Feb 2021 00:00:22 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Tue, 02 Feb 2021 00:00:25 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Tue, 02 Feb 2021 00:02:56 GMT
ENV REDIS_VERSION=5.0.10
# Tue, 02 Feb 2021 00:02:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.10.tar.gz
# Tue, 02 Feb 2021 00:02:57 GMT
ENV REDIS_DOWNLOAD_SHA=e30a5e7d1593a715cdda2a82deb90190816d06c9d1dc1ef5b36874878c683382
# Tue, 02 Feb 2021 00:03:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Tue, 02 Feb 2021 00:03:45 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 02 Feb 2021 00:03:46 GMT
VOLUME [/data]
# Tue, 02 Feb 2021 00:03:46 GMT
WORKDIR /data
# Tue, 02 Feb 2021 00:03:47 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Tue, 02 Feb 2021 00:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Feb 2021 00:03:49 GMT
EXPOSE 6379
# Tue, 02 Feb 2021 00:03:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9b1db703a337d301b1d50292acfbabd5fb3796511b962410c554420b85cd78dc`  
		Last Modified: Thu, 28 Jan 2021 23:58:38 GMT  
		Size: 2.4 MB (2423559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c0ecfd6e2eba4b46b63f4beb483e9b76877965389358309076cdd88b8d8884`  
		Last Modified: Tue, 02 Feb 2021 00:04:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da387217b889423e539e0613718b49be44f008bf38c9cc4243cc944ba128f259`  
		Last Modified: Tue, 02 Feb 2021 00:04:45 GMT  
		Size: 383.0 KB (383026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e270f6a3248b7b5daa5eb718d22a8b1d8bf965add3abd99abb834bb75521ebf9`  
		Last Modified: Tue, 02 Feb 2021 00:05:25 GMT  
		Size: 6.5 MB (6462360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a567f7705e87a33667d80add84c5b42b36d97f9ecf6eb3458527169cc24b6`  
		Last Modified: Tue, 02 Feb 2021 00:05:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a830a47fb80451e8ef582a971c39a58073152270f0dd98b8a4aa24af31922041`  
		Last Modified: Tue, 02 Feb 2021 00:05:22 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
