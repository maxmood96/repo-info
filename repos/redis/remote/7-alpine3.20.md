## `redis:7-alpine3.20`

```console
$ docker pull redis@sha256:c9a84aa6b7de7188a6f329be38cd5371232185467d9ffb38187d5a1debe3d86d
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

### `redis:7-alpine3.20` - linux; amd64

```console
$ docker pull redis@sha256:c516894338a5330979fdaa939f0cca770031d79a43dc0d6553748430130525ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d06252fad43690f61cbb858628b933fd85f048aaba4c05e577274b2c77cd7cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1711cdd203fbd8c501cc6081a8be31400c4cf3a2ad767f53301436a412d546`  
		Last Modified: Fri, 06 Sep 2024 23:24:03 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db14da7d7e3caf6f24d3914e8229cf44ce7b599445abc1ac0bb966675b2da6`  
		Last Modified: Fri, 06 Sep 2024 23:24:03 GMT  
		Size: 171.2 KB (171249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bd8946cf047a3d372e4136bac8c51f58f7b16510ecd0055daf648947b8ac03`  
		Last Modified: Fri, 06 Sep 2024 23:24:03 GMT  
		Size: 1.0 MB (1002658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6faf94f7383dc1f176091695212d1f827c3bab2b7dd766040f07dcf047a7358`  
		Last Modified: Fri, 06 Sep 2024 23:24:04 GMT  
		Size: 12.3 MB (12347166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a6f4d557ce2d24f7b326b31b1397eca32b0dd7d7c09fc8683f408bbe769c72`  
		Last Modified: Fri, 06 Sep 2024 23:24:04 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b67933c677ef5d6977690af48a5973eb1baef961082062810b351ead418aafc`  
		Last Modified: Fri, 06 Sep 2024 23:24:04 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:30dfb23ab8b1ce36233d1476f4cc52ba18ae286f6915cbb2ca300fd767f03e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 KB (488828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed30c0bafa53993dc4f48fb9653d9fe2b0c7fec8fa369cebd78d3e51455623a9`

```dockerfile
```

-	Layers:
	-	`sha256:9bedfd3492b85bceb88cab30faecc2af4acb913f29023ded6582ea762da5faa4`  
		Last Modified: Fri, 06 Sep 2024 23:24:03 GMT  
		Size: 454.6 KB (454617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570f6c632ad355dc3c2a17f4b69e130ea0e7d524bc56862df71281dc5e413d89`  
		Last Modified: Fri, 06 Sep 2024 23:24:03 GMT  
		Size: 34.2 KB (34211 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; arm variant v6

```console
$ docker pull redis@sha256:abdb535141a8c726b403f97ada5d02de47e484b77054128c5d522a3f6a1b2c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17117400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4885bb7ddae5e5dd4e5b0c7348d5e751c2e8a76fd7d45c8ddc90c525964ffdf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
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
	-	`sha256:09901396dde8fa1a69f312b9f2f67dcf129802b98609901db4cf2c2354ad5ea8`  
		Last Modified: Sat, 07 Sep 2024 12:15:34 GMT  
		Size: 12.6 MB (12607338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553d509bf425a4c34983d844296c7e80ab4b3c10bdeb244a5129c640c124b395`  
		Last Modified: Sat, 07 Sep 2024 12:15:34 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddfcf4b7ef36601f2ff75ee76ab92444262c91862b14de298c4a49e1735e29`  
		Last Modified: Sat, 07 Sep 2024 12:15:35 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:ebcb5fbb918fa9a09f5f8c344150cffd86423fcb2fe21a0cf28df3c9d3a20b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612509b4aa54f5b6bc64a05395285963eeaafc1d75f46843f3b744f496bb89b8`

```dockerfile
```

-	Layers:
	-	`sha256:9f0a996d51d1630e510e1511a51f0b51e34e5bd15e840adf105f381795b115d4`  
		Last Modified: Sat, 07 Sep 2024 12:15:33 GMT  
		Size: 34.1 KB (34141 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; arm variant v7

```console
$ docker pull redis@sha256:a09bb116fcbe209f200e9b5f3d0993129c38b5f115dee347ede34736582cec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16709832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9c45215ab98a02d5a25b5299f751d444b35cb7dcc4d4765694f0d2f2cd1c0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105a9d088dadf33d409cd9cf3f63786491329b41a701c0b780074d49dafd2c59`  
		Last Modified: Wed, 24 Jul 2024 13:16:56 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520b938dfbd5098fe610c3dd5f7a5f6f8bd9e06a88fd8ee8b69920d60924ece8`  
		Last Modified: Wed, 24 Jul 2024 13:16:56 GMT  
		Size: 178.2 KB (178159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef19d6d03ad65a522515418a2322bed3bf361a22fda0bbe8da00771ee3d8f4e`  
		Last Modified: Wed, 24 Jul 2024 13:16:57 GMT  
		Size: 971.1 KB (971067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a76d463fbf31f667a959c47660aff8d98097b4c7223a4a9b3c0da6651872b8`  
		Last Modified: Mon, 29 Jul 2024 23:57:11 GMT  
		Size: 12.5 MB (12463977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55da19dbce2ac2d715a0aadb06ac7ecbf8e9b83d116b6ddcf454d813e896ac7`  
		Last Modified: Mon, 29 Jul 2024 23:57:10 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eafdc1cbf595be1455a86ee3b4d94510fc9ec06705b9df8b4d2b2beb07f2bf`  
		Last Modified: Mon, 29 Jul 2024 23:57:10 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:47279d4fbad53b9416db495c9512c892cc0295bc259df66f4891d0dc848b36a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.8 KB (490822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d6d6cb1b8851f724eae2a29d250c69fbd38a94a76e6f27900c4a9aab78405f`

```dockerfile
```

-	Layers:
	-	`sha256:9bcea73ffda3fefdd8734c78fa0c8c09cce6385c97a425a47af63e160cfa846c`  
		Last Modified: Mon, 29 Jul 2024 23:57:10 GMT  
		Size: 456.5 KB (456462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2837d11f0f07a32dfd4024cdff510d6afa603909166ef221b8e9d4f92f80589`  
		Last Modified: Mon, 29 Jul 2024 23:57:10 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b7b10e22a82307ec3992e740fd6db023217414c16fafa43950b61edf6e719983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17707056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff9c3b883720d24f983001c2aa6b9647fec71b797df9ba81dee61bb104e4988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4aa6b3a9bb8df9cae76ef5e47ed209d6d242a79984587a064b84b0aada2d968`  
		Last Modified: Sat, 07 Sep 2024 11:31:45 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1672cbd8c2ef195dc728ccb8453d995a8a57b65566789dbabd897f83268c658`  
		Last Modified: Sat, 07 Sep 2024 11:31:46 GMT  
		Size: 171.3 KB (171262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf32e71a5b370d405c53281696f4c8ae7f766be18b92bc08c3b284b3a139922`  
		Last Modified: Sat, 07 Sep 2024 11:31:46 GMT  
		Size: 934.5 KB (934504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0559fd465cac3f9fd1d61eae217ac12914270d7c23de2c0dc318047476700f44`  
		Last Modified: Sat, 07 Sep 2024 11:31:46 GMT  
		Size: 12.5 MB (12511974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3093473339467cc486fe168b3bf26b2f9b375d683b99185b227ad54cf9b49bd`  
		Last Modified: Sat, 07 Sep 2024 11:31:46 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c10c79ca33dca7e355b09c9f6a5512e3584c08578ff5ef18d4975d794ea588d`  
		Last Modified: Sat, 07 Sep 2024 11:31:46 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:18b752e3511886dc19aad0d3c85cdbea1abf6e7b24391960873aeb77b6f2ec8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 KB (489275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fdaac7987a5e7a47b00ad2b58ca2895e21e095f637d814ed75dc633391297b`

```dockerfile
```

-	Layers:
	-	`sha256:597eaa0b4166cf204676d15a93aa45b7cd0c2948a430412fad65992f032079f0`  
		Last Modified: Sat, 07 Sep 2024 11:31:45 GMT  
		Size: 454.7 KB (454721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28035af44c363091aa75ffbc271c7e348e7ad0d6d1b9624c6efb1e1ea50496b`  
		Last Modified: Sat, 07 Sep 2024 11:31:45 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; 386

```console
$ docker pull redis@sha256:a9e2b9043217ff63f41ef3cc286ef0548fc585ba8d533720b46be1ae8e4ca7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16608591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975094eed5fbc0eb6286c75420069a526438f94aac3e893e6b24e13abd4e35bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5b7198d2664dee1aedd0d85ed182421446e50105bf47b8be62f07973521ba5`  
		Last Modified: Fri, 06 Sep 2024 23:23:28 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223f8e4193540405960397a11b8dfacb76f6ceb7cb11d5214402b04046b277e3`  
		Last Modified: Fri, 06 Sep 2024 23:24:01 GMT  
		Size: 171.2 KB (171233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52668ea53e6faef5b87e71014c4584359024f48096d9672abd424543a24f8c61`  
		Last Modified: Fri, 06 Sep 2024 23:24:01 GMT  
		Size: 978.1 KB (978118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8b222cf92756424a8fc4818cceebd1d844ff53886b262706d2353a70f23bb`  
		Last Modified: Fri, 06 Sep 2024 23:24:02 GMT  
		Size: 12.0 MB (11988410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb521bed06621e6e592ac41303bf059a4a2c21eec6d754e7e8c763d734d2df1`  
		Last Modified: Fri, 06 Sep 2024 23:24:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1106bae8ab700379b2ea137a4588011ceeed394e42f8be3994a20b1b6aac42eb`  
		Last Modified: Fri, 06 Sep 2024 23:24:02 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:c4fe25ea9586e23477c6de986834eb8acae37e77d551a8cf35467af3bc31c7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 KB (487634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953c8dc63fd009fede77f586a63a01debd9d5a3b1c035fa5057a0fea60b886b8`

```dockerfile
```

-	Layers:
	-	`sha256:2417e5e082323e38c4ae69e2dfdddb60abc2f0566509b9b5bfebb9abc530d8bd`  
		Last Modified: Fri, 06 Sep 2024 23:24:01 GMT  
		Size: 453.5 KB (453485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:580b190a69ada4263c3615a2f2088eca4e9ec9f1884c311f16460611793460c6`  
		Last Modified: Fri, 06 Sep 2024 23:24:01 GMT  
		Size: 34.1 KB (34149 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; ppc64le

```console
$ docker pull redis@sha256:009d6d8042b55736d9e3200efec24169548c981eaff34dde6970a16df8d12b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17983889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbac5ca48706acae4eaae3e0fcd80856487e5735403d13216612bd470ff006cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129d333f0a2993916c5612db3f7805fdab8c17c823950d1c0b93cc08ee8cdbb1`  
		Last Modified: Sat, 07 Sep 2024 11:25:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8ca5bc869c7f37e57c927a3683df9287a75be0b4dadb32aa8820b38ded79b1`  
		Last Modified: Sat, 07 Sep 2024 11:25:13 GMT  
		Size: 171.3 KB (171258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ceea4b902dbee92f1a3b554a5df49dd2d540cce2adbfade93211a194a85163`  
		Last Modified: Sat, 07 Sep 2024 11:25:14 GMT  
		Size: 922.9 KB (922860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73908b5bda9bce11f2744ad9700d659708cf5774e100f71e1633f54022e0d464`  
		Last Modified: Sat, 07 Sep 2024 11:25:14 GMT  
		Size: 13.3 MB (13315681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25577f5d4dab05c70e11b49d58cb7fa34f50815907d3a9efded4cc0cfd75d22`  
		Last Modified: Sat, 07 Sep 2024 11:25:14 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c534ab1d90d4cb618cc532ec2d8a80beae2673252291ca86a4f6eedca113a88`  
		Last Modified: Sat, 07 Sep 2024 11:25:15 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:a3b65c86050b12e5f359f06b5df86690fba754b2ffe02dc8b3cd2bee41643064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 KB (486996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dc10751f4d6dbabcc9692d188d4045dde1170e981218adef1a76ff32b171da`

```dockerfile
```

-	Layers:
	-	`sha256:a325ba8083ed8e6ec4a5d4d3fa6f5f28414a089b0731e960837338a097a8dd8a`  
		Last Modified: Sat, 07 Sep 2024 11:25:14 GMT  
		Size: 452.7 KB (452721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a98231ea8d1efb0fb47b91e48178dd38653822e637bf19db64bd4be33d114c88`  
		Last Modified: Sat, 07 Sep 2024 11:25:13 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; riscv64

```console
$ docker pull redis@sha256:3b165c0ff9868ee174e59feed6f3032811b7940805a656b6e2e4a5eb179de6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16461184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c49eab4dca5c6e68c01a96c5a91509e91291cec3d21de5b2293b157b031cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c2a01a76e1aa5d5065801610b4125a612681504a0535da112f941110d9cc2d`  
		Last Modified: Tue, 30 Jul 2024 00:09:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7bb0ff329046e062b87e6258f9cee14d199fe68bbdd1c254558d0675b3c0b2`  
		Last Modified: Tue, 30 Jul 2024 00:09:30 GMT  
		Size: 178.2 KB (178166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08940e0958963cb6fa6ed91b8d0f0695be5d681889ff5ae6835fb1565077ead7`  
		Last Modified: Tue, 30 Jul 2024 00:09:30 GMT  
		Size: 974.9 KB (974923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ab48ae27ef778d0c202227450be1e8f95402c4ee5be2563e14b27fbf6f41e`  
		Last Modified: Tue, 30 Jul 2024 00:09:32 GMT  
		Size: 11.9 MB (11935751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91942269588e4315abb9acfcdf329839eea1db24da4e7c37dad7a33aff9dc42`  
		Last Modified: Tue, 30 Jul 2024 00:09:30 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6b4d40585951e29b7cd279c989bf8a327f002893d697ddccf0a9709830c74a`  
		Last Modified: Tue, 30 Jul 2024 00:09:31 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:442046ddd6ac15b48d8ea39d863c1429cb28ecbdc8e4c16f865134560cd8edd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 KB (486993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2863c22d074433211abe864781884ccf1bb7d67cedb919b142cbb8ce7899f72f`

```dockerfile
```

-	Layers:
	-	`sha256:667620b7f7c193348dbf47af2bbe6c03d6fc5100ada65ef1bcc2cd3e98eec149`  
		Last Modified: Tue, 30 Jul 2024 00:09:30 GMT  
		Size: 452.7 KB (452717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d227e978788ddb8f6c1d09c61b613b45f9979af2c839f826a9e856d4263a57b`  
		Last Modified: Tue, 30 Jul 2024 00:09:29 GMT  
		Size: 34.3 KB (34276 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.20` - linux; s390x

```console
$ docker pull redis@sha256:348ed88b81c30ef20b7ba9feb3109fd2f4b22c652f7cd75d594ebc3e6ce803b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17542801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8d437de352511a8e8c07ce220fe41ed2ede8f260cbf63f98b172e36f06a679`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4a92990a25859ab465c25c337cbfc407e975b8041d60f99966a9ef3af3bc1`  
		Last Modified: Sat, 07 Sep 2024 10:29:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c429ee5e123518663143104ad8dcaafdac39fc54c9773eba6546476be1d570f0`  
		Last Modified: Sat, 07 Sep 2024 10:29:57 GMT  
		Size: 171.3 KB (171272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e19d58e5ef6c6b2190bd9d013a84aa576bf85f3bd1967bd6da21b3069a9832d`  
		Last Modified: Sat, 07 Sep 2024 10:29:57 GMT  
		Size: 969.2 KB (969248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bfc2a67b5cb882bd943df485a5783ae7ed68fc741f944de327da05bdf7fd9e`  
		Last Modified: Sat, 07 Sep 2024 10:29:58 GMT  
		Size: 12.9 MB (12939011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5368199b5970f5da7460b08c3b98abfb872c863bb2bcbb7f9497c9226e60bb68`  
		Last Modified: Sat, 07 Sep 2024 10:29:58 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a853652e3c8aef469635ff5a52fe6671bf9e2ce145651ad901a5255d216d020d`  
		Last Modified: Sat, 07 Sep 2024 10:29:58 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:0c14d065cddfb41ba19b5f615dbe59d30c6b07c41e978c63769356d357cea9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 KB (486869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b75d6e8e97dc8dfabdab74666062c0f9175f0eb3414202a2d6010bb8b4c1580`

```dockerfile
```

-	Layers:
	-	`sha256:f4fc0856e6ca64a2a83c52cafab9c7bca9188d6e5b2e3c13d9a1e3d76ad1b392`  
		Last Modified: Sat, 07 Sep 2024 10:29:57 GMT  
		Size: 452.7 KB (452663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16841ea6bb83176c8a612ce915aa988293e09b491b4201421dcc878340a41911`  
		Last Modified: Sat, 07 Sep 2024 10:29:57 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json
