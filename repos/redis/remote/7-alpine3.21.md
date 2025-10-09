## `redis:7-alpine3.21`

```console
$ docker pull redis@sha256:9aa757f58bcd716b7be8ae0e471d3264b8b7e6c1a19aae732ae22ac7f19a3adf
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

### `redis:7-alpine3.21` - linux; amd64

```console
$ docker pull redis@sha256:4912adf5f3be2530b117c7d7729330e457da2f5cfb1d99d38743141735ca1e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17232455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f703438f575677037751d8350dc8ca2b8a1075655247757048c8a86f0fb4f02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb007b6d10eee83bef5532bcee86e3a8c93d043133710528fb87431b19c009`  
		Last Modified: Wed, 08 Oct 2025 22:58:01 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf08622f74c2cb19cc42192b0711623e35b29f60ae2d9d1fcbc547a6a390d74`  
		Last Modified: Wed, 08 Oct 2025 22:58:01 GMT  
		Size: 173.2 KB (173217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516a54ddb544246c21a392fb73b12e227ee929914589f84adf8c2dfdf775888a`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 1.0 MB (1003005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a16ba242bb9fb3d8eebaea443c6cd4f2439070eed46b08f0a2dc43b1677ab`  
		Last Modified: Wed, 08 Oct 2025 22:58:02 GMT  
		Size: 12.4 MB (12412006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881684f386384ab45ba4d1530e95277fa007efc2f08b9c5364547c8008f5e0a`  
		Last Modified: Wed, 08 Oct 2025 22:58:01 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cac7f2e4514ba07d7517943694f87e4d7a338933a96150e025d1a86413451`  
		Last Modified: Wed, 08 Oct 2025 22:58:01 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:e8d1c0b034e2352ee7b5b910dcbd843a3f4a56b904e9cc0bca409600eebcacf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8f33c67b3526d7ddc0d05c3a3cd670f46635ee2b6ba0e3c25140e87cbb091e`

```dockerfile
```

-	Layers:
	-	`sha256:da9f77bde89f4f9730e831fffa88aab826f44de9cf88f77ac91023c85a69086d`  
		Last Modified: Thu, 09 Oct 2025 01:05:17 GMT  
		Size: 460.8 KB (460815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83c97ffa126c80164dfbfd7953261f28966d560873bf0655fea35d5fd6661b8`  
		Last Modified: Thu, 09 Oct 2025 01:05:18 GMT  
		Size: 33.8 KB (33820 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:fd2f8954a0f6bb24cd8819c9a1bf7e033efe9969d3b571104abb9a58c61e7068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17088692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0a59320ed82065b460799171ea607ac0575fc49f9060b97642609bad150281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c1bd5c3bcf89bbfa4794c22754dd33db5b6d1c8917d75f64a8bfc2deccc1c`  
		Last Modified: Wed, 08 Oct 2025 22:09:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f6e9bda700bc1146a24598dc4c2c82d2d6909f0696c0991bdd3079fd14c2c4`  
		Last Modified: Wed, 08 Oct 2025 22:09:08 GMT  
		Size: 173.2 KB (173222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bfe90b0ac5f898ebba3c294198191fe60216aa8f4d6055a3d9d549f8d4a2e`  
		Last Modified: Wed, 08 Oct 2025 22:09:08 GMT  
		Size: 971.3 KB (971278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb258ad19c5cb91b06333155f09d9c9f057871bd78c88989a4ea7b6dd42e6ed8`  
		Last Modified: Wed, 08 Oct 2025 22:09:11 GMT  
		Size: 12.6 MB (12577073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe384ec15a9da9568abf632cbe087cf2704a9c569a9676fad76054f26b048ff1`  
		Last Modified: Wed, 08 Oct 2025 22:09:08 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8159be787ae9b7f23a2af2121c240f1c4015794ee4d8e7cef59a43ea0c075c2`  
		Last Modified: Wed, 08 Oct 2025 22:09:08 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:5d213a51f8895ea78cf7761d178c5c2f644baa666414f9f8a7eb66de143f089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 KB (33748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a3e6e6fdc32fb8e34a15dd7aab69765392099b0930a80b7f0b387abda214dd`

```dockerfile
```

-	Layers:
	-	`sha256:117dfca91e818a2372670091e0e15ee2ff24af492b92f4c6c345334ba4b77055`  
		Last Modified: Thu, 09 Oct 2025 01:05:21 GMT  
		Size: 33.7 KB (33748 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:4bc5c146043e886fc4463d6a2864fa8b560639c35aedebf5a180f34a0a373a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f666f46e1ba5dcaa40e0eead82492ab1684aa4201751cca4747e06e78a92d10b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b97bf8353d393c4f7341462c6da607be9f2c293764932bfdd9025fe6d28e84a`  
		Last Modified: Wed, 08 Oct 2025 22:10:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8985948dead8ea63afb99a31b2e7d7af80c7ce66a84b5dd2ecec4bff01cfbd82`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 173.2 KB (173221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452aeacab1eda7d54a6e743992f19b0f261b8330a99f60155e9bce69f07251b7`  
		Last Modified: Wed, 08 Oct 2025 22:10:10 GMT  
		Size: 971.3 KB (971279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fd34d131406103d3fb363d959d17c8ba9aed1afc767fa9365176867e8255fe`  
		Last Modified: Wed, 08 Oct 2025 22:10:11 GMT  
		Size: 12.4 MB (12439624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94af557abe0776eb40bcacee84d50da4e908150ae5fcd1755e6ed8ed03a4de9`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc3ab501afd3094c911e085886c97ee8635996e5c0524bb456d2652b5ca04d5`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:28b52c4048c51f58b5a541db3ab45cc4c2adf2d01a5b7dde521ca864ebf2bfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.8 KB (497817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd47a28c4f076375397464380d320bead6d9230a3ffe9f78e3968ca1a56b6d1`

```dockerfile
```

-	Layers:
	-	`sha256:44c72eaca5efa60c7f7e4997a91a7271d225adf52a722aab751a10179de17ee1`  
		Last Modified: Thu, 09 Oct 2025 01:05:24 GMT  
		Size: 463.9 KB (463857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117a2c55fefb704382655238b007dd449f3d76492b662650ce9d642380a9a7e0`  
		Last Modified: Thu, 09 Oct 2025 01:05:25 GMT  
		Size: 34.0 KB (33960 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:84b9f0ab5eab8ced87dc1b772a01420a9ea1dd92a243deb05a19a17fdaf80f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17677686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc62053442c7078e25c5c42f15582fc0dbe9d89b3a9c2c263affb4a12471dcea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f198446ddcca47e38b6d17b852f53fa0b4783e978cca98e5539db6645de582c2`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2269ba4a5b92a09ec692de4a81042c1d9f06c3b02e2071a22e25a016e568e02`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 173.2 KB (173202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e0666ceea13dcefe1cdc618e0629575473ffd47cb80270bc70ddea6f4e2026`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 934.7 KB (934698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123324b8202bcd28bedbae64461a0757235bfa7d63aaa9ec11b813c5dbd2f8df`  
		Last Modified: Wed, 08 Oct 2025 21:45:35 GMT  
		Size: 12.6 MB (12575779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ba34ea3b6287a97d15e580909799d29ebfb42522ab2dd3d3b7d082423f2a09`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840189eb6923b53041bbd7269c764cf8daabf3c37fe1b56ebb099226d4623102`  
		Last Modified: Wed, 08 Oct 2025 21:45:33 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:d2e7a0bf9e72ba5d515db7a2e0a62006346610bdb5cb1cb2031789cf72c3c734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 KB (494897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d13e05ab1e4fec9febfc2b3ca5b9ca378487893749f3c84a60c1bb0d3b76ef4`

```dockerfile
```

-	Layers:
	-	`sha256:cd950e72adc8baf4c663a47f30b6ab79544e839437c02c85d1193ae4933db587`  
		Last Modified: Thu, 09 Oct 2025 01:05:28 GMT  
		Size: 460.9 KB (460895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5935e84587d0f07c8c1c903803c3a133088cc7db22fcbbdb7ba1639270413d`  
		Last Modified: Thu, 09 Oct 2025 01:05:29 GMT  
		Size: 34.0 KB (34002 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:868b9f50d48b702fc97bdec2ab6e6b8c4a1a8c0a3567616a6e20e52c48f47864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaffb1cd8f9e0bbe0da4dffa554784d5faca22c76bbb841b55f201cfb01dea10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba614e041997a084346390cd486c917e600dde85ce140cf265a4cdf1083e6b8`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dd3872033b76b871c8167b029d80144599b045e94f756dc40e94766c8bd2f4`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 173.2 KB (173242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4441960686ad1c53611dd7049f8a81568737db997f8978442d57eba883a831`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 978.8 KB (978804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4484d5e84993683590ff715e3221ff698b07826ec58c4b8bce581b2ff1a23be`  
		Last Modified: Wed, 08 Oct 2025 21:40:23 GMT  
		Size: 12.1 MB (12069288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d0648f18ba25d955a7de77b7d4d846ac866adfeee503ed58b387db5defd60`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d787a743218b72b3224367d51c7dfef96b390dce3ba61df5e420dd91726fb9`  
		Last Modified: Wed, 08 Oct 2025 21:40:14 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:7240b22f29b40973bc4412ae44de05441bede6be26f44fa78316e66319acf79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.5 KB (494542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d614994fed705cbd194cc6693f30bd511fad91c25661fa02928f11c10bbd44d8`

```dockerfile
```

-	Layers:
	-	`sha256:784aa83acb29e8c1de62d7100c6c2b6ddeb11c6068dd354c07d6e55050c4ac5c`  
		Last Modified: Thu, 09 Oct 2025 01:05:33 GMT  
		Size: 460.8 KB (460780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43287fe39d741ac90ad78a70eea2de1ee2efbdd11fe2c0741e5db73a020ad3bc`  
		Last Modified: Thu, 09 Oct 2025 01:05:33 GMT  
		Size: 33.8 KB (33762 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:f1c257562f3f32bfa8048eaf6af1d9cdc7644856e6ed4a19b5047cf1644dc560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48988d534f591e3e3724dbcefa77c2f28ac614e771c02a93254cd3e461f28bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b0647732a82f74082e822bba2a052fecd04090dad610843e794f37e4097781`  
		Last Modified: Fri, 03 Oct 2025 16:22:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb29456dabc153fde70f6234be9fd7bf13440b3d4aecdf6227705405113f36d3`  
		Last Modified: Fri, 03 Oct 2025 16:45:32 GMT  
		Size: 173.2 KB (173214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274e88b45c8a6853481403c40524b2aabdedcfef86bed6bcd2c3e86028237f69`  
		Last Modified: Fri, 03 Oct 2025 16:45:41 GMT  
		Size: 923.0 KB (922969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57125979e37bf3b4d5ab099d7481e0ba3959eb0513b5c3c4b663fa18c6d4aab4`  
		Last Modified: Fri, 03 Oct 2025 16:58:01 GMT  
		Size: 15.5 MB (15500096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a891e8aa687ccd8699986f61873e8295915f4e6b2c716abc83d94850a326b`  
		Last Modified: Fri, 03 Oct 2025 16:58:00 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f37b25a182c273ebf7c05dae7ecfa8249af267b644b5cc2378e3520a9d698a0`  
		Last Modified: Fri, 03 Oct 2025 16:58:00 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:db463f937659541fe2c846c00b196d7e8ea764a69cad0b4675ff63fecf1d9a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149b70ed830bbdc23c3d241e6c756fda87b48a7d88a7865559d940cbb22eec46`

```dockerfile
```

-	Layers:
	-	`sha256:e6647342cc4145957e0ab40a32cb33e518d7448a4c597e8d089bddfc784d8b69`  
		Last Modified: Fri, 03 Oct 2025 19:06:59 GMT  
		Size: 458.9 KB (458910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3e7c1f1d5d312e9b8da3b7e1c9d9497c2bb4461e3b6bb0a53f938b0e2ceb6a`  
		Last Modified: Fri, 03 Oct 2025 19:07:00 GMT  
		Size: 33.9 KB (33876 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:e6e830fe13f31082ff99bc5c4e7560a11754618e5f2e6dec9695d45f8189ba09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18428828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c94f4230374dca3236ea8599fc0808a4344856bf0725bd09bcb927bbb6198b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad511ba1cc13824e85408aecb142edd0341095119fb9f63030e417beed16b73`  
		Last Modified: Fri, 03 Oct 2025 16:50:58 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3170a4d4a8af7279c16991b0ab57fe651196128a3b19464d99b6f4139cb87b`  
		Last Modified: Fri, 03 Oct 2025 17:06:21 GMT  
		Size: 173.2 KB (173223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc4548928260e8e81f21271f39b6199abfdff007fc84803ca02cbe4d553ffb`  
		Last Modified: Fri, 03 Oct 2025 17:06:22 GMT  
		Size: 975.0 KB (975047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64a5411f407a3f9a8811642e7b8b1eab4ec2606775ff079a070e2a7afa0194`  
		Last Modified: Fri, 03 Oct 2025 17:06:28 GMT  
		Size: 13.9 MB (13929805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe921a1349a7d2184820b5243da81dd014491ba32e12c556f71d11bd71962a3`  
		Last Modified: Fri, 03 Oct 2025 17:06:21 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0c5264bdb536012e0d3b9f7c1b5844a9738a63a340632370362155d4e6e81`  
		Last Modified: Fri, 03 Oct 2025 17:06:22 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:e45a086f47a09696683b5aa5cf5fc496d9cbf269d0c8f95a5627c267049db3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1024eb2df0ec699685744257c6ebb4ba160cc61ed6278a5b2c6dcfe3a88baa11`

```dockerfile
```

-	Layers:
	-	`sha256:a42c4d7017ef0fc04d1db08b804bfc093be9a14175eede8fb5f1a3d43a4c3aa8`  
		Last Modified: Fri, 03 Oct 2025 19:07:04 GMT  
		Size: 458.9 KB (458906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cb51b92a79b1677281bfe9b0dc4d71e5e6f003c429f19e3bf0a11f6c793d79`  
		Last Modified: Fri, 03 Oct 2025 19:07:04 GMT  
		Size: 33.9 KB (33876 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:d020860fb8533d1e91fc57d4d8a24150675ea7f3b57ee50f7381810646511f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19625411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb01ae180b76b9487b9f56795d2ad83e537e742f97c5cd2cf0e41f6cbe9b732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 11:58:08 GMT
WORKDIR /data
# Fri, 03 Oct 2025 11:58:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 11:58:08 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 11:58:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc7cad86f4dcbc2b30e94c21fffc26be87554b5ab95463e852b5ec7877261f`  
		Last Modified: Fri, 03 Oct 2025 16:19:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ebe4968e227709bf2134cae018863f19501541df2596a59c1e578b010f739a`  
		Last Modified: Fri, 03 Oct 2025 16:24:03 GMT  
		Size: 173.2 KB (173236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cf24ae61617fb0f3ebb959cada338d2d12d170700f06c3b7543d0591c93a46`  
		Last Modified: Fri, 03 Oct 2025 16:24:03 GMT  
		Size: 969.8 KB (969772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a32f6d5ed4b9e326c55d4bbe729024cda46cfa0795450a2c70a01b7f60acba1`  
		Last Modified: Fri, 03 Oct 2025 16:24:04 GMT  
		Size: 15.0 MB (15018642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d876a61484e0e82d56904f01be7a21ddc609c971f04d4241869bfdd18dfb16`  
		Last Modified: Fri, 03 Oct 2025 16:24:03 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91aee8b8e8fec095239d849ef980cd68adc43ad85ed4d4963b555462b229b54d`  
		Last Modified: Fri, 03 Oct 2025 16:24:03 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:ec55f6a68f9c58fae6465999ab470d094bf12cca6b25f775506666d8cb855b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcaf2ac92761e24f6fa680178419ce35511c3fce8caf4226728606905ff47c2`

```dockerfile
```

-	Layers:
	-	`sha256:74bd32a09270acb21908c5db1c7f4bfccbe7d17f228914ec65348968faf46aa7`  
		Last Modified: Fri, 03 Oct 2025 19:07:08 GMT  
		Size: 458.9 KB (458864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc6851314be89c5790db44811612b7ba125f2f4a88c0f9d7297a4ffa1113940`  
		Last Modified: Fri, 03 Oct 2025 19:07:08 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json
