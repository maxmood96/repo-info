## `redis:bookworm`

```console
$ docker pull redis@sha256:48e2cd000323f73fab10b54ae9a262a2a8460533c3fbc1cbc520bc6464227b96
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

### `redis:bookworm` - linux; amd64

```console
$ docker pull redis@sha256:b83648c7ab6752e1f52b88ddf5dabc11987132336210d26758f533fb01325865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52439729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8c109f88b7b1e08a2ff38f73bf82aff24185247513244d06a1eef26921ad7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa85867e458cd7a42f1418cfe6fa3f16c8dab38984ce51c9a5a90b266dd2bc09`  
		Last Modified: Fri, 03 Oct 2025 16:33:02 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20770aaf8f7b8be54593b23eea462ce81ddc02d32169a1c018b9e9e08ca10c68`  
		Last Modified: Fri, 03 Oct 2025 16:33:02 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4f782b24c86694b58a58bc017d82bff4f54ba39e48f6db6665966362f8f80`  
		Last Modified: Fri, 03 Oct 2025 16:33:04 GMT  
		Size: 24.2 MB (24207176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b0785ec0d039c3dfa1ca93b94eee4fc90090495a08437abf53815b1784168`  
		Last Modified: Fri, 03 Oct 2025 16:33:03 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e44f5a6338c4fce74942b33d9942858dcf3b9f1b29c4344ed60e0e3b36b2ce7`  
		Last Modified: Fri, 03 Oct 2025 16:33:03 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:477edc4c743d7cb01d1ee6bcdbd3a4886ae20a00221ea99341589babb1c8ec92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723d2f0f53d10f2c78f851a1f95f143910db06d3d716633226e77b6a287eb25a`

```dockerfile
```

