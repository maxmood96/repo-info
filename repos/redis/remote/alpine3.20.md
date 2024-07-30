## `redis:alpine3.20`

```console
$ docker pull redis@sha256:69face9064f95854d0956673e8617297a3ab4f08100b3c23ab2f7540d05a75a1
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

### `redis:alpine3.20` - linux; amd64

```console
$ docker pull redis@sha256:f469de9fde6334a365b5203cd7adcda733b6a1c5ab4a274640bd560122d0e740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16780149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ed3031282dd6ae5bc80c7168d7290e79a11871f29fd059b38aed8807d8e7ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b829e07e5656de9ac9f9fcf760668bc0caa2fa872ec9816367a52213cfc39749`  
		Last Modified: Mon, 22 Jul 2024 23:05:34 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a7e970d1540ff3a6c9a02d280760b00b531e7c4f4e39edafea9b68677f5a9`  
		Last Modified: Mon, 22 Jul 2024 23:05:34 GMT  
		Size: 178.1 KB (178146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f8b69d3d2a62a6d5af01e20d090fea576290bfc67014f4fdc3813e73ed1ad`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 1.0 MB (1002883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6302448af5c9e34d7237887155dde63beb717e8089a94dbefeb12252d3984362`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 12.0 MB (11974558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f4f36e8a5acc5e8094c148d73cde1fbdbc2e455e280e3a98fbfc547fde1cb`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2170ed175fee6f2bbb88f1ce893fb302b7ed48bdc6e9fc7df8343672a848b5f`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:e8f7ce3bcefbe2c43baf247956b53456d381d2f9f9af64b33e8157bc3bec613b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.8 KB (488828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5038dcfc932bedb994b574422135ee3525f7b1116bc5b3200bbb413d8fb60e72`

```dockerfile
```

-	Layers:
	-	`sha256:3286406df6a9186bf3dd8f5b1777874a0aa3632e7ff995e439c69b007ad866fa`  
		Last Modified: Mon, 22 Jul 2024 23:05:35 GMT  
		Size: 454.6 KB (454617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ff9ed3e72d93eac74755f160cb50bc6495f293e10efc188f62abca65aa237`  
		Last Modified: Mon, 22 Jul 2024 23:05:34 GMT  
		Size: 34.2 KB (34211 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; arm variant v6

```console
$ docker pull redis@sha256:97b0e9ee74f5d53c8172ac542780cf5cccc5ad89053e3e44dfa8e2bf2b92e2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17123650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b764b788fc56b204e837fa11ede98b79820fdf2549ed769027d0d66ff01a2f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
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
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975494c1ca87f24a33ea0f81f1d9fe24798ab23934cf81f9a31a6ea4ae8ba723`  
		Last Modified: Mon, 29 Jul 2024 23:55:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff179908a6d10240b24daf5273ecab13f10669d6c86cb900bca191aab56881ed`  
		Last Modified: Mon, 29 Jul 2024 23:55:55 GMT  
		Size: 178.2 KB (178157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28229a302880a1cd688535aa60e2c08e00dc35ea6d03d49a143894edda9c6eb6`  
		Last Modified: Mon, 29 Jul 2024 23:55:56 GMT  
		Size: 971.1 KB (971055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b977e62dd5a3e48d6bd99bf78bfbffaa9c1a171208895bf96357af40d6c61701`  
		Last Modified: Mon, 29 Jul 2024 23:55:56 GMT  
		Size: 12.6 MB (12607579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6b296c93b09d88c61101e79c4d2acc3510750d0d6fcae1a26dd18827b4524c`  
		Last Modified: Mon, 29 Jul 2024 23:55:56 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ddb341e18ffd73cc6b8c382760e1a8e895c16823e217615e168a9430816425`  
		Last Modified: Mon, 29 Jul 2024 23:55:57 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:0cbc5db705da0dcdb1ef117d9748fbdf50c46baae79f64cdc653b8815196fafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df5c13c61aeac8e5b5a6ecaa537519e044e1e5ec84226c50870298b5e2430c8`

```dockerfile
```

-	Layers:
	-	`sha256:189eed89f750359c5fc75ec45c739c200dc603578dffc380cc95c8d90ee8cd6e`  
		Last Modified: Mon, 29 Jul 2024 23:55:56 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; arm variant v7

```console
$ docker pull redis@sha256:98e4711c4bd6c62c1f7b85837288edc91e67b0a799341ccaf6a7ee5fff870e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16269093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee869d87ff499bb7bd62c07c1bf34d8079077536efbdd00f6fa2ce3d7aa3fe15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
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
	-	`sha256:b653cc4d614722aa9e85839379fa58ae6cb2313621e4f64f5d617e05e446bad1`  
		Last Modified: Wed, 24 Jul 2024 13:19:15 GMT  
		Size: 12.0 MB (12023236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb058ef26e554ac5162363297c7c6432a7b0ba7052b1d35979a0d95f93103b9`  
		Last Modified: Wed, 24 Jul 2024 13:19:15 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f390bd4882ba498132cb044c9093a828b47d13da71039abdab770fdbd2b6efb9`  
		Last Modified: Wed, 24 Jul 2024 13:19:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:fbd9a7aeb8208fddf29f86345389346df5a2772f2c4875cfae238f7bd3eff369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.8 KB (490819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297196a77cd2b2e20bb34dd2b1bdedb9922414a4d33cb9eb2365aeffdcd4614`

```dockerfile
```

-	Layers:
	-	`sha256:61c5c245090be792c9123d2069b0c18048e280ff836adc8df6fc35cb85a7186c`  
		Last Modified: Wed, 24 Jul 2024 13:19:15 GMT  
		Size: 456.5 KB (456462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18d672b00938fdc3f2f0c86d2199756e51d15cd94cc5c671ac5421ac78a2446`  
		Last Modified: Wed, 24 Jul 2024 13:19:15 GMT  
		Size: 34.4 KB (34357 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:874b47d3fcc61c98a52d40d773860b9c387b4ce7a76e9a6e76f139b243c422a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17341769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed518de838a3d33f791651f5b7228a9a2e2214fc3c7a41abd757480649d18f0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e8b557c6d8c70b004b36c072908263be3f2aeebc24683d1b5fba7afc3e0f1`  
		Last Modified: Wed, 24 Jul 2024 07:08:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34dd9b0f2dd1dd16bdfe298ec92566414db71f9352501b080d8ddb02ffb3c3`  
		Last Modified: Wed, 24 Jul 2024 07:08:34 GMT  
		Size: 178.2 KB (178162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694450d3f4e9c13bd83f2e14a3785b1e457fe44e15036c3212447b86ea81be9f`  
		Last Modified: Wed, 24 Jul 2024 07:08:35 GMT  
		Size: 934.6 KB (934586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8ce8df6887a31cde96acf35ae3a2e7492d4d84aff245462ce92477b7bae1d6`  
		Last Modified: Wed, 24 Jul 2024 07:10:36 GMT  
		Size: 12.1 MB (12140417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6411b5598363abd4301355a6627a1551f829a171ed54d71e5b5ecde9cb94c`  
		Last Modified: Wed, 24 Jul 2024 07:10:35 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6bb5cf35179080902997125b72ca796381148213250d387dfb61f6c75c9f1`  
		Last Modified: Wed, 24 Jul 2024 07:10:35 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:7be9d33018bbec2d7a6b85c9b94d00541894540609fd049f4f5fb34200bef5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.3 KB (489275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc6c2c70da328b5013e2fafc9a675941c6ab5bac815d8e9183fc47e22442fe1`

```dockerfile
```

-	Layers:
	-	`sha256:5bf242725eb7f1fb221b1fa5f6e9c48188438e321e2d186951ac78d8b2141909`  
		Last Modified: Wed, 24 Jul 2024 07:10:35 GMT  
		Size: 454.7 KB (454721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3952ae47fdf56cc9904c1c61a69105b349698bab972df4f5b625e069cf70cb`  
		Last Modified: Wed, 24 Jul 2024 07:10:35 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; 386

```console
$ docker pull redis@sha256:6b09cae347d470165e17da457d626bb4c0e5fb4bfbbf1c263e6cf16e7bb8ee51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16280186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3277ecdf680e64a0df7e276f8efd5136da01104a89ee6e8025d46072615eee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205ff19aa6cb04d7a8ec74f4cb704b5899c15c52927995841078f6f666311eb8`  
		Last Modified: Mon, 22 Jul 2024 22:08:54 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe9f2f7f68e9419f80219b560d916ee6b57f005fc8ec4be38cb95a2cc48f924`  
		Last Modified: Mon, 22 Jul 2024 22:08:54 GMT  
		Size: 178.1 KB (178149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8923582b8a6abc9d9f844c92d3fa658a9c738edb84f64ed70e241e9bee2a4c53`  
		Last Modified: Mon, 22 Jul 2024 22:08:54 GMT  
		Size: 978.6 KB (978586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9c99ba2dd5caac0b1c9aa6d76857d58809f7bacfa6c133c2b1a3c088009cf`  
		Last Modified: Mon, 22 Jul 2024 22:08:55 GMT  
		Size: 11.7 MB (11653714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd88464a779de7df8bcaec94b83b07df49a8763eeb481b8ed500b7c4fe1a361b`  
		Last Modified: Mon, 22 Jul 2024 22:08:55 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ddb1cc0f3ca4092efdd12c31c21730eddf50965b2f48136d0b3cd9347bde43`  
		Last Modified: Mon, 22 Jul 2024 22:08:55 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:75dbf6d44b88241009cdbd0efb30a7ab44f5ec1770fc5e169b382c32960b31b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 KB (487634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598410a5e2d718b5e159450e4d9f5fc0f4312ddd335807aee0063ad389f2b69f`

```dockerfile
```

-	Layers:
	-	`sha256:3e62854f215daf9393134994d5bbe80f997406cc3ed41330944aa574afc18305`  
		Last Modified: Mon, 22 Jul 2024 22:08:54 GMT  
		Size: 453.5 KB (453485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffaec5dc2cd02870aa573eabccf795cea5ceb8f64890d77996cad608de8c35a`  
		Last Modified: Mon, 22 Jul 2024 22:08:54 GMT  
		Size: 34.1 KB (34149 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; ppc64le

```console
$ docker pull redis@sha256:80a8cadabf73bd82ec0c2f3492d41834e0cc4ff8a121df03d4726738c5c22eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17540847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7690c1ab2209a8a077910b10b8a851f25d1357e19e302524e6437884b74639a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094b442562f66fb8585af6a476e618c9c3b8fc5a01b950fe140ab4548f23c4ca`  
		Last Modified: Wed, 24 Jul 2024 10:16:13 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a9365b4f1f5a12df882df1322cc6c359a51d376c31691f89f4e6814570cb7`  
		Last Modified: Wed, 24 Jul 2024 10:16:13 GMT  
		Size: 178.2 KB (178164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf15f924ab310d6c4af475ca193e718758c67005862fb6e95d75aff2ce427a`  
		Last Modified: Wed, 24 Jul 2024 10:16:13 GMT  
		Size: 922.9 KB (922898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa63b476dc1a309255627b43d73c409ca6def5a726706826340dd8ea33fb440`  
		Last Modified: Wed, 24 Jul 2024 10:19:07 GMT  
		Size: 12.9 MB (12866552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228d95ceb744c5c2888871bf7df742d984d3874057796565f8d701f4ef803f70`  
		Last Modified: Wed, 24 Jul 2024 10:19:07 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe364ff8ccae7cc464db6cddaac4ece6a1c0530df878660f9c70bdf6c1e2f01`  
		Last Modified: Wed, 24 Jul 2024 10:19:07 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:e0f611e92ac6f8c0280df9447c9379ba2282808fbe5dd8925be82660c04a5a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 KB (486997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80943bec9bb1a7adbc0d4c6c56445e700697aa4aaa4614e2eff8a3c5f5ba5525`

```dockerfile
```

-	Layers:
	-	`sha256:9b65eb39807699e41adf5d39f6af30a8d3b6d363b493170504770d63d4d61f41`  
		Last Modified: Wed, 24 Jul 2024 10:19:07 GMT  
		Size: 452.7 KB (452721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e39173b4012416edee33c134aef268f3b548820cae8f7ebd3cef19c49aec572`  
		Last Modified: Wed, 24 Jul 2024 10:19:06 GMT  
		Size: 34.3 KB (34276 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.20` - linux; riscv64

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

### `redis:alpine3.20` - unknown; unknown

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

### `redis:alpine3.20` - linux; s390x

```console
$ docker pull redis@sha256:e0717003a46d64866f4e5dfd37080aefcfadc654832790e8c8d37bf5e2796657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17143295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd568212e46059c65ea6cab55c9d1c2685ecdbb0b47a70ad6185a33fe0290b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=7.2.5
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 22 May 2024 23:17:59 GMT
VOLUME [/data]
# Wed, 22 May 2024 23:17:59 GMT
WORKDIR /data
# Wed, 22 May 2024 23:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:17:59 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 22 May 2024 23:17:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81383681d24682c147b84494fdae555080932a1013d1e5e2c53db08239d77b00`  
		Last Modified: Wed, 24 Jul 2024 08:49:01 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0a912ebbea43a75b260de506cfe4a42009155ee2b3fc0b9854cb88d91e967`  
		Last Modified: Wed, 24 Jul 2024 08:49:01 GMT  
		Size: 178.2 KB (178165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667da4c03ae0d11f14c5d93b780ec6fc343a581a55bf9d211a067b39307aff6c`  
		Last Modified: Wed, 24 Jul 2024 08:49:01 GMT  
		Size: 969.6 KB (969640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b8393f1f7f982d79abd3ef159d62c640c7998bee98d1c236fcb4a475abe83`  
		Last Modified: Wed, 24 Jul 2024 08:53:18 GMT  
		Size: 12.5 MB (12532753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d04b0f9c28a0cf0ddf1e6506d213037c78437e4fb9a3713b9d0a0f43d3249`  
		Last Modified: Wed, 24 Jul 2024 08:53:18 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef9174121fca8b1e20bd69efaaf316daa95de72da1f09ecacb6a3cff9615cc`  
		Last Modified: Wed, 24 Jul 2024 08:53:18 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.20` - unknown; unknown

```console
$ docker pull redis@sha256:60598eab6bc6663759ada264e47b61614c4aec9d1b7d1829497eca97ea0c3746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 KB (486869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c4d53903209dfad8eb1708631ac034d8b2d25af55a2d63eadafc2b3353a07`

```dockerfile
```

-	Layers:
	-	`sha256:d2e3eebf83a2081ea0623579048ae60c88a319b67860d484038bf24588338df4`  
		Last Modified: Wed, 24 Jul 2024 08:53:18 GMT  
		Size: 452.7 KB (452663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccd16fbd572e9a480b8b05140cb39e5fae854e5361a9c8d9e39d4fa72100bc6`  
		Last Modified: Wed, 24 Jul 2024 08:53:17 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json
