## `redis:alpine3.18`

```console
$ docker pull redis@sha256:343e6546f35877801de0b8580274a5e3a8e8464cabe545a2dd9f3c78df77542a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redis:alpine3.18` - linux; amd64

```console
$ docker pull redis@sha256:7f5a0dfbf379db69dc78434091dce3220e251022e71dcdf36207928cbf9010de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15624215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5230e57b1bf430efe85d1d3dad86d2a2354d02bf3783f7b4e7d5e5e8e61a59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adfacd3b74ca05b4d5636e46f443504cff6735ce913a20c0cf1b6e2c9e790eb`  
		Last Modified: Tue, 03 Oct 2023 23:00:09 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2d8ff49f68a3d2a1ac5beb2a19077a408189262de93e26b5ce50bb8d5dbc53`  
		Last Modified: Tue, 03 Oct 2023 23:00:09 GMT  
		Size: 347.4 KB (347375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473eef84775a8dca1aeb461846f200a18d46882a5b20cdcf4ece51b1adfc2c5e`  
		Last Modified: Tue, 03 Oct 2023 23:00:10 GMT  
		Size: 11.9 MB (11872921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fc03039a58dce816e43ae300e84073e79775054a27d89082ac31f4e2f86617`  
		Last Modified: Tue, 03 Oct 2023 23:00:08 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c27b2421cc221a9bc7faec3998b9217e668b808a9de5e6f6961a45fd88ec26b`  
		Last Modified: Tue, 03 Oct 2023 23:00:10 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:a7e4cf3c21edbd9fcf5f047b4d4041862b8fa91fb7eeb0eadcb21c4c16ed6b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.8 KB (751778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec3cdba4fe26e3442e5768c02171666893849900eb84fa8b4301f5adbf6cab9`

```dockerfile
```

-	Layers:
	-	`sha256:a6907c04de9be086848c499fcc3aa89423e7adddaa68a4cede08f7899f454a91`  
		Last Modified: Tue, 03 Oct 2023 23:00:09 GMT  
		Size: 725.5 KB (725524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7474a42b76d0aee44b8367754d8db69fc7ff445a86be12cdadc81b0327ac1254`  
		Last Modified: Tue, 03 Oct 2023 23:00:09 GMT  
		Size: 26.3 KB (26254 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.18` - linux; arm variant v6

```console
$ docker pull redis@sha256:a2d95bbe81979072823160fa3fe6c6a54b47fa3aea977e9b2cc72722ff14bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15518829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26c4f7370b94100813c9dc41e42e1902754c90812c8eefc83b8b64678b916e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a61b7be475a718c982548ef463e0c9e4a89c8e4295022c7ff8dd1ca8f9b9bf`  
		Last Modified: Tue, 03 Oct 2023 22:59:50 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c175be1a443b134a9e8b9971f24266cb06f3e831d2d20258a597465cab769c5d`  
		Last Modified: Tue, 03 Oct 2023 22:59:50 GMT  
		Size: 347.1 KB (347147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfbe62b8a4d7e2537aa5584ddb3c4c0a1664391f3c54f6eee39ce7f53a947e`  
		Last Modified: Tue, 03 Oct 2023 22:59:51 GMT  
		Size: 12.0 MB (12024442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf84b2f4d65cc52dcbb58761a86e9cde9b053c4c30cec1f0e282ff9451fea46`  
		Last Modified: Tue, 03 Oct 2023 22:59:49 GMT  
		Size: 101.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d16d7f6578db378ea59d79c5cc7457c17d916ef3e83319d512a1977df75c6`  
		Last Modified: Tue, 03 Oct 2023 22:59:50 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.18` - linux; arm variant v7

```console
$ docker pull redis@sha256:6f0763a8e75c1cc5d7e4c8fbe313a309876cf6d2c738ea492f3b0ff5b4377937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15138666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad332d922af12c305900bb1e8ef6537c862c76faff7401fe14c5f3e9fe7478c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8bcc30219a3b5ad7547cb998dbc925d87391c679fec1abae88483d4839fa51`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1e96038724920ff29465fba0c7aca16d709e1f1d94b903204ed8b6af9e8387`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 347.0 KB (346994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41392cef32ae6c48f9ca900d1c4d46f1634efd46a182af89b46f2208d62fd6dc`  
		Last Modified: Tue, 03 Oct 2023 23:23:44 GMT  
		Size: 11.9 MB (11889819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86492254da2554c717005739e542d4994d17952a479d39c18db03ce65a13af8d`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c2d595a65842f06472dc89c09313cd3b01560e71faacb565785329892709`  
		Last Modified: Tue, 03 Oct 2023 23:23:44 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:6bd368ec654b98818c309421ce2d2d2dd919c1727b3f67b5c6d0f5c855e45dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.3 KB (754291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295437054c78885bffb276095b5bf2a384255fd3786ad4fad890e4a78009fa88`

```dockerfile
```

-	Layers:
	-	`sha256:ed61dfc28bfeb061a9f2febccad64f80a5c5abd6915d0e398d7949ca3f1d407c`  
		Last Modified: Tue, 03 Oct 2023 23:23:43 GMT  
		Size: 728.1 KB (728065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe52a6ec253d9611d8545f8271d38d2833a49dda068b12e49effce385f77559`  
		Last Modified: Tue, 03 Oct 2023 23:23:42 GMT  
		Size: 26.2 KB (26226 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:8831709d4fce0a40566981050dc2e7540e302b243bcca4807da66071ebe3205e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15725520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5e8ee012b565826f963ffdfacf71622c7b1ad9d9ea41e8ee8f6baa8c74d61b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0feb8fddc533ebe8fa3e28ab60443a2b6a5a7e46ff3560b1e79f4ff945a70f`  
		Last Modified: Tue, 03 Oct 2023 23:02:00 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a743b36a722987becef2b73971d75377bee67a2a6577cbdfddc1da3634eb4a73`  
		Last Modified: Tue, 03 Oct 2023 23:02:01 GMT  
		Size: 347.6 KB (347581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e355545ff456f9b7c4a23eedc4daef70995455a272dadeb8c1a0f6422d7ab83`  
		Last Modified: Tue, 03 Oct 2023 23:02:02 GMT  
		Size: 12.0 MB (12044158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd05ab5e011a9605819ac18ff8c4f7195e4546eb83a3c2786506f09eeb1d3467`  
		Last Modified: Tue, 03 Oct 2023 23:02:00 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745b79d85ea976152d4a30c78b01521274ba87187a789384bdcd04d312ffdb4`  
		Last Modified: Tue, 03 Oct 2023 23:02:01 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:c05b517c008b5471c36fa5735d24a69581d78387368f79873754e14c172f5cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **751.7 KB (751651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62dd24a47f5cd764de9bc397a2365e6bc0469bf5f1357acb43f6ac81a02742f1`

```dockerfile
```

-	Layers:
	-	`sha256:a501957bc807473296ec82c463a8ba660d5b317c131209e537aebbfa141f6565`  
		Last Modified: Tue, 03 Oct 2023 23:02:00 GMT  
		Size: 725.5 KB (725545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30c5f14dc57c36b4fab725f0b738f7edb03b7c2fea2bc6911594fe1cc868009`  
		Last Modified: Tue, 03 Oct 2023 23:02:00 GMT  
		Size: 26.1 KB (26106 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.18` - linux; 386

```console
$ docker pull redis@sha256:1a7579641f48f371d8bfa51abf0c867f3e3a2c9061d0cba1aed609410026d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15077508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ff52024cda5a55f94e3aec28d3a084d535babc5f826f43f82260f9ba0a2b1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db2856c2e1996af4bec5a53a9d1ba58d12cb42b35098c806f15addc30f44e93`  
		Last Modified: Tue, 03 Oct 2023 23:00:13 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0f5adad384e5b5d19038c17d65cf78a8d3ab9cea02c434c91b140af08c2f6d`  
		Last Modified: Tue, 03 Oct 2023 23:00:13 GMT  
		Size: 347.4 KB (347353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0267a0b234dbc2029df7a310b750b2229967bdcd34ff827f4b6b10da73c201b8`  
		Last Modified: Tue, 03 Oct 2023 23:00:14 GMT  
		Size: 11.5 MB (11492448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2e5edf093c2b400fcbf918a364f3565ced7b4517213b5a61df1c9a15d7a1a0`  
		Last Modified: Tue, 03 Oct 2023 23:00:13 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3361d0fba6803651cc8ca8a3fa69a364bcf037b59c581c775e22babe7b5e70f`  
		Last Modified: Tue, 03 Oct 2023 23:00:14 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:0c555f022eb27f7c3678a13065f3f80c51000bad68de1405fa16c263b2cad422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dc3095a1b59e69dff9a2d4aa0a3610180174233161e78d1ebdae3bb03de889`

```dockerfile
```

-	Layers:
	-	`sha256:88f0474f4606a1e486ff01930cf2f46c1188fdac56ec81e8bc55df8a0ae53fd3`  
		Last Modified: Tue, 03 Oct 2023 23:00:13 GMT  
		Size: 26.0 KB (25984 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.18` - linux; ppc64le

```console
$ docker pull redis@sha256:449c2d5d58dd88be6b12a5e8a586961a923f0d2507eacc5e4d456664f340ed02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16441853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974c2d51863bc07193b6858e826158f710cea8abba3cfa49da89e3f7d3d6df52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e963944e7d7c85e7e5202f0596efabc5d145dfc37f6e0a9b481b7e185470e576`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c07f1f59e5142c61f551a02105a3fe01c28e7ae009ba3c9ef69dc54d2c90a8`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 347.6 KB (347649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114743825e464ee129cd4bcd35c2b82d85dc6e8b02a27adac6c04ffea80423f5`  
		Last Modified: Tue, 03 Oct 2023 23:04:17 GMT  
		Size: 12.7 MB (12745744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67084ed698919bfe75b8e231da3f18283ca44002ecbe2e9930572702a5c152b`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7366e0d976b96ba71a56236bbc9275beec5b9b003af1fac46ac12a7e10e2e884`  
		Last Modified: Tue, 03 Oct 2023 23:04:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:6e5509f4b8471704f6c051fd675c489af82590f47060b936baadcbaa414bac11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.8 KB (749818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00825d8ef0905ab01a1c3e8237127e9789f4447148530724cb707643cfe1280e`

```dockerfile
```

-	Layers:
	-	`sha256:1c065a109330fac5e1aea11573062ae563e775d768dd44af4e5055406aea25fa`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 723.7 KB (723662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcdfb78d7e2b79497130d55ba50c820c6da92e3928e1d83dccd4cd94600d9500`  
		Last Modified: Tue, 03 Oct 2023 23:04:16 GMT  
		Size: 26.2 KB (26156 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.18` - linux; s390x

```console
$ docker pull redis@sha256:27e210d79fd14f21b36f128475cc61438651324a4e60b508133cca6989cd45dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15804539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40f8ff57f7cad766c3da3f48bd1cf4045945ff79624bdedddb63630486aa4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fb319e3e2b6d090a150207805753dae05abe1df53b9dae9b211d46986bb8e`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8fdacac4cf0c35819b1f0be78d8bed53f4dfdce11d17b3918d554a29299129`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 347.4 KB (347360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06e3a7ca44ac07680bf115b92e08f7d9d399fb6b401583c5b343d1f586ee44f`  
		Last Modified: Tue, 03 Oct 2023 23:15:32 GMT  
		Size: 12.2 MB (12240135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd6cd0b1d233b164af4ac63b4f5ff8fe0c3ea6930cbc7f5e501cfc77a9f95f`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf56dac1a634b541f17bf87c7ba5bfc8a6e848b6a9782c0b6d884bf302e896`  
		Last Modified: Tue, 03 Oct 2023 23:15:32 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.18` - unknown; unknown

```console
$ docker pull redis@sha256:d2e9fc086d9526853ef5596742a826c3c870a2a26292b7f2b0f8cba17a82ebcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.7 KB (749677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b37aa471a3e1650d9db4a8c6b3c211641bad2e45ec7e3121ee446a8f3c2bac`

```dockerfile
```

-	Layers:
	-	`sha256:c3216d939fa34b94a92378f55a0dd2c458c781b37a283e5c6a19c71c7ba953b6`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 723.6 KB (723592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04729441a805b800d7b877f2c42496343cd62c42ca3dcb3179619466777324d1`  
		Last Modified: Tue, 03 Oct 2023 23:15:31 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json
