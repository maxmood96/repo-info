## `redis:6-alpine3.20`

```console
$ docker pull redis@sha256:7aa7c743ac3098db284d764644ffea4d8fdeaac479dfe036c5dd55498ba6227a
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

### `redis:6-alpine3.20` - linux; amd64

```console
$ docker pull redis@sha256:b93fd5fa95e947a98ef098add6f7672de3359ac3a0bf5323f380d269e0f2680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14641471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4100b5bd17430263e85ad9d8ab851959b234acaaf378e093f1f98400f4998815`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06bad13a9cba3843082ea661f7e658f4dade90f07b9b008db2c663cc6adcf25`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebecd181d463078f6b488f93e50c7ba0cb0c5af7d6e9c08ef442c138fd2adc4a`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 171.3 KB (171277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639d6884da44432c59e44fd2e6eb9198398b50a80f61a16aea9c01b45394be1d`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 1.0 MB (1002658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0095eac60c52d8460e9217f37d2c13f18fee613fa25d976b02625a4ab499601`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 9.8 MB (9841957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3fe856cb76e3f1a8e33e03a4cfc37f7d6e692e584efa054ccba02d3e961fbf`  
		Last Modified: Tue, 12 Nov 2024 02:37:46 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe92cb740a4c4f53528e277ec28429c35a82b5e25665883146ac1c4b0540f6d`  
		Last Modified: Tue, 12 Nov 2024 02:37:46 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:36b13abb120c8f7713d1ce4e9cbd0091e5ed376eca52e9d5a0eec12e263d5951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.2 KB (488165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2c1031e5769c0a0add67110054bfbbc601b63ed7990ed974dd57f370cc3f47`

```dockerfile
```

-	Layers:
	-	`sha256:911191db1dd9dceba87970e9313b630c76ae2a99c8e0aff33fee0a551c0b3f93`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 454.3 KB (454341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6570065d991591a0e142ebe3be81690715cb858dac0277f15160938c8e9f19fb`  
		Last Modified: Tue, 12 Nov 2024 02:37:45 GMT  
		Size: 33.8 KB (33824 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; arm variant v6

```console
$ docker pull redis@sha256:a9e8fde66c9e39e3a49193968e86c714c8b9849ace4a1f19db12a4950a44a014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12122739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56932986823b9ef02347d572de6c50090ef9d1885b244f6af727c902118ae432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e85f36ff0dfdf0492003254090eb0df04b5569083156b4cb5684815bb2388`  
		Last Modified: Sat, 07 Sep 2024 12:15:33 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e64e50e95146d53b65614ba88ceea753ed1d798b3c79132f726e64ec158433`  
		Last Modified: Sat, 07 Sep 2024 12:15:34 GMT  
		Size: 171.3 KB (171271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41ea06360358ec8a40b32f042d53ff35541bbd938e78deba56145be67d771b`  
		Last Modified: Sat, 07 Sep 2024 12:15:34 GMT  
		Size: 970.6 KB (970614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84c1c232689892ccc1f943a88252a0cb040648089b9737634ba950ffbd9fd1c`  
		Last Modified: Mon, 07 Oct 2024 18:06:22 GMT  
		Size: 7.6 MB (7612679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a0279e159edb855125f6b8949bdf580bafcb117268e0ad31c351ccf7c0fb0`  
		Last Modified: Mon, 07 Oct 2024 18:06:21 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818c5d8e3e34a0ecaa2aaf84d1ba0ca2768ec5d119ce3809611349393d76ce5`  
		Last Modified: Mon, 07 Oct 2024 18:06:21 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:2ec4a23114402e3d45c8fde5b86771920f5cf25e86ada84cae9ca9b3dd77e66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 KB (33531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8edad4d0c4ae03aeedce6657d5ee00549405ce4fc38623d3f7399fdde36e58`

```dockerfile
```

-	Layers:
	-	`sha256:eaf959b854102ce602d3df75c2fb97849eee6749d7e5057e5c263805c9bd788b`  
		Last Modified: Mon, 07 Oct 2024 18:06:21 GMT  
		Size: 33.5 KB (33531 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; arm variant v7

```console
$ docker pull redis@sha256:47ea0e56a962d2ec1be9cca85cd87bdb8c44e502153992368fa798c93cf454b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11735430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab82e2c77e29d35c596ed2316a76feb003c03cffbfff856d27b1bbedcdceabf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c4af14b3ce492d093912821ca02b76e89a6cf508ecd3127b1777e2b08f7c8`  
		Last Modified: Mon, 07 Oct 2024 18:20:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa203ceced436ac59c6ed01368ca6b20432a68b719276584f662fce4f4465e8`  
		Last Modified: Mon, 07 Oct 2024 18:20:02 GMT  
		Size: 171.3 KB (171293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a0ee8ebe97580703393977c7ccee090971a8e86aad66347355456ab931274e`  
		Last Modified: Mon, 07 Oct 2024 18:20:03 GMT  
		Size: 970.6 KB (970626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124c4eec66ea32dc6c4263a44d75b30265d5bfb00a668ec85f023de9d4d48ca`  
		Last Modified: Mon, 07 Oct 2024 18:24:50 GMT  
		Size: 7.5 MB (7496338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28312c2196e5da70c740ea573a61f4ba5eee1cdeaa2b48df4384b37b93253744`  
		Last Modified: Mon, 07 Oct 2024 18:24:49 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84b8bcf010d68224d9fe6b4d18750def98b07a6f33d0b00240bc92fa0f5f3de`  
		Last Modified: Mon, 07 Oct 2024 18:24:49 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:c717538cfdfe3a8083846ac3708b247815ca719cfd151e5b0080bfc790b85477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce6d4f6dc9f385512321d021774da91ee2c038e3ab1ec76f22ec5fb2ed721c0`

```dockerfile
```

-	Layers:
	-	`sha256:8c61026de1c134bef9efb663f12891eeb4b76a6cecba10af9a24a200f63423e6`  
		Last Modified: Mon, 07 Oct 2024 18:24:49 GMT  
		Size: 457.0 KB (456952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc611e0fdcb2dd8ccfdb92dd7306db94166b4121843faa26b94cff219519bac`  
		Last Modified: Mon, 07 Oct 2024 18:24:49 GMT  
		Size: 33.8 KB (33750 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:cd9cc854cf2e6e61be880e5afd09197b242c13f8c565cd9a194e187e0bd0e8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12856344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188444e93869a5ad50565b4e68b5b9bad24b0cc644e3ef9b425bc7be1455310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2277e15e746fba6f98c449d3699f35f010d455766fb076b94a29c51e594b42b`  
		Last Modified: Mon, 07 Oct 2024 18:18:33 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbd811a3c46ce6b189162d06ea02937b834d6cd9e7323e326c97124579dc25f`  
		Last Modified: Mon, 07 Oct 2024 18:18:33 GMT  
		Size: 171.3 KB (171279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de79657b25f12ebd37c1f3b7d033b2151d632daba6178382c21d42c14441ff4`  
		Last Modified: Mon, 07 Oct 2024 18:18:34 GMT  
		Size: 934.5 KB (934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd5ebf53e63fa88c54606c643c2a9ee1f9ec437f6a0fb0351e9c8e9249c1e79`  
		Last Modified: Mon, 07 Oct 2024 18:22:53 GMT  
		Size: 7.7 MB (7661244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40597ecf766ec926d8421213071748d3a9cc21ceb6ad211517b89a857558dd3c`  
		Last Modified: Mon, 07 Oct 2024 18:22:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c148be96edbbcca3d213049605f65782e69a39c60c0f9cbe8ba578d3751758fc`  
		Last Modified: Mon, 07 Oct 2024 18:22:52 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:c3e3266896148d20cfa9a33f54a4144b0398ea75cfe70fa61cf06b7d9134b460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 KB (487909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73feff756158e742b3975b50c293834d05431e2eee124a18650243625269ec3d`

```dockerfile
```

-	Layers:
	-	`sha256:334a062661109df1249e32e22fc34750565f0b01ccc39e4a68645207b514ade8`  
		Last Modified: Mon, 07 Oct 2024 18:22:53 GMT  
		Size: 454.1 KB (454116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bd0b3466720a21ed05ac86c5f71b8ed56759e988525b05db3c0c22f1068ea6`  
		Last Modified: Mon, 07 Oct 2024 18:22:52 GMT  
		Size: 33.8 KB (33793 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; 386

```console
$ docker pull redis@sha256:dfbb90cc90ee61d82180389e9871afc55ed5cfec525740d33b6111eab32780d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14048686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8e01f91df1dec897e49f564ae2c3822aeeb76484d90e531931c48d3c09509a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0416630625483874f704c861051adc9b20f4e49ed375fc869f9f6064f681ef04`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d7842be4114721d2aab40663b29280b0f0f1c2de60cdd6e57ca4f296ed758`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 171.3 KB (171280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caea3b34d4f732beb398d9a7315b82e882e655647ea227cca32c4b4613b50f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 978.1 KB (978129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9279a697464a9486024955380a807c573b57cd85d415c29c3c6a578c4b66b889`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 9.4 MB (9428386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703d545aba216b93e35801f6b429c2f3302a592113ad305b81baee048cab60b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e027284e79c4eccd73d21b17450c682109fa974217a905a36caae656b9822de9`  
		Last Modified: Tue, 12 Nov 2024 02:38:02 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:90c295d1c037d2ddc6ca385b7a647eec63797b917a2ae97c9afc01addfa8ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.1 KB (488074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a62680e0f573a3326ef25cc0d97185c413715a434bd0b6b31ec1e5f3a6f701d`

```dockerfile
```

-	Layers:
	-	`sha256:fb0d66d640eb9762b4130c2e44e6a3841d8f391c874dce832494cd350a89676f`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 454.3 KB (454306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487b7d9bcc6127254211a375ddedd1fb8e251e7182fdf111f6f6e31cebb76b5d`  
		Last Modified: Tue, 12 Nov 2024 02:38:01 GMT  
		Size: 33.8 KB (33768 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; ppc64le

```console
$ docker pull redis@sha256:bc9ffb883462af0e9e793e376a0092510390b982bd57c7af32cfea8290b8d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12839983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79829c78992be1522615af1c13984772ee9de2bd29cbdc021f5deaaab3e31411`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1b48889342280155ae9d9f7778e32b5bf576a7748f1c8c948ea2c6a302b065`  
		Last Modified: Mon, 07 Oct 2024 18:19:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9286c847d98788c9f0c1208418340221778b9dfc358df895487bdc6b52c1039d`  
		Last Modified: Mon, 07 Oct 2024 18:19:11 GMT  
		Size: 171.3 KB (171299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a6328f1489b7c6250bc40ff2f8c1bbcfb2cf5d03a3718467ded9f8f465fd68`  
		Last Modified: Mon, 07 Oct 2024 18:19:12 GMT  
		Size: 922.9 KB (922863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3af58c4cf28b60abfc44abf0575dd1f6d658e896f53daeaa42003e8caac8f2`  
		Last Modified: Mon, 07 Oct 2024 18:24:28 GMT  
		Size: 8.2 MB (8171727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3c8d294f6b29749a0731f51e094cafa331f045c4c3d9e477f5f990c6b07d9c`  
		Last Modified: Mon, 07 Oct 2024 18:24:27 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3769ebadea73e98e391dc3c96d0d3281c2dd343fe5a8e11af3b92b77c4ad83`  
		Last Modified: Mon, 07 Oct 2024 18:24:27 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:3ff316c3137b4245666e1b0d001bf0b4a60bfb68eeb30146fb551a9dd83d03ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.8 KB (485798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16835fde67e2d9fb8c7cc622562c4cf27a32351888d0ce032e39ffa68fa42f31`

```dockerfile
```

-	Layers:
	-	`sha256:08c502ed725f1b29593d6d05e85525713f11651115b301aba0102c6239b8dd15`  
		Last Modified: Mon, 07 Oct 2024 18:24:27 GMT  
		Size: 452.1 KB (452128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd29503ef10d2e7fea2719c8f6824d5e1819cda21fbf4491edf7e4fa92d09714`  
		Last Modified: Mon, 07 Oct 2024 18:24:27 GMT  
		Size: 33.7 KB (33670 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; riscv64

```console
$ docker pull redis@sha256:d2f8eebe8a28248a14cb30dd4a31b66e707621d8acade9d36bf84e2c00670282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11867691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd45672ef0ad4c33c10945f838751546819573e72ccc4d074a33043e71d875b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace1b85a7a00c1e987f7fbf6d500396ccd30159b6ecee7b941154963e0bec84e`  
		Last Modified: Sun, 08 Sep 2024 10:46:07 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f2f2e448c90f36944b401454a106149b45fd5c4c15ed89103ffebdc6726f53`  
		Last Modified: Sun, 08 Sep 2024 10:46:08 GMT  
		Size: 171.3 KB (171277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a773d846434bf0b3d0147f818baf2133bb9051d3a9b4d8edae5aa5a175ee27`  
		Last Modified: Sun, 08 Sep 2024 10:46:08 GMT  
		Size: 974.6 KB (974581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc0ecd771b8710d5d04e42d152d6d9de4e876d1c72c0ce83176946cf7f35ed1`  
		Last Modified: Mon, 07 Oct 2024 19:14:50 GMT  
		Size: 7.3 MB (7348709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b35785b764c53fe4ed6fe1a63c049e8244400d257e6b1fe999d1a07d658848`  
		Last Modified: Mon, 07 Oct 2024 19:14:49 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493d6b135ddc58230f354ddaa2cca2054e676bb1fe3b0dd85a6adf7984c9869`  
		Last Modified: Mon, 07 Oct 2024 19:14:49 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:01c5e7b36cce848f0c47116c77b6129f38ce3c01466c1bb8600f73a4314db0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.8 KB (485797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f071cf1faf234e3d25665ba519629e8e3263a202c3818b4be6e7369bf7f7967`

```dockerfile
```

-	Layers:
	-	`sha256:39267701a2ac834ceb2af78431e56e7d49252262cf6c9e97fcaeef834e232168`  
		Last Modified: Mon, 07 Oct 2024 19:14:49 GMT  
		Size: 452.1 KB (452124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e58fd743b0eaffc02f11b2cfe174873a4c54c74d9a52781d586f39d7c6a5fb`  
		Last Modified: Mon, 07 Oct 2024 19:14:49 GMT  
		Size: 33.7 KB (33673 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.20` - linux; s390x

```console
$ docker pull redis@sha256:f911af80aede5cd9128c946392f5fd1649f71e16a481e78eacd39efcc8631e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12574590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e93adeb93ce7ed307dca7481c8ca90926493079c2b6f20af3e7a46b6b79088`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6b765491e941c995997431769204dce17f733d071855698687fac06475135c`  
		Last Modified: Mon, 07 Oct 2024 18:26:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783fce04e0c19084cd94e9d440ba64cad9c7ef9bca4d3df2aa70b2802ce5296`  
		Last Modified: Mon, 07 Oct 2024 18:26:28 GMT  
		Size: 171.3 KB (171283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f9feed30b857d20caa6668eca4507a77d88e62ca2a7e89b0465050dfdb88e6`  
		Last Modified: Mon, 07 Oct 2024 18:26:28 GMT  
		Size: 969.3 KB (969259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b17ed4aa1e7302846bf33704d564a56e810af54c516ef83baf6b547a6354f0`  
		Last Modified: Mon, 07 Oct 2024 18:33:27 GMT  
		Size: 8.0 MB (7970778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d2e27ae049744361ffa8784969ee4cd48cba4773fe2e81c1594fbdebdbe5fe`  
		Last Modified: Mon, 07 Oct 2024 18:33:27 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dcc4aaf13dd31dcd69abe4a15036da33e6a5e9e7ca80eb7a754c9d66f111ef`  
		Last Modified: Mon, 07 Oct 2024 18:33:27 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:715646cf54c52f6d9399f471b3b3866717a9620a80d099ee80dff3fa80751e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.7 KB (485694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc7e926593e6925a46503de2d7dddc3d55ab4599392e321ba64be9c3a1c7914`

```dockerfile
```

-	Layers:
	-	`sha256:633858e6f38e4a78262d7d73ecfd3a35ba17d7c98792df82a4c85f2330226e79`  
		Last Modified: Mon, 07 Oct 2024 18:33:27 GMT  
		Size: 452.1 KB (452082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc6bc550519c7d27508e97d8dade1ccc23f201cac11f0787c5e1286dec8708c`  
		Last Modified: Mon, 07 Oct 2024 18:33:27 GMT  
		Size: 33.6 KB (33612 bytes)  
		MIME: application/vnd.in-toto+json
