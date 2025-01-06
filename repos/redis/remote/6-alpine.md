## `redis:6-alpine`

```console
$ docker pull redis@sha256:eaba718fecd1196d88533de7ba49bf903ad33664a92debb24660a922ecd9cac8
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

### `redis:6-alpine` - linux; amd64

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

### `redis:6-alpine` - unknown; unknown

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

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:2c574aacebfe72ba76d6a55bcde2609cf02a39f3291bd5914f81c0e48cb58464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14067144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a15990c2a55b71f02909d094274a87e9d17ad2a45c945beda4ca32bb34d3d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dbd36403fc7a4c06047a834dbc2770334cd13e3a0e5cc9cd67dbea2fbeb89f`  
		Last Modified: Tue, 12 Nov 2024 06:23:51 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcdb894a46647b4c2b9fbc41c062b8ad68afb9179c2854bc1f73e5bca750b2f`  
		Last Modified: Tue, 12 Nov 2024 06:23:51 GMT  
		Size: 171.3 KB (171273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ac4780e695ad408ec569637bf28f4eeb209fd063ef3badb3a2af7289822488`  
		Size: 970.6 KB (970606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d79aacf45ed24d322fc8bce0ecb19bdb59fbb3e7c207862bcfd20414db56da`  
		Size: 9.6 MB (9556995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cdeff7075d04843030a3183393b6a3d85ee906eb01c9407b4dfd52ee4ef92`  
		Last Modified: Tue, 12 Nov 2024 06:27:54 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7113e10c44b238590ea68a5334a97bb7ae3c40de7b515e99f006ee23ddd62d`  
		Last Modified: Tue, 12 Nov 2024 06:27:54 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:af8da9286442bdeb2e17c9f9e67dc12e6d5e5e1b0084f7cc5398a9b9913b6d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 KB (33748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a57ec13cac1b47a08cbeba613f09194db68a0d65363d6562ead27d377eacc8`

```dockerfile
```

-	Layers:
	-	`sha256:7de49731ef1398b0dc5d1056cbbad20a5e87ed1ab8ed4e02ad5996012787c51f`  
		Last Modified: Tue, 12 Nov 2024 06:27:54 GMT  
		Size: 33.7 KB (33748 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:4829dc1a69203da00c5f7e51e070ffb6236e09426fbbd8cf4a7fce123cf86537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13529750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895fbf247e338e0020315947b20fc2b83b1e59596a2531fa239636385117f706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb40e706c9532ed6effa61312bc9de6afc7b280b1cdf1da2c7f82298c88e15`  
		Last Modified: Tue, 12 Nov 2024 15:15:25 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0704c05c0b73e00ffae7afa51484f53b77927aa7ab5369c8af455586e68e899f`  
		Size: 171.3 KB (171296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7862bb41d32b7a7fd7f1b13f64a840040e238861401b1f97483c872804c45021`  
		Last Modified: Tue, 12 Nov 2024 15:15:25 GMT  
		Size: 970.6 KB (970628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c811354232daea565b626e843cd6217053ea1cd933cd5991d4e56f95ade77`  
		Last Modified: Tue, 12 Nov 2024 15:28:50 GMT  
		Size: 9.3 MB (9290666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc7a9a76371464206698f9ef2440540436eec3494b65943c2ab87641e2d702`  
		Last Modified: Tue, 12 Nov 2024 15:28:50 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44601fbadff15850d2ed459c7bc14b1918e1895ad8d32ca2be8fd07fed4cc7b`  
		Last Modified: Tue, 12 Nov 2024 15:28:50 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:35ab17f3c7d8579e84f363bd567d13578d5a15114b12b74e527eef58d4b1bcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 KB (491220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc70562202c80d3ae918610bd283e711fbb7299538f6adcd31b297059b18e552`

```dockerfile
```

-	Layers:
	-	`sha256:2bcbd6d77a772f55331fd99d7a9d7ababc134982ee73f68a3571423154c3f9bc`  
		Size: 457.3 KB (457257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df250cb5cde126c4eea300b5dd82af088b0ca24bb04cf0c7f0cd932de19eec37`  
		Last Modified: Tue, 12 Nov 2024 15:28:50 GMT  
		Size: 34.0 KB (33963 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b5f7da7f2dd181281d6f6863a13d0af6cc1790af37391ee6e662b0aca7ac8822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15549340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdabd876a0002df57c52a7f1ff9641e5a899a92e99d1b2db7c6d905bac56ab6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5f0f82a8e96804ed40f04dc5c07f34871f503e27ea1c90bfa6d64e3e1bebe`  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b134de8fab628f0d4a2f9402496092d5d386e77c38616f8dcbea997f7fc271f`  
		Last Modified: Tue, 12 Nov 2024 10:09:49 GMT  
		Size: 171.3 KB (171287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b42411e55b3264e999bd49369c415928ab2eb198144bf2f29fdcf95d41f516`  
		Last Modified: Tue, 12 Nov 2024 10:09:49 GMT  
		Size: 934.5 KB (934503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c444f223ea7cf0e2fd206aff497c59da455ee4b774b1e5056615a6a2b5d83b8a`  
		Last Modified: Tue, 12 Nov 2024 10:27:20 GMT  
		Size: 10.4 MB (10354151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaaec890a2bf1f9562223d53fb38cae8952215ba0b44ea365ce1b3272a5fd66`  
		Last Modified: Tue, 12 Nov 2024 10:27:19 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44b005c93eb09334064a044a2c080defe8032ac123f299b92c98a89f33a23c3`  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:609fce56819356d995ec00965f97e53c92edda75a084a56a8a1e87830f832557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.4 KB (488432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56996e3f0025eb8ba18e91c085630d623c8fe69e094af37aee1da688b94b7b2`

```dockerfile
```

-	Layers:
	-	`sha256:c952d178938d9dcad3e8e56258dc5a9e5b3fb4ab3d55c917ed42220d97f482f7`  
		Last Modified: Tue, 12 Nov 2024 10:27:19 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30fe7e153ecf9fd1b4d4d09a5371007eb1926991f779f6bcd4263dcb593b237`  
		Last Modified: Tue, 12 Nov 2024 10:27:18 GMT  
		Size: 34.0 KB (34011 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; 386

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

### `redis:6-alpine` - unknown; unknown

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

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:d1fbea9d7c8d881d2cdbef64d00682400fef89421589be8e23c435acd618223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f466fe8a91f1ce9cb82eb3bc885e42160de2aadeae6f0e984d22195883a7cfc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2eba925463df7ac6ecfe77500042de73e61491219bfe290f03a60824f2b340`  
		Last Modified: Tue, 12 Nov 2024 07:52:22 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75777d0719769beed56ccb6f9189d1788ea30cb039452754a55cf158e4f91d39`  
		Size: 171.3 KB (171297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f79471afe05bd8fb0fc21847ec6a9ef6d9779fd0798efc214164a57401db35`  
		Last Modified: Tue, 12 Nov 2024 07:52:22 GMT  
		Size: 922.9 KB (922863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08130652092aba372eddf6b7072489c816f258e7a3d4ef1f30ae1f7a2fd32f7`  
		Last Modified: Tue, 12 Nov 2024 08:04:34 GMT  
		Size: 10.3 MB (10308588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe94ea9ba8c236cf4f30c94fa67d1f6adac491130d57c80232abd0c8b2ab7bb`  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349fa30bc60461e5844e106bdd91ffdfa3ee3dc78aa3598cbd13880d645ae6f4`  
		Last Modified: Tue, 12 Nov 2024 08:04:33 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:1b6d00aec070ff75bbf3ef37e68808469a3eae71bac803adde578af4b90c9735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 KB (486317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27f6fe646624cf26ddfe488df6b007883471d7000330e7154563334cd3c2a6d`

```dockerfile
```

-	Layers:
	-	`sha256:e802861598fb8adbf11c5f00bd5c32ceac2e79729364e3977fc4bd58274b513b`  
		Last Modified: Tue, 12 Nov 2024 08:04:33 GMT  
		Size: 452.4 KB (452433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee9af28308076e4a52577089fea280ca12f3d9cad9223c3e1a9aa35d3eba7d7`  
		Last Modified: Tue, 12 Nov 2024 08:04:33 GMT  
		Size: 33.9 KB (33884 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; riscv64

```console
$ docker pull redis@sha256:c027e716a934041f1551f5a3766d2a1623f81fc80fd78023757d2c386b0cf880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13825215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46dc852a0200f44cfd0097a7158972f9d7a74dce5a0a9606145982e0c1dd3ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162e3a47891a1cb322e2cc2af8038b3793c836818127d28e2c51c906207335a5`  
		Last Modified: Wed, 13 Nov 2024 00:43:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086357163ceb61db3609ab3a6280de52d5c96ab1d4e843c406e1f6948ed1cafd`  
		Last Modified: Wed, 13 Nov 2024 00:43:28 GMT  
		Size: 171.3 KB (171297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8052e1d8b36606844ede29c0efc948d25ad243783a71e13ef1eafd7afff15d8`  
		Last Modified: Wed, 13 Nov 2024 00:43:28 GMT  
		Size: 974.6 KB (974585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7350cc33604e9b58a3ca5bd197489292c2992db7ebb027a32be68a82895a86`  
		Last Modified: Wed, 13 Nov 2024 01:21:03 GMT  
		Size: 9.3 MB (9306178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd168119ac9f51cd05689cb0e10692c758b8c3b03475df313599c43f32407a31`  
		Last Modified: Wed, 13 Nov 2024 01:21:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482db81a713632b60c9914879873c85fe6a6f62cf822ea0d7f73bf20c508dba3`  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:3283189658b18d17f1431afe64fd32e219693c4de0590093e5a58a98b3af6ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 KB (486312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa4775f1d56db1c0f7b7796d961a51af2065cdd66b5644032cc0505dea27521`

```dockerfile
```

-	Layers:
	-	`sha256:aa7d4c53f1038ce0e09bf65e873ac217b3d0cfa213fb6e5ad2b4786781fa310a`  
		Last Modified: Wed, 13 Nov 2024 01:21:02 GMT  
		Size: 452.4 KB (452429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b41c3643c23b65ee3c55be2da63ef669649bd7e51d9662fcbf3fc8b5a510329`  
		Last Modified: Wed, 13 Nov 2024 01:21:02 GMT  
		Size: 33.9 KB (33883 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:6584b72b090e49408fc0fa986ad10b50d5a99ce83f022ad08a9e4d7fd0f6fa60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14610433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1fd4899e9665dbfc0022402733af878f2857e071daef889812b97de8d6fb7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d022266aa8547569a2e2483001490aee9d881ef23ce2c0bb566d9516bb51a30b`  
		Last Modified: Tue, 12 Nov 2024 08:28:23 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e3c28aa7d600ac2c53d1290b5aabb4403c457668592f45879287ae9f192d47`  
		Last Modified: Tue, 12 Nov 2024 08:28:24 GMT  
		Size: 171.3 KB (171296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022551696fb76c9c9ee0c4393029ec5ed823309810350ba508b3346d55b91b8e`  
		Last Modified: Tue, 12 Nov 2024 08:28:24 GMT  
		Size: 969.3 KB (969251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcdf60e39de051102eb463f0a19074f79105e39061bafa2df311993186b8f6b`  
		Last Modified: Tue, 12 Nov 2024 08:39:35 GMT  
		Size: 10.0 MB (10006606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e483863c0b951842c8a41f11cbf79b689a64f9e06ad480e317ad7a1a873c9d2`  
		Last Modified: Tue, 12 Nov 2024 08:39:35 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809c539220a89b41c37000107b7ea74fef384ecabcf3342d49377ab513f1e46b`  
		Last Modified: Tue, 12 Nov 2024 08:39:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:f88793c9823fa793234586496aaf77f02d2627630b0bf80e0b00d5982e101c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.2 KB (486210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bd47417a70c26250d765d14758e36ad97b91c22ebac8aff6fc9e50860dc1bd`

```dockerfile
```

-	Layers:
	-	`sha256:d6482e7ad09d1d4d1ac5ffa4534fddb465f7b8f8fcd97b30a6603eb16510059b`  
		Last Modified: Tue, 12 Nov 2024 08:39:34 GMT  
		Size: 452.4 KB (452387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353e559ecf1de09a02bff239e721f673be3d19fddddade9f0fce3069dde2338c`  
		Last Modified: Tue, 12 Nov 2024 08:39:34 GMT  
		Size: 33.8 KB (33823 bytes)  
		MIME: application/vnd.in-toto+json
