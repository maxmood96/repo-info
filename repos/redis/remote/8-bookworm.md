## `redis:8-bookworm`

```console
$ docker pull redis@sha256:3906b477e4b60250660573105110c28bfce93b01243eab37610a484daebceb04
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

### `redis:8-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:b6300dab548a9b9477615afb67d90d134b9609d4f0ca59695e1c9a93e099f27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52984231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e6be7eb290d24ebae56dd97ef9c769d9eb83114db2913dea86335549925751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:04:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 08 Dec 2025 23:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:10:28 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Mon, 08 Dec 2025 23:10:28 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Mon, 08 Dec 2025 23:10:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 08 Dec 2025 23:10:28 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 08 Dec 2025 23:10:28 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:10:28 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:10:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:28 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 08 Dec 2025 23:10:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f52e32d52074d8dfe39c76ab5a84fd83cfc5a39151fcddf2a533722045a567`  
		Last Modified: Mon, 08 Dec 2025 23:10:42 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cedcff21aff10527265d8ca7e406ec059d4cee222350b341b115fb6b4e5fb8e`  
		Last Modified: Mon, 08 Dec 2025 23:10:46 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e9940121754f18671d51eb58fb05b17a21fe9374f69aef5a1620b073076328`  
		Last Modified: Mon, 08 Dec 2025 23:10:45 GMT  
		Size: 24.8 MB (24751592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a95b931a833c2646b1fe8165f926841179c2a0f3f09f7d8e5feecd23332a3`  
		Last Modified: Mon, 08 Dec 2025 23:10:42 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16123e68fb8ce31ecab328f87167cfc2112739e6bd3b722e3575d1412d45ab`  
		Last Modified: Mon, 08 Dec 2025 23:10:42 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:87d5aa6d4419447343141b1283fbd57350af6f352049ed557a36256fd9d398e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45054a12a8bca868c25dbdffec844cb0b2099b4177cb41c64f499b5753a1005b`

```dockerfile
```

