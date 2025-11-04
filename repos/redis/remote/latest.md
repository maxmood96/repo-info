## `redis:latest`

```console
$ docker pull redis@sha256:1c589f39ec5bb0c553d680b6d7eed3b6e3686b24f87f480dabdd1e64c849aba2
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
$ docker pull redis@sha256:adee9173ad959f0f1a3515ae4c471fdd803e432f2f81dffde99a247f162480f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52440685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a5a1fa49a8a70de885af13ad3c6053914ee26cfbae9e8885bdcd93aba96469`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:37:43 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:37:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:44:50 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:44:50 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:44:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:44:50 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:44:50 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:44:50 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:44:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:44:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:44:50 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:44:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8217cff7f95ee5044c75e88ad9ffdf46e8b80d860c8ba4a35a171dc9eef0e7e2`  
		Last Modified: Mon, 03 Nov 2025 17:45:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3576da3ab552e8679bc34513f1ec5e68f3920129fe06b20f7334640dc5e820b`  
		Last Modified: Mon, 03 Nov 2025 17:45:05 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825a33bb66667718d6fa907274ca590b66c5b1c8eb00e927f3edea2e85fcb8a8`  
		Last Modified: Mon, 03 Nov 2025 17:45:08 GMT  
		Size: 24.2 MB (24208140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279f0a1c640da7b6e84ffbcf84f5f8af1c29f2bbba99fa4d24f0e8de8f046a1`  
		Last Modified: Mon, 03 Nov 2025 17:45:06 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fbcfa87f970fde182f393a1667b0511a925c8194943eabe31ae2c8f221316b`  
		Last Modified: Mon, 03 Nov 2025 17:45:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:77b6d3fd7b9c633c0aa7f8220d631e6864c5ea9772fbf8108c68abf5c2a22cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b6d4ab09b6f7d7a35fda3ed05df0926f41ec5576db9c0c351c35a9715428c`

```dockerfile
```

