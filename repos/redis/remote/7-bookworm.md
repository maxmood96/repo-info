## `redis:7-bookworm`

```console
$ docker pull redis@sha256:d59a53cbec9bfc91784c5dab0670356363e1daba316933970ed5e3f176b716fd
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

### `redis:7-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:88e81357a782cf72ad2c4a8bac4391d193bae19ab119bb1bff3ea9344ab675be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45013733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb47db47a6ab83d57592cd2348f77a6b6837192727a2784119db96a02a0f048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558c7754a337fc921b8bdc3165a910847c4d447f4ffd6d3afd106974ba7611d`  
		Last Modified: Fri, 03 Oct 2025 16:30:01 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac15709dda09878288fcbde5700c830ca1471dfd7d71cbd514d2ce4651b6dc36`  
		Last Modified: Fri, 03 Oct 2025 16:30:00 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced3efe295ee29e88132837b325aaf9dbf4d2a88566c477f0f5588ff974ddb4e`  
		Last Modified: Fri, 03 Oct 2025 16:30:02 GMT  
		Size: 1.4 MB (1438007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0e467b9617689d513ff38d5dd0c6f85d12ccf660d93650dc874b0b7f377f80`  
		Last Modified: Fri, 03 Oct 2025 16:30:08 GMT  
		Size: 15.3 MB (15344715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae579f2fcd36f376c429fafdfb734f3fdab2ae948eb58adaf15b1fd298357f4`  
		Last Modified: Fri, 03 Oct 2025 16:30:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb06eab824d1e6bfc7d7de80ef6c36d6a797c842e59f5a9d0ee387ffba79c229`  
		Last Modified: Fri, 03 Oct 2025 16:30:01 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:a4a29cc9740c630b725fd092ed3d591dc4d7b58acf3165ff27d9995796569bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e6eb0d366b8a5d2b8cf062d9e48b883794f9f378e8943c41d2df379e381f37`

```dockerfile
```

-	Layers:
	-	`sha256:e11d50783ef1b62b91152b9398e9c659a1d5c3408281e8ac8ac14f225320df4a`  
		Last Modified: Fri, 03 Oct 2025 19:06:11 GMT  
		Size: 2.4 MB (2376598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c52487e711248fb3087e6ec77711fb70a94f75e432409bc36d9342ab4716c1ca`  
		Last Modified: Fri, 03 Oct 2025 19:06:12 GMT  
		Size: 35.8 KB (35754 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:3dc8a30f9ae65f5246c86f6746170fc3a063d0d1d2b9ce4b5c25faf4abfae3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42234002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c350c6afd73fcd898f79caddfc7e8f50aa2a2f2ad9ae3a2a642895b95e93b7e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb97ee1fcd5b6a1753f7b38aa0da506b03c14a229d43dd380a38e6b8b0f4df9`  
		Last Modified: Tue, 21 Oct 2025 02:18:59 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ca70efd3d606e5514ef44f972a027ff224f48986e09aa55b4bac0d02d196a9`  
		Last Modified: Tue, 21 Oct 2025 02:18:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc1c3e03df776c16ae69e50484c04163b54cdc70919a3f599388b7192830c0b`  
		Last Modified: Tue, 21 Oct 2025 02:20:24 GMT  
		Size: 1.4 MB (1414444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3d53a32a0c1a59ae800ba7f1b7a8efbb086b1820871ae46c21fe334d4fa8e4`  
		Last Modified: Tue, 21 Oct 2025 02:20:25 GMT  
		Size: 15.1 MB (15059389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcec0d2b9d24ff89c41c2768a6e3214d163c6d5a10e01b9d595cec3bb36760d`  
		Last Modified: Tue, 21 Oct 2025 02:20:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba756d9c90621fed55545896b44bb9f65b377f9a7bf19555233b1f079074d4a`  
		Last Modified: Tue, 21 Oct 2025 02:20:24 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:1ec164f28c3bd2e585eee8da4b4fd6c6cf7924f0c00f08c95ed4b0b7b323cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88990e6d54dc521c7888223c86d1ecc2783629056deab6ec845cf692b61bd72f`

```dockerfile
```

-	Layers:
	-	`sha256:bd4f00f98b6465303c0d071e417a36528110fd9b31110acc2a07a111d95ef02a`  
		Last Modified: Tue, 21 Oct 2025 07:04:58 GMT  
		Size: 2.4 MB (2380418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba991a7fc29baca4d83c08e9aaf46b61c87ed0ec722cc9123fe361e2577db6e1`  
		Last Modified: Tue, 21 Oct 2025 07:04:59 GMT  
		Size: 35.9 KB (35900 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:6282d8ff8755c64a372234c9df230a801f6bf4b81c25a3c3c87f0c58de8e171f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40061694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7f25d25b23fe2e9d3b4851db18ef6f2d3eae49dfeb47a8df565953e7dfe3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a6507ffa4f2c7870daab02a65008b04cb6f3b49f7ab8579db765b56ba3336b`  
		Last Modified: Tue, 21 Oct 2025 02:33:30 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9fe2e231a55cb10cd885a6d4c359092e742835de266f39f2bf9df7f74fb17c`  
		Last Modified: Tue, 21 Oct 2025 02:33:30 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c70677bb1641b2705fb317be83f6c9ff2fc8dc7306e7efb25d90dfb3b0797c`  
		Last Modified: Tue, 21 Oct 2025 02:33:30 GMT  
		Size: 1.4 MB (1405579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ebffc1949b1d805c48f850ce7a9b7ca90eb1a0851e042f396cc2d92bc0e1f`  
		Last Modified: Tue, 21 Oct 2025 02:33:31 GMT  
		Size: 14.7 MB (14719417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf7cfad6125c94fd3a9a782f790ffe4dcf219564aabf8607954a7816241cf3`  
		Last Modified: Tue, 21 Oct 2025 02:33:30 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba592598db0d2a8d46c878e1f91f476381d7eea4cfabe4597f92b97e9817882e`  
		Last Modified: Tue, 21 Oct 2025 02:33:30 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:4d090ead9183311cc0957b23baea193839695ea0d95163123ae4872310c8dc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2965ef76096762b2b63b1dd594eaadfd0de97625ed0b78055ee82a8bc419d881`

```dockerfile
```

-	Layers:
	-	`sha256:88d40291347b67e6d502392137397f9737e5927b514015ca151f4713124bc124`  
		Last Modified: Tue, 21 Oct 2025 07:05:02 GMT  
		Size: 2.4 MB (2378835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:512dac1bde2f93aaabeb73c4480bc2544e1db1545c374ac123de531989e161f6`  
		Last Modified: Tue, 21 Oct 2025 07:05:03 GMT  
		Size: 35.9 KB (35902 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:f8eeb3ae0be10558f24bbd2713b8f9acfc27eeeaba2ce109274db4ee18e8f0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44822607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a2c8d8245e1622d10027210ef90e7eb652e9e366f0342b014ad813f14593eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb2e5b082786a96606607d3833d14a8fb0e072d86c951fe901bd52768ec1d5`  
		Last Modified: Fri, 03 Oct 2025 16:16:00 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788b0b1b8c421faabb49257ff41759bd2444a6a3a28a364ae26647c80953316`  
		Last Modified: Fri, 03 Oct 2025 16:16:00 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6a9715ae303e9f0b0542ad276cb193aef5acb9c1723de518a72f83bde259d`  
		Last Modified: Fri, 03 Oct 2025 16:16:00 GMT  
		Size: 1.4 MB (1369525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095281e017e3953cf0dbf5352ce928f798a6d4b0a47ba1dbf3f3395ca84ec9a9`  
		Last Modified: Fri, 03 Oct 2025 16:16:06 GMT  
		Size: 15.3 MB (15348265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689d11b2e562ca732cd3ce9c5630b41c1b74007f39e5bdc86019f793860162c6`  
		Last Modified: Fri, 03 Oct 2025 16:16:00 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce644bf6fe4024cd80b45ea90433d96fa84686030a7d83a888a3a1fcc64bd8c7`  
		Last Modified: Fri, 03 Oct 2025 16:16:00 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:cc1f25dce64433571084c968e3e49b062c4df98edc94e82739e6a2c51c5443d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066a114e0082ac262a11ee7e5ba5f61f8a7e8f911765bb4da120d63a129397f5`

```dockerfile
```

-	Layers:
	-	`sha256:92691a8847897757c5a5e7a797f37d13e22ef619e07936116706e64806731d6c`  
		Last Modified: Fri, 03 Oct 2025 19:06:26 GMT  
		Size: 2.4 MB (2376879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4aeb988f5edc6fcf582d1344deb95ac5bd5e09974b77bacf8a2d8c4ddc6bb7f`  
		Last Modified: Fri, 03 Oct 2025 19:06:27 GMT  
		Size: 35.9 KB (35942 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; 386

```console
$ docker pull redis@sha256:07e0192c97eece6c42f5af943462e7227ebe0f0b136c7416d3800b49b018ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed9b411b63df3dac695024270dc6c54f8e54aeadc76671bc8c1620e4cb78293`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96847fd9d506b26b1a4417bf55e85e94a2e0e6cdb8ee36ca44cacc3fef57bec7`  
		Last Modified: Fri, 03 Oct 2025 16:15:06 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03f130e94b30ba7ee4185dc84407592306e0a25161d80f650bc5e707719b0cc`  
		Last Modified: Fri, 03 Oct 2025 16:15:06 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148a6849018316a530523d652b2193082c4e2f3bf7bf0f2c09c12fbc38568da2`  
		Last Modified: Fri, 03 Oct 2025 16:15:06 GMT  
		Size: 1.4 MB (1413367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024d38b7dcf9182d9e0c094f7beedaf6e36420cb4dae004646e7468a17a0680e`  
		Last Modified: Fri, 03 Oct 2025 16:15:08 GMT  
		Size: 14.9 MB (14869692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5862b56fd96dd8f7ce8ad87f5517a95f4afa316796f4c18234614e8d2b64cd`  
		Last Modified: Fri, 03 Oct 2025 16:15:06 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434d8521246837e6286965a1a700e434b53675795a10c0284325915a9581122a`  
		Last Modified: Fri, 03 Oct 2025 16:15:06 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:15b3275e021e30db83245647a8b045bdaf72524280ffbd5b6bff586dbc0a0826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2ca522f63e444423169df75bf366ea6c6489d5ecd7c6805bc4fc3de7258bac`

```dockerfile
```

-	Layers:
	-	`sha256:a3f521b956f9d7d028739596522329013f2ef14091fa7e2673017f996221d9ec`  
		Last Modified: Fri, 03 Oct 2025 19:06:31 GMT  
		Size: 2.4 MB (2373771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539ac00e6ea606d5b893a8e086d324bcc6de0379cb70cd779f1a78155c617140`  
		Last Modified: Fri, 03 Oct 2025 19:06:32 GMT  
		Size: 35.7 KB (35703 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:1c78fdf889be91ff77409273994074c5f8217b18df71fe99bb638123574e98de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45273675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb647dae588ad03b3a2e356b991a062412c080b1bacda76330f77f0ed7a092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a19feafca17c760a41bd8c0a6def5d305ec6c2bd7db3db110973a223ea103`  
		Last Modified: Tue, 30 Sep 2025 13:33:19 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c49c53b836615ff43d0954dfccb2d1511e63910baaa76f6f8b400de8faa4a`  
		Last Modified: Tue, 30 Sep 2025 13:33:19 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565c86150dff7363e46160d6364294ad494c9e1a0caa14a8c4d29930df19ce`  
		Last Modified: Tue, 30 Sep 2025 13:47:11 GMT  
		Size: 1.3 MB (1325516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ac06cec09367fc614e366d5e08f29d044c991f913459910df0b5f696346fbb`  
		Last Modified: Fri, 03 Oct 2025 16:32:16 GMT  
		Size: 15.4 MB (15431808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9e06a54807129c9c57352318c87905c34e143a1efaa67b79e24e2b0416f4fe`  
		Last Modified: Fri, 03 Oct 2025 16:32:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09893a906dbbfc583cfe84035edec0b5cde04bb6eea07b983616adc4f43dd5`  
		Last Modified: Fri, 03 Oct 2025 16:32:12 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e8434bd8abdfb19eda7c6bc9a3d1315e56a3d8ade12c756315c39ac0a53bacd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b469d1efcb7dc1cbecc9b3f202a2dc055acc7d19edbe3b7b09fd87c10f9ae7`

```dockerfile
```

-	Layers:
	-	`sha256:d66b15add535c7fff2afcd82d6d911edc79d23ff67b9ea54682adb3d33766c14`  
		Last Modified: Fri, 03 Oct 2025 19:06:35 GMT  
		Size: 35.6 KB (35635 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:9d7c68c924037bc11268e8b1e4cafe2c69989a37e2ce6a3bc86c126aeb6f0fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49941066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf26db70e6e89f64297b97a0a42501425e73c2179b0fd33939874ea3e190ccf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da6a8cd4724a4e2bbf8542bc2de9103d3e2aa4bdf7ed45f7ea94b42239abc1`  
		Last Modified: Fri, 03 Oct 2025 16:15:00 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a7dd308e7b513678843762328d79bd02598d462221a11ce5a806d9536346d5`  
		Last Modified: Fri, 03 Oct 2025 16:15:00 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c48d95cd22983a8f2831062839a9c691a5184bfad1020ffda3a48ac5deec344`  
		Last Modified: Fri, 03 Oct 2025 16:27:15 GMT  
		Size: 1.4 MB (1360332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a0dfa9989340124614171b527eeaa7999226bd54b38cd185c5abfd62b6f828`  
		Last Modified: Fri, 03 Oct 2025 16:27:26 GMT  
		Size: 16.5 MB (16509364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653e65e7df11b768d12eefab1a6c8cf530cc4b85ac236e464aa77b62cb182f3`  
		Last Modified: Fri, 03 Oct 2025 16:27:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0b347635f5937c762786bbede91992c1e682cb159649bfb383fd854c521e9`  
		Last Modified: Fri, 03 Oct 2025 16:27:15 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c7d324777ef028d016be941d9efc3f84c562d836994b2fd5463291fd7ef19517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01c53d22e51219bd29fe197558b33f16af9b2aefdda8f258bd6e687ec708389`

```dockerfile
```

-	Layers:
	-	`sha256:384b91ded15ae233ba1828924835c519b34292c103f0ab118712e510b88c9733`  
		Last Modified: Fri, 03 Oct 2025 19:06:39 GMT  
		Size: 2.4 MB (2380992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafc7eb43d615b15835c57d99a88770d2dce63f45c4ba8d555ddd764da46f93f`  
		Last Modified: Fri, 03 Oct 2025 19:06:40 GMT  
		Size: 35.8 KB (35818 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:6311fba9d493c959883a46dd5611fc96ab1e7ce1926bb668d1fc123d15146612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43673213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eef9ee34e1d2a823218ae7c7493681f96aea13b9e4f52f0815d9c9d97e2c4e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV GOSU_VERSION=1.17
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_VERSION=7.4.6
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.6.tar.gz
# Fri, 03 Oct 2025 11:58:08 GMT
ENV REDIS_DOWNLOAD_SHA=73b94484e00fb4c2440b490dc4021142fb0b6efc8b64c6329c10d24f0b531c99
# Fri, 03 Oct 2025 11:58:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de9b72c52e45b5b170643c3f9f5f4d2406510bdeaa2013b6e5c5cd248c29c7`  
		Last Modified: Fri, 03 Oct 2025 16:14:14 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8c807af78cf545b4e3dc2352b1736378972bf4e39ebd16e827231ee29c36e8`  
		Last Modified: Fri, 03 Oct 2025 16:14:14 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2200d79919e6dbd0a00ef4f1ecb2b2a6f661837c759ea9c55056050d32b4926`  
		Last Modified: Fri, 03 Oct 2025 16:21:58 GMT  
		Size: 1.4 MB (1403187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0095631c29aac121a4da6111b757716114dfb568e67aae07bdde5d99c727bd0e`  
		Last Modified: Fri, 03 Oct 2025 16:22:06 GMT  
		Size: 15.4 MB (15383031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489b8d0f0ab43b15843c1406c7580a401ae37ea9dee3604c985659f322432489`  
		Last Modified: Fri, 03 Oct 2025 16:21:58 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf579192868b46e86e5049786496bffcf453b2e3da06515554fef1649b822a6a`  
		Last Modified: Fri, 03 Oct 2025 16:21:59 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:559d8fc99293189ec189151ed9cc037fc227dab8c7fc361ef1467b39f21c5a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a60a0dffa43f74e7b2220aa4679caaad8b72602dac4d920ce24d0c63bff048`

```dockerfile
```

-	Layers:
	-	`sha256:eb43e73534429703a4be0ccd833c2bfbdf9b8ea87ce8f40596ddf15a19278149`  
		Last Modified: Fri, 03 Oct 2025 19:06:44 GMT  
		Size: 2.4 MB (2373430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c17f6b4dab446add8ee1677e3eb1debd74df27f0b785a60ab9e06a0ee93e7a`  
		Last Modified: Fri, 03 Oct 2025 19:06:45 GMT  
		Size: 35.8 KB (35754 bytes)  
		MIME: application/vnd.in-toto+json