-	Layers:
	-	`sha256:0da4a8de5351cdbb4b3e3744ba3ee21a4637c88e88e6d074a7d63d3f2dfffd5f`  
		Last Modified: Fri, 03 Oct 2025 19:09:02 GMT  
		Size: 2.4 MB (2373626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af036139953b974cf968af189f6cb1972f466147540b0887589ca1960e3e2971`  
		Last Modified: Fri, 03 Oct 2025 19:09:03 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm variant v5

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

### `redis:bookworm` - unknown; unknown

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

### `redis:bookworm` - linux; arm variant v7

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

### `redis:bookworm` - unknown; unknown

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

### `redis:bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:f5f9251c84737d6ac408a2ad46f5b0106ccc28ed8140e951c07f2b0ea7c98011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51899043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7e962f53cb8271dcda7f2946c9406d60b9a465235faa39c31a2d01844e2af2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc907446c47cf8cf0e5dc23a3c6d9cbd1c4970dc2d858650fc109d9b5d026b`  
		Last Modified: Fri, 03 Oct 2025 16:18:10 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bedfd7c51def6f84f3f7989a2ccfd7ca101f58e9c93992bea90e3b40350410`  
		Last Modified: Fri, 03 Oct 2025 16:18:11 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd85a8f632f4149bd0344f2f39e41f5f5f1733ccef759d823280ea04d97f403`  
		Last Modified: Fri, 03 Oct 2025 16:18:16 GMT  
		Size: 23.8 MB (23792682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a4cbf7c41ab43b10506d474dcc3a24b34079b19804d5cd0ee5d5a0ac711348`  
		Last Modified: Fri, 03 Oct 2025 16:18:11 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1284bf9d175c607da545f4ddf55f02970436f388040bc4feecac52c36b471549`  
		Last Modified: Fri, 03 Oct 2025 16:18:12 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e8f133f74fcc2810ed6a91ca3e50ae69374b5150c6d002ed6363d68e4f5ee472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5dd934b19e8f796a4c6abcfebc8285683f9ec292a3cde9e07e3e6f662dabad`

```dockerfile
```

-	Layers:
	-	`sha256:77edf6c1b0171627617b19c06c48d2eb649c739b7e79d3699ae3a77fbd4966f0`  
		Last Modified: Fri, 03 Oct 2025 19:09:18 GMT  
		Size: 2.4 MB (2373931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbdc9149c6e5172eb0e8159975bec3476e009305ac933d8d19a8b5595d81724`  
		Last Modified: Fri, 03 Oct 2025 19:09:18 GMT  
		Size: 29.9 KB (29912 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; 386

```console
$ docker pull redis@sha256:dc874f095a8dc6425f9b77d42d1fbbb61a1b81597f30700132833e16f1cebafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44388481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7bad0a44655140bd1740eccf6c9deed06d03c0d815dd56f4541f0f184df4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019e529dd100c88c7101e6def10c427c20b5fa45d2dfa55e9ac0a239c8c905cc`  
		Last Modified: Fri, 03 Oct 2025 16:14:00 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c9d001c6ace78426144d83795756baf7154ff0f16ac165d40880ac9978e688`  
		Last Modified: Fri, 03 Oct 2025 16:14:02 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e144f31ddd7ef960a54c6282633b7e7d6dd848c82e5cd8b61327655c2c9d50`  
		Last Modified: Fri, 03 Oct 2025 16:14:02 GMT  
		Size: 15.2 MB (15174642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bb22b397ac59825099c2a595b39ccd0df87336f226d0e9da6fc43618c03df5`  
		Last Modified: Fri, 03 Oct 2025 16:14:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeca3de5a4b59154f93dd7dc6e834db4ae131755ef1bcdbc208b600efa9b661`  
		Last Modified: Fri, 03 Oct 2025 16:14:00 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0ca8f32edc363fa0f7d200310d564f35e7b2d4a956ac21a1ba97a0f68ae359a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0104331e263d97059c7c18577062bb57ae9b6bd1f7a12b831cff0c09d6bbc9`

```dockerfile
```

-	Layers:
	-	`sha256:ac2543ad71d1a8301ab38a8957dfd1e57d7773fb09de56b367f662b1dd0d505d`  
		Last Modified: Fri, 03 Oct 2025 19:09:22 GMT  
		Size: 2.4 MB (2370789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9ca80da36a7430545b26d6d7b38ed4ae56c734d1d7d3b90c26ae1ea9c3b54b`  
		Last Modified: Fri, 03 Oct 2025 19:09:23 GMT  
		Size: 29.7 KB (29657 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; mips64le

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

### `redis:bookworm` - unknown; unknown

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

### `redis:bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:e01834aeb641dea2d730a65a4915dcf124461f26dd9da735c658088e3a89fc33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a85514cd026085a816380df291bada2a4919e9f2987f67d175fc36440fc54a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:fb9c4182713141f2b88d014efd6a22d8787ad64c259bc1b521e7dc35a4e6e099`  
		Last Modified: Fri, 03 Oct 2025 16:15:09 GMT  
		Size: 16.8 MB (16835659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9296c8ca8b112701d46b48eb304ba8a447e75a8e95836bbe269298b5da37db02`  
		Last Modified: Fri, 03 Oct 2025 16:15:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517d7b84a1caeb594800a3b108af78bc7e4d720f771ac805e8014f959fd607a`  
		Last Modified: Fri, 03 Oct 2025 16:15:00 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e2c9ced9d0791d572ba00e6057e5e18fb37b33ccba7a14f6ee273979b662771a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b66e5d28186d80551aac0f936c79d1335c0a7897b00f7c8dd3cb7a64bf5c2b`

```dockerfile
```

-	Layers:
	-	`sha256:d903032317cec1a3381a3b2f268cd72cf738881d94e5199a3535f1bab5f5f0be`  
		Last Modified: Fri, 03 Oct 2025 19:09:31 GMT  
		Size: 2.4 MB (2378032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9e9f141ff09adc0e3e9138c9d20b3809fe00861e8fbe70a6e93bb6b41a1f`  
		Last Modified: Fri, 03 Oct 2025 19:09:32 GMT  
		Size: 29.8 KB (29789 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; s390x

```console
$ docker pull redis@sha256:d6807857f06d010c24729f8fbad3906c573e483223844b778fc9af12c78e2df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42554796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4054e1c902fd6fdd5a1e894ee0e5cfb76f6b6f4ed7a6d9ae16c2f537eead506f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:df89d6a986eb116a00dce3ddc71c22ce19544170df7433be04ac590b0a34a5bf`  
		Last Modified: Fri, 03 Oct 2025 16:14:16 GMT  
		Size: 15.7 MB (15666265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999cf8be81e0efc77770ac4a17c02233dd5a8a9eb366b21da7dc734714f8ebf3`  
		Last Modified: Fri, 03 Oct 2025 16:14:14 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359708c83c62a6ee77068eb80e3e253e445f507cf48a3cdb06b23966c48711bc`  
		Last Modified: Fri, 03 Oct 2025 16:14:14 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:2e44d12d761a522210bf858eb92e43fc2c76a1e2c90e56ecdc19356c2b2796f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d6b6e0f85303bb2ee45e99ecab6896b783762a885e35edfe5404393c0b0449`

```dockerfile
```

-	Layers:
	-	`sha256:617cd5f01544a6f6c21f71c3d3cdd5e8bd51b9f026428da9b9ee1ae4e0aa0b48`  
		Last Modified: Fri, 03 Oct 2025 19:09:37 GMT  
		Size: 2.4 MB (2370458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc52af853c5a8f12891de34d0f3a65234ad63fe3fc7f9dd07776a1d94396a0ae`  
		Last Modified: Fri, 03 Oct 2025 19:09:38 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