-	Layers:
	-	`sha256:cde3dd8e78aa14e9a7f731c41df1ffbaedd890322abd5023311c2fea3a0078d1`  
		Last Modified: Mon, 03 Nov 2025 18:07:08 GMT  
		Size: 2.4 MB (2373626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c525e57f859103ddbf9fd91068edb9f43eb234c8c18d44a0ce044a0746d340`  
		Last Modified: Mon, 03 Nov 2025 18:07:09 GMT  
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
$ docker pull redis@sha256:d385cc794b9647467c2a750f10d94f178b20e4dcac9b7d6932e4a24a2c12966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38934890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291052e0e7c0cf5d0aece6f7febc97c664a6f7ab8dab3b770f1a7912aa52dff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:39:05 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:39:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:39:59 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:39:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:39:59 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:39:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:39:59 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:39:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15ae80ec197ccde848fea30103d93e120d48b7e1d5e3b17c2b8d19e336302a`  
		Last Modified: Mon, 03 Nov 2025 17:40:17 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cba48c3cfced1d071350111fa1c493259184e6f79d4986aeaa8ebe29e4d8ac`  
		Last Modified: Mon, 03 Nov 2025 17:40:16 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a63c02bfa2696e3d1dbd0d9736d95bc6ee5c11f52be87cde00ddaf893d56fc`  
		Last Modified: Mon, 03 Nov 2025 17:40:17 GMT  
		Size: 15.0 MB (14996648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f7c13656a32d817b70e3818554bb05adeedaa846299f5e8cb6fcc58bdc1203`  
		Last Modified: Mon, 03 Nov 2025 17:40:16 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c84885565688bdbd1249d4d9ea86c5580ffbcd9d72afa486f595519975c9109`  
		Last Modified: Mon, 03 Nov 2025 17:40:16 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:ffd20ec1f76c46b1dcf6d7b7db3bafdfbe06e79f3f2ae6c809830171f85045a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8329994c94dc481d58251181c80d01f2fea996a26dd1990c83ba710402c601`

```dockerfile
```

-	Layers:
	-	`sha256:0ce4aae5d28c289e44e5ad98f40fa647b9a71be3205aa4ca410738d87a19b750`  
		Last Modified: Mon, 03 Nov 2025 18:07:19 GMT  
		Size: 2.4 MB (2375879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360334d247155bcf1be24c9886bf284e4137ae495222d91adbb2078c9adf3d5f`  
		Last Modified: Mon, 03 Nov 2025 18:07:20 GMT  
		Size: 29.8 KB (29822 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:be46e0fbb5d2df80e6e392b54334f7b07548c91ba81885a87b268aa0c7700b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51898189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9daacb56e0e0c7a6d6bb5c541f7047dd655c50488c9ad7ea9f9458ecaccf71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:37:57 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:37:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:44:13 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:44:13 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:44:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:44:13 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:44:13 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:44:13 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:44:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:44:13 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5d20a52f7b129054facd4c4f8d357e8a99aa880c8877d10e2fad1e9aad9f83`  
		Last Modified: Mon, 03 Nov 2025 17:44:27 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622289bc1cbaaa0dddbd373b9c7105115932581bfa70ca970461d296ee7d9c6`  
		Last Modified: Mon, 03 Nov 2025 17:44:27 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea941de2a1ac8c69f74fbcdb21f030e91e73e16124e0e047b7aaa1155f00186`  
		Last Modified: Mon, 03 Nov 2025 17:44:30 GMT  
		Size: 23.8 MB (23791781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691978d5f1fda08ed3d1c141272ed39ef4d05a394ea695a4f44ab8b1ebba8df1`  
		Last Modified: Mon, 03 Nov 2025 17:44:27 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1266b44a55fbcb5add6d06e181f0288a7fd1a6ef106fbdc8e671a8d874f98909`  
		Last Modified: Mon, 03 Nov 2025 17:44:27 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:54c55b27cea34dcb8f5e6dba5392f70ad409924c58db4ab938066cd4154e4c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f1b67154827b0ab0d3c19080ba7278214542dd5c1cef1e610ca5694ac7a850`

```dockerfile
```

-	Layers:
	-	`sha256:1e079fec9f32d2ef66848c6737ef7de9d412433c977a89b381f630867cb79e68`  
		Last Modified: Mon, 03 Nov 2025 18:07:24 GMT  
		Size: 2.4 MB (2373931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c26c624f71507d49299012a2fb93a51e4e1ec9e14d5606318f3dbb367f1836`  
		Last Modified: Mon, 03 Nov 2025 18:07:25 GMT  
		Size: 29.9 KB (29868 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:2d6722b4cc5566d157228ec3779628d6b6cefbd9ce388d5a2125b3ecec64691e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44389418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e5814911c44bcb086627dc64317eb13cf061209789338fdd55266d80826f60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:37:52 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:38:53 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:38:53 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:38:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:38:53 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:38:53 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:38:53 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:38:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:38:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:38:53 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:38:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa54d782574d04b3c5fa2318710d282b3291002d966db954c56660560db3f52`  
		Last Modified: Mon, 03 Nov 2025 17:39:10 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a76347999d757a7adba9fc7355bd1d8f079d722514de7b6e675528ac6c9d1a`  
		Last Modified: Mon, 03 Nov 2025 17:39:10 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c866d896e280219911ffb5ded1f15d9dcacdfdab90dd047cabd4ccd68ef5fe0`  
		Last Modified: Mon, 03 Nov 2025 17:39:11 GMT  
		Size: 15.2 MB (15175524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af4fd7f24a1957572387ca1a8bf2378769e93b3948f78727325e76824a6ded8`  
		Last Modified: Mon, 03 Nov 2025 17:39:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817f93ff259a89ada5c9313e30a9f5d50b4191f0597d0cd853002d23eda0f62a`  
		Last Modified: Mon, 03 Nov 2025 17:39:10 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:5d78f1bc467fb156a64e92ae9b629bf1077d2939ccb7a6e7ca7938042d483a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde8f78a0439b52789ef2a24c432b40d620a3a1fdcb6431aa67a9c0d392cda47`

```dockerfile
```

-	Layers:
	-	`sha256:b0542ca8fba3c9300696a5393844e1386bd8aa24c87e8b93a6c26e701836f950`  
		Last Modified: Mon, 03 Nov 2025 18:07:30 GMT  
		Size: 2.4 MB (2370789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af52913cd0e08e7015ac8b32d07ac697cf5ce025e983114dce2dcc6938b87954`  
		Last Modified: Mon, 03 Nov 2025 18:07:31 GMT  
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
$ docker pull redis@sha256:b7cc85a962e6fa77f5cd50cc88e7fa3c8e5c7d81d2eb2a185ba8a6e86565aeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9697945cdbbc2a4e21afd938924e6cd01726a0599b2a37237d64c096a66dca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Mon, 03 Nov 2025 17:36:56 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 03 Nov 2025 17:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 17:38:34 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.3.tar.gz
# Mon, 03 Nov 2025 17:38:34 GMT
ENV REDIS_DOWNLOAD_SHA=42d4d3f037db92eea4437ba03f87627cd636ed15a1f2dde7af9650aa94b035d8
# Mon, 03 Nov 2025 17:38:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 03 Nov 2025 17:38:34 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 03 Nov 2025 17:38:34 GMT
VOLUME [/data]
# Mon, 03 Nov 2025 17:38:35 GMT
WORKDIR /data
# Mon, 03 Nov 2025 17:38:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Nov 2025 17:38:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Nov 2025 17:38:35 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 03 Nov 2025 17:38:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e9c257e42d61cb5a25c1e05839ba21af48f97e34f035f0384c8ad46144764c`  
		Last Modified: Mon, 03 Nov 2025 17:39:04 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330f25f319adf8a554c1c9871a905169e37d8e5fa9aaef68ce172cf2b768417b`  
		Last Modified: Mon, 03 Nov 2025 17:39:04 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c3e6206fdc0dc62d57f9923f85c431c2e991d64a3327bd78e5f29d2350adb6`  
		Last Modified: Mon, 03 Nov 2025 17:39:05 GMT  
		Size: 16.8 MB (16835674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73fa94f1183180938af46320f0999e12bfdf7b8bd2c4b9219dbc92c6e097666`  
		Last Modified: Mon, 03 Nov 2025 17:38:48 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78a954dcb84d3a72861181065a286c466fea21751f0c3a921f8b320f76fe71b`  
		Last Modified: Mon, 03 Nov 2025 17:39:03 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:83434b5f6f3cb278d18a42bff576b1ca349cf1982b1316d31938427f0f9a8abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676cdef188f87fe8be2b29b1c39d2f455a8f20e11da5d241e743efc70fc17f9`

```dockerfile
```

-	Layers:
	-	`sha256:d0ecd67cfa795d09a564e9509e7f00bdb5d4c85e88cf5c956462abdb21b28e65`  
		Last Modified: Mon, 03 Nov 2025 18:07:38 GMT  
		Size: 2.4 MB (2378032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35bf9e4fee4995bf2fb137051be26b3087af339909a48344a1eae9836ebfe098`  
		Last Modified: Mon, 03 Nov 2025 18:07:39 GMT  
		Size: 29.7 KB (29745 bytes)  
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
