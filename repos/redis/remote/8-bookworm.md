## `redis:8-bookworm`

```console
$ docker pull redis@sha256:dbda186a12cf9a780a0991529a4a4007403e2374da22421363c30dc853d4cc1e
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
$ docker pull redis@sha256:3e3982fbc94dd878eaafd21c068aa8ed9f6246440676849cca46bf46f9c4012f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52439784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e5b1da2ef27f8c769875a8b17a50edcb0731ac9207b47b0e22306d95362bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db098501f0180a914d9fb6113596aae512ba1074f116a04becfef0fd2b9e347`  
		Last Modified: Tue, 21 Oct 2025 01:46:48 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19d868f3520c1c625e233247074e3087fc3f86d2f7e473da8f93d73872532a`  
		Last Modified: Tue, 21 Oct 2025 01:46:48 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89fb5fc7ff710de261eb00dfe8cad7b85b842056521e765cd64fcde306b475e`  
		Last Modified: Tue, 21 Oct 2025 01:46:51 GMT  
		Size: 24.2 MB (24207248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4668b306bc3de6a44034f41969353ef8b9bcf952c969dbdc2ff3c16b2b0f24`  
		Last Modified: Tue, 21 Oct 2025 01:46:48 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e796aaa0bae35accf59feb53d75f2232e5733c170f172bbbcf4a4d0ffeb48e`  
		Last Modified: Tue, 21 Oct 2025 01:46:48 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:deadf5c9a66189e3e87e04a273b36f3686a43793d3cb666c68ec33429b16c023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab98e7436ce07831615fc624bc69853d238c2c2ff8b57d6a219ce1c26f90a6d`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1cdefc161f022cb40c1c801796df06fd4085a85e6316752724e8aeccef5a9`  
		Last Modified: Tue, 21 Oct 2025 10:06:16 GMT  
		Size: 2.4 MB (2373626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db6821b4d936dac4165045f5903ea92c3e621d33a1b902d42dacae65d200bf3`  
		Last Modified: Tue, 21 Oct 2025 10:06:17 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:30ef8b4a8e58a09ee915f67adfc8018302c292ccaf2ed7d154ee5f26e59876d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41116497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24de3c77fc64f434699912363ff6cef09d7ec2a80775faeaf26daf7b06f1f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deb77ce3fe9d702a77b781ebad833818d28d1fad74bc4346b0c3c017a134d87`  
		Last Modified: Tue, 21 Oct 2025 02:18:54 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af60431b3112ff07999abf60080d6bc7885478fc1b40a4c3961ce9f345dd23`  
		Last Modified: Tue, 21 Oct 2025 02:18:54 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b5731b641343dd2307d3d6b9f8b91b5fa46c3a487b0c866c1a47425bbb474e`  
		Last Modified: Tue, 21 Oct 2025 02:18:56 GMT  
		Size: 15.4 MB (15354792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de87ce47e66ad8c1670b492f988a7866611cfc7afbd3cb3d1932dac7e2a2faa`  
		Last Modified: Tue, 21 Oct 2025 02:18:54 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52263d9bf0f961a25ec8e7d012dbeec2582a4a450f048548bf4aa1cf4e3df043`  
		Last Modified: Tue, 21 Oct 2025 02:18:54 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:b19c54037fa29c6589e14398fd02fb1aadff22203dcdc65aaa221d1c93df2a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5360d78b2c34bffdbca120d32d1db3a1c4fac5a2ba6dffbdf3ea9ceea5f52453`

```dockerfile
```

-	Layers:
	-	`sha256:35d84e2dd36258bd204bb1e3846fc8b1962598eb0afbe6f1d042a83a3fa60a04`  
		Last Modified: Tue, 21 Oct 2025 07:05:51 GMT  
		Size: 2.4 MB (2377462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179ccb25716bb52cf9765b939660c23acdb4b3d543f3bd5b6240bac64b1764b3`  
		Last Modified: Tue, 21 Oct 2025 07:05:52 GMT  
		Size: 29.9 KB (29866 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:d6ce71c9725db15c612b32d26e94bda0b8858a31138743eb2d7b51d3386a5c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38934611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2939928b40f503db0f94d89623506de63de07e65a6e073fe8f450d590a9eb588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499c2e208ea028459000fd92ea52b267e7bf0bb9e2399238e5dfdc0af8e90d8`  
		Last Modified: Tue, 21 Oct 2025 02:32:42 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6195a2cebb056ea76ec82089a2dde838e8eab8f7dd8ddbb4c2a64d025479fc71`  
		Last Modified: Tue, 21 Oct 2025 02:32:42 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe5e760030852dd3757d22a1a1ffd0407469ed74c534146dfd700e7d0f368c2`  
		Last Modified: Tue, 21 Oct 2025 02:32:43 GMT  
		Size: 15.0 MB (14996379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2bd9392c12cdad9311234a073de5e037f05c51d416f23702e82730c2a47edd`  
		Last Modified: Tue, 21 Oct 2025 02:32:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e9108ce7586d9d4c55b1093f57250a6fc5a9a0b4ee2186e1c4bc60e1dc733e`  
		Last Modified: Tue, 21 Oct 2025 02:32:42 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:1551ea9d238e6d776eb5c520f2247091691fe5cde8c03c59fac29976bb2c5d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92394b3522981b3cee84b4971a9b387459e4898ad8659f844f8989c41284c7c0`

```dockerfile
```

-	Layers:
	-	`sha256:b70eff0c7c8e83fedbf1d45aa16e5d600e524a7952dee49cdb916fdbedef6cdc`  
		Last Modified: Tue, 21 Oct 2025 07:05:55 GMT  
		Size: 2.4 MB (2375879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a36875a5e7959bf7fd358bb165f598682909dcf0b6bf56febc68898da6cbe7`  
		Last Modified: Tue, 21 Oct 2025 07:05:56 GMT  
		Size: 29.9 KB (29866 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d8bcbaa48ddf6e88479e36b4dd28c3c2a91750efea80d310975139f7350a22ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51899109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51427815565fd6189270196007a76b5f04a1f420940fa0c92a48b9d3f796f3d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e98ec0b9a176312ffd04d83c7b76fdea198d4196fea91a79b1e1010c90a2b1`  
		Last Modified: Tue, 21 Oct 2025 01:50:48 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb69b944eefe041c10b0842a32dee074f5822c64ff56b3e145a97b8760e822`  
		Last Modified: Tue, 21 Oct 2025 01:50:48 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a71f4220f1313d350f1845f126c0b3da53ef156df0cf131cf5c66cda582a1c`  
		Last Modified: Tue, 21 Oct 2025 01:50:50 GMT  
		Size: 23.8 MB (23792703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55609c24330b7153b01b8a899d2442d7700033163664d504eb7e6729a6a0f57`  
		Last Modified: Tue, 21 Oct 2025 01:50:48 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afca14402032141896e07faca3f9765c1216bbed6bcf0fafa250387260912ef`  
		Last Modified: Tue, 21 Oct 2025 01:50:48 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:026231294652d24ef3467f81284bded44939515fd6cca667114391562475b6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73640c9211e9493736f33b0422f52f12e3a1bf1f267d20366bf8aa6424ca392d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce61dd0fea78f36def72fd30b101573082e730081ce16ff8b90c3774c94de12`  
		Last Modified: Tue, 21 Oct 2025 10:06:25 GMT  
		Size: 2.4 MB (2373931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8760ea4c03a3a7af34e2bd5ed263fc7e35dc0facbe5eded19378ce11ce307fd9`  
		Last Modified: Tue, 21 Oct 2025 10:06:26 GMT  
		Size: 29.9 KB (29912 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; 386

```console
$ docker pull redis@sha256:e5aafc7cecba5c418f744d1d16b82ffa30b7445df0d769082f12651c661f6880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44388524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d226874b90efb697efb382a83499b2b8f1b04b547a09f0e3f76bde1d2a8eaf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c784b836bbb9ff8c9c9f60f5e05f62257527428e17b3d206672ad0897ad9af`  
		Last Modified: Tue, 21 Oct 2025 01:51:24 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1be6f2fb29072114637184bddb5cedc79645f1c2088fd55375b61a2e02b720`  
		Last Modified: Tue, 21 Oct 2025 01:51:23 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7f7de52db89b02bc42859e95e883a74dd07be5661adbcc1403b26b87c1581d`  
		Last Modified: Tue, 21 Oct 2025 01:51:25 GMT  
		Size: 15.2 MB (15174642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb5f4806068063e292687af6eb6033523d5399c26db50d37a0386652602899`  
		Last Modified: Tue, 21 Oct 2025 01:51:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016a1b10529aee5fd8e7fa91b04f1d5b26485e8dac00bf50565b31eba9b90b43`  
		Last Modified: Tue, 21 Oct 2025 01:51:24 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:a77b80caa8d623d44a6b574cefeea63306cbcb45c5ea358af73930b6232cc7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718f78d24e524705b6a7055964505622d7c5ab75ea819025e5ef9d96fead3288`

```dockerfile
```

-	Layers:
	-	`sha256:338b2997065574a81a23bcc6c41275c333f15bc66cfcd3945a766d326a774e37`  
		Last Modified: Tue, 21 Oct 2025 10:06:29 GMT  
		Size: 2.4 MB (2370789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4815d859acfac0dadfe83f411b1dfba1609432acebba7348695e330ca1c7d6`  
		Last Modified: Tue, 21 Oct 2025 10:06:30 GMT  
		Size: 29.7 KB (29657 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:d655ea05dacc712ec9072b553a1c8f635ae96fa4508aa25671607f5ef386608d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44287945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86339b6d2407d22191e0a6d4b49173d40fc197666d75075d55960a5dda4b154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
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
	-	`sha256:27878b507f96d9a5d3ba4ffb43a8b608b6ee37f3a3db0e552f60918bc4e0704b`  
		Last Modified: Fri, 03 Oct 2025 16:19:12 GMT  
		Size: 15.8 MB (15770056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2661fd16574b435add511988d3603c9c837236d8972cfcaf74070898847ad082`  
		Last Modified: Fri, 03 Oct 2025 16:18:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239826294ac13588835d1c94e565933802e19d84649bf176447035888b6276c9`  
		Last Modified: Fri, 03 Oct 2025 16:18:57 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:990941b8ac59e1b73fc4dc7d52768c9576c349f0273aee09d672509fd83c4472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2342c373f98925366d0a8196dd49839d12247737009d8c0fef5642d4dc44649d`

```dockerfile
```

-	Layers:
	-	`sha256:57be1b76e77f936c584f3928c3adb75b0652d7746aad269a1f176cf02819d8cc`  
		Last Modified: Fri, 03 Oct 2025 19:09:27 GMT  
		Size: 29.6 KB (29610 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:4c03077d81df314b41c3b312aa2a3969fb08ceecc35f591441e12bacc6107e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0077effecda3b89018c012c913cbc09551927485aa88cbdecc0cb616ee66ab34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
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
	-	`sha256:3280b16000444817b0cf00cee121616f99feb8f2daeb4c691d1274d447d8550e`  
		Last Modified: Tue, 21 Oct 2025 07:14:28 GMT  
		Size: 16.8 MB (16835535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fa5dc07f208530fc33410785522e7a7ea639cbfe7ba8aa5940fb1e547ec553`  
		Last Modified: Tue, 21 Oct 2025 07:14:25 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b931dca1c660b488ef74c708f7d54386f1b1769ec7e423e04fe76afb4189723`  
		Last Modified: Tue, 21 Oct 2025 07:14:25 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:800a24add13a624b6f4a91beddd5e42f85e2d3bee95316edc8887554d25abf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c2f86ebc98ec4330b186145024863868d8db706191f06b27414cb137fae2b8`

```dockerfile
```

-	Layers:
	-	`sha256:536229bcaf47e6b0e1d653a2571545d10b543aff30a5d8ed67aa63e2a53b8aca`  
		Last Modified: Tue, 21 Oct 2025 10:06:36 GMT  
		Size: 2.4 MB (2378032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5f6d6f4d102aac3e0ef8e59fb00cd841092759a9e523803e1acc2b9f153419`  
		Last Modified: Tue, 21 Oct 2025 10:06:36 GMT  
		Size: 29.8 KB (29788 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:40a71e8eb6c2034012fec79706235962cdf0b544a6a5e46ebb401c86b2e9279b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42554974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db11f96a192086014ecaa4bb0507eeaed2d150568de4e71e366045d784a0bcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 03 Oct 2025 12:18:48 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.2.2.tar.gz
# Fri, 03 Oct 2025 12:18:48 GMT
ENV REDIS_DOWNLOAD_SHA=e355378d7f97efd06321fff881efc452a9673cc27b3a6d0dfd2a45fbcc83349c
# Fri, 03 Oct 2025 12:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
VOLUME [/data]
# Fri, 03 Oct 2025 12:18:48 GMT
WORKDIR /data
# Fri, 03 Oct 2025 12:18:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 12:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 12:18:48 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 03 Oct 2025 12:18:48 GMT
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
	-	`sha256:45897ee5d731e2e78c5f3f46b9ee8e1873ff2d1d2d952e7c916f3a89e271e65c`  
		Last Modified: Tue, 21 Oct 2025 11:46:18 GMT  
		Size: 15.7 MB (15666404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421eacd4f44dd91af287772022262f8b71d2e49f355c71c766a66ba0e26a9eb9`  
		Last Modified: Tue, 21 Oct 2025 11:46:17 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6183883c1d33426e797b4f549effc74d5ffbc1a9f56dab2c839c9645eff3acab`  
		Last Modified: Tue, 21 Oct 2025 11:46:17 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:133e21008ba9a6d1c52d92e9b521a148e2b1ad533c167afeb47422635aa78942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbd950826fe5c8f002cb54ded6dbbe6f209a28ecba001a4b371dab2ddf647a2`

```dockerfile
```

-	Layers:
	-	`sha256:6a2be5d8f2238fd83f9478cd6f6cfa60a6f33391e8a8343a2634b2ad55b94795`  
		Last Modified: Tue, 21 Oct 2025 13:05:55 GMT  
		Size: 2.4 MB (2370458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5985aeb09f8b189f6c9af9732160d19e516b195ae49bc87f78e6a7fce0d99363`  
		Last Modified: Tue, 21 Oct 2025 13:05:56 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
