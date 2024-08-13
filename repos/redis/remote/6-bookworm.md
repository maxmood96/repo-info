## `redis:6-bookworm`

```console
$ docker pull redis@sha256:9f3ec228b48b7aa6388a18b6cf0c8cf6a262fb1a8abfb5c54d1e8de9190ed59b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redis:6-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:140dcd869d7c68ad7fc7ca96b580f199fc7b9da7568022155f395d3c83dbe009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41053752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88bbcf9a61e2046667bc70fa2c1241784aa2d29289cc1a9082674f2333b0de1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f92814471937a30e48cc3fef57764014666ea6957e6de64becd18d4aed583a`  
		Last Modified: Tue, 13 Aug 2024 01:14:04 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff738a6dba7dd616817c2f1f76a6dac16c1a62527f3bb7422baba48602b6d0d`  
		Last Modified: Tue, 13 Aug 2024 01:14:04 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bb1d67c09a51e358d409fc7b13bcd75d77cb50a465fc5d42ecda9249302aab`  
		Last Modified: Tue, 13 Aug 2024 01:14:04 GMT  
		Size: 1.4 MB (1437676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc428a4299777ef31e31a0d38677830379ce02b9903f57a82d783acd369080`  
		Last Modified: Tue, 13 Aug 2024 01:14:05 GMT  
		Size: 10.5 MB (10487168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4e1688f3fb5e5350439364908350558178985ac62f17b2f1e458bcf93f710e`  
		Last Modified: Tue, 13 Aug 2024 01:14:05 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5310b32ab44b07faeecf6a3c9438c815f79c62732da0268f5557768f6314d6f4`  
		Last Modified: Tue, 13 Aug 2024 01:14:05 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:30f5c1f9b11e53726efff4dbb2f750dcdf668994c115bdb9fb09b9c7d357c539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7826f0f4ae44756b4bd12558b24e312356c6af8b97f07dcce21452b125aecac`

```dockerfile
```

-	Layers:
	-	`sha256:0475d138827531e7fccf0c0011dd17598f7a681ffd8d18d22a63dd55502a87f0`  
		Last Modified: Tue, 13 Aug 2024 01:14:04 GMT  
		Size: 2.3 MB (2256919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a1605cabe48be2fe076b52622369136aad9f82af51cf9cc8ec2c47ae2714078`  
		Last Modified: Tue, 13 Aug 2024 01:14:04 GMT  
		Size: 35.6 KB (35584 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:02c511daf385abcae55426234e3a1e149cad495ef79e6f2f772e022a26369929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38373344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2c55131714aed3e33a8fd1bbc33a33f5df7bec6aae9eb1338e56d480984ed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54e8100dd848a8f531b3d5119942261d71bbbcb591ef0f521266e0ca151b4b3`  
		Last Modified: Tue, 23 Jul 2024 15:52:10 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f5304a2092faa13ef8e9e5597ec7d7073f79a859f68aee575198a2d669e0fb`  
		Last Modified: Tue, 23 Jul 2024 15:52:10 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ab70ed742c1d8c85aa7818454914324623865f532a344252e881c8fc6edbf`  
		Last Modified: Tue, 23 Jul 2024 15:52:10 GMT  
		Size: 1.4 MB (1414258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951c22242421707546cbbba15c03f1003582631a56d8c4c9b2f663f37ea488f`  
		Last Modified: Tue, 23 Jul 2024 15:57:41 GMT  
		Size: 10.1 MB (10069114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cac108c3746f73684dfbc92ce32244fcb42d61cbc418f0aeea355be0af3dd5c`  
		Last Modified: Tue, 23 Jul 2024 15:57:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b7fffdf6352421e6caa073674aa2dd4800abff13feed42df06a137bdde1d0`  
		Last Modified: Tue, 23 Jul 2024 15:57:41 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:2c475e1719c57b8f9bef20fcac7b78d384a81c34b40046fcb740bcf3c0493c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb8e09cb225509b7c1ddf8659c7315d9a07713b97118fc265083948551779c8`

```dockerfile
```

-	Layers:
	-	`sha256:35425e4e6d158fd7addd2e89d92edbf1f0283003e166dc14f65dd83a5be4671e`  
		Last Modified: Tue, 23 Jul 2024 15:57:41 GMT  
		Size: 2.3 MB (2260324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8a0d66fe6c25addde49e348805136123b0430ca667ce7fde2a41763759f6e3`  
		Last Modified: Tue, 23 Jul 2024 15:57:41 GMT  
		Size: 35.7 KB (35722 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:fcb8efcf70fdf64dde33d7da8f122bceee98655b6328201e48729b476d09ad2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35910826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce55995eb254f87cf2082d8ef256ef306ea72d949689238f0ad901abb64c34d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44e2d64ffb7f063a43f9bd157416c17e8d968f8f0d990034ea12dfff5195c5`  
		Last Modified: Wed, 24 Jul 2024 13:15:45 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b33f3a0aa42ad75007b0fe13942b85eedbbf482c4b90ec5b7d4b387c966e97c`  
		Last Modified: Wed, 24 Jul 2024 13:15:45 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132fafeed9aa7eec7740b41645f5b64728503bf86f74dc3e665a9e594c30cb61`  
		Last Modified: Wed, 24 Jul 2024 13:15:45 GMT  
		Size: 1.4 MB (1405427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cb5235b64a95a530d6897cbc3ff134fe8e0b8b6efedccc0b0f2b2024bbeea0`  
		Last Modified: Wed, 24 Jul 2024 13:22:26 GMT  
		Size: 9.8 MB (9784522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e89912be34afc077e963f82036db09aa73d50d8d8586571923771fd30430e4`  
		Last Modified: Wed, 24 Jul 2024 13:22:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b597ef238a024e42f077d9c7ae4d2e82e14d32ab8b9f537bbbadc53589c03`  
		Last Modified: Wed, 24 Jul 2024 13:22:25 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:53ce8f310f8970a048dad9029625d5b497b55e7c6856377af3f50afe31828118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826f36977228532ece87ebaef604bc31ae13384b0f57aefa638d3d653d5ff1c2`

```dockerfile
```

-	Layers:
	-	`sha256:432d272269d0c7d15d2767e7291a0b96da5e051e2892f171ec5814f483fed4b4`  
		Last Modified: Wed, 24 Jul 2024 13:22:26 GMT  
		Size: 2.3 MB (2259155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d231c256cc1d0c996fb0e15735d17216f3c33a961564605ca78d0312ffce5471`  
		Last Modified: Wed, 24 Jul 2024 13:22:25 GMT  
		Size: 35.7 KB (35718 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:5037fb7596761d30f9146c5c9964a97ab5e8b7008a4f0c45c55d62832c58c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40950795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99777670aa526ab18644b8fce10b373ef034393b95a5247b66508a3dad53689c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a82edef47f5673dcc373185fb441612a18881590e5e3dc5e4ea5ee0db414ceb`  
		Last Modified: Wed, 24 Jul 2024 07:07:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f823bf37ffc705cc7cd63eb08b21c97180712735ca2594709db02e5e60214f83`  
		Last Modified: Wed, 24 Jul 2024 07:07:33 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02fd610b0277274fd0ab2a1eaf283cf3b335fcfae75c65f1cb5ba5b2170915d`  
		Last Modified: Wed, 24 Jul 2024 07:07:34 GMT  
		Size: 1.4 MB (1369363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44335e62cd27557253f4422b8b5c38982f766ed5dbf14d464f47fe3d2f715a69`  
		Last Modified: Wed, 24 Jul 2024 07:13:20 GMT  
		Size: 10.4 MB (10422180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66960466e6a90a6b87a0022a40cda83a7260f0b4abcca03bf5631339188e51d7`  
		Last Modified: Wed, 24 Jul 2024 07:13:19 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b3c5896ec22ebe8febb2a75f361cd0a0028e4b400a315515b2ab8d263a76db`  
		Last Modified: Wed, 24 Jul 2024 07:13:19 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c9fb0974ca48ffe06612575951b7b3ca6400eb1e0c13a5ba9a813295782776f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32edaab05ea60ca532e485f357c1233f6610f292afc9b50645a906706a27c4b7`

```dockerfile
```

-	Layers:
	-	`sha256:760e33b10dc0e9db8f31affd31204c6143116c643701374441e6f4c0d7394661`  
		Last Modified: Wed, 24 Jul 2024 07:13:20 GMT  
		Size: 2.3 MB (2257199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3bf9a73c250b0c34657b2a56ef7a19176f0853394fdf0414dcf8bb75e44374d`  
		Last Modified: Wed, 24 Jul 2024 07:13:19 GMT  
		Size: 35.9 KB (35917 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; 386

```console
$ docker pull redis@sha256:e2815aca1e33266b39c11938e4f52e2018635b42fc9d493b2ddb8f984a73928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41779023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bf23619497b1437f6224a696ee8d6f075d40e7d43742bb303527bc4d2ae9a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efff8d96afc28d33f6a9e14904dea2bb1415b638772fca210e8d6a10b5b347a`  
		Last Modified: Tue, 13 Aug 2024 01:14:21 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5f6531abe13f94d19f171479725cc2af6837f1c91eb87f63bb3544a23c7d75`  
		Last Modified: Tue, 13 Aug 2024 01:14:21 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efb7e2034fd2deaa98516fa562b864a6e7129d2201db8faff07b2c2972428c5`  
		Last Modified: Tue, 13 Aug 2024 01:14:21 GMT  
		Size: 1.4 MB (1413117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cf230af4b48cdc7e9c6ffb2fec8c9de62a02fad48e08e0d3dc9fa6062c8a7d`  
		Last Modified: Tue, 13 Aug 2024 01:14:22 GMT  
		Size: 10.2 MB (10218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de72c5afc5e1aab2fa0fea6ceaaaab6b3b59a76b9f0e88e0f6cf832ad87335cc`  
		Last Modified: Tue, 13 Aug 2024 01:14:22 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53a863c6ceedc6a85680d93483f95971a49add43e78a5bd4c862fae162f23d1`  
		Last Modified: Tue, 13 Aug 2024 01:14:22 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e3c94c9965261cc48e45384241729413911e7ac862acd907d7e2bd36489a0b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084df53e4a8c25c343558b118417f06cc436d32d7a456b84b3c77380024fb14b`

```dockerfile
```

-	Layers:
	-	`sha256:b93fb09988bfe0d6425271994476b80dac737ad614d3ef7fe23a114c9599ded0`  
		Last Modified: Tue, 13 Aug 2024 01:14:21 GMT  
		Size: 2.3 MB (2254051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8c8d86f8ed05079b47579dbdb107e09417ed64789b5c85fd38a419940f14db`  
		Last Modified: Tue, 13 Aug 2024 01:14:21 GMT  
		Size: 35.5 KB (35537 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:7bfb2d2f48005cf5b213eec5b14e5b89566c3cb8ac45a48adfeba7fafa0df191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40875216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c264d8da3875892b54a3a54d10256722bf049efd0f1a4824ea75615acc1940`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba894a7ebfabcfee107c5dfacb464553112c7046c3af0908c3917f9b71029ad`  
		Last Modified: Thu, 25 Jul 2024 10:16:02 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd8586c4dc8957bbd16706caf534f8b6338d0a369ea4bf0152de264af41e283`  
		Last Modified: Thu, 25 Jul 2024 10:16:02 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c87834da4aed9895b8e665438b1f17f6b03dbfb179949e427c13eeb78532e6`  
		Last Modified: Thu, 25 Jul 2024 10:16:02 GMT  
		Size: 1.3 MB (1325327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c3164af00431d21997b7112ca50b911897ad706859a5d8a41550164a44d61b`  
		Last Modified: Thu, 25 Jul 2024 10:32:56 GMT  
		Size: 10.4 MB (10422285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21c896d3558e6b5bbeda6b1687691c2d8656ee51350e7d69443f376ffa6976d`  
		Last Modified: Thu, 25 Jul 2024 10:32:55 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b7bcb2aade110a10d0dde5adb8d406d574b87ac0f97150850d374f734c5ea`  
		Last Modified: Thu, 25 Jul 2024 10:32:55 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:f2b32679e5aec86098ef103ed78ef9ad8273ffa5e1a4881bcf6da860cb1dc835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932b3efad89393a569dff6e8255313337c11a554ad448d7c9b5a430719747b16`

```dockerfile
```

-	Layers:
	-	`sha256:d501ef5bc060c8fe82cddc40d49b7fd6f8d6f23f9085c1c5f3e90c798cc4350d`  
		Last Modified: Thu, 25 Jul 2024 10:32:54 GMT  
		Size: 35.5 KB (35452 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:90797613421dc68ed43c3959a5706b15c2a1a9324d4193416a7f442842dcef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45819607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599da21655aeff4d8b971b7a7773a858e3d73300e682082e5e08299f11fdb9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b74042a0ea7209037dee6054ac964cab3452e4ecf8f7dda7bc5abb053ea314`  
		Last Modified: Wed, 24 Jul 2024 10:14:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7186439d6b4d01e0debcfefc87c21a960f616e1052df7f1ccb71f17e67bf332e`  
		Last Modified: Wed, 24 Jul 2024 10:14:33 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2cd2ca44e585cbdf536e71e9ce11a7c7cf3b5785bc7c7946c38aea1b4dd1c1`  
		Last Modified: Wed, 24 Jul 2024 10:14:34 GMT  
		Size: 1.4 MB (1360060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8e6081bfc0c0f5f7202f84fbf7fdfdab8d2422cfe542db10a66bf816444901`  
		Last Modified: Wed, 24 Jul 2024 10:23:40 GMT  
		Size: 11.3 MB (11334592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826a6c568975731d446006ec71deb026a5233ac27e3e0db8136532f261c4551`  
		Last Modified: Wed, 24 Jul 2024 10:23:39 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c4964e20ed086b0d4beb8dd111502fc787a97c90e623b076a994b5a42a19aa`  
		Last Modified: Wed, 24 Jul 2024 10:23:39 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:928c6d17b899de29b605307a5d08098fd66e898c4ef4b7ef155cd26ffc8a3ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eca11854f933f7e478d9abf5071411acdee023337bbe071b44c283cd96d184e`

```dockerfile
```

-	Layers:
	-	`sha256:7782e99dd9b40c2155e3fc5373cd5482737ae27e5231d5e8e94b1a3cd2e60a7c`  
		Last Modified: Wed, 24 Jul 2024 10:23:39 GMT  
		Size: 2.3 MB (2261220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db777e8071efc956be996316e7ae1f36cd3b835c7cef996e123f525f80e8929c`  
		Last Modified: Wed, 24 Jul 2024 10:23:39 GMT  
		Size: 35.6 KB (35642 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:62f5f1457b33257c7c6a8eac63b1d969cd5c04acc64e8ff97aebdd631c57317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39349900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a8358304766e5fad2e23819c8af1f714bc25aa19cd6afcef2ce9c98cb13626`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 22 May 2024 23:17:59 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Wed, 22 May 2024 23:17:59 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV GOSU_VERSION=1.17
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_VERSION=6.2.14
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Wed, 22 May 2024 23:17:59 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Wed, 22 May 2024 23:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42759d6a2a9f7ec60bd2c9cc03e009a19349894e22f5c65464fee6b44aa45a0e`  
		Last Modified: Wed, 24 Jul 2024 08:47:24 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e65443cdd01ce3e9a30f12049cc966ab520679e67b6d42cd60263dcfbbb160`  
		Last Modified: Wed, 24 Jul 2024 08:47:24 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1364f37eb38f24d8321c8e71a8a905efbb35a7d51418f7b2e2e733b39a02ea8`  
		Last Modified: Wed, 24 Jul 2024 08:47:25 GMT  
		Size: 1.4 MB (1403102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d15c0aeba1b59ff2dd803e420473081bf5b0a19105f4c50c78ee1dd4fcf6b1`  
		Last Modified: Wed, 24 Jul 2024 08:58:36 GMT  
		Size: 10.5 MB (10454020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820cfb06598a2f888e4f6f76663ac4171efdc2fcaf475a577a9a8350d8d644e8`  
		Last Modified: Wed, 24 Jul 2024 08:58:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f397482f1a82381748b0c457c510a7d2d908229ae1f1435e6f4ee67f009c4`  
		Last Modified: Wed, 24 Jul 2024 08:58:36 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:757df3c9872a54734f9e0492d100b22a8a19f9b31cf8cabb90fbf5deb6e71665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d0851c485e17c94f38e71ec42fe4f4b89588f899b1721a95e0d2f16dfe98f`

```dockerfile
```

-	Layers:
	-	`sha256:94153685fcee6d272054900b5ef2ab05b8c6693c12c9b7d88d6a0167f9a6eec8`  
		Last Modified: Wed, 24 Jul 2024 08:58:36 GMT  
		Size: 2.3 MB (2256750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3498b3dd00a05f0f4b440f5ad5e6e945d0cbcdaa792d3e85e65cec8466bc303`  
		Last Modified: Wed, 24 Jul 2024 08:58:36 GMT  
		Size: 35.6 KB (35584 bytes)  
		MIME: application/vnd.in-toto+json
