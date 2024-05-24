## `redis:6-alpine`

```console
$ docker pull redis@sha256:029ccef14795fb59bb8d8dcd6d40f1cfd0636dd5ebf7b2d289db4842c78fc746
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `redis:6-alpine` - linux; amd64

```console
$ docker pull redis@sha256:98e528a0da430ecaf3cac788453214e1160c5f926f50ffd40724c129c3c6ec40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12372622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0b666ef9eb249e61edd4e2ec434a328e98117079727c5e7cf6dc9a00d7a94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205036f487725e3b6bc595a08c187ddca5752de1c40e6becf41539937021b617`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e87f9f54a092cc332430e4bd16a6728fb03f5b0c3bdcbb9ec1b35608d713ca`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 178.1 KB (178136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cc1d49cd6cef8c24f1a6c3d773d7be04bda58590503760c73a55bf9978b48e`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 1.0 MB (1002880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a601d45fb8eac2ecce4239a6629efe02ef11591bec7f4556baca3472e839f`  
		Last Modified: Fri, 24 May 2024 00:55:25 GMT  
		Size: 7.6 MB (7567845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406579fbc90b640e633b62e164a1a03deccb8d924b84121812ff6d9ea04a5d56`  
		Last Modified: Fri, 24 May 2024 00:55:25 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2c855c8f42a66190ff97ba2a5b996fecf6a0296204a3309be0bdc6c851bb12`  
		Last Modified: Fri, 24 May 2024 00:55:25 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:c84b29b985001660d22d8ca4b1fa7c91b6d722ab8cdeb9d963cdeab16e70cba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.9 KB (483916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20635a56bd4a837b5c8f557b1ea74137e6cb6cdaa07bef40d246902f2836615c`

```dockerfile
```

-	Layers:
	-	`sha256:558939008ba825ddade8274e29fc37ba6ce668f878912eb4fea5f8f3d40694a9`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 450.2 KB (450220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfcf5fe13f8526aff9183e46f45f248401ba2b2ca45291140df593139423de5`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 33.7 KB (33696 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:a6cda5b68a90c193274f8865be0bcdaaea2b2e8234028cbcc5b8bdfa9190e92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13858644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0080bde656348d79d2d276ddc9ddf09343365485c94d106a575c6cd4072f63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 May 2024 21:55:46 GMT
VOLUME [/data]
# Fri, 17 May 2024 21:55:46 GMT
WORKDIR /data
# Fri, 17 May 2024 21:55:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 21:55:46 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 May 2024 21:55:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a4b0a01970352d337c0eddaa9b5696b13253841963d6405e3694c076547859`  
		Last Modified: Fri, 17 May 2024 22:56:35 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20064aa4589f68a1825d19a2f9d7e020da568003321d738e4cdd402cc091dae9`  
		Last Modified: Fri, 17 May 2024 22:56:35 GMT  
		Size: 343.1 KB (343090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a304a6fa6a6cecebc4a27a2d2e80757166ccb67fdade0cc1f990e8148d81f5`  
		Last Modified: Fri, 17 May 2024 22:56:35 GMT  
		Size: 981.7 KB (981678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b8146009df80198dce2ab0b81c63a9e250705470eaa213c43cae6822c8b4d`  
		Last Modified: Fri, 17 May 2024 22:58:18 GMT  
		Size: 9.4 MB (9366534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c638ef08a6fce0c9ef261efa65906bd9ad373177a0e46e28757e11628b79941`  
		Last Modified: Fri, 17 May 2024 22:58:18 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34212377985935cfbc9823f4d253b80ab6bfa11bc84680ae6e4ba1aa7ffb947`  
		Last Modified: Fri, 17 May 2024 22:58:18 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4be3d1568ed515d08c60e81e733af8c2209e4590be68aee6451f2d8b3c5dd6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acdc23a6a23b433672fdbed73084405cde34b04c2f2cc2784a3360c15dc86dd`

```dockerfile
```

-	Layers:
	-	`sha256:6a30ffa76160b37a45ef11784af3b47d89d67ae9b4dafa7b9222a200cc858a23`  
		Last Modified: Fri, 17 May 2024 22:58:18 GMT  
		Size: 34.6 KB (34574 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:fa6276a80c5fe86ca3695f2f5f945ffb0ef49c3bf8918f974c9c74c2a7e27b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13377794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d237003a649c029b983c1330b7ff5339f19f90758387403309f865b1a29bb70f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 May 2024 21:55:46 GMT
VOLUME [/data]
# Fri, 17 May 2024 21:55:46 GMT
WORKDIR /data
# Fri, 17 May 2024 21:55:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 21:55:46 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 May 2024 21:55:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb73dfa04a35760b4f48f062be2f8da70acc67c230d0672c9b165c98aab76ee`  
		Last Modified: Fri, 17 May 2024 23:01:16 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8760d2301a34cbd7ddba83e58e8345948464fa23226efdb3a435a3f53edb7694`  
		Last Modified: Fri, 17 May 2024 23:01:16 GMT  
		Size: 343.1 KB (343111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca019b3b4c373f859616be984f0d533df1db3be9ac36a4ee862c4169c5ecbcf`  
		Last Modified: Fri, 17 May 2024 23:01:16 GMT  
		Size: 981.7 KB (981700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8015098e7e044bbf387c519755d25873da8a4774782150c6b02d70d2d9722c04`  
		Last Modified: Fri, 17 May 2024 23:03:07 GMT  
		Size: 9.1 MB (9132142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c1cd25851887a08a9b614714a2cd9fd1d38ccd13ba45badd53eda4403964bc`  
		Last Modified: Fri, 17 May 2024 23:03:03 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a992ba228d2fae0195de8c59e742e1baa09080c3a9ebc58850798a6242f125`  
		Last Modified: Fri, 17 May 2024 23:03:03 GMT  
		Size: 565.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:2c45db5f7cff76c56accdeaaf978cd2a9691a255a9482dd5a46e151bb26de154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.5 KB (866471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3190c722ab770493d55df3c597920b4c3685e5bb96db1c36344b2a0f94d5d6f6`

```dockerfile
```

-	Layers:
	-	`sha256:047d0969f370f4b941146fd59f7d85b5c63d748228c361a35540caa40b0e4b1d`  
		Last Modified: Fri, 17 May 2024 23:03:03 GMT  
		Size: 831.7 KB (831678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9255abbe80eb8b193e9098ab3c84196feec269923c87cd496327fa856530d4`  
		Last Modified: Fri, 17 May 2024 23:03:02 GMT  
		Size: 34.8 KB (34793 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b5c7218efcb3f22eeb1a8eca0f3d9d69a8e61c45bda0bba26286ad64c557d886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14260772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e5a15d331c9c599b37d1539a4d5b10beac27b071c5fd383123b60fd6aa7ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 May 2024 21:55:46 GMT
VOLUME [/data]
# Fri, 17 May 2024 21:55:46 GMT
WORKDIR /data
# Fri, 17 May 2024 21:55:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 21:55:46 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 May 2024 21:55:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d95c83bebf859be16e63985d06bcc6d719327255d9bc299d99b249e2c437b4`  
		Last Modified: Fri, 17 May 2024 23:18:44 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d2517194f97a48485d82b084fec2cc1c69c406ec4f955a46c08620ab253b7`  
		Last Modified: Fri, 17 May 2024 23:18:44 GMT  
		Size: 343.1 KB (343134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df855f10a8a24d8786e6379fbcae108408ed90fbe8233bdcf7cdb5baa4ebde7`  
		Last Modified: Fri, 17 May 2024 23:18:44 GMT  
		Size: 944.7 KB (944661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff16adf59b01bb64b7d1cf1561f04bca631def976befa4718e38af47e00483f3`  
		Last Modified: Fri, 17 May 2024 23:20:30 GMT  
		Size: 9.6 MB (9623318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044309a138ac1b675c56eb72105eaaaecbd348ef94784f5d4fe3d10cac54c227`  
		Last Modified: Fri, 17 May 2024 23:20:29 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7144867ec8c0e4f5d72678d98eb0fa8c7f1d368240835edf2a5c431d3743f2cd`  
		Last Modified: Fri, 17 May 2024 23:20:29 GMT  
		Size: 565.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:165a6adf8f328436cf5651aed799e5af40dd1656989547910abdb92bf14380e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.7 KB (863731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d458806c0441d3a018f40db724a84d315561bad4aa8ab5e1508241385b697c2d`

```dockerfile
```

-	Layers:
	-	`sha256:03d77325250761c0944247778fc1483fbed17ae2df8076dbd69d2f33601f3c6b`  
		Last Modified: Fri, 17 May 2024 23:20:29 GMT  
		Size: 829.1 KB (829063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead418ae159e2ebdd242ba91987cf70a2234acb3c299ca7cd8f2424b9374321c`  
		Last Modified: Fri, 17 May 2024 23:20:29 GMT  
		Size: 34.7 KB (34668 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; 386

```console
$ docker pull redis@sha256:354000670cce088186612a3ea2cd6eadc3e28b6a21b01a34cdf036d1de0c91b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf783ebd37d844c77eb3234304c0264a0343b0808fb1c92197e677d73284b4a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
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
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
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
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7307e5ee6d153bcea7505ae1648280b7b816c7ef8b2157da3bfaf6ae014ce5`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0d8ae77c682eebd3a6386fa4533d34ac7456c4c7d733a6088b726f1166f57e`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 178.1 KB (178149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b91c188e766a14c6dfc09d8de7905093b688b6aba73db81aea32b674b04d3f`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 978.6 KB (978570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15cee6a3caa59e86ddcb52c883f11032d1ec5414f71a9245a4d4bd8d1e695e`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 7.3 MB (7317926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8812dc57eb57b51f30cca68893b2e53543800529b3d45f05edec3351641d601a`  
		Last Modified: Fri, 24 May 2024 00:55:25 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2a97f8749112627a416cef5a4030186ffff6ae1a2404911e04437e34aa4982`  
		Last Modified: Fri, 24 May 2024 00:55:25 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:69934d982b0ed7efdeb7c93a0dd4dbd28f78ae1278988c36c3d6fbe6139fe915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.8 KB (483829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9c423e801a5f6e312722ad1de094ba2700cff2504f2efca8990530878bb6fd`

```dockerfile
```

-	Layers:
	-	`sha256:e0ccc7b2c3101d198699fc951496afe1b04e93e5e75625be7a8bb5d0a7c7e11b`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 450.2 KB (450185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fe26ae9eab5fb608792ebfa72648f42db5eda0801ea71720be61f4a6f71db7`  
		Last Modified: Fri, 24 May 2024 00:55:24 GMT  
		Size: 33.6 KB (33644 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:ece62909f0ab90e6557191ded16460b6a8119fc4439c3cc077ace63d2cd3a06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14742147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7259aff9d4300ee543e9c6923402dc05477ef0bc056c2102d17654347087112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV GOSU_VERSION=1.17
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 17 May 2024 21:55:46 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 17 May 2024 21:55:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 17 May 2024 21:55:46 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 17 May 2024 21:55:46 GMT
VOLUME [/data]
# Fri, 17 May 2024 21:55:46 GMT
WORKDIR /data
# Fri, 17 May 2024 21:55:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 May 2024 21:55:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 May 2024 21:55:46 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 17 May 2024 21:55:46 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5fa700c7deb276f5a55746cb828c2473dc096d5659eb75fd22f1623efaf952`  
		Last Modified: Fri, 17 May 2024 23:04:41 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ffbe9a8b4be8c5bd4d2c868d7eb8ca39577340257f5abc807ed86730e833e6`  
		Last Modified: Fri, 17 May 2024 23:04:41 GMT  
		Size: 343.1 KB (343130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba93c60fd86efe8732bf5521a21415c691990df019c50b27088a818d94151e4`  
		Last Modified: Fri, 17 May 2024 23:04:41 GMT  
		Size: 935.0 KB (934984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12fa2210c384fb02d79c074969ac0757d40b3ac2b71de8d2977f91db000731`  
		Last Modified: Fri, 17 May 2024 23:23:56 GMT  
		Size: 10.1 MB (10103732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0d5445d00a5e8f3021ca7cf0a9176ce6a275fa14e239c1bc62628ce2d2ea96`  
		Last Modified: Fri, 17 May 2024 23:23:55 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c634b71b33e67f74cf71996e762aa6d039c920fb2e4144b004b972951730c`  
		Last Modified: Fri, 17 May 2024 23:23:55 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:c6e189fff3c27fc5d5a57f4963290c2175d20d98049abfd784721fe557ee1809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.9 KB (861857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6bacbcdf828801beed1ddc18312ab22251eb4500720b9c15a321b480a7fb426`

```dockerfile
```

-	Layers:
	-	`sha256:6d65d98416c578dd40c4256f0e9dc546cf41d7c21753e7db9b19be3c969bf546`  
		Last Modified: Fri, 17 May 2024 23:23:56 GMT  
		Size: 827.1 KB (827140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc573732741aeb0bb3f0447d5ab48de664e2086c5b210238f05c4667d1ecf025`  
		Last Modified: Fri, 17 May 2024 23:23:55 GMT  
		Size: 34.7 KB (34717 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:b89d45f9199060d452c2cde54dab279054f4fb68caa9e48c5fe80fac825accb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12581069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc90607cbd08c13f961d7b8a93fccf6f0a36889441e1968e75d761e583fafb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26f42952284b89f1d3022f34c77a727dcbd35b3881451f766756948f3167fc7`  
		Last Modified: Fri, 24 May 2024 02:09:56 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64db0a7b431d5aa1a2582ce9bb427a97b76a402ea42cee07fba42185c809b15f`  
		Last Modified: Fri, 24 May 2024 02:09:57 GMT  
		Size: 178.2 KB (178159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98509ad6d0975da44f97a375950d638186bfa297b192cdf81a7234c207f052a8`  
		Last Modified: Fri, 24 May 2024 02:09:56 GMT  
		Size: 969.6 KB (969619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4881b2f87867f8b26c52e15eed4a12de0f115530c90ab0e22ece900b6ecd675`  
		Last Modified: Fri, 24 May 2024 02:14:31 GMT  
		Size: 8.0 MB (7971287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f33d095961cdcf34a9f8c2f1d4bab48527127e6d9395a68abe7de2fd9813e`  
		Last Modified: Fri, 24 May 2024 02:14:31 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4302b5cdcb64eb58f9e3689d6d690dee9a00ab34e018d822babfc7d7012babb3`  
		Last Modified: Fri, 24 May 2024 02:14:30 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0bdde18d3ef3a63ad5f8af0527c3ff3a4190e4ec530a4699fd4ee6eef7820130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.8 KB (481788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c011d333448b0d6f17bf218b454f93f2005c87c6b0f6497e316a5f40d938f83b`

```dockerfile
```

-	Layers:
	-	`sha256:753f437d04dbac0468eb930a48f273ae0dbcef576145d45ee9209c3d65f6f089`  
		Last Modified: Fri, 24 May 2024 02:14:30 GMT  
		Size: 448.3 KB (448266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c899d078adbecafc1fc86e788d0f399e8453de84ddb9220a1b5ff9cdcea1a74`  
		Last Modified: Fri, 24 May 2024 02:14:30 GMT  
		Size: 33.5 KB (33522 bytes)  
		MIME: application/vnd.in-toto+json
