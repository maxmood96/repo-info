## `redis:6-alpine`

```console
$ docker pull redis@sha256:974e9d3062b72f59332781aae917b1f49b6a314b7dc7cddeeffb75f4f30df153
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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
$ docker pull redis@sha256:cd67e73ee8d945f3974e2054b0fe6b309a721bf13dbc1e4891afd5007d279f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c412dc298714b5c26feca1330d8f743b48caf0b1feeadfd554d7d446f985a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 04:08:17 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ed65a553abd2114189c43ebe81ea9e3d356b2ab20d20cc972b1edd11716c61`  
		Last Modified: Sat, 27 Jan 2024 00:55:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02229dc2ffa41b81b60c356a65cfb2f6f3ec8c92e4b8ab1fb824db8f907c10`  
		Last Modified: Sat, 27 Jan 2024 00:55:11 GMT  
		Size: 345.4 KB (345355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876d718c369ba014c9cb5ba011dc9e41ff7763be526b049ae76fe996f09393c3`  
		Last Modified: Sat, 27 Jan 2024 00:55:11 GMT  
		Size: 1.0 MB (1015376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7a611aab9afaf1d6db213e44769a24dc3b717a16e26bda25db142969ab74f`  
		Last Modified: Sat, 27 Jan 2024 00:55:11 GMT  
		Size: 7.6 MB (7573253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271aea565ef9cc83783a858563f339dfc61f77bf2ad03f7e00569caeb5c3eacc`  
		Last Modified: Sat, 27 Jan 2024 00:55:11 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99016e57f4857837581e488eec1ca5bc083985a9f60ed513359f92aa40ea2ff`  
		Last Modified: Sat, 27 Jan 2024 00:55:12 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:abd6d6ec995e874ba92c24eb47de79ce865cfe8bc76277c5db8dc227dd2a881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **728.3 KB (728348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d27b44c89f8e7038ae9714d3c6b5f31dcc7966ad0e607d528147066b08871`

```dockerfile
```

-	Layers:
	-	`sha256:229a652a295ec7b4ffa89026ee1d8be17db48d0d828ac7dd962c068ddb183718`  
		Last Modified: Sat, 27 Jan 2024 00:55:10 GMT  
		Size: 693.5 KB (693529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16b39c238278c8537401598d7779a498dde2680edbd7691ac391b4e79622fd7`  
		Last Modified: Sat, 27 Jan 2024 00:55:10 GMT  
		Size: 34.8 KB (34819 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:aa2205e2ae493e6ffac775cfea6bdfc148c22f525f22f8f5076a9eadf6c553a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12113336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed2a95170fce0668ed1f9d3cf46c56bab12009b62da177739398c95617db205`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15513cd9cea097c1921c9f08e8fac00098368ba235b464628834dfc302fb8ae7`  
		Last Modified: Fri, 08 Dec 2023 21:43:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a53b50774dc0da01401e192404fea5dcc1e19182aa7b55ca2e2720e74a9ec4`  
		Last Modified: Fri, 08 Dec 2023 21:43:24 GMT  
		Size: 345.0 KB (344964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5268407b1c98a778587e2afabab3573fc54108f90e060fcb1b1c0428ade07d9c`  
		Last Modified: Fri, 08 Dec 2023 21:43:24 GMT  
		Size: 981.7 KB (981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b51b3189d4269b4668e4f5256bf33cdb2ccacb832859f5418070ce6dbe00ed`  
		Last Modified: Fri, 08 Dec 2023 21:49:46 GMT  
		Size: 7.6 MB (7619560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c3a8e3c52fb32c1faf68d5a95237602ebf8660054e885ca094403a9b548b09`  
		Last Modified: Fri, 08 Dec 2023 21:49:45 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dee3a15dd978c3578c578b35ba1575483dc38936ba3d48d21576db6ab4afa24`  
		Last Modified: Fri, 08 Dec 2023 21:49:45 GMT  
		Size: 568.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:32b8d94868391f8abde5509b9586da49b05e7a564169baf979c13abcca3bddd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11754884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bc505979ee902520ebbc8c0afd4739ba9a83b762398e0c68db58dd29b25e0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 04:08:17 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18b12023bf6b94641f89ef4b8827383cee4a894d41952214755878f01aae697`  
		Last Modified: Sat, 27 Jan 2024 19:34:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34b2f5a273de1391d29bc19629602feca5fd2ae77191defa566091681e05ac7`  
		Last Modified: Sat, 27 Jan 2024 19:34:02 GMT  
		Size: 345.4 KB (345373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a098f8049845d64c1e216dc5438b4f34dbc5331039934a39643dc906abfdb14`  
		Last Modified: Sat, 27 Jan 2024 19:34:02 GMT  
		Size: 981.7 KB (981697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd42c30a90bdceb71df878de6697e25364e08c78596713c0417881560a108c2`  
		Last Modified: Sat, 27 Jan 2024 19:37:06 GMT  
		Size: 7.5 MB (7506975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebfae9bfe373f73fc97ecd35ed7e88727653f4d97c03f810cdaf5e35d8b4001`  
		Last Modified: Sat, 27 Jan 2024 19:37:06 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7bcad258143a6673ae8356b9c0dbb27107fed8f9628d63f09eda99b9bad984`  
		Last Modified: Sat, 27 Jan 2024 19:37:06 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:fa479e3b23eb6b7e696a74633604edadc37ece2dce10ee3dca6664eea5e231da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.8 KB (730838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff84100d14db26e111976e51637c9603f7a3d1152039ff983cface45ef265bad`

```dockerfile
```

-	Layers:
	-	`sha256:40c331980c752bbcf08f3d13b264d2031322fb160c2ab7b3160ecb3d09c3bf4a`  
		Last Modified: Sat, 27 Jan 2024 19:37:06 GMT  
		Size: 696.1 KB (696053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d07ad4e102dd12a02312a7210ed07b2d254ecd6ef656dddede6f482cbcbff99`  
		Last Modified: Sat, 27 Jan 2024 19:37:05 GMT  
		Size: 34.8 KB (34785 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:5bdb86e812a9a610528c7c3bfa6cd8a191d80c1857a662a5993fc1e094b0d2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12309502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c4961039578c0de302ef184716b57cfedfa454e4ae32d7a2b35ad396c3d03c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e707cb768757a1743289ad9b2eabc8ef57096d6165fe291e3be6d4f4c7ee47a`  
		Last Modified: Sat, 09 Dec 2023 06:05:44 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a20ff430bc91dded8f48df7bd61d565d3b9cec1ab7652fb595e4b00ceb0041`  
		Last Modified: Sat, 09 Dec 2023 06:05:44 GMT  
		Size: 345.0 KB (344961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d326b14c5477cf0f21043b97fa9df35978357c9a88fd21e3f53596259b00b9cc`  
		Last Modified: Sat, 09 Dec 2023 06:05:44 GMT  
		Size: 944.6 KB (944605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadb440b840ae62c113f234cec880276e34b7258ce2f941f8766bdffef92a4e6`  
		Last Modified: Sat, 09 Dec 2023 06:09:21 GMT  
		Size: 7.7 MB (7670205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21969f446631caeaae7d647169de9bc0c7ee57f1e05dff13aa5d954e81024af`  
		Last Modified: Sat, 09 Dec 2023 06:09:21 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6992c2663d386d5fe2edfc3e6a15989c525a94238d92815d42dbc290faf5326`  
		Last Modified: Sat, 09 Dec 2023 06:09:21 GMT  
		Size: 565.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:afebc93ff7f44b0ee8ac661ab848945106d6d2ce0da9010f98e9385e44b45490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.3 KB (727254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaa210758eef6fd46b7cea7a1f1382a037a7ef6062343945accf13a114210df`

```dockerfile
```

-	Layers:
	-	`sha256:6c635f353c1c42ac63f943a32c2a37a4b42596d65fb5d96555eb5e1d648f5f5e`  
		Last Modified: Sat, 09 Dec 2023 06:09:20 GMT  
		Size: 692.6 KB (692592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166cbb20d2dfc19a352b5d844bfe7158a2ddafe0f3fcc946ce09f39f4b24ecf4`  
		Last Modified: Sat, 09 Dec 2023 06:09:20 GMT  
		Size: 34.7 KB (34662 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; 386

```console
$ docker pull redis@sha256:e38f4cdfeb04bbcf4b7a2c41b47fe11538b5831596d8a8619066411af5942556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11905123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387e95193931fed346c45b2b16fb40781031df81afc5612960ee26029b901a15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 04:08:17 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0280d4ef1ba785efbb218aea0c48d95c5e7271d33573448f8fd8efbfc31109`  
		Last Modified: Sat, 27 Jan 2024 01:55:44 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0660d2da8323966ba3314d63d41d9bf41d2e71cbdea9d14dc2c83ae0b20740b`  
		Last Modified: Sat, 27 Jan 2024 01:55:44 GMT  
		Size: 345.4 KB (345363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638e000be2d7614296eaac2050185fb3b129b4e7e4a752e140cc39c9a7880bf8`  
		Last Modified: Sat, 27 Jan 2024 01:55:45 GMT  
		Size: 990.5 KB (990502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decbdf5d0107aa0da079d3a42edf3d74347192495716535c1bfa300f2a78f9fd`  
		Last Modified: Sat, 27 Jan 2024 01:55:45 GMT  
		Size: 7.3 MB (7323227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97de6dc77ea9110fa165fc417a3e54de9cec36f105113521ed9b1acb204dcc4f`  
		Last Modified: Sat, 27 Jan 2024 01:55:45 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45724021e2a1b4d881572f57c3e84dcea46922279d344a8c2e82e9f6dce1d4d3`  
		Last Modified: Sat, 27 Jan 2024 01:55:45 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:f21188250ce4a1b5e9ef62975172972378d76b732dc9029583a2003c9851d500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **728.3 KB (728264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e31d086add6260b3b67294ae956027291eae72b80128e79787543543c7cd34`

```dockerfile
```

-	Layers:
	-	`sha256:09177f453501b3e065f9433e00ce67b7dfd976053789ad12d774082fe9277769`  
		Last Modified: Sat, 27 Jan 2024 01:55:45 GMT  
		Size: 693.5 KB (693494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af6c4df99d8920cbf9bb05d4b4a1175a2597216d4fd3f2de8009081849ba4b3`  
		Last Modified: Sat, 27 Jan 2024 01:55:44 GMT  
		Size: 34.8 KB (34770 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:6d9a4bc1f3f87c72d71f15f59dd5b333a1f549fbbd5eae4da909e40918d1c280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12813484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f23e8c1bab2d24d6da7b8d86e0cd9bf42443a117f72d3f036206c506b2907`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 04:08:17 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c78b7b6858858bda25f99a452e85422066e61443fe1eea0afde98b1dfa1a104`  
		Last Modified: Sat, 27 Jan 2024 11:11:37 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf33341dc4eef85f0c2f73e9df258babe09a77538455f8bd70ce492e8ce96039`  
		Last Modified: Sat, 27 Jan 2024 11:11:37 GMT  
		Size: 345.4 KB (345369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8558453bb01d189799aa5a587568afb2212427d4b4315b7c6ac55478780150b2`  
		Last Modified: Sat, 27 Jan 2024 11:11:37 GMT  
		Size: 935.0 KB (934981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a081bffa092f76ec4237b6206bdca164ef6539f4a09964f52697ab45dfe6d7`  
		Last Modified: Sat, 27 Jan 2024 11:15:06 GMT  
		Size: 8.2 MB (8172835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25649ee66a1804e38dfefc10e67fcbad3086724d4c9620c356354aec64cebe4`  
		Last Modified: Sat, 27 Jan 2024 11:15:05 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668dd487396882143b5b9a8000d22393919a20040a1d077770df689a6e20380d`  
		Last Modified: Sat, 27 Jan 2024 11:15:05 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:4668db57554b20828fbcf96529415b6e4dc95dc05d989c6aa684cef71afe1dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.6 KB (726648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58355ab7b27848e11afd03c362f9917043db38a7d6af87318e38500d60acf79a`

```dockerfile
```

-	Layers:
	-	`sha256:f439c23193a5ab5f72597434bf3f3fec3b590e4eab9bb676c6ee711956d193a7`  
		Last Modified: Sat, 27 Jan 2024 11:15:05 GMT  
		Size: 691.9 KB (691939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf54a936ddef098faf412d9e8ba05b777cb844c32be12573c69c5859afb4f855`  
		Last Modified: Sat, 27 Jan 2024 11:15:05 GMT  
		Size: 34.7 KB (34709 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:9c707548456b2b7ca9db4bcc72af563ad60410acca1fa321b2a3654c4d2192c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12549704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02f3e59047d72659c43a0141259b66c86203130e6fb3e43f9e148bb892c4556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 08 Dec 2023 04:08:17 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 08 Dec 2023 04:08:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
VOLUME [/data]
# Fri, 08 Dec 2023 04:08:17 GMT
WORKDIR /data
# Fri, 08 Dec 2023 04:08:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Dec 2023 04:08:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Dec 2023 04:08:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 Dec 2023 04:08:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965d4e9f11aaf54ddc8f41acf2e021fd00ce3476ec31607febca7112f51c655`  
		Last Modified: Fri, 08 Dec 2023 22:32:36 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cbd28413e82f02a4c81d1afc99a2d1d5f21c96af1bf30306c93012f22a6b31`  
		Last Modified: Fri, 08 Dec 2023 22:32:36 GMT  
		Size: 345.0 KB (344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d416124e22a7946a00399ac2e14731c1516c0320893c15e0178b17271453cf5`  
		Last Modified: Fri, 08 Dec 2023 22:32:36 GMT  
		Size: 979.0 KB (978996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc91b9337157509d41e17cf08e90e1068fc9ad0ee590165f03aba8339532b743`  
		Last Modified: Sat, 09 Dec 2023 01:24:59 GMT  
		Size: 8.0 MB (7981472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca074bab0c375e9bfddcb62004f24265aba1475e60f35714901ae4219c78866`  
		Last Modified: Sat, 09 Dec 2023 01:24:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964b0f457d56f3b91927bc914b6d5d7d93c22149ffe1c46e60db611cda5598a`  
		Last Modified: Sat, 09 Dec 2023 01:24:59 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:0f36452cf3216ad85b5e7c28da3ddd1e36c20ef8ba384aee9361e41c93f1631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.6 KB (725591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752aeec8e84523ccfeccef13e38f8b3dc3bd05008a56279266813b854b30d15e`

```dockerfile
```

-	Layers:
	-	`sha256:f6758112baf7f892a7ee406c1ecd7322389fc3a4efe8aa5020225b7b72301cf0`  
		Last Modified: Sat, 09 Dec 2023 01:24:59 GMT  
		Size: 690.9 KB (690941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7156fe80ef6809d5d72fa51178664aeac71065a4b6d82d3b4fb2ff7e2e207d8f`  
		Last Modified: Sat, 09 Dec 2023 01:24:59 GMT  
		Size: 34.6 KB (34650 bytes)  
		MIME: application/vnd.in-toto+json
