## `redis:7-alpine3.21`

```console
$ docker pull redis@sha256:86c23b252bbdaa1a867e0e360480de1aaea96e6ab3b1e69743c626c07a2a0c17
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
$ docker pull redis@sha256:fc0099e9af31874b5520788cf428630f72d82fa44cb775dcbebb382d803b8175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17211622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c6eca9018f674072c229789ae825797b97d5c4c389ef15314636341582a63e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c2fa01aa3f1460add318eb8efcb7d4443cc4acc6ebf56f243aab18fd877f33`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d715f8cdcda609f617f6790ad185a638950305d1c42773971f830409cae74659`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 171.7 KB (171720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18abdcc1fc4932c6132e8b1ff89ac44928b0d5a0b14209b1c619c7f6a3582e15`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 1.0 MB (1002988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0023bf2abd011193b993f417b0a715ac576df07d5a79cc2786a122f3979fea`  
		Last Modified: Wed, 08 Jan 2025 03:46:52 GMT  
		Size: 12.4 MB (12399027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7e31ff3ce8c33166fff70a3d8c463864f32995167ef87cafd2388ea5b3b8cb`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa08008717425c073515633efae091c33c3f537791d8864e2ac7a9653a5cff`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:49ee2f8ed49d325444c71eaf154c3c95d64f987cb51a055024c84ae19e378c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 KB (494411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96edc1d8f076e5e554812d0e8353638a2ed5133f819cc86f5bf43d57e3a338f`

```dockerfile
```

-	Layers:
	-	`sha256:344aafc88037d5063199badf0027f51c97bde6bfd28027e6416441cca2dbe94b`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 460.0 KB (459992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd1cfed6b627157dc6d2a605f68b8e6c61fa04f898ab7d71fdf9eac9e036e83`  
		Last Modified: Tue, 07 Jan 2025 03:16:48 GMT  
		Size: 34.4 KB (34419 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:99bde665030822d0d6414b27b0c6bda5b8230ef2b50ebc146209fcb0d3ed4850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17070857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5610fb582a2a24158ce0f836492fe2b254a0edd787ee62950ba10ee4eec10c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0145b28ff4d6e700b507efb76af92ab2fc38289fd754ad18326ca840b6178ab1`  
		Last Modified: Tue, 07 Jan 2025 06:39:58 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d5ac43c233c18cf168c990308f77eba07d935c77385647c62dea26ccbc4715`  
		Last Modified: Tue, 07 Jan 2025 06:39:58 GMT  
		Size: 171.7 KB (171725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0872edb9d31a44bb053d847dd5aef6b05db6a3f37948d3b4dd479d2ba7c386c`  
		Last Modified: Tue, 07 Jan 2025 06:39:59 GMT  
		Size: 971.2 KB (971227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4a6737423c2dfaffa6e1f42cf1a077969c61849fdf93ac6e93bbde86aed97`  
		Last Modified: Tue, 07 Jan 2025 06:39:59 GMT  
		Size: 12.6 MB (12565203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb76d62301c6e52e51a994604ac12f961de59700524c52e6e8a0d814590ff2b`  
		Last Modified: Tue, 07 Jan 2025 06:39:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e263e14eca295e0724fa6e23d8f4cd72378c769efc6643923d6408115c21c98b`  
		Last Modified: Tue, 07 Jan 2025 06:39:59 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:eeede9910647a7a851989025620d3148444ac22aa4393e13e9586018dc28ceb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bd2feba498dfd406705fc15a80519a3110a99b883be2211ff38403c6fb1705`

```dockerfile
```

-	Layers:
	-	`sha256:86463d4b47ff56e10c1e00d94e7c2e25c629c87c4ba65e239dd2ed6785527af9`  
		Last Modified: Tue, 07 Jan 2025 06:39:58 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:b0bfc10f58845770d9e5aa089d74e358aefbe80b96bf3a1100c11821d9b038f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16660745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715b11c5ff98fbeb4530f213bace63d48c4c605e6956ec56adad96e8e72fed74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3435b3ffd16955729296e04a8946eba0594f99dd1c152c6470ad5393c8c1d0`  
		Last Modified: Tue, 07 Jan 2025 06:16:35 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566c0ecc54398a021d28d2ea8c35d06570ee03c93020fd9310d345ac23903fbe`  
		Last Modified: Tue, 07 Jan 2025 06:16:35 GMT  
		Size: 171.7 KB (171748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f62649c18901937021afb2b8ae6c67109480d849b46cdc0b90119840cfd1325`  
		Last Modified: Tue, 07 Jan 2025 06:16:36 GMT  
		Size: 971.2 KB (971228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cc7291bfa6a6790160a9502928ae788b1b5894e1d672cb4e84d15a0433376`  
		Last Modified: Tue, 07 Jan 2025 06:16:36 GMT  
		Size: 12.4 MB (12422857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f000175f92aeac57964cf63acbd6ed41f3c7c73addaf56ebfdb7f4553c960d`  
		Last Modified: Tue, 07 Jan 2025 06:16:36 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ae007d38972eff5fae574d365173a56a3cc948549155bc32137ce5785f2d2`  
		Last Modified: Tue, 07 Jan 2025 06:16:36 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:8ae56b7c74be46fde2d31b2b3bdb62e7cc4a1fe785c1a4944bbc3de5e1b258e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.4 KB (497448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a1559eb5682b5a59f9f69ede01efd2ad59959e81b0c5134efca6cb70436dae`

```dockerfile
```

-	Layers:
	-	`sha256:5d24680d9f490f32d28fb6d139fb2248a6c796ccf85da7f8a47b0341a2de5ce5`  
		Last Modified: Tue, 07 Jan 2025 06:16:35 GMT  
		Size: 462.9 KB (462873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c83b982b43afb2c56f0923e5d30dccacf1a46c392f24e9294f753a55f73ac17`  
		Last Modified: Tue, 07 Jan 2025 06:16:35 GMT  
		Size: 34.6 KB (34575 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:6b4529e6b015e8b8c2d1e490716e60a60b7bba6104dca072d0f0be12314bd7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17652356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bbfa28ff69f7a059ba155b8c58475c8c31180d926cabc89ec9c596b8471321`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b3665ba479eb4838170acd620d1c9ddecc77f4b75e931ed3ead4b016384801`  
		Last Modified: Tue, 07 Jan 2025 07:06:43 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41645f532390f0d37899fb1047adf2583b55a8af54b6733646bfe47c441addc3`  
		Last Modified: Tue, 07 Jan 2025 07:06:43 GMT  
		Size: 171.7 KB (171738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b373e6b75f402083871f030fca998490db8768edd8bc71d34dea49971e37f234`  
		Last Modified: Tue, 07 Jan 2025 07:06:43 GMT  
		Size: 934.7 KB (934693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe4e327428083ff28f635e4a8d252829abd687983be12b7a250fe24cf135c6e`  
		Last Modified: Tue, 07 Jan 2025 07:06:44 GMT  
		Size: 12.6 MB (12561255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ea990bce782daee0e7426ce3839c14ca02f5b2714d04b2356519e2c2f2f281`  
		Last Modified: Wed, 08 Jan 2025 02:52:59 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e495b92fa400b0a370f7981919d9044a3bc672cc43f7b9e8d1eafef33bf679`  
		Last Modified: Tue, 07 Jan 2025 07:06:44 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:fb9f61833586309f302bb14fd332f09aab1cf8e9495f2cd96b18cc044b187cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.7 KB (494722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bf2c7240983825d99f5a869e3d6c37c9b2ef4030211781ec7b5dfb7fe102ea`

```dockerfile
```

-	Layers:
	-	`sha256:6823055cc9d5c017ddf4a63945b09ac1a54b39544dc62250fccd891a73d7cf47`  
		Last Modified: Tue, 07 Jan 2025 07:06:43 GMT  
		Size: 460.1 KB (460096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17dd17282d0671d8f7db63518cdca4b9fdc73f1971c937034cbb6834e97426a2`  
		Last Modified: Tue, 07 Jan 2025 07:06:43 GMT  
		Size: 34.6 KB (34626 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:3fd4ca93f58bb5591f5636a2a8f59f9de8f885833a9d4e0055c0619f0ebfa487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16659209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be468ef765e119850da32d2e49935d4132df6015c4469bb94927ec88161f0930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Wed, 08 Jan 2025 03:05:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e18913d655ac9a2e7e46cda55eb0e58cb05a094de4ed009e0c2bea49883584`  
		Last Modified: Tue, 07 Jan 2025 03:16:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771049662e30b7dd04a32bbfe5dff5cfc8218f99351430d02b70181ca4e3f882`  
		Last Modified: Tue, 07 Jan 2025 03:16:22 GMT  
		Size: 171.7 KB (171732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84e52a349ea08d1d5b2fee8120d0128c7ba042f7f41271944b6f9f7d2397f2`  
		Last Modified: Tue, 07 Jan 2025 03:16:22 GMT  
		Size: 978.7 KB (978719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2f467dd1be634fc6b594c80612b54ab4e0a1919265f21e033bd4d79992d9a`  
		Last Modified: Tue, 07 Jan 2025 03:16:22 GMT  
		Size: 12.0 MB (12048827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4968d0ab160a1cc827386c1105a66294c835865fe18facaacfba3ee4c3666cd`  
		Last Modified: Tue, 07 Jan 2025 03:16:22 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c28da901bcfd498f7bac2689a322bac6bedd302561cda7e704bb29707f0905d`  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:a4c0f7267fe1da3ebe7c8dc148c0789873bc6c9b1a659995a1749fac3d9c432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.3 KB (494302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2b7655cf38c5af737c789cfa6b4050269b73dd9f0c1e7805536991ca2f360c`

```dockerfile
```

-	Layers:
	-	`sha256:da735dfec7b9416ba17899521d850ea71dd84266a09362d4dee2fbfc28ce9a85`  
		Size: 459.9 KB (459947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c26288fb9b2e3c76b61d123f174e7f90e81cb5353ad1cdfc09eb982c85f311`  
		Last Modified: Tue, 07 Jan 2025 03:16:22 GMT  
		Size: 34.4 KB (34355 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:5b56e2687e37b681af79e6804678b2e6cbcc1645e802b75811bfc924533047bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18005907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67505bcf47426dbaf3d1193aa25b97227fc1397760e88f2952e4bd697e74df5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7edf40e5adb5bbf7171910b0f4c5644d737806d790cf626ff0e71fb4d2bad5`  
		Last Modified: Tue, 07 Jan 2025 06:09:36 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d5ccdbdcbd596e1df6a58936caf46b7a886ecb2b52888df99480493bf2416a`  
		Size: 171.8 KB (171751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189c3f1a89c5e275dc128ca36f98c20a1880eba4547647736af1179da2ed8bad`  
		Last Modified: Tue, 07 Jan 2025 06:09:37 GMT  
		Size: 923.0 KB (922962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab651793599d4e0067718555961ed7b20262e59c73df6395f321f82dc8fb9b72`  
		Last Modified: Tue, 07 Jan 2025 06:09:38 GMT  
		Size: 13.3 MB (13341780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b138e7ae29cfd703d1a21d2b14479b3bcc3175a43898c2bf0e58ef266e67b94`  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2548a76371446b72c2ea66bac0277c8065545bf419201ab289f28c2003b026a6`  
		Last Modified: Tue, 07 Jan 2025 06:09:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:4d7a8527f22c8da07802fec963a13efed0c29cbc3bff1792f2ae298b8e610d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98044df4125cde6fa1a9b78eba5a64d4bd87a9e0493b400c41bc9bfa51e0330e`

```dockerfile
```

-	Layers:
	-	`sha256:375fd54632c7607c6c1205bf3d4c7dead8a0a9ba7954ed46a4701f533ef8803d`  
		Last Modified: Tue, 07 Jan 2025 06:09:37 GMT  
		Size: 458.1 KB (458099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e002fb7ec1265286d8c5df0e85a993832660025786a6666951488d359a7424c3`  
		Last Modified: Tue, 07 Jan 2025 06:09:36 GMT  
		Size: 34.5 KB (34491 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:76ff7ba5f7d79da23d752b149c94d24a44cc809f4b87dc3abd5f835ebd044401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16462225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48322f3b4e7c340ca73d49f47a1c0684c49a7f9b195fb8284c0130a92a837b22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620a48aed48bcee03cacbc4a1ec8aed3e31297a31811a25a369e1a38883c96dd`  
		Last Modified: Mon, 06 Jan 2025 17:43:09 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df55e05d20ab6ae4c5bf63be9ff5ccfdb04c777d231b18b82baa1d4b308f9d10`  
		Last Modified: Mon, 06 Jan 2025 17:43:09 GMT  
		Size: 171.7 KB (171716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cb753bd85e6fdbc0d0798a90a9bcb3d11192b8571a4ea30680cd3a5ee09896`  
		Size: 975.0 KB (975022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703c13422b5cc76a3851e18835cac2e003be7d50b7eb8562518afbeda5e9319`  
		Size: 12.0 MB (11959792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53feac84757b8fdc19669867cb790b83c2e18ec04363a4d04b5c02e5c6973c66`  
		Last Modified: Mon, 06 Jan 2025 17:43:10 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ab6ef8ac52abbc3b885ccbcd986a6b04ad2130b73eb38d0d51690ad5dece2`  
		Last Modified: Mon, 06 Jan 2025 17:43:11 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:1ff48b2da7f18367859191e9baffdda1f9d2eadebdffc580c872abf305389e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7965c430c6432b1cdbdf899c8212703305464bae8c04117e90914050cec5dc62`

```dockerfile
```

-	Layers:
	-	`sha256:2e92c65d241e782425a93baf0594773f3024ccfee346105030f746f2aeddd1e6`  
		Last Modified: Mon, 06 Jan 2025 17:43:09 GMT  
		Size: 458.1 KB (458095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06974a207334d856f61eef69badb42b8f369d4391c01389446855215abf560bb`  
		Last Modified: Mon, 06 Jan 2025 17:43:09 GMT  
		Size: 34.5 KB (34487 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:76e861db78c9ef8b5e6afc7be6ef97ccbd9b9445aa3ff11f9c3c73e9229760c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17574406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583949cc5f84e4e080c2d38ec1e144818e12424fdf1d407783c8791d43c492dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168f4c26aef0ea573263e209255e29475e8d710b58328e8f2f1b3bdc8f014b89`  
		Last Modified: Tue, 07 Jan 2025 06:14:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802019cf05c589205a26ed030fd85cc5ced340370621a8ecb360a271e71f1f73`  
		Last Modified: Tue, 07 Jan 2025 06:14:33 GMT  
		Size: 171.7 KB (171714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fc2aa02740a85d0b4befa4470fdfeb8202eaf3f0df42bd4acbdf67d673494b`  
		Last Modified: Tue, 07 Jan 2025 06:14:33 GMT  
		Size: 969.7 KB (969734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24a2f34a23733952e59c7e6954962fa7356dcf1980f97ec694ffe99eb8f1433`  
		Last Modified: Tue, 07 Jan 2025 06:14:33 GMT  
		Size: 13.0 MB (12971844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398ad3ae4a28defcd6aae301bf22b76bcfdb2c061ab8609c7346dacb3d6edda9`  
		Last Modified: Tue, 07 Jan 2025 06:14:33 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeebcf5dd3927f71872a9a21ffdf99007bb0f185c83b1fd40d371f6c976c82b`  
		Last Modified: Tue, 07 Jan 2025 06:14:33 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:d0c17944825baf069f56eccba51caa02594a1bbc7ba23305c8139ed12b73bc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 KB (492456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4b1968cceea42fe55f5fdedec27df1085c4e7ebc3beaaacda98ffac4685411`

```dockerfile
```

-	Layers:
	-	`sha256:f193a2a993f5f1790f5ee100a324e02fa4d0f535042c9fd24ff045bf45f18203`  
		Last Modified: Tue, 07 Jan 2025 06:14:32 GMT  
		Size: 458.0 KB (458041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d02eda8224e3e8d42ae3d42a680f026d8778a3ce680d5c86687641056dbfa7`  
		Last Modified: Tue, 07 Jan 2025 06:14:32 GMT  
		Size: 34.4 KB (34415 bytes)  
		MIME: application/vnd.in-toto+json
