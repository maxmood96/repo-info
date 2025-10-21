## `redis:7-bookworm`

```console
$ docker pull redis@sha256:6f62de13d7abd913fac367b522b45bb736437460af5d680f36c4b7af34b2160d
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
$ docker pull redis@sha256:6a11fed904cf317684ebb75bfe987d4f777c605d6f4e98d1bf3066db6c58f0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45013670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e53bb4637c329c42395eec0b86851f5314f6ed597ec217b5e4e19f7c102c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a885b7860523a94b64cbcd56de2715c54c9dccb5e4c952ee436ead9b0e3b9`  
		Last Modified: Tue, 21 Oct 2025 01:41:42 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f4ace27ff206cbd8a9c4abfc0f355e3e60620576cd1cf5ec75b0c809d87ffb`  
		Last Modified: Tue, 21 Oct 2025 01:41:42 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87862acd3083203f6262575f30a6afee27485f0cef5e302d5008552999de67a0`  
		Last Modified: Tue, 21 Oct 2025 01:41:42 GMT  
		Size: 1.4 MB (1437977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c23e505b671a33c97a2b3431411f0ec39e4eecf4be0d1b341cd73f4fff7177a`  
		Last Modified: Tue, 21 Oct 2025 01:41:44 GMT  
		Size: 15.3 MB (15344699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7985e01408e3ac79b266bd6a0dc89e0153ff002da2c6983ceedd2940daef2df4`  
		Last Modified: Tue, 21 Oct 2025 01:41:43 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477049afe86c4a5f253fbff063e0cf056f3b6936b0faadbed37a7ee0c9125b0b`  
		Last Modified: Tue, 21 Oct 2025 01:41:43 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c836ec3b30668beef8aec94c57914d3fe82314798936d1386b004fc997baafb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d27e61e9a1dedb207164fa7188abacc367da7319648cac6fcec739a89c04dda`

```dockerfile
```

-	Layers:
	-	`sha256:e9024e773e7113f5ee58042de714c475d462a6bb0cb3fc7615bc30c755e027f3`  
		Last Modified: Tue, 21 Oct 2025 10:05:08 GMT  
		Size: 2.4 MB (2376598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026a660d268196785bf84ebf510e56a1bc7e16dc3b83bdf302f440127d1a00d8`  
		Last Modified: Tue, 21 Oct 2025 10:05:09 GMT  
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
$ docker pull redis@sha256:44990485ecd14fe108d88d4191ec08a0e5de7543069497171a790e182af20e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44822707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1137fc13726186110714a43bd3d34f120549d9500d6824152ae5202d8e711d2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228c8d577e5bb616d013803bd49aba17c83ab1a9e0a267cd587c4c6ba027d9a6`  
		Last Modified: Tue, 21 Oct 2025 01:45:46 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daa074842f453c2a88387fb4fe9198a097972fec02291b054f7a33d83d63bb9`  
		Last Modified: Tue, 21 Oct 2025 01:45:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ef46a5c972cae4bb7f0783ac4520307cd3f7266b55907d0afb559d38a4eb6`  
		Last Modified: Tue, 21 Oct 2025 01:45:48 GMT  
		Size: 1.4 MB (1369539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432d0d8e03aa57f539d5a5cb23914d5c0b46a8375d737fb0ec733356f96bb66c`  
		Last Modified: Tue, 21 Oct 2025 01:45:50 GMT  
		Size: 15.3 MB (15348306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5107a8b547a60129a045555074dfafe44ff4a550422c24d2172bafedcc72e309`  
		Last Modified: Tue, 21 Oct 2025 01:45:45 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f52962261e96a6b0178d5e0076cb2f0e07821211264f2045bd697fc690a368c`  
		Last Modified: Tue, 21 Oct 2025 01:45:48 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0c268de86ae9c2d566097e8ebd3880fde8942e87f23684e3a037e3f70f382fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc42833b4d8ed0e576084912165cf8c16774bcd8b9e9f243e0635d56cdde8b9`

```dockerfile
```

-	Layers:
	-	`sha256:1f713eb51ace5b0b5feae633f2da00846c7d423582f69fe550a02bb85ea1f7d9`  
		Last Modified: Tue, 21 Oct 2025 10:05:18 GMT  
		Size: 2.4 MB (2376879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf7a15f4cb10e7c1e9818483ba818f651a8bcc94836ee2d135c417a4567efab`  
		Last Modified: Tue, 21 Oct 2025 10:05:18 GMT  
		Size: 35.9 KB (35942 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; 386

```console
$ docker pull redis@sha256:813f73ea9b1830bbff90fec61e759bd8a7e24c5c8db87dd320984fc29f1fcb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45495272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35844f197113b50d3f039b7e07b08473e7d35e9d97e4a8adeaed824ba1724e2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
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
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ae8cfbcc27245edcc06092b995e19aa308530d4e90eb79736c288e1a8d69fd`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f60b71b6b0dc44e1673016cee4bc5d45e2264f2ca6d1e1991709df01c5650a0`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495da821bd5f58620b17c9847b556513c0c3577a6a9810de10732c71ccdc04d3`  
		Last Modified: Tue, 21 Oct 2025 01:52:18 GMT  
		Size: 1.4 MB (1413296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94088d80083675811dc5c714d84986b1c675c135ad0b5cf63083d4b7df4c5069`  
		Last Modified: Tue, 21 Oct 2025 01:52:18 GMT  
		Size: 14.9 MB (14869623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d599e2e52c33ed3e951247de1083ae2546e38f614d19668cd0e0655d1ccf84a`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a404ab9a6f06ab6fc3ce2454ce9101128e3f71c9bed3a24b3d7eb1bb36b0da45`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:3e6ed7d5b2cea31c8e06c568c8b575c0756ea3f918a4f1263df44fa761d4bcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715eca21f046196e91372aab5d22259fdef5a266a794dc588904f8fab05c5bc8`

```dockerfile
```

-	Layers:
	-	`sha256:68a166bf7c4743ef0b8ce7d101ee78104c3a1d86bafb3b55b23370e0390968fe`  
		Last Modified: Tue, 21 Oct 2025 10:05:22 GMT  
		Size: 2.4 MB (2373771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0add381ceda79874c96c4587cda892dde975a8d101d1faf8e99b091f3a341d72`  
		Last Modified: Tue, 21 Oct 2025 10:05:23 GMT  
		Size: 35.7 KB (35704 bytes)  
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
$ docker pull redis@sha256:812c809e3bed5c19ed3634a053d908d4bc2956c00ad22d20e20432454b0fe02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49940635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9708ffb57a1278d9a7ee07824a1156989f2a724c72df1adeba8e16163b841e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670bcaa739da53ea8d2c479ad22300dc08f628515e529adf4cd97cab6cd17cee`  
		Last Modified: Tue, 21 Oct 2025 07:14:26 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81870df8086a8043780727f133bf08165b94f948e9194ffda7b8c5601ac4685`  
		Last Modified: Tue, 21 Oct 2025 07:14:25 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c6d5c03f8c6c53b165b70b160a1f1e4ce1b2b8ce2871901ab166fefa0387c`  
		Last Modified: Tue, 21 Oct 2025 07:19:19 GMT  
		Size: 1.4 MB (1360152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74b22e7117b57fe58e157f7b29c3f353d56d3a180a64e33f5725d2cbb22a97e`  
		Last Modified: Tue, 21 Oct 2025 07:19:19 GMT  
		Size: 16.5 MB (16509026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b051ecf6fd90a70003e73a287a2cd6a0293d61fd33aaa40ee1569d92780639e`  
		Last Modified: Tue, 21 Oct 2025 07:19:18 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ea047d4792b8dcb21183d10d0ed084dc869abb690c272bc5f278a16904180`  
		Last Modified: Tue, 21 Oct 2025 07:19:19 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:15de7cb2b8a17ace9dcb45540d69ceb1a7906b084066be2ead3e10487b8ca5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b3587f713717a0f875526c00a761127b2fbe0b53f611cc9a62068ff7c69303`

```dockerfile
```

-	Layers:
	-	`sha256:643aa7e9dd79f791af575eb72b438ad4f8da1255673b51d327bde72b2ab2ae60`  
		Last Modified: Tue, 21 Oct 2025 10:05:28 GMT  
		Size: 2.4 MB (2380992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9fc0407af4d750e8b8a30e71ca68da24e065aeb015f61fdc2f88e07e2f5807`  
		Last Modified: Tue, 21 Oct 2025 10:05:29 GMT  
		Size: 35.8 KB (35818 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:11064da968418c62d93036d559b76f6590426610ec08f48d2289ff3600f8daf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43673469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046aecca52690c9cdf8faca11ec925014ecc520772709fbeb79c1b7221198824`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 11:58:08 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1509abf4b4c38990a4fe82c37fd4d043936f31d0eeddee2cebe407738f5736`  
		Last Modified: Tue, 21 Oct 2025 11:46:17 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf201e071618c2ccbfe58cf8ad4e65036ea2737544ad6de06d19a037dd8e1c34`  
		Last Modified: Tue, 21 Oct 2025 11:46:17 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae27249a02e71b20b1ff2256866dc8033f0ebf407f4bc917db68c314e3858e`  
		Last Modified: Tue, 21 Oct 2025 11:56:23 GMT  
		Size: 1.4 MB (1403267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2452c042eff8fb3f93d93958cb46844d24a2e6f79b7915a6e41e3966a6bfdd`  
		Last Modified: Tue, 21 Oct 2025 11:56:23 GMT  
		Size: 15.4 MB (15383169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624aeb37fdf2b166ddd5864176d9cdea202352513cba7f947b802e80df18fb2d`  
		Last Modified: Tue, 21 Oct 2025 11:56:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f4bb38c921cbf07840e84fe62d892ef42721988bbc92abc2695abcd421bd51`  
		Last Modified: Tue, 21 Oct 2025 11:56:23 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:16e413d44f37db53b3f6e22807294e3970d28ab4bc76d6ca746400bbe0812a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057cbf17ee278ee2122a8338d6f340308267b71cb27792eb5f73e777d7185162`

```dockerfile
```

-	Layers:
	-	`sha256:ce6dd730255bdf23f1c78e67a85059e90d9374f39765492d7031b6b54a930cd4`  
		Last Modified: Tue, 21 Oct 2025 13:05:07 GMT  
		Size: 2.4 MB (2373430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7830cb7489e9ea95bb64cc02c45ae0b7e445766b66b11b61d7058ce656b0c428`  
		Last Modified: Tue, 21 Oct 2025 13:05:08 GMT  
		Size: 35.8 KB (35754 bytes)  
		MIME: application/vnd.in-toto+json
