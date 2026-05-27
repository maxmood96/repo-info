## `redis:alpine3.23`

```console
$ docker pull redis@sha256:ad0a6eff0a40304ab1ab4f50f0dc192d82b071e1094eac961bcb6106092f8a4e
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

### `redis:alpine3.23` - linux; amd64

```console
$ docker pull redis@sha256:5537c97815045421d01e97b82940bd2a61efaaf9dee820cd6d3ecd75c9ee763b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37645256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a02d38405dc12092032737fdadd513729a81efca8439d1d7eef883e6e67e26e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 20:09:39 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 26 May 2026 20:09:41 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:20:26 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:20:26 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:20:26 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:20:26 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:20:26 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:20:26 GMT
WORKDIR /data
# Tue, 26 May 2026 20:20:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:20:26 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:20:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c44b6f30ad0d695c22a20207c60f1b50e2c4345e1951dfa5350b8a37828eb`  
		Last Modified: Tue, 26 May 2026 20:20:34 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537bc096dad5277afd74f633c060216218016f9c18b11ff6c2b045e0e8b62d67`  
		Last Modified: Tue, 26 May 2026 20:20:34 GMT  
		Size: 197.5 KB (197498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fe44424473378fe9ef1a327a57de619d1b5dcc870932347e1e61681fbdae5`  
		Last Modified: Tue, 26 May 2026 20:20:35 GMT  
		Size: 33.6 MB (33580381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ee05ca5806a4f5d8f5e20ed7a3bf70004a08b9952a7a0b0ac0145b3313cb8d`  
		Last Modified: Tue, 26 May 2026 20:20:34 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f21fb9c363e747fe9d94848316e77bcdf3e2dca671e1ba0190b5929dde4413`  
		Last Modified: Tue, 26 May 2026 20:20:35 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:e3069f7fbe08107e3a858093440be7e641459f95d1eecad7db2281d4e01d1e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb60a6b025bb84f077635c1edade5e45be9453fb30e96e381dbc529d4f5f2a5f`

```dockerfile
```

-	Layers:
	-	`sha256:710e2faa951ecc46d92020ce72e7e774b9b38578a8349af0c839c9a6105ce480`  
		Last Modified: Tue, 26 May 2026 20:20:34 GMT  
		Size: 467.7 KB (467661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7d412e56725c2cf3dfa732914e9107f6f6480dead0368d626708af225bbd8f`  
		Last Modified: Tue, 26 May 2026 20:20:34 GMT  
		Size: 31.3 KB (31281 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm variant v6

```console
$ docker pull redis@sha256:454515b423531051f6a493f6de39dc2ad51b22eea35c95ab908f9fbe359e4b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17681519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b45c4fcf0bdfc18414de74efb864936db2ea61bcb41b51591a61d08b46668d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 20:01:23 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 26 May 2026 20:01:24 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:02:51 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:02:51 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:02:51 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:02:51 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:02:52 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:02:52 GMT
WORKDIR /data
# Tue, 26 May 2026 20:02:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:02:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:02:52 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:02:52 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3f7eefb9064971c9ed7e9bd928d6a9efb541e6f5c780c0d4b55900787b704`  
		Last Modified: Tue, 26 May 2026 20:02:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bacbbafe16c9d82d5e85e49312725cdd5abc26e37b7c27b142352db81626133`  
		Last Modified: Tue, 26 May 2026 20:02:56 GMT  
		Size: 197.8 KB (197847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d860c69aff394fa99dc6309c6b05e274e622a5b7dfde114cf5210e0545d82ff5`  
		Last Modified: Tue, 26 May 2026 20:02:57 GMT  
		Size: 13.9 MB (13908618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db893d260d231001c06ddd0991b03721a8e0b7a8fa3dbe455b7e93f7cdc3ffb5`  
		Last Modified: Tue, 26 May 2026 20:02:57 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b55f0411604e23f48eb94ec7e8e5d945ff12417313f7458e22fde29fb275865`  
		Last Modified: Tue, 26 May 2026 20:02:58 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:851dad0f52385f2c350065085e56c906d76afb3921947b923377ed5e101dc144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a8b22f4bcd5bcce0152d14ba047f3bd94a8980f8a77913de46e99cb6c585ee`

```dockerfile
```

-	Layers:
	-	`sha256:56821323d9206951fe000b28e609bfa03cd7531ee8b90b27228496dd5a70f6b6`  
		Last Modified: Tue, 26 May 2026 20:02:57 GMT  
		Size: 31.2 KB (31217 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm variant v7

```console
$ docker pull redis@sha256:ba004313deb421cbc27f119b8d09c7ee1da2da1684faafd3ba4f396609aeef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3cae7c2b6553d4dd71bad737e71aabb3d560ac3698076885a680d954080d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 19:59:34 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 26 May 2026 19:59:35 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:01:03 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:01:03 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:01:03 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:01:03 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:01:04 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:01:04 GMT
WORKDIR /data
# Tue, 26 May 2026 20:01:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:01:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:01:04 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:01:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88628447969e224ed2d119eafac042a67f04f72f87311a6fb84ae28a2cf47553`  
		Last Modified: Tue, 26 May 2026 20:01:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107a6401cab333728c41d9b3ee8c9030ddf4ce49a35989ac5e82e9f5af0346a1`  
		Last Modified: Tue, 26 May 2026 20:01:10 GMT  
		Size: 196.1 KB (196091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5f279f25c1ef85534bebfb10622853c33e1797b57a0e1a2f70027a513de35c`  
		Last Modified: Tue, 26 May 2026 20:01:11 GMT  
		Size: 13.7 MB (13732479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fc22a07b0de3ba22f2f4831637889fba2a0f2a1e6c95d930cb998a1b3755c3`  
		Last Modified: Tue, 26 May 2026 20:01:10 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c521d3f7d28c0dbf1077009564b52e8da2ee5f920e299ccfdaa19c231638d`  
		Last Modified: Tue, 26 May 2026 20:01:11 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:557b21a93021e7455233f52a4c02c2c7bf3676396a78be681a66a8d408d12301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.5 KB (496521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40045a47b8272e8167288a453331cbfadb2c4b94d42b001e85442d19abf93236`

```dockerfile
```

-	Layers:
	-	`sha256:40ff45217f0249934e3b2ea23422d6919f232572dde8e7fac5fa1f8e16350459`  
		Last Modified: Tue, 26 May 2026 20:01:12 GMT  
		Size: 465.1 KB (465089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf0d81f6dbdc939bc13352ac7141d912b40e3cb4e3629a392d20c2c80b023e0`  
		Last Modified: Tue, 26 May 2026 20:01:10 GMT  
		Size: 31.4 KB (31432 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:e7da24ec0f24b115e16319f5ec946677d2c36ebc75a5cd022f259e360b371883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37301663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b92846b980b38e90a87474199f87c063099ff91370a9fcdddb70e00363e2e11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 20:06:19 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 26 May 2026 20:06:19 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:18:28 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:18:28 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:18:28 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:18:28 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:18:28 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:18:28 GMT
WORKDIR /data
# Tue, 26 May 2026 20:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:18:28 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:18:28 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512b984184f1eec6562af017a9c4db1e5f9603865ed7e888ba8f91ccf088ba2b`  
		Last Modified: Tue, 26 May 2026 20:18:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d9392e02daaaa6c91c310891dc71269240faae97c67effebfbbed047fe79ec`  
		Last Modified: Tue, 26 May 2026 20:18:37 GMT  
		Size: 199.6 KB (199578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c0fc51270522b579e47b94d13cc7ae9ce30c5bbba7c788a10ca46feac58c60`  
		Last Modified: Tue, 26 May 2026 20:18:38 GMT  
		Size: 32.9 MB (32899030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ec7abf509de818a0836f4336d1694413482e766f80b4065317acd32aaf7e24`  
		Last Modified: Tue, 26 May 2026 20:18:37 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dad54effa862d2505141b1bb4158fc21568ffd26cc44fb493d02248af2da22b`  
		Last Modified: Tue, 26 May 2026 20:18:38 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:d54046a659509e251d85ea8f1b67fabc16c0ca606da2fa343fb1c0f144da5021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.6 KB (498591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927bc0cdc6c1a2b75d47dc31927ce3d3d0f9177abcc6394ced022ae6adc26016`

```dockerfile
```

-	Layers:
	-	`sha256:9299821832f5b1740c286113675b7e0cf6b19298f170e005ef2ebc1689df0a72`  
		Last Modified: Tue, 26 May 2026 20:18:37 GMT  
		Size: 467.1 KB (467115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d58db74d32485e408d042761739e396b6214e5293b6314dc69b8f60f9bcb7b`  
		Last Modified: Tue, 26 May 2026 20:18:36 GMT  
		Size: 31.5 KB (31476 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; 386

```console
$ docker pull redis@sha256:c1577292d092f1bfa6c91cbb13ca3368448d6331b22f43fca39b082795245327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17499100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d30d03e9330be99485ccf483621df31778e39b6df7c03b89e2df4c440872ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 26 May 2026 21:41:51 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 26 May 2026 21:41:52 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 21:43:32 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 21:43:32 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 21:43:32 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 21:43:32 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 21:43:32 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 21:43:32 GMT
WORKDIR /data
# Tue, 26 May 2026 21:43:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 21:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 21:43:32 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 21:43:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd978e43d3f574209b1ba5465b3231f966aae0a02b13871f10bd32bc1516eed9`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5c7208dde0efa463988216c6c350ed15fc1503ad9e0917a282674a66ebd353`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 198.1 KB (198122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed1b54fe2078f7fb928757b8de28a396d3e1e0fb5f5a7f29e6902792e0f153b`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 13.6 MB (13607340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2716bfa00fa5af1bb512bd843d0ca789da1532fbfe309a9ff86e6b1ac1c7f5`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a086455a7f9e2603a656cb88ea458b87be83a515d20ec144fdbdd10521a8a5af`  
		Last Modified: Tue, 26 May 2026 21:43:40 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:32c7681e0becd01e79ab9ff6e7e5cb5ba5b35a402eb1c12b78f0960f3d19b9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.9 KB (493862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f16c230f585f52ad62b1c65d65affbb1fb3bc2bd2402029b64129aa2bc1f04b`

```dockerfile
```

-	Layers:
	-	`sha256:19009ead57d0093ba31778d38b052b6d696f4ba08c8d46745ba3207c67cd62e8`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 462.6 KB (462636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c8d2485efaba5a1f85d7facb37a5e58b71dae12a6371e0f5ef7b5385ecaa62`  
		Last Modified: Tue, 26 May 2026 21:43:39 GMT  
		Size: 31.2 KB (31226 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; ppc64le

```console
$ docker pull redis@sha256:8e544070ed6cfac46f26c86126cadf3a0089ae0741206a3a671139fb76e0012c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19018109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02db2e06fa6561289df24492db79bcacee5f1fb51fa6f7b5b371ed92ed63020b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 21:15:56 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 20 May 2026 21:15:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:20:22 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:20:22 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:20:22 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:20:22 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:20:22 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:20:22 GMT
WORKDIR /data
# Tue, 26 May 2026 20:20:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:20:22 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:20:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f378e45f73a880dc7c63250acc778460398f24f6a3323b12cb6d8307ac4ae843`  
		Last Modified: Wed, 20 May 2026 21:17:46 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca89d902ef68dc176ab777bd8a32ef9048f4f909a348d23b00d2a72be1e298f`  
		Last Modified: Wed, 20 May 2026 21:17:46 GMT  
		Size: 200.7 KB (200697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b751e916322519a00a71af938241769ad870ca7c391b8867984879aa3fc532`  
		Last Modified: Tue, 26 May 2026 20:20:37 GMT  
		Size: 15.0 MB (14983292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22594894846164e59da4fa705830a8d878591d2b1b84e7402a8508183645c89`  
		Last Modified: Tue, 26 May 2026 20:20:36 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580ffc2e89b4b4938143a35432ac97ad210c04a6caabe5852037fba9e6a55517`  
		Last Modified: Tue, 26 May 2026 20:20:36 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:43a83a6523b6176da3bacab655d27c8b9bef42e73215d6e6255fd35f5525d411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45cf6da7186549ca9b689cc2c8fec660d4b2e233edd1d4d5ffd4251d734768a`

```dockerfile
```

-	Layers:
	-	`sha256:770990f753a5f4232e9c5ec63e37013dd718e290b8e575392dc4407b13033562`  
		Last Modified: Tue, 26 May 2026 20:20:36 GMT  
		Size: 462.1 KB (462088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3920868a06658b069f98d869d836bd930d93b4ef48f29d1c964f1fd2347d7a11`  
		Last Modified: Tue, 26 May 2026 20:20:36 GMT  
		Size: 31.4 KB (31358 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; riscv64

```console
$ docker pull redis@sha256:74875ffdcc50ebb8e33b378282aea72937dda8740afba65def9cd687d1374cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20246690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45629516da6a403681e14cb7560d0ae1aca9ccbcdf43ad2a16faab4480ca3cce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 21:45:04 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 29 Apr 2026 21:45:09 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sat, 09 May 2026 13:33:40 GMT
ENV REDIS_VERSION=8.6.3
# Sat, 09 May 2026 13:33:40 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Sat, 09 May 2026 13:33:40 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Sat, 09 May 2026 13:33:40 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Sat, 09 May 2026 13:33:41 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Sat, 09 May 2026 13:33:41 GMT
WORKDIR /data
# Sat, 09 May 2026 13:33:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 13:33:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 13:33:41 GMT
EXPOSE map[6379/tcp:{}]
# Sat, 09 May 2026 13:33:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1788c30e356c5e9d99c480c065a5e2fa6b40b0b92b37b6754031da338ffc0b6`  
		Last Modified: Wed, 29 Apr 2026 22:04:14 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8860521955fe62c79fada8fd04be057b306b2bd6fadbcd20133e15a0c6c6b44`  
		Last Modified: Wed, 29 Apr 2026 22:04:14 GMT  
		Size: 197.7 KB (197723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22272e3e904d1e47cec2ad1a5a154f33dcfbecd00f081d6777a55fbec2015958`  
		Last Modified: Sat, 09 May 2026 13:34:38 GMT  
		Size: 16.5 MB (16458111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb2b39bd94a035cd0e98926141e50d56e8d2c54c7ecc28743ca8922de59673`  
		Last Modified: Sat, 09 May 2026 13:34:35 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8a4a23cfb056ccf53941f8789458c679234e473e219055aebb1c013b86edf`  
		Last Modified: Sat, 09 May 2026 13:34:35 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:3f972c66ead9dc120030add818ad24441b44df8cb1a55a54def0c89441098c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.3 KB (498269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3623c030b8174a43c2fe0cae8abaef7818f6475006162e3a9e73016346f370`

```dockerfile
```

-	Layers:
	-	`sha256:2d603763db78417888ec7fc6e9d4c3f595af64f41abc9f44d49c590bd809b31e`  
		Last Modified: Sat, 09 May 2026 13:34:35 GMT  
		Size: 467.1 KB (467064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbcfb4bd9beff6d40e052363371ac8742b4f16d6a8de47487bcbd01784332e7`  
		Last Modified: Sat, 09 May 2026 13:34:35 GMT  
		Size: 31.2 KB (31205 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; s390x

```console
$ docker pull redis@sha256:8bdd687016f51cd308eb9acc5d7915ad9dd466e66825482038d9781d8e8c12ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c47e4e0f7fd9e0170b796b2f6b8fe14c48f02fd651c8f83417058e0d59523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 20 May 2026 21:16:05 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 20 May 2026 21:16:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 26 May 2026 20:04:09 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:04:09 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:04:09 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:04:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 26 May 2026 20:04:09 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:04:09 GMT
WORKDIR /data
# Tue, 26 May 2026 20:04:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:04:09 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:04:09 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae4223f744ab940cb03a83688e5584372e30dddb7a90f1a7440845c7dc9b569`  
		Last Modified: Wed, 20 May 2026 21:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcd8d40e2504674417db39da0fbd1325588d9cb05867475d42eb552aac34c37`  
		Last Modified: Wed, 20 May 2026 21:17:21 GMT  
		Size: 199.8 KB (199765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f5d5a23509acd077d7402494fd74be2bf42d654fcf32b02db5395fdff6adf2`  
		Last Modified: Tue, 26 May 2026 20:04:21 GMT  
		Size: 14.4 MB (14386986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa04f3397e0907aec4d75ebddb06e718da33167315eb07a46783ffdf2bb5bd9`  
		Last Modified: Tue, 26 May 2026 20:04:20 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38effc5615924b38e2848f95869cc5c4b964532f9bf896af5b7d822af1aea198`  
		Last Modified: Tue, 26 May 2026 20:04:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:068edf01c0f24095885b8f1dcf0344e927ceb3376047b0ded1407381d5ffc874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 KB (493311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e907490b259dc4e5165ae72c392ec8145871d39961807b7fbe3f825745610c0`

```dockerfile
```

-	Layers:
	-	`sha256:a431c579f0b4f2e178f256e2a4b6301375fe928de5a1ac057f8b1b9e9c283a43`  
		Last Modified: Tue, 26 May 2026 20:04:20 GMT  
		Size: 462.0 KB (462030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a57651fbebc813f36671506f94b2ccc2c6353003cc9498b8a22f862d3b45a07`  
		Last Modified: Tue, 26 May 2026 20:04:20 GMT  
		Size: 31.3 KB (31281 bytes)  
		MIME: application/vnd.in-toto+json
