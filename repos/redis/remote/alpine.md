## `redis:alpine`

```console
$ docker pull redis@sha256:1bf97f21f01b0e7bd4b7b34a26d3b9d8086e41e70c10f262e8a9e0b49b5116a0
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

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:98217a7f384c8774efa23afa27963ae63e1b6af6103f10fe8550e57ecfe3ff72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee33180a84379744659cc28442b8c9754ced5a0253f2596602f51f7e70ec81f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fe5ac456cce632f5b074c2c69ad4293ad9da10ef9dfd69cb12645aa18eebff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388474e9a6f984f3d62598d05682d9e2de9562f3487073ee93448f7a6ce31543`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 171.7 KB (171716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb45f7190c7284a3939f44212676fd769d988cb2cdabda1cf0c64a803d3ff07`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 1.0 MB (1002978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3502a8ad59158ec148d9d61921e6e4c41874a70b5651bc42797ee3fa6ded4bb8`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 12.4 MB (12398952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05de3e1b5dd0f1cad6cbaae74afbfe2ba18d13994f0701c243975271bbd9507c`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a863f8dcffe5eadb1aa48d1a408b643abf97231fc121fcb9665b7bbc74999163`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:b926170df194c96d69772e2c84f0bf99147b5bbdab21ee31f206dbd0ff1c3947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.4 KB (494409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c6847cd977c2b2d89eb5645ae3fc70633a9633c4c2f2edbefb0273f31d7f1b`

```dockerfile
```

-	Layers:
	-	`sha256:287578a548986097527fd1eecdcebb283adb7b482b8b01d4acf482751e5f65c6`  
		Last Modified: Tue, 14 Jan 2025 21:43:33 GMT  
		Size: 460.0 KB (459992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9347dc7b71dcab1396197bab413e612acd4e10ea618e1c33804f00cebb47abfd`  
		Last Modified: Tue, 14 Jan 2025 21:43:34 GMT  
		Size: 34.4 KB (34417 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:9c9ed3ab0c44efd7220b10ca231ab1ea4daed9b8767ea1290b0e19497636c7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17073702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f722be7f2fb31f001a9b0dd7992a2e77502832e05198189b096cab489ccf32ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff53ab9baa18bb4d1ad66011cc8ba63a94c5516abf6c210729d5924f3a4f1f5`  
		Last Modified: Wed, 08 Jan 2025 21:46:56 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608fb9e021fd7a0b8306ccb5d4c9fe2a7d7cc32bbf627127531cca0f9947f765`  
		Last Modified: Tue, 14 Jan 2025 22:32:17 GMT  
		Size: 171.7 KB (171735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f004c2c3b14cd869dc3182e39a7dd95828c3c721a7f442d6f447a03bed3ea09`  
		Last Modified: Tue, 14 Jan 2025 21:43:33 GMT  
		Size: 971.2 KB (971218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726de6cb4a0ff424667195319543b57e1e23f29f6a4b656c4c6417eb16c67267`  
		Last Modified: Tue, 14 Jan 2025 22:32:20 GMT  
		Size: 12.6 MB (12565204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037737543a95a5798c479b989f80f83f5a9403863deb8b933acf327ff493edae`  
		Last Modified: Wed, 08 Jan 2025 21:46:57 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58dc34eb22e8e9b47471e3199d6a6b7f08b9958819e52049d2a0e7ce7285b62`  
		Last Modified: Wed, 08 Jan 2025 21:46:58 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:42ab8c48df56c4df3169e601ed26b15a2e36edba9812ae054de6e643a457391a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8761247eb7ffde4b7550cbeb73493d0f7704006117a91f87992773d0bf35611b`

```dockerfile
```

-	Layers:
	-	`sha256:c2461b27b09b14b9d8ac8b00f9584c50a5202c08b8c2f9bcf813693878faaea1`  
		Last Modified: Tue, 14 Jan 2025 21:43:33 GMT  
		Size: 34.4 KB (34360 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:a0c65b725aa09064d9aa5b67ee8f1e9d77e75b61a5bf0e118510896e791b1e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16664580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5438d2fed2fd7603d570ad809e334da469ac85d1ed7aecb0b1a14f36790094`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0460fffee88d30c6e41724858dc5384de92ba011548b97bb7a1d6d3e8fb00`  
		Last Modified: Tue, 14 Jan 2025 21:43:34 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e56c1a9b127178dd4cb930e92101899bf761da36a8f76d37516ad09f4b1b103`  
		Last Modified: Tue, 14 Jan 2025 21:43:34 GMT  
		Size: 171.7 KB (171744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa56c5140a65cd66e1e57395abc5a4ff440e3bbbeb38efb3a563d76714d674aa`  
		Last Modified: Tue, 14 Jan 2025 22:27:52 GMT  
		Size: 971.2 KB (971210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce38682d111a0f232e48130004b8f73eba0913a6c8e436b8524f1b7ac6113d8d`  
		Last Modified: Tue, 14 Jan 2025 22:51:27 GMT  
		Size: 12.4 MB (12422847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837fec29662b8da74c6021b6cb9b162d2fcf7c3985b80e33a1e7e3b2d1b9d4ed`  
		Last Modified: Tue, 14 Jan 2025 21:43:35 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7150da33f105537625dd3bdeb03ce5e9d70b89ef03f3aa687d6b4af9b4a7af`  
		Last Modified: Wed, 08 Jan 2025 21:52:24 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:2a353c2a005b68b42c6aecf90b99a82ffabdbde6d2c726d1dac5a591ee12ebee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.4 KB (497448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f5e7cc393526e05b51ca4001b318daa45b5f3181371b1e27ebda38b266771`

```dockerfile
```

-	Layers:
	-	`sha256:467d84e22511d9d2f0c286ee2a809f2e05c87e0f514d6d8b22da7401955d4137`  
		Last Modified: Wed, 08 Jan 2025 21:52:23 GMT  
		Size: 462.9 KB (462873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20f1a588e4a908f3c800fd84c23f8b79a728d019d4da64f6567d5b3eaa51aa1`  
		Last Modified: Wed, 08 Jan 2025 21:52:23 GMT  
		Size: 34.6 KB (34575 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:c0bc635ecd7c6670499620a6839a9b176d08cb9cbea946e020bf418d100c8cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17661703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3476e78e24d81d14c06907e3be39f6d0a2d0ad7b2a483491f95428c7426e06f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eda723fc9bbc2ed3a2aff1b1d69056c29ad15e04882245f77dfa35e4230bee`  
		Last Modified: Tue, 14 Jan 2025 20:34:32 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572a44f2e990b6fddc91602380ad6ee1966451f980a0fbafd330c57255dd82d8`  
		Last Modified: Wed, 08 Jan 2025 22:04:10 GMT  
		Size: 171.7 KB (171735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5fcaf70e1fa7381783e23ff25e1ed91613b2be397349bad6eb8a0ec9020b6`  
		Last Modified: Wed, 08 Jan 2025 22:04:10 GMT  
		Size: 934.7 KB (934698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55763761dd3d3740d62aed994145ed14d940f4f44fca429601c14cc32778c5fd`  
		Last Modified: Tue, 14 Jan 2025 20:34:38 GMT  
		Size: 12.6 MB (12561244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd136d59c0cce11fba9ce081adfdc9397ae17c92aa35e1c3b352cfd331772b`  
		Last Modified: Wed, 08 Jan 2025 22:04:10 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed994dafae2ac4c1281091945c3288b0743506a44680f039e6d8fec43ddd6fd`  
		Last Modified: Tue, 14 Jan 2025 20:33:54 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:aea0391dbe338008ecc31c055c86917e3b0949f4d3a8e29c89898e123733ca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.7 KB (494723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7d35a4cd172a2548fdcd80d6e056decdd76575ce1b5c3215d27b9a090465a`

```dockerfile
```

-	Layers:
	-	`sha256:227f78e2a4a6185ccf5fb17736c464fe9ab37cc57f5872cce70c118082096c14`  
		Last Modified: Wed, 15 Jan 2025 02:01:59 GMT  
		Size: 460.1 KB (460096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d26afc2ed9fb132b175bb303bcd94de01bb806f3a26bf00b2eaf3b7fcb458f`  
		Last Modified: Tue, 14 Jan 2025 21:43:35 GMT  
		Size: 34.6 KB (34627 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:5c30ac9c59d8fcddc368d0dd98f544b8b5ab3a981c633db59da7eff9d76b97cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16664025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3ff7e8ab9ccd232c4214f0195c601ba8ef84ed4552648b35653d2602b2829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5770d21d3afeacb9bb34a13f1fe49917188cc496a53927d72ce245994dba3e1`  
		Last Modified: Wed, 08 Jan 2025 18:08:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436cb2cd99ca18e300bb9322d23e0646e82429b93143451343ffde8409152dd`  
		Last Modified: Tue, 14 Jan 2025 23:06:27 GMT  
		Size: 171.7 KB (171732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6efc37b1956f94ad7b177e57876b9875f54be20b8b36267734988d8cca7a8`  
		Last Modified: Tue, 14 Jan 2025 21:43:36 GMT  
		Size: 978.7 KB (978723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61e49f6b12b7fd4830d6da16b5441b2e1c8ee34297f69d3af47fefb4a44ec4`  
		Last Modified: Wed, 08 Jan 2025 18:08:21 GMT  
		Size: 12.0 MB (12048777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04c1a394b18923cb5cb42d2e5e240fb88e6aded495999483f6a623c20ff7eb`  
		Last Modified: Wed, 08 Jan 2025 18:08:21 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a70ff98666fd0045c460542306a136390cb2b23029851088ba66756cee97b`  
		Last Modified: Wed, 08 Jan 2025 18:08:21 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:e7258f04b86b0518ddedfbf163a33b4ae590812a31c606116a1f7aaa95fd9bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.3 KB (494302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720b04d6ce4603325a2d601798f1b50f41076f89becd90f5781ac2a699eb623c`

```dockerfile
```

-	Layers:
	-	`sha256:b1927faa8c51a47782c0116a262a6402b8e0525b18d47e6eb10b9ac785b19b70`  
		Last Modified: Wed, 08 Jan 2025 18:08:20 GMT  
		Size: 459.9 KB (459947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c32d0611c340b7b95d8c9e1cbd0d86a9d07379012babdcfe6b7c37f3236484`  
		Last Modified: Wed, 08 Jan 2025 18:08:21 GMT  
		Size: 34.4 KB (34355 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:b02d7c3f9fbcd5cf724ad9db8cd1d3e4db138456dbd97da144f4436f49e57efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18011744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c048711a7623ecd63000ffb0d315c88226a3515ba7d5b722fdecee7ca00e958c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af5ba8814f34e6a0d618744fd7087a19ce41b60c3fb8542a3e6b510d21c355e`  
		Last Modified: Tue, 14 Jan 2025 22:27:55 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68fa155140df0012bb517145f72a076af593ed160b8851488698d3f004035a5`  
		Last Modified: Wed, 08 Jan 2025 21:25:20 GMT  
		Size: 171.7 KB (171741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fd71b0c63d4c20e8d4b16a7453326549c8e9ccd6070554fd6be01a802c7bc1`  
		Last Modified: Tue, 14 Jan 2025 21:43:37 GMT  
		Size: 923.0 KB (922966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45fa3dbbd8d8f5eef31bb1dcddc4c1e85b4b325ba1b0bc820c7dd12ac4e8504`  
		Last Modified: Tue, 14 Jan 2025 21:43:41 GMT  
		Size: 13.3 MB (13341771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9d0dc7a3981241119f8ef42df6e766b8b4aa2613421c3f5c90e6c5cf21a051`  
		Last Modified: Wed, 08 Jan 2025 21:25:20 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cddd533ac4d5f5ef418d94320422301ddddd0a17fb25f26fd707c0cc0266de0`  
		Last Modified: Wed, 08 Jan 2025 21:25:21 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:863189e663fa41eccd683cabb88c833fb7d08971552ab94f0ab4c88356c2de0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaaa27147ec431ca150825cc95d43851a14096fadf0982e5ea9218fa12f3d2cc`

```dockerfile
```

-	Layers:
	-	`sha256:9106ba51870dec064c6da09a28b5aab3fa14e954fc980d214c2a1e896bb476b4`  
		Last Modified: Wed, 08 Jan 2025 21:25:20 GMT  
		Size: 458.1 KB (458099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f730c435125dc356695318428db9ed4694b2bf0c48db2734ddcf2a2ed58b350`  
		Last Modified: Wed, 08 Jan 2025 21:25:19 GMT  
		Size: 34.5 KB (34491 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; riscv64

```console
$ docker pull redis@sha256:91759d3215e729d401f5107bddc5bfbd75508a7e3e9d093ae160db338b37e4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16458496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e0d7dfe3deb8bb9c6b765acba847bfc64a3d2448c6b1f7192e3d23ed2d72be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff867c0dbeff1fef06f836196342ca3e8606b395317c6c53757713211f00196`  
		Last Modified: Tue, 14 Jan 2025 22:27:55 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db024b937d6abed6abc299d016ad4f9ff785be5a92c87887d097530b869ae78`  
		Last Modified: Tue, 14 Jan 2025 21:43:37 GMT  
		Size: 171.7 KB (171726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d1ada5c52c3a7cc6660fb7b47855c1d1106862c7be8dbde294500b553a72bc`  
		Last Modified: Fri, 10 Jan 2025 16:04:28 GMT  
		Size: 975.0 KB (975014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869b682f2fcf1e9955ee8e06f30dea721705f80a4762f5d1816d783e794bbd49`  
		Last Modified: Fri, 10 Jan 2025 16:04:30 GMT  
		Size: 12.0 MB (11959829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747ab74ca7bffa190414e831ac24340a46be87128666ed0f993614bd21b6d2bd`  
		Last Modified: Tue, 14 Jan 2025 23:06:42 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347a25ccc063e23bced28a799e963e72e892ab45eb7d22cc1cb339f67353e8c`  
		Last Modified: Fri, 10 Jan 2025 16:04:29 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:a57b04716b643c451cfc63068659bf6e894f5820ec38e840a48a915495c5235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037cbf56b6aad0e76f8703ebd3eacb094ab58844af62b52a813ae4f8ca7929d0`

```dockerfile
```

-	Layers:
	-	`sha256:8bfc1d4dec84b721effbc7245462cf168c4bedc8b14a4aab552593cd5e84dae8`  
		Last Modified: Tue, 14 Jan 2025 23:06:44 GMT  
		Size: 458.1 KB (458095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944dfbad4b30fd57d5f6efa6ccd1da4653895c5680692baeb09944543c0cf8e1`  
		Last Modified: Tue, 14 Jan 2025 21:43:37 GMT  
		Size: 34.5 KB (34491 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:858f8eadcfdc9dc04461df9e0aaf0db53a041c1a9bad0ca57d1a5bce99f61f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17581795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd401b63989c43fddd0abead5744728901706422f470c12a651f6728faf3dc6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368ae800cb699efacb7d029cf9dc1ba045020a06fb570d3771c2f141016ac48e`  
		Last Modified: Tue, 14 Jan 2025 21:43:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653518c4f8851ba76117b5d5a64ede302eaa62b143b0fd1f090ab12e75cadc67`  
		Last Modified: Wed, 08 Jan 2025 22:03:07 GMT  
		Size: 171.7 KB (171730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaac5e1152fd871935fc6b024ab9e8b806d58e2f03e3b90d08a97f876566e9d`  
		Last Modified: Wed, 08 Jan 2025 22:03:07 GMT  
		Size: 969.7 KB (969740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7701eb00a9e6c949ae18613dc24f5d639e3f253e7159a5dfd4f501076e0e742`  
		Last Modified: Tue, 14 Jan 2025 21:43:40 GMT  
		Size: 13.0 MB (12971792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a7bfb6c4ee34da1e2f1dae49b7d73b1cdc971c3dc59daa2367748f47614d1`  
		Last Modified: Tue, 14 Jan 2025 20:54:14 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fce7fb2a932f7bb98f05f744ede25fc6ef338be6052117d4e3eef0941bd452`  
		Last Modified: Wed, 08 Jan 2025 22:03:08 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine` - unknown; unknown

```console
$ docker pull redis@sha256:fc2ea0d7b8e5cbe318534d7d060acf660404bffd182e04dd79c07c4adef209f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 KB (492456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c024a7fca86776ecce3a11d69fca82a3df291dceed8edce8a9602177a783823`

```dockerfile
```

-	Layers:
	-	`sha256:0851752798adde4ca06c63d65605f064ac81c101019eff20f792bb470b2d2ca3`  
		Last Modified: Wed, 08 Jan 2025 22:03:07 GMT  
		Size: 458.0 KB (458041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447d8a7ffc188ace2e52567c0b5a3cdf57104a921e9e20de23f814a284b78629`  
		Last Modified: Wed, 08 Jan 2025 22:03:07 GMT  
		Size: 34.4 KB (34415 bytes)  
		MIME: application/vnd.in-toto+json
