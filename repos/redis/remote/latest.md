## `redis:latest`

```console
$ docker pull redis@sha256:d318520052025d3cc5850ba3de966810916c7a7b327b412322399f38be39a39c
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

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:b6cd50158f60fec3a8638e485385284bcfb1495617281adba2ceb1b020eb281f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52440907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017b1c12abf9d52fe40dda80a195107ea2c566a0035b59ffcc67af8b4c32c736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 00:26:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:13 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 00:34:13 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 00:34:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 00:34:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 00:34:13 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 00:34:13 GMT
WORKDIR /data
# Tue, 04 Nov 2025 00:34:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:13 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 00:34:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22506777a0967f1dab1482458243f44d5999c59598ba2345179682a43bdab5a0`  
		Last Modified: Tue, 04 Nov 2025 00:31:15 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec27664782f2fa9c102300a9bc5f37d11a8dac0777d6c8da5487b041c43a9c`  
		Last Modified: Tue, 04 Nov 2025 00:34:29 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60b18d70d8666d5a02605836237e5a14f5f6687f2485550b8417018e2dd9b7`  
		Last Modified: Tue, 04 Nov 2025 00:34:32 GMT  
		Size: 24.2 MB (24208129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729797e636a78925c7402aadf339e83c482757792f152016f52cd9ed8ae51086`  
		Last Modified: Tue, 04 Nov 2025 00:34:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c981fc7c62107e8a2e8837e0867946a55803bb70858b75c758885712169e94a`  
		Last Modified: Tue, 04 Nov 2025 00:34:29 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:3f964922f37cf75072e5ecf2126e97abc9c7b88cad9fadd7ce26c5c858b01080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f86efa349d9b51a7369bf6c777b47dafc5ca8d6143ff9ea29678d5c374d1f6`

```dockerfile
```

-	Layers:
	-	`sha256:a683b50407f2f382e6a06366996ae067db20c44cd36b482bdc286e8302f41f61`  
		Last Modified: Tue, 04 Nov 2025 11:08:32 GMT  
		Size: 2.4 MB (2373626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32897d9501345f16a4f57234351ee7ac9eacd54f3065c5ee79926e5ece8ae8b`  
		Last Modified: Tue, 04 Nov 2025 11:08:35 GMT  
		Size: 29.7 KB (29672 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:b76e5b85bebeaf8ee421a5d88ad6c70f0b3830756362f624c3dd4a94b795bba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41117115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3221081c7d76380d6b3e528891735c16c45c36d5e5f9ea195ede92d46c248dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:23:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 01:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:24:59 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 01:24:59 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 01:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 01:24:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 01:24:59 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 01:24:59 GMT
WORKDIR /data
# Tue, 04 Nov 2025 01:24:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:24:59 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 01:24:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8176e188a5ea5487d369614fb2cebab9001c2eb2aa3a7c4781a6cd97a48563a`  
		Last Modified: Tue, 04 Nov 2025 01:25:12 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b773fd41b771acf327bc83f6c35165aa6b4c30c97ffcd5ae9f87a14aa50906`  
		Last Modified: Tue, 04 Nov 2025 01:25:12 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ff8659b42aaa69fd4f0826156b7500e2b64dc4e6334313189c1c42cbf0f820`  
		Last Modified: Tue, 04 Nov 2025 01:25:13 GMT  
		Size: 15.4 MB (15355252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4c8fddd28d42e85b79c76f1a8c3c495ecef334ad0f4350ab25b3b86ec8a7e1`  
		Last Modified: Tue, 04 Nov 2025 01:25:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a613aef41f80804bdf686c54302b57116603eaf683e4eeac53ef100a8f4fcca8`  
		Last Modified: Tue, 04 Nov 2025 01:25:12 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:665447c7d737e706ce49fa3e341cbb21756ac278d216583797a0a139cc3a6ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a52b1575b3454bbc3652dadd3fdc144aaaf8e5036a1d065656fd99c06d00cd`

```dockerfile
```

-	Layers:
	-	`sha256:d8e79367b0fdf6c2edd0b533d5dc057f350582f07433baf1d384401b80adbaa9`  
		Last Modified: Tue, 04 Nov 2025 08:05:55 GMT  
		Size: 2.4 MB (2377462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283bb724c31725bba4ed60faa46bc0ab6dc71dd3996c0a6d46d33f38fb04f816`  
		Last Modified: Tue, 04 Nov 2025 08:05:56 GMT  
		Size: 29.8 KB (29822 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:851d148f94b8aa558d56d048f682dd823b9474069c583038e7ac25a945ecf28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38935022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d31c962d58f739ed793f6a310a070e9acca081c11c6e4d338346c4e8b3ceb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:17 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:29:15 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 00:29:15 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 00:29:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 00:29:15 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 00:29:15 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 00:29:15 GMT
WORKDIR /data
# Tue, 04 Nov 2025 00:29:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:29:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:29:15 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 00:29:15 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ba9fb4748e629052c4240fc8dfa30d3d557e7ef33d114f2bd5bdc0e04cfb74`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b0640ee5da65dab848fa882ff665c77d82e649eb315d318b72d81743324cdf`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd363d17b9b6879f2cc02e5998cef9369065dcc511cd3c82442dc149bcd4f616`  
		Last Modified: Tue, 04 Nov 2025 00:29:40 GMT  
		Size: 15.0 MB (14996692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eace8cddb4ae348929a6f92c79878dd20fc9aca8c1b99b28ab3095ba083b3cfb`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a216bce884371f14aad026f78c2968fd4a95aabdb8cd281fecaa14c07fbe891`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:933cdb55fecdecbfa1d7f5f782995524f1d6b068c16e5f18a56808ce6055030d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dff1f5b801ebec1949d6f0941aae7997633eb1e5cf9fbb8dc96659080969008`

```dockerfile
```

-	Layers:
	-	`sha256:bd75625b0ebaffd6907a2018f3ff729ee5d2d40a48157cf439196d30278f7963`  
		Last Modified: Tue, 04 Nov 2025 11:08:41 GMT  
		Size: 2.4 MB (2375879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a17ffdc7eb62608a1785514073a45d0da22246947fac3f9d6ef1d4ee16dca3f`  
		Last Modified: Tue, 04 Nov 2025 11:08:42 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:07bbefab85debf3ddd9a840a98ede602f9aa15389707831061c215291b74aa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51898371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270303235932f6f767a9f35cafa598f44b9e6c4c3caf052d74e6ceca40f82b39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:08 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 00:28:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:55 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 00:34:55 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 00:34:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 00:34:56 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 00:34:56 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 00:34:56 GMT
WORKDIR /data
# Tue, 04 Nov 2025 00:34:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:34:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:34:56 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 00:34:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8d328aa30f90028b57a46782e088bf199556a3fef7f0b23ddefe5bd2471fce`  
		Last Modified: Tue, 04 Nov 2025 00:35:12 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a43c015a6824d6839ce7e69c8c362e62bcfe6ba974c5180558b3d68aae3beba`  
		Last Modified: Tue, 04 Nov 2025 00:35:12 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f585395e02f5b00e9428ef100fa49cdb3a2dfdbbcec1fe31e165ef8a2c2e88c`  
		Last Modified: Tue, 04 Nov 2025 00:35:14 GMT  
		Size: 23.8 MB (23791783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae7e27b42c9f8e0075d70480f32aa4c371b877b2f6145c8b28a965753eafa99`  
		Last Modified: Tue, 04 Nov 2025 00:35:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a316313799b0808b59916fc3d01af95e800a4cd463d55268736a31ab4ef9c676`  
		Last Modified: Tue, 04 Nov 2025 00:35:12 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:917cc5a8faded49a545b48116a9353917f7e6d7b52a8b9fc965923f041b5e7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d84ad3a2ed8c21e7c869f996e308d562c5b405a468af45b0e341ed5f2c30b0`

```dockerfile
```

-	Layers:
	-	`sha256:c2c920b3aaf7580d5dede5ac9bb93a559a6a4778008a1b2fde70bcf5a43d7762`  
		Last Modified: Tue, 04 Nov 2025 11:08:46 GMT  
		Size: 2.4 MB (2373931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8904fd9e7eaa7712f925cbfe6a386d3052bc0726c19b81c020b1a50e54d86552`  
		Last Modified: Tue, 04 Nov 2025 11:08:46 GMT  
		Size: 29.9 KB (29869 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:873414ee61eacb6056425244092f34c77aed65f9d0dcf7821107e90f7d1b819d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44389598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c04d497672044ff0e0dc1f74c4a63f961b39d990bea65386839e8a4349f3741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:23:57 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 00:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:59 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 00:24:59 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 00:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 00:24:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 00:24:59 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 00:24:59 GMT
WORKDIR /data
# Tue, 04 Nov 2025 00:24:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:24:59 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 00:24:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4550e1aa0e910a5efb947e63971290facc6f25ed51cca3c9899e1df53451f8`  
		Last Modified: Tue, 04 Nov 2025 00:25:13 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba94ff53687077e637d70539439eb6fa87f276dc52b9c8c5b2bbd5ed542df2d`  
		Last Modified: Tue, 04 Nov 2025 00:25:12 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666544ae63c15b747cc471a5869940511226855c3df8c65fd6480e7d134311cd`  
		Last Modified: Tue, 04 Nov 2025 00:25:14 GMT  
		Size: 15.2 MB (15175551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c9c6c9b81b15130f73ed2f62da417ce7c56e07c3f1cfa5685159bd08cb5e27`  
		Last Modified: Tue, 04 Nov 2025 00:25:13 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa93e91a0865eb7c4cda4478d3feb8e3f7520e21c4b39918fda36b8d08399e23`  
		Last Modified: Tue, 04 Nov 2025 00:25:13 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:2c2907a28d55e5519f133f9ad0a02146004e6dc14752644ed2639e06f8ab8ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ee289771ef8d5f33e0781140161e9e4962b05a6ed3a5c881c923ef6077e2ae`

```dockerfile
```

-	Layers:
	-	`sha256:11d946bb0a8036c90daa50444abdf7114931af821a1354c782fa7895127833dd`  
		Last Modified: Tue, 04 Nov 2025 11:08:51 GMT  
		Size: 2.4 MB (2370789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853d834afaeb19b917fa169a1c0006fddc0cd38c1176e25ccf0074b4d3197278`  
		Last Modified: Tue, 04 Nov 2025 11:08:51 GMT  
		Size: 29.6 KB (29614 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:9a66a9065e7373f7b6fe55692875d6268a4fd31818c800e7bdb82769737050be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44288532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b9006d76c44b82dfabe1fcbf29322ddfe5ede3b47e372294221eceff6e2a97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:37:01 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:37:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:43:09 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:43:09 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:43:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:43:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:43:10 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:43:12 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:43:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:43:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:43:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:43:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:67737a113ff8fe4461be953b475f1930d91e20d222e9a1f4e55ddb9bf4c2c6de`  
		Last Modified: Tue, 21 Oct 2025 00:19:57 GMT  
		Size: 28.5 MB (28513717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfe8096667344f7ef5002e9c1982e411f75fed7e5b225031f74146e6a5ac017`  
		Last Modified: Mon, 03 Nov 2025 17:43:52 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19f078d5533ff68c55bfb86041a6b905239998050f23fc778e2904ed307835b`  
		Last Modified: Mon, 03 Nov 2025 17:43:52 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b23367a0e549e9c4e2c968f70aabb750bc080e29b1cf80c7f99440baf2bacb`  
		Last Modified: Mon, 03 Nov 2025 17:43:53 GMT  
		Size: 15.8 MB (15770589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ba30cd3cf504f62777c68e717c5ac3608f55597aaf4027dd3e8fbea00b3e67`  
		Last Modified: Mon, 03 Nov 2025 17:43:52 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4753c00164c27f34a3bdae7c464109c74fd0509fd8ec0b05c54116b5cf4672d3`  
		Last Modified: Mon, 03 Nov 2025 17:43:51 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:e547162e82592a1eb495e0f2d0badd72a9674925597d728b1652ac11409fc949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ba1521594c6f5bade215748d4f6287b9d7c502546abc1a080d5745d0f168dd`

```dockerfile
```

-	Layers:
	-	`sha256:a7c8c0d39d12ee28557ff919c2b6a59228026e635410cf77087be229ae64e08d`  
		Last Modified: Mon, 03 Nov 2025 18:07:34 GMT  
		Size: 29.6 KB (29568 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:36672bc4a48cee26029ad48e0db1df76f43d90d58c30fe213eed7ba6278b1a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05fc5524f1738f4acefff85d17c662c33962b692741368aa7e8bc009700afe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 05:56:24 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:57:51 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 05:57:51 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 05:57:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 05:57:51 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 05:57:51 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 05:57:51 GMT
WORKDIR /data
# Tue, 04 Nov 2025 05:57:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 05:57:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 05:57:52 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 05:57:52 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a89ae01cefb31afd038d45b0b95fdbdeeabc787270a7edebb661c04ba406bd`  
		Last Modified: Tue, 04 Nov 2025 05:58:19 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b7809c02d2f8fa2836b1b5d6535f758840324fa91cbc52e99c6bb96cc4bd59`  
		Last Modified: Tue, 04 Nov 2025 05:58:19 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e9e7c611a8b1b15b3e69bf27b3caef7b5c59b968e9767d07e43fde0c02a10`  
		Last Modified: Tue, 04 Nov 2025 05:58:20 GMT  
		Size: 16.8 MB (16835612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd1f853009b7d164db13bd40959ed1bdf089ebe4e523dc147010882b8f2add`  
		Last Modified: Tue, 04 Nov 2025 05:58:19 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2cf96df05f6ab9785b510fb1a85902f444fb6a785f4b5adcfac23c82252597`  
		Last Modified: Tue, 04 Nov 2025 05:58:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:fa1269d8b24a89a380c3581d227874fee826f0be71345a901c9721bb7d01f5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8e4596af6d60115c69e97883f2d29564a3a3fa5f0242be133bd2c05707cbc3`

```dockerfile
```

-	Layers:
	-	`sha256:a2deed216c95b94b41aeb27266133b99bb2c76e87417543d75fe6eec12aa0051`  
		Last Modified: Tue, 04 Nov 2025 11:08:56 GMT  
		Size: 2.4 MB (2378032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d60cf23d79759d1d9cd7711786a9ed33fcfd48eb03f858d1893d399b21c6aa`  
		Last Modified: Tue, 04 Nov 2025 11:08:57 GMT  
		Size: 29.7 KB (29746 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:91b76bf501e71fbf59cf4d3ec93636e8b80441284c9cf6d42ccde51741bc1243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42554987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553a5cc533001bad4c699f90919268f609015ebf53b55fb1c3db95194c770816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:04:38 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 04 Nov 2025 03:04:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:05:47 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Tue, 04 Nov 2025 03:05:47 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Tue, 04 Nov 2025 03:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 04 Nov 2025 03:05:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 04 Nov 2025 03:05:48 GMT
VOLUME [/data]
# Tue, 04 Nov 2025 03:05:48 GMT
WORKDIR /data
# Tue, 04 Nov 2025 03:05:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:05:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 03:05:48 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 04 Nov 2025 03:05:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fe7c2a1ae660861cca9677280e1b7a2947411e6541f5e5bdc2d0f1ce998515`  
		Last Modified: Tue, 04 Nov 2025 03:06:12 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4149e4125514dfc5dd874845a60bc1770aebc1b63cb19125e091cbf31d0cbf7`  
		Last Modified: Tue, 04 Nov 2025 03:06:12 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502dd4833880cc4374ed696f4a472c36f22f40caa7f8d00c23d8fab2b3e50117`  
		Last Modified: Tue, 04 Nov 2025 03:06:13 GMT  
		Size: 15.7 MB (15666233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9844527cc4a88fef7091a0d1238def4e6f867b95cf1ef1d7671dfcf14b115c`  
		Last Modified: Tue, 04 Nov 2025 03:06:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0fe218aa32e789dc24402a776058af3694178c5db279bf64ade62d84f6c06`  
		Last Modified: Tue, 04 Nov 2025 03:06:12 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:d712e4f8026688dd18fea1ddbe90ca965fefa62fcf438089d79037613be20fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c97134a8c31d0be4786a09b2290a6663208b3aedc68b6b1cc68b76b05779f9`

```dockerfile
```

-	Layers:
	-	`sha256:157e7424052b260a9e05ec08d4bb75b3f75d5fc38c8bf500be8ba86a7b9710f8`  
		Last Modified: Tue, 04 Nov 2025 08:06:12 GMT  
		Size: 2.4 MB (2370458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06c25bc252d03cefb4fb5d535c07e3e55b7e098a446fc55e2893ff32a7ad851`  
		Last Modified: Tue, 04 Nov 2025 08:06:13 GMT  
		Size: 29.7 KB (29672 bytes)  
		MIME: application/vnd.in-toto+json
