## `redis:7-alpine3.19`

```console
$ docker pull redis@sha256:a40e29800d387e3cf9431902e1e7a362e4d819233d68ae39380532c3310091ac
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

### `redis:7-alpine3.19` - linux; amd64

```console
$ docker pull redis@sha256:3487aa5cf06dceb38202b06bba45b6e6d8a92288848698a6518eee5f63a293a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16755322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435993df2c8d3a1508114cea2dd12ef4d6cbab5c7238bb8e587f20b18982c834`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3180d102093de53ebc54b965de6754cbbb344a30e2bf2f5d17cbc3ac1d50b5`  
		Last Modified: Fri, 15 Mar 2024 23:55:58 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76326fd8e6b93c5ddd86c0795b0a04c186faf08ce032c102aa9b3671276019a`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 343.1 KB (343091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034c076ba1e793bb3f31ae4f06a1737a362a34ce9e843c6c15022cfbec955bb9`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 1.0 MB (1015382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffcad17539bc6497d8dd4bd24f6628013eb413b988050010925cb2ce4382291`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 12.0 MB (11986182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5913474e0f39b23ca3d952a08c0008364c774a07984efaf8ad3a5ba8e04d31f6`  
		Last Modified: Fri, 15 Mar 2024 23:55:58 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6fccbbefa3f40f40b56bb79e12ea0d1712b5b2421e04b1e0086c222e43da52`  
		Last Modified: Fri, 15 Mar 2024 23:55:58 GMT  
		Size: 565.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:a3dcaf2ef3f1bd9a07c8d7ef5c19a4997d74cb43900465284751046dbffd259d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.0 KB (865048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8b4e9a1eb6ab58845b855064e00729767ee20acd06cf88976e4d96aa1dc04a`

```dockerfile
```

-	Layers:
	-	`sha256:82eccad30d4ba0fdb62025aa4913b621920d8fd89af5521d382d4279f149dc76`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 829.6 KB (829640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8948f0d5b81b87926f343abe15dd4a41ce97dbf597cd90ddb472a41b6d09b1`  
		Last Modified: Fri, 15 Mar 2024 23:55:57 GMT  
		Size: 35.4 KB (35408 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; arm variant v6

```console
$ docker pull redis@sha256:8e8a6c82d3d959bc119f49554a47c259118dd9731d40d5c456726cb68e5a6cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b34bdd29092e4cad7dc40b20f88937858fff470d20a3d62fb1e4c80ae2a3cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e9524ea8498e93529782b28faecc67a324ce610c4782b9a3d007c6a22c8cd`  
		Last Modified: Tue, 19 Mar 2024 07:58:26 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f543daf223677ba73a15d7b16df743ad8a57a95b6bb8936e9a67293684a076`  
		Last Modified: Tue, 19 Mar 2024 07:58:26 GMT  
		Size: 343.1 KB (343105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cabf822f7c10ec6c69791bf239bf5af11c4d042e341e43051de1fab5db1e30`  
		Last Modified: Tue, 19 Mar 2024 07:58:26 GMT  
		Size: 981.7 KB (981686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f3892303d74fde1258f66c86d7d11dfa8e771af75acba4ac0ec587e00b2d94`  
		Last Modified: Tue, 19 Mar 2024 07:58:27 GMT  
		Size: 12.2 MB (12156099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c61ecaa0311ca0ef02204b4dcda9a5bece416adbacb47966a2b09d4734612b6`  
		Last Modified: Tue, 19 Mar 2024 07:58:27 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f5c69e801c334c6356a345d488482c22b688082c47cb5e71716630be95b9af`  
		Last Modified: Tue, 19 Mar 2024 07:58:27 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:15b1e4f89095ed6789cf25ce7b5dccc3a27ec0dfcc85c9a3d550810986bbee69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080a53d1df8be094f97eb1089c1f6edcdc60938fc5d94bb7543727d4a2698c4`

```dockerfile
```

-	Layers:
	-	`sha256:a8811b57a2dbdbcaefa043f07374ffc75b3be68c0dc18fc4142c58e2e1833951`  
		Last Modified: Tue, 19 Mar 2024 07:58:26 GMT  
		Size: 35.2 KB (35180 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; arm variant v7

```console
$ docker pull redis@sha256:47d346c4f0547366fa79fc67497e21d59515dcf1b021eb3c1edd28f901a12bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16278780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48c195e625b4a73dcb67797897bb8721a0407e8379e998aea42407054b5011c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43155b765fea2ee128dd1790fb9654dbb30657cb09eeeaa327c3482016b44422`  
		Last Modified: Sat, 16 Mar 2024 17:49:06 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744efd0f35b68361b570054c4f513de5a5e43f8266e1da3db5f9ed81960cdf76`  
		Last Modified: Sat, 16 Mar 2024 17:49:06 GMT  
		Size: 343.1 KB (343098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15881660cbaf4c0d5cbe6e2122a7efddf1f3ade70e594ff73e8fd6f8a69dc4f4`  
		Last Modified: Sat, 16 Mar 2024 17:49:06 GMT  
		Size: 981.7 KB (981697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740ee8e6691a86619b420c09647c206de62bd4144fa05d3f923f9ec0a4ca19f3`  
		Last Modified: Sat, 16 Mar 2024 17:49:07 GMT  
		Size: 12.0 MB (12033137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4741d657cd2e742728837ebf3fc2acb9ca05ead394bc74257d10393b79ae427`  
		Last Modified: Sat, 16 Mar 2024 17:49:07 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bced711e73a45c2ea9bee92f634ed5dde9aae9e6a4fb59b98a583ee0311c2c77`  
		Last Modified: Sat, 16 Mar 2024 17:49:07 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:a15c3cdb4e0a6f26ad7bf1a4a2b7f0eedaec661bda334637e36994b3c282f31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.7 KB (866737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ada3b6957baec97fe67ed942f7f9516eff622ffc58aebd6e622225e13e017`

```dockerfile
```

-	Layers:
	-	`sha256:808d434325ae8972be1523a5724ba7c6efda4080dca4fc7521033f634904aa09`  
		Last Modified: Sat, 16 Mar 2024 17:49:06 GMT  
		Size: 831.3 KB (831342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f742d0b4f1d122014f45f9a7e2eb1e597bb5fdb72b68bb6aba160198a14b37`  
		Last Modified: Sat, 16 Mar 2024 17:49:05 GMT  
		Size: 35.4 KB (35395 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:ead9002c1f4f7d4c8d6fd7f277cfa7f22f38b6a74cc72069a9d8c20ed395d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16787438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbdda94acb95472e716b5503a206f5fe0454aedb7b8c1dd2f2bad34848f5b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd12c8e0707ba08c7f157138df2265a5de67c0882858ea090529024e47198e`  
		Last Modified: Sat, 16 Mar 2024 16:42:23 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a71491b5fd761710452f4e7a293a5ac5070a0ed33711dfd922605d22e930d7e`  
		Last Modified: Sat, 16 Mar 2024 16:42:24 GMT  
		Size: 343.1 KB (343097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12253d34a72a075553377d1665a9375174bbf14b2626c0439e1eefdc1cd7a79c`  
		Last Modified: Sat, 16 Mar 2024 16:42:24 GMT  
		Size: 944.7 KB (944660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2309646ec81c6f8382ba0e81b53cc9c6d9f4efab68ba32526da96379f7f6cc1`  
		Last Modified: Sat, 16 Mar 2024 16:42:24 GMT  
		Size: 12.2 MB (12150030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c7ab2c74087fe5c97d747ff41c9066c06bd2596e9dc149babf3787a103003a`  
		Last Modified: Sat, 16 Mar 2024 16:42:25 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399b1f823fda9e4fa98fda40b914a5ef865b242ff465b1e68a61b05fbb732449`  
		Last Modified: Sat, 16 Mar 2024 16:42:25 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:9c58cfef28d3735556078d1bf165b5a1034db14a9243752449756d8e2de108bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.9 KB (864915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cea3746213b0642456f87f6286551936401ce0b9773a0dfed0169d2d658afad`

```dockerfile
```

-	Layers:
	-	`sha256:7b8eb470a0ac307817209701631c17877ec1f3f54d6ccabf6b9c349e15f90257`  
		Last Modified: Sat, 16 Mar 2024 16:42:24 GMT  
		Size: 829.7 KB (829659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965a1c591a9f0c5ec4251437c8ae0d2b377e0778be4bbc5c778bb4bea9aa7383`  
		Last Modified: Sat, 16 Mar 2024 16:42:23 GMT  
		Size: 35.3 KB (35256 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; 386

```console
$ docker pull redis@sha256:a08efb7ac7a302465f03b8debfabcada6738d9042ad266b24450b1879e433d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16244700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d9977e3288495a80560557ccb8fb611e8c29f562aa879178fe847babbd838f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9916e68653b313c5c186acd9209d471aaf505f40688dd4428125bd1873d1f9`  
		Last Modified: Fri, 15 Mar 2024 23:57:51 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41879fe025fd318663bc4fe568207cce9c06366119b093e21bdc870f633ae184`  
		Last Modified: Fri, 15 Mar 2024 23:57:51 GMT  
		Size: 343.1 KB (343088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d66fb91c6290ef162d54f633dece5523ca7171ace465746b706105555921de`  
		Last Modified: Fri, 15 Mar 2024 23:57:51 GMT  
		Size: 990.5 KB (990502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e081bc16e9726cb840a54698c8731ee20a7381bc4779873476f0ee234511af6f`  
		Last Modified: Fri, 15 Mar 2024 23:57:51 GMT  
		Size: 11.7 MB (11665080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fef9076fc90b8dd88440d2645fe3c06d0a390cd1358bba26e851eb683c32b4`  
		Last Modified: Fri, 15 Mar 2024 23:57:52 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b42b44ca3aa8caaa5f48e08467d071c847041315df352784761d749a378632`  
		Last Modified: Fri, 15 Mar 2024 23:57:52 GMT  
		Size: 566.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:5a86e5f52989bbea25f8cd7d707cbcf5fd480d635da2e02b8dc7278ddb5fee61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.0 KB (864001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a3c9ad4e2a407b58d2e9e26c9d8185f503454d0b739677d0b2e07113c6903e`

```dockerfile
```

-	Layers:
	-	`sha256:c12270ac55e4976302fb5482665e2dff7e0efc8e16a19f79b4c8a182a3c373c4`  
		Last Modified: Fri, 15 Mar 2024 23:57:51 GMT  
		Size: 828.7 KB (828651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3eb4eddf3cce519c8de5f2c4057880d628355e555266f790630353f1190da32`  
		Last Modified: Fri, 15 Mar 2024 23:57:50 GMT  
		Size: 35.4 KB (35350 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; ppc64le

```console
$ docker pull redis@sha256:cdb2b8f004cc7cd2e281dc83f6106ec94e556d29a920a6a232f8b2ea21bc2883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17526506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449a7545328b1737d3242177fb1274c1cc16792c1ad08c8bc97f69e7c4170dcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf779fb9481bcdf70e5162da98da16d8e9538fd96e761ef255b7baf71319a3`  
		Last Modified: Sat, 16 Mar 2024 11:32:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3e5d04d8eba7fa64f903b57007a0a124f6c87e227acf6348f5c90d25e02269`  
		Last Modified: Sat, 16 Mar 2024 11:32:29 GMT  
		Size: 343.1 KB (343094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75acfc9ef04a539fccda1bca14051e475bb7e0f10cd0c5b28f9042aa34f6715f`  
		Last Modified: Sat, 16 Mar 2024 11:32:29 GMT  
		Size: 935.0 KB (934989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5880611d1e864254948c65d30bba84a12af623425e4d61510036d8e2f6b1b7e`  
		Last Modified: Sat, 16 Mar 2024 11:32:30 GMT  
		Size: 12.9 MB (12888124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df21a7e958ec6e496246fa87ec4c8bcabe0aaa62b409282305b6386e235692a`  
		Last Modified: Sat, 16 Mar 2024 11:32:30 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c06f2a450e44d81f1ac6a476b90057e81afae65fb4590f09d947e922fe918`  
		Last Modified: Sat, 16 Mar 2024 11:32:30 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:84c3abdafd7e235c3a08645ad0ecb25f21035ec4441b13680c26748143811177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **863.1 KB (863055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7fc429fefd874fbe40c9604fcc975d0a6299888789080cb867c7b5c7ae0975`

```dockerfile
```

-	Layers:
	-	`sha256:4ae5e48eeaf254bb04d88de82d61339d91b11e00df6979f19c0b59f256397fec`  
		Last Modified: Sat, 16 Mar 2024 11:32:29 GMT  
		Size: 827.7 KB (827744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae92aa574a4a85938ec153423b3482ab67561cdb2c0ea1c3d47c83afdbf05e3`  
		Last Modified: Sat, 16 Mar 2024 11:32:29 GMT  
		Size: 35.3 KB (35311 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-alpine3.19` - linux; s390x

```console
$ docker pull redis@sha256:a476f030ec86a4ae190e79a72d236e98abb1865011fa085a4d08a86c6851fedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17106772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d0bb7d0accecd748ea4e22334f119091ccc554a4fd0154bd83611520d75c84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2024 16:09:57 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV GOSU_VERSION=1.17
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_VERSION=7.2.4
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.4.tar.gz
# Tue, 09 Jan 2024 16:09:57 GMT
ENV REDIS_DOWNLOAD_SHA=8d104c26a154b29fd67d6568b4f375212212ad41e0c2caa3d66480e78dbd3b59
# Tue, 09 Jan 2024 16:09:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"7.2.4","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@7.2.4?os_name=alpine&os_version=3.19"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
VOLUME [/data]
# Tue, 09 Jan 2024 16:09:57 GMT
WORKDIR /data
# Tue, 09 Jan 2024 16:09:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 16:09:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 16:09:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Jan 2024 16:09:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111eee02494239d08b36e35b8d28447cf504ebb0aafb510f8059cf0c66943184`  
		Last Modified: Sun, 17 Mar 2024 06:29:07 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5335d56562106960df02a6285b36df1c0e594f76bac3473fdfe60734d47655`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 343.1 KB (343106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723379cdf669c6f92346e2b15527c35b54cd60fa9a9465f5b29bd10729bfa90a`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 979.0 KB (979030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b441b28f3ce855d88a6e41514cbc3184074beff73d139ae80a4c8f34be6a9b28`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 12.5 MB (12540060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940501557d3dd3e6845a9df3e4d73cf342dc2d847e748b0e6e45abd12bacba75`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd325dcca1673f937b8c09a4e26924d49e11a053ed25de817f76bbbc033596f`  
		Last Modified: Sun, 17 Mar 2024 06:29:09 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-alpine3.19` - unknown; unknown

```console
$ docker pull redis@sha256:58348c71ab68d29402dc1f309098020c0023ce5595c7375a8b37203de211137d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.9 KB (862927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6aa579244bbf0eed4d5248770d2ff6f2ae30dbb058c78f6bfa58cb72ab1a04`

```dockerfile
```

-	Layers:
	-	`sha256:b3959feac97e06afb092bea74738b98c1968b834984b2407dddce701418a6cea`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 827.7 KB (827686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9544fa1a1a8def88da8339df6cd2615e99797cfcfcdc80ee79076d5b779f08f8`  
		Last Modified: Sun, 17 Mar 2024 06:29:08 GMT  
		Size: 35.2 KB (35241 bytes)  
		MIME: application/vnd.in-toto+json
