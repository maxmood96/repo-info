## `redis:6-alpine3.21`

```console
$ docker pull redis@sha256:5cb97148754ce2ad8a8364a1c0fb266d355d203dde69a75656129fee4d9b73da
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

### `redis:6-alpine3.21` - linux; amd64

```console
$ docker pull redis@sha256:06ca86a2130235868e8688e47988030cfb0b3560970349e3a23a2f4a62f6c594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c77ec7e49d73a86e345ccd2c4a53a5f43b485691294d3af63a2a1af4d6170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:37 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 00:21:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:21:48 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 00:21:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:21:48 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 00:21:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 00:21:48 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 00:22:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 00:22:14 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 00:22:14 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 00:22:14 GMT
WORKDIR /data
# Fri, 17 Apr 2026 00:22:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:22:14 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 00:22:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff27e14e041024c937adb04e970d11afe2a72ceed6634bd1d0db8c9202efd4b`  
		Last Modified: Fri, 17 Apr 2026 00:19:11 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a09b46cfe90d5bd3c4e24fd9bb2b1ccedb10e16610be838e6406a9b02ceb7d`  
		Last Modified: Fri, 17 Apr 2026 00:22:19 GMT  
		Size: 173.1 KB (173135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd2f7b33c2c249056c67dfffdadd038b27579377fddaa1b6077fb3feb60f23e`  
		Last Modified: Fri, 17 Apr 2026 00:22:19 GMT  
		Size: 1.0 MB (1003020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc91f6fe10c59f117f513e190c9f3744e914996cabceb80813e9df93705920`  
		Last Modified: Fri, 17 Apr 2026 00:22:20 GMT  
		Size: 7.6 MB (7599835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a4e6723bde5d27ad686e3727a4eb50d5d034fd87187ab3a4408610fec8247`  
		Last Modified: Fri, 17 Apr 2026 00:22:19 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c804a45187b537c415e86aaac3703b3dc4fcee3713d07c472d6157429760a313`  
		Last Modified: Fri, 17 Apr 2026 00:22:20 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:a47a8ac070a063ace15da8dfc795de3630c862699fb17406836192bf2d3933cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa9af6c11ba7f230c7a2ec05ab285af2526ba6fc50efbfe7b38102fa9078159`

```dockerfile
```

-	Layers:
	-	`sha256:d00f82c950033f32b8dbcb0b8b2ec263498f5b97dcef81a47dac476ac82abdee`  
		Last Modified: Fri, 17 Apr 2026 00:22:19 GMT  
		Size: 460.8 KB (460825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b50dd6c53594c426c80b880b2d820245786be690ceba03d1f12f94524913ce8`  
		Last Modified: Fri, 17 Apr 2026 00:22:19 GMT  
		Size: 33.8 KB (33781 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:272d23af3cd2155827153de2b1ef92dfc57482fe15a1087098774a6436710e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12149892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00052e0016662ad803c23b97d6973f737a8682f07f4ce87305da0d01d8962f5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:54 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 00:26:54 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:26:57 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 00:26:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:26:57 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 00:26:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 00:26:57 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 00:28:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 00:28:30 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 00:28:30 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 00:28:30 GMT
WORKDIR /data
# Fri, 17 Apr 2026 00:28:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:30 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 00:28:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1315d92cd23b7cfead104b630224e8478707cbd4c78c25c8876e4abac199b5fc`  
		Last Modified: Fri, 17 Apr 2026 00:27:48 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d45c24a925144ac53d18ed26b6ccc9f3df3630c0b011dfd07cf0c132ae33e6`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 173.1 KB (173141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1038954b39e8a79b9d9a0f3f11320a5aa30ef9784e7af13a870a7a50417f278`  
		Last Modified: Fri, 17 Apr 2026 00:27:49 GMT  
		Size: 971.3 KB (971285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34fa8e45d494628c6c6167a01d35aa59619d702aa6b4da77b15446c94f7b3a3`  
		Last Modified: Fri, 17 Apr 2026 00:28:35 GMT  
		Size: 7.6 MB (7634755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1cd2673237f3c625ad78348132f59a94aec2caaea023a52a807d7170f7121`  
		Last Modified: Fri, 17 Apr 2026 00:28:34 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983a14569014772a952e1ef51fc26dfc1c3f3e9ab62919451b7b0357d33a5aa3`  
		Last Modified: Fri, 17 Apr 2026 00:28:34 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:c0bd5b47ff9de9f42af7f3907b17d4bdf1473f08458e5cf1e29b06983089bb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 KB (33709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428a875b1b4eeaae77f0748e5ad6e5076e0579251981c57684336a996fe57005`

```dockerfile
```

-	Layers:
	-	`sha256:da3a2c139cddf243bd03b6c3ad55ea01d053614169586dcccf8518d424ba65b8`  
		Last Modified: Fri, 17 Apr 2026 00:28:34 GMT  
		Size: 33.7 KB (33709 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:d3c9f387aa34196883fd8f7ce2a1eba15f3bfc8eafc83cbeadd170c59373a030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11765103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9577c35ddaad52ba0bee5a9a234115d4e179d28077c2429c3c75a1fcf397975`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:13 GMT
ADD alpine-minirootfs-3.21.7-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:26:52 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 00:27:58 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 00:28:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 00:28:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 00:28:01 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 00:28:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 00:28:35 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 00:28:35 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 00:28:35 GMT
WORKDIR /data
# Fri, 17 Apr 2026 00:28:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:35 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 00:28:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7957b137a4005e85cd17d3e5e1bbc7099f5f082aa28f72387126a1c8449672d7`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.1 MB (3101912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d88e6c0ede937d43f97665680d70de058df62ee243e06d6936fbb75c59535`  
		Last Modified: Fri, 17 Apr 2026 00:27:50 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b23e687dd63183050c6f010c6526f45b0140914c0b70ae8cd137e44eb5f708c`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 173.2 KB (173152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6592df2d26996612f8327032d85cc872e3aeb85db939583cf02438703a5df803`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 971.3 KB (971319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0365d140c15c6df4bddcb8e2ee2b8e9c981eaa928d36ab94a9179bcdd9a7ef09`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 7.5 MB (7517068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ae7018b74b8b9151caa98213f783c8ee49a552dbbb129ff7b6e7a667bac4c`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfff79f27aac42fba1491fae66545885870ff60c66ec0324e76f753d1f1124`  
		Last Modified: Fri, 17 Apr 2026 00:28:42 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:01a59930f76e28e0b3733fe81b5a53b0362914c9bc207e6872538cbb0b71b750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.8 KB (497788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ef155658fe5427441009f581acf76faa01f01d05d7491f8a86f44338d5a715`

```dockerfile
```

-	Layers:
	-	`sha256:79cf4ee20a226e599015af75a5bdeb287cfad4e5a315e5f84ca33b216c7f270d`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 463.9 KB (463867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b07d8c2600b6a67fc2069bcb922d31203d84739b7aada24462d584d8e61b2b`  
		Last Modified: Fri, 17 Apr 2026 00:28:41 GMT  
		Size: 33.9 KB (33921 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d0d3a0cff409bcea8197b93963b2464bc327418742b0a468b97383df402270fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12762431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbbf2bd93d5b2b61c203b72547863eede7972b886a4b605628909e7259e0d21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:16 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 00:23:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:23:19 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 00:23:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:23:19 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 00:23:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 00:23:19 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 00:23:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 00:23:52 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 00:23:52 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 00:23:52 GMT
WORKDIR /data
# Fri, 17 Apr 2026 00:23:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:52 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 00:23:52 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5505c194645e2e4cc777b173b1184497bab4434c7313eaddfa9e191a2fdcf8e`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed1de29d3d5d20529d86725c59cb4f5d01413064a7409d073ab00a99c74c86f`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 173.2 KB (173158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1096579b79ae80bd014963809b50fb82fa7c6cee8fe44e226342bab298fdc1`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 934.7 KB (934725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d3d36991f1a813eb4e602049dd3230d0bbfe909b429a906bf929d5f8b1e5e`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 7.7 MB (7658426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54c1ba6b1ae24fad555acd578258a9508fdbddbbdd202ba0907d0db79cd1729`  
		Last Modified: Fri, 17 Apr 2026 00:23:59 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772304f9729b23cf8ea605743b77f547bb54893a9e50dab724da9fde96faf75a`  
		Last Modified: Fri, 17 Apr 2026 00:23:59 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:e5ccba9aa7ec508a58638f43ed8b3455c741907165bd4e15582e2c57e93ad413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 KB (494869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9812d5a29cfdb112b13bfcf4183ab545586ee9e95222c841ab213306b2f4d5b3`

```dockerfile
```

-	Layers:
	-	`sha256:c17854379e08271ea2886dd99d3cf3e37c74e590c6e5940ad42ad55d4f9858eb`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 460.9 KB (460905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1865038e19b42887fda63a76a17e005ffbcff0c029e08024ee6b834e7729499f`  
		Last Modified: Fri, 17 Apr 2026 00:23:58 GMT  
		Size: 34.0 KB (33964 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:f61f3b30f4c35729440f2d86669654c4b3e19c204beea66205cd27777244f5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11961004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57515ddaddaaf41e1bffe8ada52ac9dbe870a5009aa4e6bef08fc8148034f3bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:35 GMT
ADD alpine-minirootfs-3.21.7-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:35 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 05:54:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 05:55:01 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 05:55:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 05:55:01 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 05:55:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 05:55:01 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 05:55:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 05:55:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 05:55:33 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 05:55:33 GMT
WORKDIR /data
# Fri, 17 Apr 2026 05:55:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:33 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 05:55:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f6078c6ba1ececd5b6486ae9f846f15a21622e1b802bfd96f0334235ac0b75e0`  
		Last Modified: Fri, 17 Apr 2026 02:42:40 GMT  
		Size: 3.5 MB (3468819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792920ed6bc88f2888a6e912277830e73a8ba027f37d4dac3163de60d03f2e7`  
		Last Modified: Fri, 17 Apr 2026 05:55:39 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa825688713f0eb56d66109cdd1c704ae336ae682a38ae82328425ab8ca47f85`  
		Last Modified: Fri, 17 Apr 2026 05:55:38 GMT  
		Size: 173.2 KB (173159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5c0e30406a0126092b33a98a0e9476f2d0c9fdf09d24dc6a26453941c6aa35`  
		Last Modified: Fri, 17 Apr 2026 05:55:38 GMT  
		Size: 978.8 KB (978807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95bb028758aa8b9910fb451b738ea9a47a3648180b4720e6e2f27afd23262b8`  
		Last Modified: Fri, 17 Apr 2026 05:55:39 GMT  
		Size: 7.3 MB (7338558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bcd3df669ee2d3d9de9b25ff5e1e8314d51cee6718090b5e188741ab590c85`  
		Last Modified: Fri, 17 Apr 2026 05:55:39 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158ff94df57d37b5f6302210a2b52c02e2f0d85e227b53bdcb52ef8d4b390560`  
		Last Modified: Fri, 17 Apr 2026 05:55:40 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:ae10bbf1766e4a0795b6ba0ec9fd6370558a137b5e881dd3805e53b33611e70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.5 KB (494516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bf2a6c0142a20d69e116f120145f697458c9d1c5bd3e3e41525963add27ccb`

```dockerfile
```

-	Layers:
	-	`sha256:73b9d947c7e10735fff3e4c6edcb6a5cefc39036a88f09ed6f13ea1715a262fe`  
		Last Modified: Fri, 17 Apr 2026 05:55:38 GMT  
		Size: 460.8 KB (460790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30831301e1a045641cc0744d3808212b7b709dd00161d98013e65063db05eff4`  
		Last Modified: Fri, 17 Apr 2026 05:55:39 GMT  
		Size: 33.7 KB (33726 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:830392cf45d7f62011eb5fb6711019856a290edc92fd4cdd66ea190d904b2927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12871611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8c1fa0289efe1aeefc13878654e75319165e6ae662013ebd4cd9f4dbf05801`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:31 GMT
ADD alpine-minirootfs-3.21.7-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:31 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:09:58 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 01:10:16 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 01:10:26 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 01:10:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 01:10:26 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 01:10:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 01:10:26 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 01:12:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 01:12:50 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 01:12:50 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 01:12:50 GMT
WORKDIR /data
# Fri, 17 Apr 2026 01:12:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:12:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:12:50 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 01:12:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fe51ead1f71865857c2c015e74518a0be9e72c6a70a845d843f7dd0cd2ee6e2e`  
		Last Modified: Fri, 17 Apr 2026 00:00:41 GMT  
		Size: 3.6 MB (3578920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80be0004502249448034dee5406e4f11ddca1e98f6415ac7f7b4ad0b61e6d2c`  
		Last Modified: Fri, 17 Apr 2026 01:11:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4637659c6195eac11f8fb859475a960ec94f7ed00c73e1b8a00bc86c5c090b43`  
		Last Modified: Fri, 17 Apr 2026 01:11:45 GMT  
		Size: 173.2 KB (173153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c58fb3b5f244bbd819c4801655ce8da06c49bb8c28540e218954e8582c24f9`  
		Last Modified: Fri, 17 Apr 2026 01:11:45 GMT  
		Size: 923.0 KB (922980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed280f8d8ae12cc56280e9c6c615cefe96c75ce65b71a19b5a9d69b29d4b9b23`  
		Last Modified: Fri, 17 Apr 2026 01:13:14 GMT  
		Size: 8.2 MB (8194899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa52c17febcc1704b90d10ee8d31ad5b9424eea91f0e618fe843b6e1ce7832`  
		Last Modified: Fri, 17 Apr 2026 01:13:14 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87958518def1f05049f7b7265d631291a1f8d20de34f2c291141e6e9d4238c`  
		Last Modified: Fri, 17 Apr 2026 01:13:14 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:838ea31915599f4a1b3ba02297b5e6aac2045d3fefcf7827d56e6347a42f2d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba04a01ddc93a8792ab2f7c04c4196d7266e4a61b88bcc0b67414ce18e75964c`

```dockerfile
```

-	Layers:
	-	`sha256:ce8dc3a94cfdca3cd4c4b346e46b3f504a42a15489c9b5ffeda09ef823fb98a7`  
		Last Modified: Fri, 17 Apr 2026 01:13:14 GMT  
		Size: 458.9 KB (458920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c257ca469b66de78d355f1d985b1d03261ce25c50085bbe1664fe81d0865cd1`  
		Last Modified: Fri, 17 Apr 2026 01:13:14 GMT  
		Size: 33.8 KB (33840 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:c6829b61b8938d33fffd3c825fa4f6920b0f40da85f70cbbcc15f76e451146da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11876700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f755833dd60ac5bd465fa9d0e141ba22369327b08efa498ff195febbaa74a5e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 28 Jan 2026 03:52:05 GMT
ADD alpine-minirootfs-3.21.6-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:52:05 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 17:55:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 Jan 2026 18:12:28 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 18:12:41 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Jan 2026 18:12:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Jan 2026 18:12:41 GMT
ENV REDIS_VERSION=6.2.21
# Thu, 29 Jan 2026 18:12:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Thu, 29 Jan 2026 18:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Thu, 29 Jan 2026 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 Jan 2026 18:52:37 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 Jan 2026 18:52:37 GMT
VOLUME [/data]
# Thu, 29 Jan 2026 18:52:37 GMT
WORKDIR /data
# Thu, 29 Jan 2026 18:52:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 18:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 18:52:38 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 Jan 2026 18:52:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d9004d3bcc0dc8e7661e1984e1d95b59d7ae869e3d04a461926d42455ebac19f`  
		Last Modified: Wed, 28 Jan 2026 03:52:37 GMT  
		Size: 3.4 MB (3351733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bae849a93a742e4a13c7feadfba6bc0c684127a3e48cf290e93e1b5f4a3b97`  
		Last Modified: Thu, 29 Jan 2026 18:11:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee74d0238d7d8634f23351b7df8b29f2624b52f7c3ca3f13a826c76046366d7`  
		Last Modified: Thu, 29 Jan 2026 18:27:21 GMT  
		Size: 173.4 KB (173352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6edb4d42d2aa9c3f2dbd765121e0d58db3e96b8f2398ebcf23e62c6d51adc0`  
		Last Modified: Thu, 29 Jan 2026 18:27:21 GMT  
		Size: 975.0 KB (975045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226708acc811d21b4de880532e2a2d2944240152a2123cc0beb7d5346ce18e19`  
		Last Modified: Thu, 29 Jan 2026 18:53:15 GMT  
		Size: 7.4 MB (7374910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0808f51af66ae54facd892adb027f350ee3e8a62d8fc3f4156dd9434d30937ec`  
		Last Modified: Thu, 29 Jan 2026 18:53:13 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a04e5f16ca15559bf39f1b52968ec9553d46df4087f8c8d81743c36eab95074`  
		Last Modified: Thu, 29 Jan 2026 18:53:13 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:cf65557451539d9ed7018ab97cdee756ba758c5d524ee240c3fbbccacde9d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6006170c967d679b52b7b590fbd73c556436cea86274016af5676c3654186e76`

```dockerfile
```

-	Layers:
	-	`sha256:1697f0d250948f7b61a7756108513e4faf75be814743917da3b4dc93fc6d40d5`  
		Last Modified: Thu, 29 Jan 2026 18:53:13 GMT  
		Size: 458.9 KB (458912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb74942f4c9bd4a88d942d0dcadfaaed0101f90471da4fd61a0fce79bd10343`  
		Last Modified: Thu, 29 Jan 2026 18:53:13 GMT  
		Size: 33.8 KB (33840 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:b04287c5a4f3b5eabc5feeb1f2652df1ab9168c1e4c30ed5b95644cf8f8e6199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12592217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3eee75fbf547d84eb3c6c66e69c65671e43dcbc82cf68bdc3be94b8f31dd75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:58 GMT
ADD alpine-minirootfs-3.21.7-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:58 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:37:41 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 Apr 2026 00:39:49 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:39:53 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 Apr 2026 00:39:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:39:53 GMT
ENV REDIS_VERSION=6.2.21
# Fri, 17 Apr 2026 00:39:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.21.tar.gz
# Fri, 17 Apr 2026 00:39:53 GMT
ENV REDIS_DOWNLOAD_SHA=6383b32ba8d246f41bbbb83663381f5a5f4c4713235433cec22fc4a47e9b6d5f
# Fri, 17 Apr 2026 00:40:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 17 Apr 2026 00:40:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 Apr 2026 00:40:40 GMT
VOLUME [/data]
# Fri, 17 Apr 2026 00:40:40 GMT
WORKDIR /data
# Fri, 17 Apr 2026 00:40:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:40:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:40:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 Apr 2026 00:40:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4dde3be1ef4aac98984d14e789ca07a8f41fc8984a89741b58981521dba1d412`  
		Last Modified: Thu, 16 Apr 2026 23:54:18 GMT  
		Size: 3.5 MB (3469813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132d2a478fe1b7288f7b1abbb978c8941c15ca52f514843958f12e81f07c5370`  
		Last Modified: Fri, 17 Apr 2026 00:39:29 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde3bc4530ef4df94c902f71577bd3a65e8f36c207bb275959ff5548bfffb183`  
		Last Modified: Fri, 17 Apr 2026 00:40:51 GMT  
		Size: 173.1 KB (173149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685fe50eb6a63cf15ea483ea2566ab083f6e2dcab44c1904ec852bcc563d511c`  
		Last Modified: Fri, 17 Apr 2026 00:40:51 GMT  
		Size: 969.8 KB (969779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48431f412841714d56b488af2804e4e7cc2f6e7321391924ca0547bc661e4fb`  
		Last Modified: Fri, 17 Apr 2026 00:40:52 GMT  
		Size: 8.0 MB (7977821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394074e2c3e854ea5595d950371b1016de7762a5cecedc1143797ded100daa60`  
		Last Modified: Fri, 17 Apr 2026 00:40:51 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad6c85a7450e91081de738c93386ff353ff701e0d06de497f01ee1b98ecc2c2`  
		Last Modified: Fri, 17 Apr 2026 00:40:52 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:adac4f098c6ba507457c0cae58223631a8500cead13d1dd636e17837e0c6ac00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b377641e4346ea6e500bd412d0a9353475d2a09d250155f7e7dcb559af3adc35`

```dockerfile
```

-	Layers:
	-	`sha256:9f6b69614f19b7fe959e6f935cc2d3e83ad60ada85ba7dd670cbb75bd7e97e78`  
		Last Modified: Fri, 17 Apr 2026 00:40:51 GMT  
		Size: 458.9 KB (458874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecf94e289e2718a0797b6ceedde0f7980ed437070c43e44e2e1cfc252e7998c`  
		Last Modified: Fri, 17 Apr 2026 00:40:51 GMT  
		Size: 33.8 KB (33773 bytes)  
		MIME: application/vnd.in-toto+json
