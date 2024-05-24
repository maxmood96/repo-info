## `redis:alpine`

```console
$ docker pull redis@sha256:a21f7b14380b046297e24c19490b5ea38a3d13eb5f8228f4d60ff6ef7232bf95
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

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:f3f71a5da1c19fcc960eb556d9c30b5afe67b951d2f5fcdc789788f1fc307032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16779376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f597a450f4646ec002b71036f8f6ecb18d61876b0e9df37004939f19b26f0ed1`
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03b02e01fda776798e965f59ceb1357c65a8fd39f20ff0d8989b8cd2638d103`  
		Last Modified: Fri, 24 May 2024 00:55:43 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8eb84c453519920ebe16ddb731780690540a6bbba234cf7e54e5a59ca2ed6f`  
		Last Modified: Fri, 24 May 2024 00:55:42 GMT  
		Size: 178.1 KB (178146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34468061c329a8ace0552fcf00ed588ee0b154e53b10ae485cdcb42ff055a3`  
		Last Modified: Fri, 24 May 2024 00:55:42 GMT  
		Size: 1.0 MB (1002880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f4ad8ba58b43a3fcdacc8111e5d9375174ec54baff136ac98b30d46243cc3c`  
		Last Modified: Fri, 24 May 2024 00:55:42 GMT  
		Size: 12.0 MB (11974589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3e0605beb65c08576b3e04fc9f573764f66a2749a64fcef1a32120edfffcc5`  
		Last Modified: Fri, 24 May 2024 00:55:43 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44457c91edf58730334c370c65aca2e208742cbf5226699aeecc8bf361e47aa`  
		Last Modified: Fri, 24 May 2024 00:55:43 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:e05a33547c85ce4e2262ba111dd3f88f4d0531385b20e1f1946b1c7c0d0458b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.1 KB (485106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbae0e58a908043eb648bf1d8cb36eb0c221964b917f2aad12c69521867784b`

```dockerfile
```

-	Layers:
	-	`sha256:7afe4542bbab2581eb53c0dc986d828cab3faa57aa8c80fa3731fd507a43985a`  
		Last Modified: Fri, 24 May 2024 00:55:42 GMT  
		Size: 450.8 KB (450814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e34f22f9ff606488f2e4babe541c34efad3ad06bb9c2b741e0a8dc36c7e1f445`  
		Last Modified: Fri, 24 May 2024 00:55:42 GMT  
		Size: 34.3 KB (34292 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:fd35a7b743414f68ffcfe3b357e07e42c404717ea114946629e027ef0915efc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18395558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec93e504c3ee0847b7cfdd6f2139bb62f9415995972b77eb9bf20438772b5e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_VERSION=7.2.5
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.5","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 19 May 2024 09:03:19 GMT
VOLUME [/data]
# Sun, 19 May 2024 09:03:19 GMT
WORKDIR /data
# Sun, 19 May 2024 09:03:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 09:03:19 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 19 May 2024 09:03:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13f4159e6b6a23705139cb6408922c427d57328dd23d8a92e82d6fce36bd9c`  
		Last Modified: Mon, 20 May 2024 17:53:29 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c497fd8a7aabd585578525de298379dc7440523676a1293981ec771019dd3850`  
		Last Modified: Mon, 20 May 2024 17:53:29 GMT  
		Size: 343.1 KB (343103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8655b241998b4587518c978403fc9d44fb9da41f22603bbc9d44d243e41ee51`  
		Last Modified: Mon, 20 May 2024 17:53:29 GMT  
		Size: 981.7 KB (981687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96814d364e7f6d3c9abc8bf8f5ccda0a85a65aa1da981764898840a43dec361b`  
		Last Modified: Mon, 20 May 2024 17:53:30 GMT  
		Size: 13.9 MB (13903428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5d6f263b45d972d3c61badfb4eb78f4f2fe152d4f9b2b0996d216b4e8453cb`  
		Last Modified: Mon, 20 May 2024 17:53:30 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89b8f0f75ff4247a7646b7c179ae39d690c752bd7e611dadeed87579125d34c`  
		Last Modified: Mon, 20 May 2024 17:53:30 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:3438669dcdc3e8cd829bdb9d5dd3a9523cb7197b330ff7ea672e57895e45a644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c04e746d7ba04717ba48cb8d90babbbaadf76a04d718f6eb908cb5ef13268c`

```dockerfile
```

-	Layers:
	-	`sha256:cbb3aa4717d8935e4b9c47becc1ed3b7cf14ff0427e1ac5eafcfe1e50d6d5a30`  
		Last Modified: Mon, 20 May 2024 17:53:29 GMT  
		Size: 35.2 KB (35177 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:f822a56b97dba531f1b3d76547d6b5a004f7109685f4f2ce26481f2da9abb5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17898977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e952de6ee4d7e0cf398bad624d4e7699ad8089992934941e871cd97191c580`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_VERSION=7.2.5
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.5","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 19 May 2024 09:03:19 GMT
VOLUME [/data]
# Sun, 19 May 2024 09:03:19 GMT
WORKDIR /data
# Sun, 19 May 2024 09:03:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 09:03:19 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 19 May 2024 09:03:19 GMT
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
	-	`sha256:5a06735478a07a823e028976c26c70f79c72359fa0e1a7a0f452235579c61a5c`  
		Last Modified: Mon, 20 May 2024 17:57:39 GMT  
		Size: 13.7 MB (13653323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd04ca4aa9e04450188cb9666d56a4f008da70fcc0e27313dd2cc197d1c2303c`  
		Last Modified: Mon, 20 May 2024 17:57:38 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f8a07c3e03cde734e5492701a0ca43084c82a1e47f5a90cd5f218c5c05ca6f`  
		Last Modified: Mon, 20 May 2024 17:57:38 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0e1ebce77e4e29199831ec7eb88390fe0257b936d691db80571db94846043e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.7 KB (866740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9a49470cf841f276b8fe93975ba4580010b758391e87807b8e87c582b4431a`

```dockerfile
```

-	Layers:
	-	`sha256:b11838ea2865319b2afd3581b1864466717859e77c9113409fb7809203a18687`  
		Last Modified: Mon, 20 May 2024 17:57:38 GMT  
		Size: 831.3 KB (831342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35aff390b73e0e2518628074288e98c738634ec09d6b996b9d54a44a6fef8f9d`  
		Last Modified: Mon, 20 May 2024 17:57:38 GMT  
		Size: 35.4 KB (35398 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:aaa756b1b0030abaa667439cd4bc55c2b22c43d927a899a33357092a732815d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef526621d55d7373b63031f881ddcbeed518df6a968337f601024d4f81470d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_VERSION=7.2.5
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.5","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 19 May 2024 09:03:19 GMT
VOLUME [/data]
# Sun, 19 May 2024 09:03:19 GMT
WORKDIR /data
# Sun, 19 May 2024 09:03:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 09:03:19 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 19 May 2024 09:03:19 GMT
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
	-	`sha256:0320506b2e0bee89181b864965f5d17276364d9b30747b887869de5b5ee574d9`  
		Last Modified: Mon, 20 May 2024 18:22:43 GMT  
		Size: 14.1 MB (14106375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fdc861af68ee4140a5260e7fc6cb73974b29ab191987589a0133e83d431fc4`  
		Last Modified: Mon, 20 May 2024 18:22:42 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6fbece4c811dd476de819b6b99c872270a12d2dc22c43a8dd3b7f1633e4345`  
		Last Modified: Mon, 20 May 2024 18:22:42 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:ff5cca7cd24abb2603d211e714d103323234236f5b04f531f34788e5be4d1e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.9 KB (864921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2c1057a082ad6eb63e4768145c051275366abda3b8a860391667af9089e90b`

```dockerfile
```

-	Layers:
	-	`sha256:724f9744e6a12bfe169d6a048a2408aea6147437b120a3d7700c1d466d120e1e`  
		Last Modified: Mon, 20 May 2024 18:22:40 GMT  
		Size: 829.7 KB (829659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e289dd39c081219f3a22512e250737c74af17cab23210e4e0dfe05af0f2d183b`  
		Last Modified: Mon, 20 May 2024 18:22:40 GMT  
		Size: 35.3 KB (35262 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:7ce4f639055cd7a95fb08650691f4b678a9a8ce40270fdd7d60e7d5aa7323756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16279311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a67537773d1529a77251923736277e7b6724f3d5b2d15d3fd33bb7e2f7bf9e`
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
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c81fc90b3a76b9379573f915a813f68aad98113d36f5482c4b206019513b7`  
		Last Modified: Fri, 24 May 2024 00:55:58 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16068903901cb4ddd3a388a4e0b39ae3a552402239afa9faf506292e765472ca`  
		Last Modified: Fri, 24 May 2024 00:55:59 GMT  
		Size: 178.2 KB (178155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ecb0efb663cce658d7d0a46f1dbe111ae7c347fd07842c67e33f231b271a0`  
		Last Modified: Fri, 24 May 2024 00:55:59 GMT  
		Size: 978.6 KB (978574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833b648c1ebf5d89629c6a61a7500a0d875044421dc45477ee72dbd05bd4d01e`  
		Last Modified: Fri, 24 May 2024 00:55:59 GMT  
		Size: 11.7 MB (11653732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae01acf512d3f50636ab4fdd9a2d358f4e8bd0772976a43ef1a8dd736785718e`  
		Last Modified: Fri, 24 May 2024 00:56:00 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67988cf9ecc1efe7cc62281ffd16992d362b3f68de61b931afcca1ba90608f`  
		Last Modified: Fri, 24 May 2024 00:56:00 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4a4434178d6dba965309fe63da8060c3c0e5eaa323a2fca2ee667b6ebaf0251b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.1 KB (484055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca7f44151d30cd6b25ba129b428e8b8a5dc4db6098f5408f2dc58b425cb6a7c`

```dockerfile
```

-	Layers:
	-	`sha256:0ec76b22a86407ab9a7ae7a8e974f8b3b70e2c5af28d186bc8b657535b91c280`  
		Last Modified: Fri, 24 May 2024 00:55:59 GMT  
		Size: 449.8 KB (449825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f8645765e60bbd63cc0befc9bd06ebe9969247f91ec8822bd886460c155e2d`  
		Last Modified: Fri, 24 May 2024 00:55:58 GMT  
		Size: 34.2 KB (34230 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:3f7a6763a319edc281bbb6eaae6e06702697fddaa2521e2143c067d462776c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19448567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d47c932d46774f3f27664ba7d3271041a831f4a24002f9122b4d118a8ed544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_VERSION=7.2.5
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.5.tar.gz
# Sun, 19 May 2024 09:03:19 GMT
ENV REDIS_DOWNLOAD_SHA=5981179706f8391f03be91d951acafaeda91af7fac56beffb2701963103e423d
# Sun, 19 May 2024 09:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.5","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.5?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Sun, 19 May 2024 09:03:19 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 19 May 2024 09:03:19 GMT
VOLUME [/data]
# Sun, 19 May 2024 09:03:19 GMT
WORKDIR /data
# Sun, 19 May 2024 09:03:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 09:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 09:03:19 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 19 May 2024 09:03:19 GMT
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
	-	`sha256:cdad36770623d92696f912598329823a806147e1654225c35893a8ec60526c74`  
		Last Modified: Mon, 20 May 2024 18:15:25 GMT  
		Size: 14.8 MB (14810152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57038f6c1903816ffe1dd3e76986c810c9cd57a8024045c2820068c9bdb375bc`  
		Last Modified: Mon, 20 May 2024 18:15:24 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9955c8f0489bc850b71e79d4e7e54fc9b4bf7d8a3687cf615f0d725227f18`  
		Last Modified: Mon, 20 May 2024 18:15:24 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4fe3b29530ed547798cc93ef20d35eeaf42da5d9159bced76b9bdaadb60db940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.1 KB (863059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9357ba3350ae9b1c6ac7102e4381688f289fa45cad98a2a57600ddcacce675`

```dockerfile
```

-	Layers:
	-	`sha256:f784e16ab78956676c2ba7a16728ae0500d676a8d3cde8dd0f36b46eb5647187`  
		Last Modified: Mon, 20 May 2024 18:15:24 GMT  
		Size: 827.7 KB (827744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5052776a56ce0d28a8cf27bed7c52bc2b019f669f9dabb38d3b3d236f8ab690`  
		Last Modified: Mon, 20 May 2024 18:15:24 GMT  
		Size: 35.3 KB (35315 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:3022d6bde5a9d9da63a413e24b2c93907e4d64b396ab69791ddbad147a9defab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17142563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7d1bdf845f543498181e634e9f7cf2a36223a55261e7eabfc43257126f5bf4`
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
	-	`sha256:5592f86f8dc5bac9aae08011cad3e0fa358382bb245d7c72cdb334a2bbfbd36a`  
		Last Modified: Fri, 24 May 2024 02:09:57 GMT  
		Size: 12.5 MB (12532777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f590fcc27aa8b8680013d7d2154e61a1f22b77018e78616fb21c5db72a277aa9`  
		Last Modified: Fri, 24 May 2024 02:09:57 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d961076165eb61e9a10fa74a44ba438daa7dd9574ca84867b8873963db54290e`  
		Last Modified: Fri, 24 May 2024 02:09:57 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:21e5199760a3befcf46fbda531eeaece4faf31b7dab6df067005b88a6ea4e552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.0 KB (482977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f38deab38e6269393812db2cc5719e679002601de96e178b09cf1ef1cbfd80`

```dockerfile
```

-	Layers:
	-	`sha256:e3d5129a015a80c3c63b78a59e07b0a1a79890452ce9665544df62cb149d7ecc`  
		Last Modified: Fri, 24 May 2024 02:09:56 GMT  
		Size: 448.9 KB (448860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b52da716f09e96b70cba5fd65ed3cd981fc5a04856cb3ad8a59458a39c3a95eb`  
		Last Modified: Fri, 24 May 2024 02:09:56 GMT  
		Size: 34.1 KB (34117 bytes)  
		MIME: application/vnd.in-toto+json