-	Layers:
	-	`sha256:5cfcc0f8ac58f02f81432a59285ed69babffeabcee447798a28294e7d199fb12`  
		Last Modified: Tue, 09 Dec 2025 02:06:54 GMT  
		Size: 2.4 MB (2373626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db91eab6df361daa9efd3966d6a7c0f1105b578764c2b5651006045529f470d4`  
		Last Modified: Tue, 09 Dec 2025 02:06:55 GMT  
		Size: 29.7 KB (29672 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:1d87ec779a50a538e78c7b7a1433a51772dbdbd159261d3463a9109783aa3abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41456084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c059bafc67503ebcd0ca0588f9db57f2d89382f748c45772276856f0ced2c7d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:43:09 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 08 Dec 2025 23:43:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:44:13 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Mon, 08 Dec 2025 23:44:13 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Mon, 08 Dec 2025 23:44:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 08 Dec 2025 23:44:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 08 Dec 2025 23:44:13 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:44:13 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:44:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:44:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 08 Dec 2025 23:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141a8691ba8e5ebe356fa1eec9edaed53002720c7aeddfb0ea29299b55793f`  
		Last Modified: Mon, 08 Dec 2025 23:44:28 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f9b3f25eebedcd2b7825cb54e8df73d73025b2fd4911ebd6b761b9cce0f1c`  
		Last Modified: Mon, 08 Dec 2025 23:44:28 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9139ea10984dc278a633da23383012ae7832df373e226d4528b8dc2f993d696f`  
		Last Modified: Mon, 08 Dec 2025 23:44:29 GMT  
		Size: 15.7 MB (15694288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672d1f80a04df4960fd33404ceaa4381bccb62651964c071689f084b8acba2e4`  
		Last Modified: Mon, 08 Dec 2025 23:44:28 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98573826e80a50aa54d4683930cb8e6032be7acec10b929a0edb819365474714`  
		Last Modified: Mon, 08 Dec 2025 23:44:28 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:61dfab83fd64787e0eb2a6ed509a53238e15dea9c97580a62eafc8c8ae628fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1843fd0ec7ad26355b42d0ddb2abe08126479577e8c267f14c79a02dc1bf146`

```dockerfile
```

-	Layers:
	-	`sha256:f2cc1e847ef13b2461f9a47829c61e2dbd57c90dbe77be201190830c018c5314`  
		Last Modified: Tue, 09 Dec 2025 02:06:59 GMT  
		Size: 2.4 MB (2377462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f3f8f9514c1a6626e85f7bface32d730b8f8de58e7b89db94ba099937fce92`  
		Last Modified: Tue, 09 Dec 2025 02:07:00 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:3fdd5b5d611e375730f1bdcfa64039fa1bdf49f55c4ecc6ff90e42fc4587a1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39253902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb6333b10bdb7d3289e5434a0490672a1a78922baad01a1892332a40f668fca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:04 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 08 Dec 2025 23:53:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:54:05 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Mon, 08 Dec 2025 23:54:05 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Mon, 08 Dec 2025 23:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 08 Dec 2025 23:54:05 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 08 Dec 2025 23:54:05 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:54:05 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:54:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:54:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:54:05 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 08 Dec 2025 23:54:05 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670dc1fceedb73bf471f9d92562e9fa95aca59c0219510deec37373372913a0`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cb6804cf34a748355a6599490bd3ad56a811e39e3cfd458536e90cb969c8ab`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63887f371861dddbf8e89eff5d065a7c89f842dd7d839a5205ed9f3ff7a7dd35`  
		Last Modified: Mon, 08 Dec 2025 23:54:23 GMT  
		Size: 15.3 MB (15315675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9743bab015df9e24372512eac61960dc0fe61ef85788f0f0ef3469764fe0a`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0ba102de8e7a5b6f49e4cd32cb0d094b918af8170018dd5d71ac8e4ff8cf34`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:af05e7a1a9628b9881d137b50544584b084dc592167b975ad136ed92bd4b2148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7377562591b9b386b67cfc48c533626c178f8e831d35d241081c9a7ec1181ea`

```dockerfile
```

-	Layers:
	-	`sha256:d2c3da83fb8953ce6ba3fededc781e93e1bd3ab4e9c377b9ae47be81c7fc2b87`  
		Last Modified: Tue, 09 Dec 2025 02:07:03 GMT  
		Size: 2.4 MB (2375879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0876006a7f26f5c8bf37922893fdb945080b6f6f22699ac11e8661fb51f0f14e`  
		Last Modified: Tue, 09 Dec 2025 02:07:04 GMT  
		Size: 29.8 KB (29822 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:79abb36c01d293cba035a1a97bc2e017e0c33e6b711b2819337f41fd1aa0bc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52447344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d2af51b03c6453ddf236a4d612e03d36d41c57939622c6bc7d58160132e8f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:00 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 08 Dec 2025 23:08:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Mon, 08 Dec 2025 23:13:24 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Mon, 08 Dec 2025 23:13:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:13:24 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:13:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:13:24 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 08 Dec 2025 23:13:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9932af406cdcafe888914aeccbbfd495b8659cbb94b1eff57a9f8e2525c7b9`  
		Last Modified: Mon, 08 Dec 2025 23:13:40 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec619332fda12d1caa3058e6c64ba6e51c212abe573e0e3a5abb0a634944149`  
		Last Modified: Mon, 08 Dec 2025 23:13:39 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc53e9f6c8eeb4fac8a07fa88a8b92826cc55bf02852a9dd44a2ebe7313b57c`  
		Last Modified: Mon, 08 Dec 2025 23:13:43 GMT  
		Size: 24.3 MB (24340906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca582f13b52b8e2ec155899d9b09557e13001d52f000a65a7b38bdef44d91f03`  
		Last Modified: Mon, 08 Dec 2025 23:13:39 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dce6b69f21b7ddbd70b9a297205d1d072c60b071000d1d7306bfb719789f7ec`  
		Last Modified: Mon, 08 Dec 2025 23:13:39 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:3bef1ceab41afb1bdf8e3a827ba709b95808facc7f7bacebac86a0006eaa7668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a94a52cb4bb5e8d639b0cede0f5ec7c25ed6c36789812bd6aab29c3106956a`

```dockerfile
```

-	Layers:
	-	`sha256:f3a9eadbe0ff0c06995ef695ba4bd475a6d2b5a33da5d3939d17527d0dcb591f`  
		Last Modified: Tue, 09 Dec 2025 05:05:23 GMT  
		Size: 2.4 MB (2373931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca6b5e95f6c2c7e8a9c3c797608018c04d029167d37cb0d2ca78c79121cbfcf`  
		Last Modified: Tue, 09 Dec 2025 05:05:24 GMT  
		Size: 29.9 KB (29868 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; 386

```console
$ docker pull redis@sha256:74a27985321f06e8d3a74e93c2fd1a527e855a0812d7d9be9a60a8930bf26c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8cd3cd453587122d9dfe59115294906705b5ffa7b8a116d5ab1fa7be99f50e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:16 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 08 Dec 2025 23:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:12:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Mon, 08 Dec 2025 23:12:20 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Mon, 08 Dec 2025 23:12:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 08 Dec 2025 23:12:21 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 08 Dec 2025 23:12:21 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:12:21 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:12:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:12:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:12:21 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 08 Dec 2025 23:12:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bbae2a86fb92ffd9315b285f586e662f0a499019e957397c4a52acae6d706`  
		Last Modified: Mon, 08 Dec 2025 23:12:37 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a9fd1f0791d6886b3187e648b925dc38048daf4ea375efddb74d26badd7727`  
		Last Modified: Mon, 08 Dec 2025 23:12:35 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d10906d7e224ad8ee77b97d644751a14f6413183294601d492991fed9486cf`  
		Last Modified: Mon, 08 Dec 2025 23:12:36 GMT  
		Size: 15.5 MB (15486115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32352207a822086ce0dbbe5c8e4e7e9869e0f32dcade810e78bfad6876377855`  
		Last Modified: Mon, 08 Dec 2025 23:12:35 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b6ab5609da4fc1a1613f0fd2e296999b7a6354664c1a136538420f2568865`  
		Last Modified: Mon, 08 Dec 2025 23:12:34 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:7e9a9099f4efbce669eb8002a5da2c10d4aff72ae3fe59f660a27c3372a867ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b443d32eab6fa280c76c1197596f0c84ed9b2417bbe5d5e574addcefb391dd`

```dockerfile
```

-	Layers:
	-	`sha256:a2559a4745c933a65badfda96e530bf47868213b422812b77eaf097dddcbc17c`  
		Last Modified: Tue, 09 Dec 2025 02:07:21 GMT  
		Size: 2.4 MB (2370789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c5cee4b5ca87a2bce377c58adf60f9d0a1dfb24a2014852d2bc72931a4628c`  
		Last Modified: Tue, 09 Dec 2025 02:07:21 GMT  
		Size: 29.6 KB (29614 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:182f6d684799566da3ddb4b5f214cd38f09f6150e7bfee68834d7503a44b4e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44633065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58672bd5d7682bf8ed1ad8dcd0ca0bfe22a57f4b0a6ab61fc8b3b4c8f96e482`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:27:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 09 Dec 2025 14:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:34:03 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 09 Dec 2025 14:34:03 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 09 Dec 2025 14:34:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 09 Dec 2025 14:34:04 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Dec 2025 14:34:04 GMT
VOLUME [/data]
# Tue, 09 Dec 2025 14:34:06 GMT
WORKDIR /data
# Tue, 09 Dec 2025 14:34:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:34:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:34:07 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Dec 2025 14:34:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe183e86bc5e2b40f4c30e7e177fc5a974454e886f5552caad5dc080695315e3`  
		Last Modified: Tue, 09 Dec 2025 14:34:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094f1894b6458db814134e5b9f40e2cfb1332a2e25eb26ed10e088a138243a2`  
		Last Modified: Tue, 09 Dec 2025 14:34:45 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8b7935de6bac4eb6bab4bd207ba1a074cee092ab80128516c0a14015e3541b`  
		Last Modified: Tue, 09 Dec 2025 14:34:47 GMT  
		Size: 16.1 MB (16115049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c9621382c2a3322c6c12e2ae626edb9452fe47f0f52fa59c967563e2a1060`  
		Last Modified: Tue, 09 Dec 2025 14:34:45 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd9c9c0f46f791512ace799c7d37f3b8a1f0391df60a793a8a9dae95aed5b53`  
		Last Modified: Tue, 09 Dec 2025 14:34:45 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:2fe45221ea2a2e89d8e4997e40af62f73ba55669324b66d215f743e0fb4ffc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7306a27afe0980ad1c5730b8bb4c38b9e1641e4dc1de0b7b16f69674978011fc`

```dockerfile
```

-	Layers:
	-	`sha256:df6dc8c463fec861fa38dab17e71a7059ba6aab90e91a1a1a903a9006f874dc0`  
		Last Modified: Tue, 09 Dec 2025 17:06:11 GMT  
		Size: 29.6 KB (29568 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:4f931e08e9a18aa5a51293878d7e7724146626bd31c25a0a2426a328508f3b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49296384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d0e9b63ab8423fb4b1888fcf03b5c2dbb992217bf82823f4384cca3265bc01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:13:29 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 09 Dec 2025 14:13:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:15:25 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 09 Dec 2025 14:15:25 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 09 Dec 2025 14:15:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 09 Dec 2025 14:15:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Dec 2025 14:15:26 GMT
VOLUME [/data]
# Tue, 09 Dec 2025 14:15:26 GMT
WORKDIR /data
# Tue, 09 Dec 2025 14:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:15:27 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Dec 2025 14:15:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f9b71671587fa3336c18ab69611fa672f6c805bf1280f98fea746a206a8fb`  
		Last Modified: Tue, 09 Dec 2025 14:15:48 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce583d0e612f6929a11abefa154d5bad93a1b6296a805253e9ea77c50017afb8`  
		Last Modified: Tue, 09 Dec 2025 14:15:48 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea583081df74f74c5f848478239ab3888935f2567729b3d1ad191c3b6aeb9f09`  
		Last Modified: Tue, 09 Dec 2025 14:15:49 GMT  
		Size: 17.2 MB (17223333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d5076025c3430be740a363a3a32a376407137293f102bdc52bf73f9606997e`  
		Last Modified: Tue, 09 Dec 2025 14:15:48 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c25f707ac040a2ce56d3a92e45e9547ed932ce85ec657b95c4823bf61b9252`  
		Last Modified: Tue, 09 Dec 2025 14:15:49 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:88ebbcd0b7bdd992a4f9783cc072e226b32417a46ee4643363883fd3709b25ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8165a24bbd96c71d9aac87499d54093088bfeb418ae8ceb2eddb2c8a18959ee2`

```dockerfile
```

-	Layers:
	-	`sha256:54dd7c878d63951a73ea9e01f2f91554b1dce1d2a86657fbb35e551a4c8e3337`  
		Last Modified: Tue, 09 Dec 2025 17:06:15 GMT  
		Size: 2.4 MB (2378032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60df978664f25b943b8fe55bc287825da0133846901400913410f4a3bcbd3b39`  
		Last Modified: Tue, 09 Dec 2025 17:06:16 GMT  
		Size: 29.7 KB (29746 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:fe89c019a8c4e9b48f959db858eb131890de5a5e151fd426dec885d08544a2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42902049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264513ecc3bcd33b981cc71441261022763f0c08350055f53596a122db2bdd00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:03:39 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 09 Dec 2025 00:03:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:04:40 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.4.0.tar.gz
# Tue, 09 Dec 2025 00:04:40 GMT
ENV REDIS_DOWNLOAD_SHA=b947d9015622669b5bee8ec954f658b3278d42dbefae23a92d9b7704bfe143f9
# Tue, 09 Dec 2025 00:04:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 09 Dec 2025 00:04:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 09 Dec 2025 00:04:40 GMT
VOLUME [/data]
# Tue, 09 Dec 2025 00:04:40 GMT
WORKDIR /data
# Tue, 09 Dec 2025 00:04:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:04:41 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 09 Dec 2025 00:04:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0a0a379d6d4a2710ce5b7318052e698ca0d5e8fd10455ad043a2af7f5b0cb9`  
		Last Modified: Tue, 09 Dec 2025 00:04:58 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca62ae59c500e2e6c06a824abdca056d4f4ed1bb4efeabf48d1f6b03c01c92cf`  
		Last Modified: Tue, 09 Dec 2025 00:04:58 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bd9309dc7fab886a355daa3519f10f2221c685f87833fa4e70ad64eb536ebb`  
		Last Modified: Tue, 09 Dec 2025 00:04:59 GMT  
		Size: 16.0 MB (16013410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91faf9ae9b3a2e62592d70a5d78ba0b707b620c9a39e76dfdd0d23c148289c`  
		Last Modified: Tue, 09 Dec 2025 00:04:58 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cbb2c9501469fe662e64bce20d561107371c3ca7a2915bdfad258e5304462a`  
		Last Modified: Tue, 09 Dec 2025 00:04:58 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:ff38f72a1a567198c78b4278c368302722ba011bf2b6c2ad8f4f740bc1918c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ce11474f5f5576746f26f327ffd5ab258ff42343cc7dce842601e56ff0e8af`

```dockerfile
```

-	Layers:
	-	`sha256:01bac2ef8f3c500b3d70ce9d1e4c3b541cbef5cf62c22603c5f3eb26edebe8e2`  
		Last Modified: Tue, 09 Dec 2025 02:07:30 GMT  
		Size: 2.4 MB (2370458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac29ae6d5cfc74729dd7e72cc72f528db36700afdd14aa1df87d25283c530f2`  
		Last Modified: Tue, 09 Dec 2025 02:07:31 GMT  
		Size: 29.7 KB (29672 bytes)  
		MIME: application/vnd.in-toto+json
