## `redis:4-alpine3.11`

```console
$ docker pull redis@sha256:344140edd4147197d2ae2f5e18cd8c6e5d5aa4ea957891a41225266f64e7ec16
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

### `redis:4-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:b2bf19db472e101d4158b805e346b70df605cc492c7b70e2078fb41cf18ad0b6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7707667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c45b0328e1b552cab82419dde9d51b444ed3dac454195e721df395cc9dcc47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 19 Dec 2019 23:21:54 GMT
ADD file:c7d28fcb71c026d7956b381180e4792c8219b04904e726a9266322ef5b256df8 in / 
# Thu, 19 Dec 2019 23:21:54 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 17:57:31 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 17:57:33 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 18:01:52 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 18:01:52 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 18:01:53 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 18:02:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 18:02:51 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 18:02:51 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 18:02:51 GMT
WORKDIR /data
# Mon, 23 Dec 2019 18:02:52 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 18:02:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 18:02:52 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 18:02:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:63bc94deeb2884fd684a72d356164664538ee55cd82a9e65afe300a432092744`  
		Last Modified: Thu, 19 Dec 2019 23:22:17 GMT  
		Size: 2.8 MB (2801746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828e397560e3f433323235a7b574889ae44269b4cdb9f9a7e49ff97c88fd59fc`  
		Last Modified: Mon, 23 Dec 2019 18:04:05 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5902d88df6c21a394367845e8f15a2c6a4cc170caabebd97f484311c6407c1f2`  
		Last Modified: Mon, 23 Dec 2019 18:04:05 GMT  
		Size: 402.5 KB (402544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3be5d4595c10138c81ef1666cdde750198be9b5b46aaa799b61ae251ed5d1`  
		Last Modified: Mon, 23 Dec 2019 18:04:27 GMT  
		Size: 4.5 MB (4501633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0976e50085ecbd18677085968bebb12d281bbdd59570846c777a7311ad889`  
		Last Modified: Mon, 23 Dec 2019 18:04:26 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62431ad8a6a877123fe8dd73e25e1597be753e7a715c2abf6c4058b363fcc826`  
		Last Modified: Mon, 23 Dec 2019 18:04:26 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:f4975c6b6b8b21aba2710f2448d2c32a8b3b806654538049f1aab1f6f70a4c77
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f879d6d033b24d1406e464a3c221e80465170dead2c5cdae1a6e52121be810a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 20 Dec 2019 00:03:15 GMT
ADD file:ec205d683a66c8a5c4a70c7ed6ff96c1b1f90b21431ffbbd1f2eb8defb3408f1 in / 
# Fri, 20 Dec 2019 00:03:16 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 18:40:30 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 18:40:35 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 18:44:11 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 18:44:13 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 18:44:14 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 18:44:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 18:44:58 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 18:45:02 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 18:45:05 GMT
WORKDIR /data
# Mon, 23 Dec 2019 18:45:06 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 18:45:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 18:45:08 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 18:45:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:78285f4ddf5d90a7220bed4c538bad44a42bd7cbd64898efd1cab6e592518cf0`  
		Last Modified: Fri, 20 Dec 2019 00:03:48 GMT  
		Size: 2.6 MB (2612091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79538ca8fe2c9f6653efd92965593d3aaca0c06eca1ff798ba55bcbe416bdf2`  
		Last Modified: Mon, 23 Dec 2019 18:45:41 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027e3bcba8299765dadd22aceb42b6b9ec44956b51523ca51cf1782e8ec26d78`  
		Last Modified: Mon, 23 Dec 2019 18:45:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610037872fb3d82ac7f9c90a30221b64e97dcba4e4b020c165776d7bb8492979`  
		Last Modified: Mon, 23 Dec 2019 18:46:10 GMT  
		Size: 4.3 MB (4330787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626d1d4aceb236476beead1b82d6ae86916780bf7bedd952101bc89391c08ba3`  
		Last Modified: Mon, 23 Dec 2019 18:46:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10356c6d8704443973b0579a4f0a9e5e0e90a8d7532974143e6a23ea97e69ef0`  
		Last Modified: Mon, 23 Dec 2019 18:46:09 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:d9f195770258b90760f696dae5321bb6d4b02f00fd7d46ed5e45503e5acc6edb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a118f4ac852c5cee0aa6c382e3fae6808dfd9b1c055e1ef1f7f7eac1aa95413e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 19 Dec 2019 23:59:01 GMT
ADD file:250d98c0ca20fcc8895da5d2c1fda5ea5a2945454a9d35e350816e91dfb420b2 in / 
# Thu, 19 Dec 2019 23:59:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 17:20:50 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 17:20:52 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 17:23:07 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 17:23:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 17:23:08 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 17:23:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 17:23:33 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 17:23:33 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 17:23:34 GMT
WORKDIR /data
# Mon, 23 Dec 2019 17:23:35 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 17:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 17:23:36 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 17:23:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:425066605c7f3f988db19ea1d5d77a89b86a124d90db4f9b4ca601ee32d74c90`  
		Last Modified: Thu, 19 Dec 2019 23:59:42 GMT  
		Size: 2.4 MB (2416682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec82a9feea3350f064d13e6807d60277cad29f8d944ce365cd7a7bfbe930c24f`  
		Last Modified: Mon, 23 Dec 2019 17:24:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f822b8b5123694c43431a29e5f126ba1865a41c2f313fcbfb2fc4f06f1d77e16`  
		Last Modified: Mon, 23 Dec 2019 17:24:00 GMT  
		Size: 399.8 KB (399765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9aaac50eafaeb636df2f0beee85789e5bc16fa6f970899eb3640f3b26b31bb`  
		Last Modified: Mon, 23 Dec 2019 17:24:32 GMT  
		Size: 4.3 MB (4254599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d1f582ec61112283877bb2897901d555ecc2a160438b1d0559544cea0e8848`  
		Last Modified: Mon, 23 Dec 2019 17:24:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cfe0103353dfa7ff6f40cad83edcad52517350bd88f118c478c69212342aba`  
		Last Modified: Mon, 23 Dec 2019 17:24:31 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:294eb2057b4bc6192016df94cfffa09cf2d15835e5509643e7e6b9e4435c94ec
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7528432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ee98a20523e080ba3c919cd9e7ca03721b4439d4a296ac7c00bf4a12909b93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 20 Dec 2019 00:09:38 GMT
ADD file:dc0b469a046c06ee4bcd4fff3ddd629d446d80fd5c04fccc2d569f6404d12bbd in / 
# Fri, 20 Dec 2019 00:09:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 18:28:40 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 18:28:45 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 18:32:00 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 18:32:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 18:32:02 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 18:32:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 18:32:49 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 18:32:50 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 18:32:51 GMT
WORKDIR /data
# Mon, 23 Dec 2019 18:32:53 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 18:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 18:32:55 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 18:32:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bcec9af2f9a2e6b85072026048ad7eaa22fe41ed31b648d91993d16d5d6358fa`  
		Last Modified: Fri, 20 Dec 2019 00:10:17 GMT  
		Size: 2.7 MB (2719180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71643b56e033163cb83432253e84dadee8995713d12c47cd3c5c4398803bf9c7`  
		Last Modified: Mon, 23 Dec 2019 18:34:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9969c8a4e52de05fd0d38bf304881b9c8ddad79475f3c190a640fb2bef93dd`  
		Last Modified: Mon, 23 Dec 2019 18:34:00 GMT  
		Size: 404.7 KB (404670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2392e001fa9f880b8a2f0f85f741351894c72bb1ed33c0ae94c0e2fd8410e329`  
		Last Modified: Mon, 23 Dec 2019 18:34:39 GMT  
		Size: 4.4 MB (4402773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557846bcd940ab53ec58a3d5195a447e8c7d4b80d1f2e77ed808adaed410c13`  
		Last Modified: Mon, 23 Dec 2019 18:34:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac31a8395129e73804c582d3eaeffeb252e1560eadeff49cb567ede240d0b154`  
		Last Modified: Mon, 23 Dec 2019 18:34:37 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:a02f4bb1f7689c66f717dab535c53a5730ec308256249fb75503269314d59906
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b990429304304eaf0fbb3610939a40ae41c28cb38bc9c4b2262907bc3c9711b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 19 Dec 2019 23:39:07 GMT
ADD file:1673706680d7b52c2ebbcedb7487d7f409ac30dd981113b1054768dfe313d34d in / 
# Thu, 19 Dec 2019 23:39:08 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 18:07:43 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 18:07:44 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 18:10:33 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 18:10:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 18:10:34 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 18:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 18:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 18:11:09 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 18:11:10 GMT
WORKDIR /data
# Mon, 23 Dec 2019 18:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 18:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 18:11:10 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 18:11:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9680c0e936f79794dbf7ca3d1bfa62665de2eab226477692ae1b5dea6790cad6`  
		Last Modified: Thu, 19 Dec 2019 23:39:33 GMT  
		Size: 2.8 MB (2805033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6453f7cac276b9eefe2a0538fb9552ba36d2c80767633d38137cb027170a161e`  
		Last Modified: Mon, 23 Dec 2019 18:11:40 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9718f6a45a7ac81f23b275787fbe4712704bcd5841fa595e0ba52f7b1851fc6b`  
		Last Modified: Mon, 23 Dec 2019 18:11:40 GMT  
		Size: 407.9 KB (407912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be1c03b4b4ebd83eb5c18fd4f7cdb9bfaf0fe0ba5cdb8fd7745fbf018433c5`  
		Last Modified: Mon, 23 Dec 2019 18:12:00 GMT  
		Size: 4.3 MB (4259165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14448b86070a8f081a1b0d9cc84225f4c8a51298d217c20a402ad15308ab3c`  
		Last Modified: Mon, 23 Dec 2019 18:11:59 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3617a5e6f17e8d884f81a368d0a6fa60c154d04f17b30684da13303aa359ef`  
		Last Modified: Mon, 23 Dec 2019 18:11:59 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:5378c40e56cd93c25699d11185a81247448a4de43750d00fc0bc4815e6122c19
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7911327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f13741747a8b4756663390f77a890858a3e3a9110db2462ab8888b63131c183`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 19 Dec 2019 23:37:02 GMT
ADD file:f3e7e107e2972b4b00970eb9be40652042303a7783596a6c9cd1212a26309bc8 in / 
# Thu, 19 Dec 2019 23:37:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 17:34:02 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 17:34:11 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 17:37:43 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 17:37:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 17:37:48 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 17:38:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 17:38:20 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 17:38:23 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 17:38:26 GMT
WORKDIR /data
# Mon, 23 Dec 2019 17:38:27 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 17:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 17:38:30 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 17:38:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cc1702756cf1ed12718b42717fddaa5c49572ef0e8f7d94ab4b77f403e335899`  
		Last Modified: Thu, 19 Dec 2019 23:37:45 GMT  
		Size: 2.8 MB (2816542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ffd24b8283ce7d2ad815fc5ef902f3483762e42c23b0bb26079322482700e0`  
		Last Modified: Mon, 23 Dec 2019 17:39:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e89c2403d06550ea3de83546dc9442c9804e1eb6d52f83d566cb9a1ff3fdd2`  
		Last Modified: Mon, 23 Dec 2019 17:39:36 GMT  
		Size: 409.9 KB (409876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f5c9c96279e60a32efcca82d30396c0ea6fc559b408a02ae169a6b76fc890f`  
		Last Modified: Mon, 23 Dec 2019 17:40:43 GMT  
		Size: 4.7 MB (4683100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74076feb17b2fc0a4ae18d0722c8190c2ab99de72201eccc83c7ce87752c7a5a`  
		Last Modified: Mon, 23 Dec 2019 17:40:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69134ec828a3667c2c9733d4b93fd00788e53b69433ea952058759b5ab761e89`  
		Last Modified: Mon, 23 Dec 2019 17:40:42 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:498164cee497b106e43ee5ed5c2e047b2340ffd6fcc89e4cbd55289ba7e8b66a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4491b75fd24e171bb19057a8d8dc871f5304dc8cef042da7b072b77910592f3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 19 Dec 2019 23:41:47 GMT
ADD file:76b98628dfe42e69b2ce24e40f1d584b0245c65db7fd20160787dba84f6d01fc in / 
# Thu, 19 Dec 2019 23:41:47 GMT
CMD ["/bin/sh"]
# Mon, 23 Dec 2019 18:02:03 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Mon, 23 Dec 2019 18:02:04 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 23 Dec 2019 18:03:28 GMT
ENV REDIS_VERSION=4.0.14
# Mon, 23 Dec 2019 18:03:28 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.14.tar.gz
# Mon, 23 Dec 2019 18:03:28 GMT
ENV REDIS_DOWNLOAD_SHA=1e1e18420a86cfb285933123b04a82e1ebda20bfb0a289472745a087587e93a7
# Mon, 23 Dec 2019 18:03:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 18:03:44 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 18:03:44 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 18:03:44 GMT
WORKDIR /data
# Mon, 23 Dec 2019 18:03:45 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 23 Dec 2019 18:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 18:03:45 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 18:03:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cde57aed53ae0e310089f2638677af1321dcf6e45d514b758c1f637f1a2d2f9b`  
		Last Modified: Thu, 19 Dec 2019 23:42:27 GMT  
		Size: 2.6 MB (2579533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117e4f76f3ae12d50f3f212c82ac6b42946a8d4409f097349a4ad3d75b2e70e8`  
		Last Modified: Mon, 23 Dec 2019 18:04:11 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf76e3ceb33e9e2d6b630550894c0fe2e242495e5aafb25a52ff3ff5dbdbdcd`  
		Last Modified: Mon, 23 Dec 2019 18:04:11 GMT  
		Size: 407.4 KB (407357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2d00873521107f0ae7397d0d6c711ad81749a7dd0fcde07066135d055b057`  
		Last Modified: Mon, 23 Dec 2019 18:04:33 GMT  
		Size: 4.6 MB (4564771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9cb1bf474580a925e552a3f940513ede1e5e46eedc2d980eec4ecb5369ff74`  
		Last Modified: Mon, 23 Dec 2019 18:04:32 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b86054490c095b5ddf167768902518f1a200812af92097bec9800c53a8ce60`  
		Last Modified: Mon, 23 Dec 2019 18:04:32 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
