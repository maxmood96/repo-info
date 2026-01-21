## `redis:7-alpine`

```console
$ docker pull redis@sha256:ee64a64eaab618d88051c3ade8f6352d11531fcf79d9a4818b9b183d8c1d18ba
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

### `redis:7-alpine` - linux; amd64

```console
$ docker pull redis@sha256:4706ecab5371690fecfdd782268929c94ad5b5ce9ce0b35bfdfe191c4ad17851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17232428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13105d2858ded45aedf7b24f0870e6a4e7ce4964924bffce68e562ca72149f1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:39:12 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:39:13 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:39:16 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:39:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:39:16 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:39:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:39:16 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:39:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:39:59 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:39:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:39:59 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:39:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c57c0072ef228501beec5a8bee0d7ecc882dee9afd91fc7a58e3f9d9da64c5`  
		Last Modified: Fri, 02 Jan 2026 18:56:28 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4343b4accd46fa853b1de6ee0ca92ab1f7080db3af6c4948678534d69cc159`  
		Last Modified: Fri, 02 Jan 2026 18:56:28 GMT  
		Size: 173.2 KB (173218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380e8aa8b1fdbd2887f9b1fa3e9d3cba192f9ff87956981dc8bd73cc6da39bfc`  
		Last Modified: Fri, 02 Jan 2026 18:56:29 GMT  
		Size: 1.0 MB (1003015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70aae7b5e0d75367bcf5d40074ae8e28d17793c251e0d505321aa8ea4fd91fd`  
		Last Modified: Fri, 02 Jan 2026 18:56:31 GMT  
		Size: 12.4 MB (12411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232f7549c9b07a752bb00c7d7a61b3bfe6af3f15a711ba643c132f0e51922a64`  
		Last Modified: Fri, 02 Jan 2026 18:56:30 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75b3becd998021da3bbfcb31fa6580676396f5244243670f57920652cce8038`  
		Last Modified: Fri, 02 Jan 2026 18:56:31 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0aee8a08a4509640029b3dcd2b55d9b1529994b9be897eb4cde35d4a39f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1198ea9c6c7fd32831b5f03ab26e31ac5ea925fc6a6edf0f3863caab050966b0`

```dockerfile
```

-	Layers:
	-	`sha256:5f8375faf7cbdd96cc1ca85b22d4e8bd833a145ae10f45f891333e20fa0ab318`  
		Last Modified: Mon, 03 Nov 2025 17:40:06 GMT  
		Size: 460.8 KB (460815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95050f4fb5365851ff9ec3d7a211848fff777e2b7b2ee8a2bf9b0e9e9665956e`  
		Last Modified: Fri, 02 Jan 2026 18:58:57 GMT  
		Size: 33.8 KB (33777 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:71cf7e25b58d01e5b2cb1540b3adf6c582a7853e8c86d8b822143f34e2ee3e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17088891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9df30dd83b0b8cf94d3953c760ec43bc2f0349051273dbc95902b5bc009503`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:38:45 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:38:45 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:38:48 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:38:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:38:48 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:38:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:38:48 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:39:34 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:39:34 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:39:34 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:39:35 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:39:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b68327216127a9503238e0586c942213a03acd96b1d2b718aa23012f786dca`  
		Last Modified: Sat, 03 Jan 2026 03:14:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066febb4dc81042a1fa78ea016ae0e6d06b29734ee09ccb90f457e82805320c`  
		Last Modified: Sat, 03 Jan 2026 03:14:06 GMT  
		Size: 173.2 KB (173222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4409cb58a9d7512ccf811615f656fdcf38089fa9da2647f58051899dae842966`  
		Last Modified: Mon, 03 Nov 2025 17:39:40 GMT  
		Size: 971.3 KB (971304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c80acfe059778f86cad89156afd6fca85037739a6b672ab321ccc6801644d55`  
		Last Modified: Mon, 03 Nov 2025 17:39:41 GMT  
		Size: 12.6 MB (12577236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed79377df4a0b383e16a8f84f078c864f932bc5374e09c99b644c845c9f48325`  
		Last Modified: Sat, 03 Jan 2026 03:14:06 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff64c2ebcd7bfaae45909fb1b8e5a45bf4c8080a07b439e9b11f104df16fc9f6`  
		Last Modified: Sat, 03 Jan 2026 03:14:07 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:98aa36bf3d26d436a8faed6b94dde3ec7bec24e774f89e86db3056bb253697f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 KB (33702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c387676562c2e720d9f778ef8a40588b8eb9edaab5b3c7113e3925ddea0de1f`

```dockerfile
```

-	Layers:
	-	`sha256:846d2fd82d78e000253d2d3ba2c7f38059b1a2358f89eae829e933dafdde01fe`  
		Last Modified: Sat, 03 Jan 2026 03:06:44 GMT  
		Size: 33.7 KB (33702 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:92ab0d6c307f258429c6a078b680b7a1bbacfc6d4cee9e60c2abbffded9611cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59331f0b2c9d1c8ef21b63fcb96a4383968c3506c1e501e81dc2db0fcf905b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:40:03 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:40:04 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:40:07 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:40:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:40:07 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:40:07 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:40:07 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:40:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:40:53 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:40:53 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:40:53 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:40:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:40:53 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:40:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb645d239b056901800f6d35b55c991873c3a77505d6c3a0e0c751962fbd80a`  
		Last Modified: Sat, 03 Jan 2026 03:14:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aafa40f0c2551e3298cee05960209d83104898c9e30623ba40546d0f9ec786`  
		Last Modified: Mon, 03 Nov 2025 17:40:59 GMT  
		Size: 173.2 KB (173226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ae490363a9907c3fd7c7dcc41bacfb2b5795180169e83d5244c10c3412d0ee`  
		Last Modified: Sat, 03 Jan 2026 03:14:11 GMT  
		Size: 971.3 KB (971286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fa0d1bc8bd22c3c628f100f050f2ab418c2aa0a7783271c1fa7fc9a18b8f77`  
		Last Modified: Mon, 03 Nov 2025 17:41:02 GMT  
		Size: 12.4 MB (12439715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c19dc494884970b62b066c934aabc76852db7bf5f966a17b2f010f6932ffe2`  
		Last Modified: Sat, 03 Jan 2026 03:14:11 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec681e7db65dd78be1ceac755e39fdcd763134c1e2c71beb447717170452abe`  
		Last Modified: Sat, 03 Jan 2026 03:14:12 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:57fd51ea56a3bcf44b704aed851c77bbb528aa06db08b991a8c87dedb07fedd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.8 KB (497774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2676ed826ff6947578de3619e4af769f6ed6ff1ca110853195f25f10b7f63bc8`

```dockerfile
```

-	Layers:
	-	`sha256:e11b16d2740ec93f1c2c7b98b4ce6f4bd32d6912eca5f758ddad910d9324873a`  
		Last Modified: Sat, 03 Jan 2026 03:14:14 GMT  
		Size: 463.9 KB (463857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef2957717bb53af092241bdf0328561292baa0c0340ad4e395a591f2d45733d`  
		Last Modified: Sat, 03 Jan 2026 03:06:45 GMT  
		Size: 33.9 KB (33917 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:1f456c9fc77eec35fc854105dd5072a1293da0a40fa826e8d5739d45d6c7e650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17677959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffaab4a072b3790ac200c04f8b825bc805c5c17e245f4c27c9867188737739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:39:34 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:39:34 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:39:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:39:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:39:37 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:39:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:39:37 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:40:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:40:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:40:20 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:40:20 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:40:20 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:40:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644b71be12e61094de912c81eab06eb25f8515dc20d05a745df05332ed75513`  
		Last Modified: Mon, 03 Nov 2025 17:40:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7069ec89863791efda36b68238c42c776f567ebecd9c432927056771ec0541`  
		Last Modified: Fri, 02 Jan 2026 18:56:36 GMT  
		Size: 173.2 KB (173222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cd490265becb809d7ebc53c74d921d04612e0dc6f62c49349f8e602ce8a121`  
		Last Modified: Mon, 03 Nov 2025 17:40:27 GMT  
		Size: 934.7 KB (934720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1bc2ae4829bf26ca9034ef54917dbd7e9fead336b459e0b4593a6fbf070c4`  
		Last Modified: Mon, 03 Nov 2025 17:40:27 GMT  
		Size: 12.6 MB (12576007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda2dfd82503d7263bff5e1d5a0596adaf80156e939956ca87f92d9234a86634`  
		Last Modified: Fri, 02 Jan 2026 18:56:35 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43997775f51142f8bd7d1ad0b28a3216ce7c7baaf736652298e55fa0c75c4e9`  
		Last Modified: Fri, 02 Jan 2026 18:56:35 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:1e1563a628a478beab215202a3b5ab345e98adfb826802e01dcf196572c4cd7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 KB (494851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a901735839226fbed6fe8dd4e419a8ce9924719cf628ca318bab5da81d752ddd`

```dockerfile
```

-	Layers:
	-	`sha256:dcb2e590091c9451bf9ec064da6b74e11f253d755dacb5c7ad1084a61fc8ca86`  
		Last Modified: Fri, 02 Jan 2026 19:00:53 GMT  
		Size: 460.9 KB (460895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f459f3b393ef4d0d10831206ef81fc59bb523a822b6458f25ea23ce956edaaa`  
		Last Modified: Mon, 03 Nov 2025 17:40:27 GMT  
		Size: 34.0 KB (33956 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; 386

```console
$ docker pull redis@sha256:4e0a898c867701197ee5aa93313fef52fecedcabc0f9a6dd30c8a888d568de2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7d5dbbf98b3da57967318beb91903d2fc468d56ff3ac48d0a20323f6a03793`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:38:53 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:38:54 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:38:57 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:38:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:38:57 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:38:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:38:57 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:39:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:39:45 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:39:45 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:39:45 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:39:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:39:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:39:45 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:39:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Sun, 07 Dec 2025 18:13:29 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10156b7935e354919298ebd170430c5830b2c7ca0f7a813766b16f298a9c3a`  
		Last Modified: Sat, 03 Jan 2026 03:14:20 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a9149ad00bd6d4f7bd7df75eec575c8c941c8a600f798c4c03240d9cc21afe`  
		Last Modified: Sat, 03 Jan 2026 03:14:20 GMT  
		Size: 173.2 KB (173241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0699cab2fcf8e9722d361842afbb93e1d6e9acb47b3afb5dd46a13dadf98a884`  
		Last Modified: Mon, 03 Nov 2025 17:39:52 GMT  
		Size: 978.8 KB (978810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16500a9306cab767e671a6d43b3ec43680baaec2423de8111c2d8802137a7de7`  
		Last Modified: Sat, 03 Jan 2026 03:14:21 GMT  
		Size: 12.1 MB (12069300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9cb190d19bd276534466e8f273abd7a03ab368425bf3d3854deeb8a7a1c95e`  
		Last Modified: Sat, 03 Jan 2026 03:14:20 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b11e36a145511c5733a1788d4919f72291207e9c5732a28f836c522670053f9`  
		Last Modified: Sat, 03 Jan 2026 03:14:21 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:dccd9986da0bcbd141f250caab1fc903ff59cae5c9de8aec72a12db6ccef169b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.5 KB (494499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d0fc8ee75f6e12944eadd0658374e99b98d5ace83547eaee4207bc1b38da0a`

```dockerfile
```

-	Layers:
	-	`sha256:aea57ca6b1fecc4c6226744bbb729cec9eb0f774dd40b668afe9d0fc1361bcd8`  
		Last Modified: Sat, 03 Jan 2026 03:06:55 GMT  
		Size: 460.8 KB (460780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b070a8dc55309fb544a9f0fb35deb12c2b9787485d4ea19afaab73d281887f3`  
		Last Modified: Sat, 03 Jan 2026 03:06:48 GMT  
		Size: 33.7 KB (33719 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:9607ae5c170d110cf28cb3504e68128fdc153bd4d8c6d5b030ae49086d3f69e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18032339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69295a52a0772f8444149b8bca68295cd6fece778bcf4633a8def6f1cac90292`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:42:54 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:47:20 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:47:24 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:47:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:47:24 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:47:24 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:47:24 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:48:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:48:12 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:48:12 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:48:12 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:48:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:48:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:48:12 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:48:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc0d69726a0c7ec43e0fbeed5a8f5232b10a0f7dfdac49004bc5ab58460587`  
		Last Modified: Sat, 03 Jan 2026 03:04:57 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4b47aa0d1c972041518691db5b6e3e7d5a58b117711509270c314426514ecc`  
		Last Modified: Sat, 03 Jan 2026 03:04:59 GMT  
		Size: 173.2 KB (173231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0619eee1676f4aed529fbcba837c1f1e9e5ceff1b9b4736c81bd2f1cf2ece8e7`  
		Last Modified: Mon, 03 Nov 2025 17:48:31 GMT  
		Size: 923.0 KB (922973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb7d212a932dc6496c27dc21347d8669770300121310ce82bac5be9c2f4f48`  
		Last Modified: Mon, 03 Nov 2025 17:48:32 GMT  
		Size: 13.4 MB (13360402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf847cead84c026779e23709ea86534ac10da3953088f3444c33c439afa0e2b`  
		Last Modified: Mon, 03 Nov 2025 17:48:31 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eb201dccf245031a0ca1e586395b5b5878f152ef26d664b420c72c1e38f6a1`  
		Last Modified: Sat, 03 Jan 2026 03:14:26 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4630aad5443d9703d4589c02c57fe9922213f441ead474f8fb134ca3c19c7b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89540a3a5deb3567f8c2e7b081a0362a7f741699acd6864f6db133bed9af7da0`

```dockerfile
```

-	Layers:
	-	`sha256:cc9d96a3399f9af37a3e71086beacd34021a53b8738485d6dbeca9e0f539f5d6`  
		Last Modified: Sat, 03 Jan 2026 03:06:57 GMT  
		Size: 458.9 KB (458910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a6e3cffb1c1c81712a0adede77c34d38cce4d27d36d415c4cc634c426982f7`  
		Last Modified: Sat, 03 Jan 2026 03:06:49 GMT  
		Size: 33.8 KB (33833 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; riscv64

```console
$ docker pull redis@sha256:40051048fc5a6843dd189a39edfae095fa8da769a8e60c347a651149358030e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16476513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f5149f168fc24f4225b300cdf3d38d00c70d948e2357ac48815c08b9c3f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:54:38 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 18:11:37 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 18:11:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 18:11:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 18:11:51 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 18:11:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 18:11:51 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 18:26:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 18:26:04 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 18:26:04 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 18:26:04 GMT
WORKDIR /data
# Mon, 03 Nov 2025 18:26:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 18:26:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 18:26:04 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 18:26:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:18:42 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24226564e4ccb978b7cbbafef0d2759d71e29e26fd89bae43205cecfdb06c7be`  
		Last Modified: Sat, 03 Jan 2026 03:05:16 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538313d697b43a5a929c18f057132adb4a1843214733b82c3b8211cd71a5a6f`  
		Last Modified: Mon, 03 Nov 2025 18:26:48 GMT  
		Size: 173.2 KB (173228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d728e560844b1b0d2ce770af3232b136f54753b0580dc934aa59469fbe9da6a`  
		Last Modified: Mon, 03 Nov 2025 18:26:48 GMT  
		Size: 975.1 KB (975054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b059e775b938f57113a4f226d5e017d4fa7a8d5d766e8d2dd9ae91f1faea9ed`  
		Last Modified: Mon, 03 Nov 2025 18:26:49 GMT  
		Size: 12.0 MB (11975572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa79a3c73099e5a0efeb01b76ba5cfbf5e864cbcd3a4498117428884317b52`  
		Last Modified: Sat, 03 Jan 2026 03:14:30 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353d0f7d7f33c66856667c09fd65d6a09d715ba773a7fade543422043900e8e`  
		Last Modified: Sat, 03 Jan 2026 03:14:31 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:eaa27d6c3dbaa73e6cc0dcc05a0b92f99f960bae528fd897f46273244fd5eb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0fadacd9511ab5c789f79e9652858d79a859d9809a1788e34624fd9058b769`

```dockerfile
```

-	Layers:
	-	`sha256:33353da4df0c5b25ca1acd0a16c92b15beeb03c190774fac65720e058ed7f38d`  
		Last Modified: Mon, 03 Nov 2025 18:26:48 GMT  
		Size: 458.9 KB (458906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb20af14464772cd172c10593b7db20e22a356eec3f083c7fefda928d63a76bc`  
		Last Modified: Mon, 03 Nov 2025 18:26:48 GMT  
		Size: 33.8 KB (33833 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine` - linux; s390x

```console
$ docker pull redis@sha256:9533a62e1003e6dc4a341e8049a82c00c492b7c1eb82ce860aae446865ff5d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17592340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb0622e244cd805b06e889aa82316a93003425f7c5e596c32bc68e459e9bf90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 17:42:49 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:46:13 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 03 Nov 2025 17:46:18 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Nov 2025 17:46:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Nov 2025 17:46:18 GMT
ENV REDIS_VERSION=7.4.7
# Mon, 03 Nov 2025 17:46:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.7.tar.gz
# Mon, 03 Nov 2025 17:46:18 GMT
ENV REDIS_DOWNLOAD_SHA=c97e57b0df330a9e091cacff012bebe763c275398cf36ff44cdba876814b595b
# Mon, 03 Nov 2025 17:47:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:47:12 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:47:12 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:47:13 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:47:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:47:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:47:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:47:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2f0df25441e144b5f6a3b7d2606a4d3b1cedcbdaef685b75b321c8a63bf051`  
		Last Modified: Sat, 03 Jan 2026 03:05:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbcc0a001f8a201d097b574f8eaef5714314e4de80747a5c8a6fdde9716d761`  
		Last Modified: Sat, 03 Jan 2026 03:05:40 GMT  
		Size: 173.2 KB (173246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0896854c8fcc5615b905ee4b26e87ab4f04e7ab27892bdb8901d19999117d`  
		Last Modified: Sat, 03 Jan 2026 03:05:42 GMT  
		Size: 969.8 KB (969779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57260d3c207b7700e362efcc5da7dcf924d218ebeac3bc5e5efd4588732dd93d`  
		Last Modified: Sat, 03 Jan 2026 03:14:36 GMT  
		Size: 13.0 MB (12981223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06f81df22c0900b1758e346e7d547bd2ca4c09f6e80f8bbd0496099447cbc6`  
		Last Modified: Sat, 03 Jan 2026 03:14:35 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352279bd4c9f0f375cc1e9747cd8dae58cef8f024387119be41743f075add0a0`  
		Last Modified: Sat, 03 Jan 2026 03:14:36 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0c68dd72a009de9272ff517defbccbc41895bbf0bf52b6f4e3520c9a41a4c319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b657949c1fb682df77c179abef6a7fd3b3a15e276695f6011eec259c970d119`

```dockerfile
```

-	Layers:
	-	`sha256:b0097fbf3b9c5750846378631ebe264bcee5941996b74cae0cd3211e089cdaa1`  
		Last Modified: Sat, 03 Jan 2026 03:07:01 GMT  
		Size: 458.9 KB (458864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748d0b98f1ca85d95be94bf0b04d9a81285d42d1c56d626cb94acb6e7a28759f`  
		Last Modified: Sat, 03 Jan 2026 03:06:53 GMT  
		Size: 33.8 KB (33769 bytes)  
		MIME: application/vnd.in-toto+json
