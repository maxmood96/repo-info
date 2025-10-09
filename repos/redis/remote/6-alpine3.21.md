## `redis:6-alpine3.21`

```console
$ docker pull redis@sha256:3148a32742f80c3b85a988e60d9f5d39d8eccde859bda69960349ef03e1d5160
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
$ docker pull redis@sha256:5e6071fb51f97ba92d40bb67d6aa46751e086d852a4c78df7e6df4e026b70883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12420255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58b74ba639d5fc6b58d6de08ca498a0fbc0aba5721104a216a203cdc8ef1c5b`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:e19c7f987b90ce8ab7d98c3cc57962c953770ee043641f3e16f2fe521b475c69`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec86d8eda96326976964b3aa8f14e3c86b5d9c8b0239d4cd44c933a0d460b34`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 173.2 KB (173201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fb2c5cb2c679a52f5d642f3f324df5f6f2d807f480026ca6c20ffea3282f89`  
		Last Modified: Wed, 08 Oct 2025 22:58:06 GMT  
		Size: 1.0 MB (1003008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9ddbc60e3ec80bcd4566efad43ac6068e594ac0a18077626feb3b3b8df500`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 7.6 MB (7599823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca07f9e0c8578395f4492d5bf8d55437eb029b849833cd097adfc4a662245866`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0392188f011d3e3cf07269a99f3a9e188bad780c35f916dcca988cefe4491719`  
		Last Modified: Wed, 08 Oct 2025 22:58:07 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:0de7140c57f5139ff73d5218c80d3e0d8b5792bb4117f32aa752ca24085a76dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b87836790048b22a4cfde8343ccc10580a3318274f0c0f5afa4cf4ca33a3e6`

```dockerfile
```

-	Layers:
	-	`sha256:151e6b899cf75a3ce4bc5b42a71fce6de25952696efd98485a9e50544feeda49`  
		Last Modified: Thu, 09 Oct 2025 01:04:36 GMT  
		Size: 460.8 KB (460821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8027c735ca2b3e3f7d027257dd599a331ec803b2b76434965e0705a07f295377`  
		Last Modified: Thu, 09 Oct 2025 01:04:37 GMT  
		Size: 33.8 KB (33824 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:00c61f9ee40f82645e88261e7ffcc3ce9e51dff532605ee4f30cd04f10df7a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12146595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30172db55e7525569205d6b8f39be37f86c5fb66d80d22bd46c977d20f1bf6f0`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:aee4b4c1f967f60f5cd310e3f36d81c81cb1fa4bef6fd6b53129573492d05ecc`  
		Last Modified: Wed, 08 Oct 2025 22:18:12 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6d7c15dda646ea2450ffcf0e28fde81b622b4c8f10cdc18295a6b6c2ba07fa`  
		Last Modified: Wed, 08 Oct 2025 22:18:13 GMT  
		Size: 173.2 KB (173230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d706d08cd7f293f106c51a8ea2a3a7b461c2f77d49f7e2b9e02c63e50354634b`  
		Last Modified: Wed, 08 Oct 2025 22:18:12 GMT  
		Size: 971.3 KB (971283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c69281a35a55c442e230414f433f173295d2d5ce8379e98cf451dacec1a69d`  
		Last Modified: Wed, 08 Oct 2025 22:18:13 GMT  
		Size: 7.6 MB (7634956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc4b9e0f27c5987e6a399c3a6e0435e9d7c74732f5fb0850749ee250fd622f`  
		Last Modified: Wed, 08 Oct 2025 22:18:13 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91bee2dd94729ba9dcef003713c8715c64fd5412d86489a710a7abfeee6e088`  
		Last Modified: Wed, 08 Oct 2025 22:18:12 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:04f5b07192477988079a6009f0904b84ae4ddcbac9c00a76be846683912c1558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 KB (33752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470b1ded6a3c9a8d69d37e5eeabd455bffd0d3fe0d8df6b0bffd4c6dec362608`

```dockerfile
```

-	Layers:
	-	`sha256:7e87e42dd1fc30a4e0e401b23ac4594af6b6e9c46a04a6a0c7edf46abe568a08`  
		Last Modified: Thu, 09 Oct 2025 01:04:40 GMT  
		Size: 33.8 KB (33752 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:75a8450924f9921c4bb9644f32c32c663ca8159f54f660b237a50524c680591f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11761929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac192c97dca21f3d83a3e0f5582acfde4fe188dc6136d4e54bac75d14c1ce53`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:70067bc5aa1501f2ffabb3b07e38929b546b795858a6eb42077539289f678a75`  
		Last Modified: Wed, 08 Oct 2025 22:10:24 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9074edc0a628b37ea523def42f4d7def0490a37b4484b9a748b1802109eecfc7`  
		Last Modified: Wed, 08 Oct 2025 22:10:24 GMT  
		Size: 173.2 KB (173234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145fdda09ce378780e438130889ed495354c3f2947174a7bc595e2d9660ecdc`  
		Last Modified: Wed, 08 Oct 2025 22:10:24 GMT  
		Size: 971.3 KB (971272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadfe67a360d6d7be68be917003e5de71727b0e645a17a32064b60018d712ce8`  
		Last Modified: Wed, 08 Oct 2025 22:10:25 GMT  
		Size: 7.5 MB (7517154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02c6d398a232e1e7b159f10d1764ab2ff165f483187efa9f27b01311674cf1d`  
		Last Modified: Wed, 08 Oct 2025 22:10:24 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac522bc827d4fa115e75a5bbbf4b7e6f09b6092f29d8d0c63b7f7d60816c328a`  
		Last Modified: Wed, 08 Oct 2025 22:10:24 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:beb129070cb367a4bed7fa7affb9241be21a7127b9f2e8953cfd911ddd9a456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.8 KB (497830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c251ffe8968edf49a3b06d757b37efd365a6fe0593ba646ad1b034af0e71304c`

```dockerfile
```

-	Layers:
	-	`sha256:3213ccf1dd0a404127a6caf87fa291053222be3622c894a653df22628f12cecc`  
		Last Modified: Thu, 09 Oct 2025 01:04:43 GMT  
		Size: 463.9 KB (463863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d620a6d95af0fb9c84249592f8cc57e0856a27084ce8c61b40558768282f80`  
		Last Modified: Thu, 09 Oct 2025 01:04:44 GMT  
		Size: 34.0 KB (33967 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:0d5c58268231806643c1c0eb3f6e6c44b95d208974ae75653111edff74b01fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12760259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda066b200f73df49eaf78a88a51d0d784956482ddfcc6c1f16e528475b87ee6`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:b1136aae3a7908854e71bef1a2edd647fb78bb7d65fdf005f59eba371a517655`  
		Last Modified: Wed, 08 Oct 2025 22:35:02 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30550e35aae00794066c60832965119ceacc86b80e05a3ab11ed3792dd7b119`  
		Last Modified: Wed, 08 Oct 2025 22:35:02 GMT  
		Size: 173.2 KB (173210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb27f56be75777cf2f2af9b964e037e047c381373b072a62b464da988af097`  
		Last Modified: Wed, 08 Oct 2025 22:35:03 GMT  
		Size: 934.7 KB (934702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fcd14331ccf16ba60a0fb7fcf6731c7e7db416c05c625a97dab08110d080ed`  
		Last Modified: Thu, 09 Oct 2025 01:04:49 GMT  
		Size: 7.7 MB (7658341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd536aaa38170f1b0b867de7a021d79e3838546ed8c3f1be2bde8f9f7ff7460`  
		Last Modified: Wed, 08 Oct 2025 22:35:03 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caec2faa4355937cf5e10c30ab4e2cdc072c4f46f113b558059068ed20bfeb86`  
		Last Modified: Wed, 08 Oct 2025 22:35:02 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:7f6329cecb234eb4867ffd1e10e9c4301117a38e7550a11eb52a1117e239cc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.9 KB (494905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a012d37a0a19720f383df9f046742a1f60d4687e4ba2b62d456730362e89495a`

```dockerfile
```

-	Layers:
	-	`sha256:95504e5640b79215eb2b28a76db134bf361127df6e41ad09694f0ac49a811ca1`  
		Last Modified: Thu, 09 Oct 2025 01:04:47 GMT  
		Size: 460.9 KB (460901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b476070fbaebb00ff995ad1a5a61886cb800201f2047b73277ee3a6f7895e4aa`  
		Last Modified: Thu, 09 Oct 2025 01:04:48 GMT  
		Size: 34.0 KB (34004 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:0e2e853efd5c253bacaa15e7e9f10c467153d53b3d2fab62c5de6bdd60cd38d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11957001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3360ccd19ec4badaf14b950a99e6933f057081744c963ff693ab46bcba71131`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:6a1ced240f2a14eeb06ab3506b60a3e6c71975017b9857de2923c0efe9792c48`  
		Last Modified: Wed, 08 Oct 2025 21:40:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e127da127b402e4a83eb4076edbc44bbe1e28c358f03607b274e2f566cbfb7f9`  
		Last Modified: Wed, 08 Oct 2025 21:40:06 GMT  
		Size: 173.2 KB (173235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c6480df46b5da26a61ba921e38a160d08cfecc351868faadfa8fa489006859`  
		Last Modified: Wed, 08 Oct 2025 21:40:05 GMT  
		Size: 978.8 KB (978783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50102f8131695175913e3d611afc6c8cc5538a0bf71023788c0b21caa6bc8a01`  
		Last Modified: Wed, 08 Oct 2025 21:40:21 GMT  
		Size: 7.3 MB (7338626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c240cf885be5c596a7bb7b2b67644d6250a5314914e36e627cdb84cc9ea2ef`  
		Last Modified: Wed, 08 Oct 2025 21:40:05 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3da8a249fdad2471752f97dc55826662cd2c4eeef083bd7a0ee52e0bc896726`  
		Last Modified: Wed, 08 Oct 2025 21:40:05 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:c9b3f2448b2abfb7564ba7a85158436ddc0f8f004a625b17e2a15d88e9306e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a945d6edbb25c752246f1d748252563daa044a835d5b74e7e9eff17e5674a54`

```dockerfile
```

-	Layers:
	-	`sha256:8c8a85588e345a001df58b0a278930f0d01fe1e506af528f429c7deadf1e5954`  
		Last Modified: Thu, 09 Oct 2025 01:04:51 GMT  
		Size: 460.8 KB (460786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206ba5e3216245774fdc247fa9cfdf116e96e20f8170f6a90ace8f7e8ce52089`  
		Last Modified: Thu, 09 Oct 2025 01:04:52 GMT  
		Size: 33.8 KB (33766 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:214c668b06c75b356f78a9ee721db9ac464538220c2efc19bedf56a96ad9c8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12867022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a196e11144d23b0a078ade7c143bce20156d8ed5686c022ebbeeb3be9ea035fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1092c1077edc4c57be68e09def6f2ce8d9074c368920b39c86e5962a99ae40`  
		Last Modified: Thu, 09 Oct 2025 03:27:14 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1dcddf996961930034a92def9e6e58fa47c92a0827f5e1d290e2c79ca544b6`  
		Last Modified: Thu, 09 Oct 2025 03:41:48 GMT  
		Size: 173.2 KB (173228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb116ef0c01ff97bd298303744fe9b7d814a1839a615bbb24f970d67996572`  
		Last Modified: Thu, 09 Oct 2025 03:41:56 GMT  
		Size: 923.0 KB (922976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2c0de5defcf90816736806b6588b60b4e0a61f52696d62f6062ad33be192c9`  
		Last Modified: Thu, 09 Oct 2025 03:31:06 GMT  
		Size: 8.2 MB (8195085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592decb1e5f8178106a95eabb50746b680b9e4a8217610bbfd54cd197f926377`  
		Last Modified: Thu, 09 Oct 2025 03:31:05 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac043b05825890c7124730710cd0ab388a961d3e66567cbe52d1c8dbb235a019`  
		Last Modified: Thu, 09 Oct 2025 03:31:05 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:722064d8f5c81a70759fd18741fccfcef908c31c21574e48880153167eae5e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9578a4997a51afe672e9c8091d406da3bc5470423b95e5567d7cbf41a896d915`

```dockerfile
```

-	Layers:
	-	`sha256:739c4a91965b663c4b6ebdc8e0e6335937d8e493d818c5f2ead26506b2832795`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 458.9 KB (458916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e99dcc6d813d63efb613884ead51bb8e788cd7733dd72232f5920b169f03ec`  
		Last Modified: Thu, 09 Oct 2025 07:04:30 GMT  
		Size: 33.9 KB (33883 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:2906e2a54aa8805d95f3acf31a4baf80800a4524fa081cbd80ad5448a8123d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13821941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ac382eebb512aba5e31425d52f63333b71a7263eb5943c31cda78a3e438b34`
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:e560e6fe1af72e6bc418d25257f7e1e715d9300a788e8103c4ebb06c4b01196d`  
		Last Modified: Fri, 03 Oct 2025 17:40:02 GMT  
		Size: 9.3 MB (9322924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dced60d08a10c89e3ff3bbc69e681e06031b4ffdaf91604a4c4782f772a7e94`  
		Last Modified: Fri, 03 Oct 2025 17:39:59 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f6f93f4d92a1bb08a8314667bddaf0cfaeb4379c04d30b1d6a6ee6948abadf`  
		Last Modified: Fri, 03 Oct 2025 17:39:59 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:7fc32bdaa36049e03df0e575ff15ba9717a6c5e0ebbca4dc750b2740836a8797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13342cac1d612ed72377605ad1f9865219fe378a0e20625d109378c61b307560`

```dockerfile
```

-	Layers:
	-	`sha256:ebf01c206176b77b492101c8fd185f42200136f6686e4b1224fc37e4db2435ab`  
		Last Modified: Fri, 03 Oct 2025 19:05:36 GMT  
		Size: 458.9 KB (458912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42e9af2ed1e3a4427e9560a7f883c099c17805a9d4b55fdbf5126872e70dee1`  
		Last Modified: Fri, 03 Oct 2025 19:05:36 GMT  
		Size: 33.9 KB (33880 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:66ef8b447a3d5fae05121a9dd50427417bfff12798fad79d0e580277bf883cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12588965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1922da8d4bceb519c4a29a2478f5a536bc198bb73f4ce4f1ac38d12b8aed5940`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
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
ENV REDIS_VERSION=6.2.20
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.20.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=7f8b8a7aed53c445a877adf9e3743cdd323518524170135a58c0702f2dba6ef4
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
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810e45b07495012cccd89aa1bd092feb58b89435999a7ebd87d05d914e2a5e83`  
		Last Modified: Thu, 09 Oct 2025 07:49:05 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113e97cd345efad0f55ae2f05f3b7e7738fa4622bb59cba1d8d76e7d04540db4`  
		Last Modified: Thu, 09 Oct 2025 07:50:24 GMT  
		Size: 173.2 KB (173242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e848b4e662c941265f3b674d311da6d8e9e5bfad6b1ed851ca39f52ce1a11bbd`  
		Last Modified: Thu, 09 Oct 2025 07:50:24 GMT  
		Size: 969.8 KB (969768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa7f701e8a957f27ae8a786d282d6c9fd53c854512093e2e8dea591f9d5a40d`  
		Last Modified: Thu, 09 Oct 2025 07:53:06 GMT  
		Size: 8.0 MB (7977866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745909eddadd2ace64db3af75c9cbe5ea0c6f86815973d6295a09ad81421d139`  
		Last Modified: Thu, 09 Oct 2025 07:53:05 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173e1bc1091ba903c9d7a045e7b381f3a6c0900bee0f40aa4fbcd5fd5293f0ab`  
		Last Modified: Thu, 09 Oct 2025 07:53:05 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:06540514ed4c282630803b0fb7b377205c9b56ab3c71e10334e2f60ba1d6f3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8fd6706eb4fa144dd46ce585d0ee29c990ba3f7c87b7d657e7f35dd6929acb`

```dockerfile
```

-	Layers:
	-	`sha256:994ac0b7a4c538c79eb7269fc40e9e164f3b1208fd7075a6692b9cae95e321d8`  
		Last Modified: Thu, 09 Oct 2025 10:04:36 GMT  
		Size: 458.9 KB (458870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf027753847e6ad8556628bb49de30bbd8a82ad76248f281ff68847bd97890d0`  
		Last Modified: Thu, 09 Oct 2025 10:04:37 GMT  
		Size: 33.8 KB (33816 bytes)  
		MIME: application/vnd.in-toto+json
