## `redis:alpine3.23`

```console
$ docker pull redis@sha256:9eb6a7ba3d344e1958c7e1589fa3dee90373a934e8159c634562a91d622759a0
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
$ docker pull redis@sha256:cd5f3ac681c77791c6a8eaa62de876ad2be043ee5a428afb7c0095aa08246277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37625446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55563f45704d59e891b6aa643014bb6b562abf21909a44b3b297502415b68e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:26 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 19:50:26 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 20:02:55 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 20:02:55 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 20:02:55 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 20:02:55 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 20:02:55 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 20:02:55 GMT
WORKDIR /data
# Mon, 22 Jun 2026 20:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:02:55 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 20:02:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cd4ffd5c9d3953225a6a0a92d18c48a798a69e9957400fd090c91e69a4632`  
		Last Modified: Mon, 22 Jun 2026 20:03:04 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeab38c295a8c51ef6a036ef3f8d201f2735e356db19ef9abae8bd0ab5377422`  
		Last Modified: Mon, 22 Jun 2026 20:03:04 GMT  
		Size: 197.5 KB (197505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da8100e7e6818f7e0741b6b94d465d0731f2b9bd0255e8df21f529f009ed891`  
		Last Modified: Mon, 22 Jun 2026 20:03:05 GMT  
		Size: 33.6 MB (33580340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3229b74aabefa6686d1f0dad5c375d4a9bb8b4dfe3ece0c5bbd67b2b344016`  
		Last Modified: Mon, 22 Jun 2026 20:03:04 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05922fb64b4710ace916fe9c9e39308ed039f270c169b01f64e1975da8fb79d8`  
		Last Modified: Mon, 22 Jun 2026 20:03:06 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:e54ff4c93c17c7e4974cbeb2b8fa9df348273c9871d867392563b99d7188f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5c317e9a08d976847bdc633bbe3af2b9dd15ff8fb724016dd99d87020d0c37`

```dockerfile
```

-	Layers:
	-	`sha256:d4b045aad402b39c569b3bfc9063d52ecc9659837b52d09c70d5689532d05190`  
		Last Modified: Mon, 22 Jun 2026 20:03:04 GMT  
		Size: 467.7 KB (467661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e61ab637961c783ed46c5aced0729f3cfa27520d3db1e2bafa325a3a9e10cf`  
		Last Modified: Mon, 22 Jun 2026 20:03:04 GMT  
		Size: 31.3 KB (31284 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm variant v6

```console
$ docker pull redis@sha256:9bfb7fad4e9d70d60f6497986e31255613062c5663c869bca01fddec0f2fee81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17662249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2376749b91bb78de3230fd2697598236ae35d7c0264d824119a0f7c42c6448a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:57 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 19:50:58 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 19:52:27 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 19:52:27 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 19:52:27 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 19:52:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 19:52:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 19:52:27 GMT
WORKDIR /data
# Mon, 22 Jun 2026 19:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:27 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 19:52:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad22aa46e14f73459529f409a9da29c8c45e8e9bac4a19a2e9bc6cea61b22f`  
		Last Modified: Mon, 22 Jun 2026 19:52:32 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c7d93b1b065b25f66fc3c7c421f6c0983d57972595b5a5f098d24d5ff10c71`  
		Last Modified: Mon, 22 Jun 2026 19:52:32 GMT  
		Size: 197.8 KB (197845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9b66d9440cb14c7c95b8d6bc697de14c640093b42526767a3ea007b527ab0d`  
		Last Modified: Mon, 22 Jun 2026 19:52:32 GMT  
		Size: 13.9 MB (13908625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1a0c1aaf88970602d7fde1dc1f199fc3cf1f416d00c02942e8f2bb6f6ab02b`  
		Last Modified: Mon, 22 Jun 2026 19:52:32 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900f99320ab005da567a80021911ed34b92bec255cb1fc21459a177205895e4`  
		Last Modified: Mon, 22 Jun 2026 19:52:33 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:3491e46eea2df7e8e795d4a40b8d10e6c1bdec925366d9e9521a0816a7061e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7b7110e117a8c31b7e04c1c9a39cd86d8976ce488ca5fd3ab244f45cb4c8d`

```dockerfile
```

-	Layers:
	-	`sha256:0154adbd5fa800a639e8cdc4ac6091cbd9b41e00c940a4121aae406d2450288b`  
		Last Modified: Mon, 22 Jun 2026 19:52:32 GMT  
		Size: 31.2 KB (31220 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm variant v7

```console
$ docker pull redis@sha256:a318218e9cee69754e040a86fcd344f442a6b70ad039994b7b5a63e0cb174463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dd558b48e8bc5653acd554ad15ec7c31086b16b968554a257f9b7609f0502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:06:11 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 20:06:12 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 20:07:40 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 20:07:40 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 20:07:40 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
WORKDIR /data
# Mon, 22 Jun 2026 20:07:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:40 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 20:07:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96d288a4afe98876117fb561bc094cbe46236f92a13b5dd7b420852f1badcaa`  
		Last Modified: Mon, 22 Jun 2026 20:07:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a52059481d3d97a85169647083b81f7d09dfe2fbb380a6a4bd2d36fcb2b5e2`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 196.1 KB (196070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1284ac8fcdd0a2d9a121691755fa8d4d60ca5ad82824395c3353ef9e998b5aa9`  
		Last Modified: Mon, 22 Jun 2026 20:07:47 GMT  
		Size: 13.7 MB (13732483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19accab0a1a45ba4910c5a0832682c1794885379b7597cdb72dbc8b544e8bb`  
		Last Modified: Mon, 22 Jun 2026 20:07:47 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd095241029d4b96623e50214dc3cf9900e6b4e74263d23b09a08454581a522`  
		Last Modified: Mon, 22 Jun 2026 20:07:48 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:529fe81b2f43889faff6e358915bae42b8d13a5baad8ca62c2959a9fa5aa0188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.5 KB (496523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15420e1988388357f078f24cc143876bc52b6aa091862b09980ec4e0fc203044`

```dockerfile
```

-	Layers:
	-	`sha256:7ff1067b923f9c6e3990e61e3e3344197befb24d62c1464ddaa864092ac1cedd`  
		Last Modified: Mon, 22 Jun 2026 20:07:47 GMT  
		Size: 465.1 KB (465089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a68751db7afd38afbdda5715be8d385a776c6e7ac9e59be7d87559dda7009954`  
		Last Modified: Mon, 22 Jun 2026 20:07:47 GMT  
		Size: 31.4 KB (31434 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:a7bed941ab9b77ce455c7833d728c7c24459bcd9097a06fd3b246be7f2ac629a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37283620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4f5bec2c472de82ee9ec09d917d4fbcc879bdb0763a2f00c798652a7c0553a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:09 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 19:52:09 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 20:06:22 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 20:06:22 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 20:06:22 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
WORKDIR /data
# Mon, 22 Jun 2026 20:06:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:06:22 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 20:06:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac1488648a26c722d14c99eb6dddde0711695467148969b698d6581163d9de2`  
		Last Modified: Mon, 22 Jun 2026 20:06:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5216688a6342b7fbeaad36e071101507926e65af8c2b29bbe214bd433555c5`  
		Last Modified: Mon, 22 Jun 2026 20:06:31 GMT  
		Size: 199.6 KB (199575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92934b8c5e08515d479f869fc5b8a7d6ae12bb1bf9ef640d3ae90feab259fdf3`  
		Last Modified: Mon, 22 Jun 2026 20:06:33 GMT  
		Size: 32.9 MB (32899002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65085cb90cf27c1c0eae47eed8557f02132c92a76ea82ed9ec4d36bdc643b66`  
		Last Modified: Mon, 22 Jun 2026 20:06:32 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41fb3b6fd436ebaaf709d89ebadf44886def9d97f436d0453c13d36366895da`  
		Last Modified: Mon, 22 Jun 2026 20:06:33 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:871a2a7dea1a3e3cdc0fc3a8aa80abd706165ed857bbd20f189395ca9b0ae100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.6 KB (498594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e0b08aaa349b9e7bd4d17217dd35e4ae933700c0d6aab5d04f728d11f749fe`

```dockerfile
```

-	Layers:
	-	`sha256:28339d8711d0a310575666127f17bf9efe14bf3e306ec8e6f1d7c0f21d9c2b53`  
		Last Modified: Mon, 22 Jun 2026 20:06:32 GMT  
		Size: 467.1 KB (467115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6184d8f1f235013079d357c6157415b40c7fa7685eaa0f2b9cf5b3c6be69ba`  
		Last Modified: Mon, 22 Jun 2026 20:06:31 GMT  
		Size: 31.5 KB (31479 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; 386

```console
$ docker pull redis@sha256:54ad8a3259096602368e6b4984ed9c17e58e935a5614b15b897cbb2f26ca8e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17476603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7243059bd48cbec7955653bd42454243e3ce532ff70712819d233bc3af3495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:41 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 19:50:42 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 19:52:20 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 19:52:20 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 19:52:20 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 19:52:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 19:52:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 19:52:20 GMT
WORKDIR /data
# Mon, 22 Jun 2026 19:52:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:20 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 19:52:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a11f7244fa3bfdc83d4e2585a2644c2de6628c0ab112edb290142f5e6b723f`  
		Last Modified: Mon, 22 Jun 2026 19:52:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b386645715506bf4cddc49b2d7ca0ad2722eca8ccf3fd896c50418f6c9ad7f`  
		Last Modified: Mon, 22 Jun 2026 19:52:26 GMT  
		Size: 198.1 KB (198119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d098f6e04e2413479d2b2621de98af5ff07ed0163f27811442ba755d68e64`  
		Last Modified: Mon, 22 Jun 2026 19:52:27 GMT  
		Size: 13.6 MB (13607310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07c2a513950a7c35cb58b28cb84fe59a3f10803bf3eea9eb41d2b966139ef4`  
		Last Modified: Mon, 22 Jun 2026 19:52:26 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83236f4f6bcedc8060d773297d2024687b12654cb8b38a84753a514b1a5361c`  
		Last Modified: Mon, 22 Jun 2026 19:52:27 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:788ea93daa2b9cc5e89922e7f0b42b9873ab1ca2851f7cea8d4039d708096bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.9 KB (493862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f54e4a0feb3ee3660acb586aef14b0440c0d4e11266e521db8d9cce271f2dc`

```dockerfile
```

-	Layers:
	-	`sha256:b210ac011a9a654e0636dbe5529d39d2030fb2f1fbeea8f0c0460d4e2891f600`  
		Last Modified: Mon, 22 Jun 2026 19:52:26 GMT  
		Size: 462.6 KB (462636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4b7acb76d85d8b7fc0575129278b60b03e826a63e3ddfa8cda87ef6476f7e`  
		Last Modified: Mon, 22 Jun 2026 19:52:26 GMT  
		Size: 31.2 KB (31226 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; ppc64le

```console
$ docker pull redis@sha256:5d38fa9f619309501d880b33084d69aef37f90abb230bd1b87d97926cbd514aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18999450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4aacfe68ecdbf766d348fb950beacb5869e1ab98312f33ea42521ddcb668df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:45:37 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 20:45:39 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 20:47:29 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 20:47:29 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 20:47:29 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 20:47:29 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 20:47:30 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 20:47:30 GMT
WORKDIR /data
# Mon, 22 Jun 2026 20:47:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:47:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:47:30 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 20:47:30 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb06bb6568c307f582b24bd1a7890036c12eff67a16f2457e02dc69cd8c6a720`  
		Last Modified: Mon, 22 Jun 2026 20:47:25 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0615e2b24a3d07ebd59746526640351b8c2b17a8223ddcf2bb70f56b80608d`  
		Last Modified: Mon, 22 Jun 2026 20:47:25 GMT  
		Size: 200.7 KB (200682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f7cd2524ee42e9796d5c9e7b20f0fccc3e665472c1b7ffd40621e591c83ed`  
		Last Modified: Mon, 22 Jun 2026 20:47:43 GMT  
		Size: 15.0 MB (14983282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6d80f2082ccdff57eb017a0e043b9d241e099f0544df951331152ad407f64`  
		Last Modified: Mon, 22 Jun 2026 20:47:42 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290bc039cab42fa6cc6ede4b288f0f58d18c96b1fb2ec78498b5edcafd4dfbf`  
		Last Modified: Mon, 22 Jun 2026 20:47:43 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:9f6bb4e888837fe1d7431ae0c12d1ccfa2842ed50af29f62a90e4d5ee83fdef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3063c5d8fb589c5c0be7af371e5da84b4f3a2a7e55bcc91f7812901b845667`

```dockerfile
```

-	Layers:
	-	`sha256:e3b00184447c0e8295d1ef83fbf3a7835cb1a55511d582a26c9791ac32cb7b1a`  
		Last Modified: Mon, 22 Jun 2026 20:47:42 GMT  
		Size: 462.1 KB (462088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c29fe60d473153411ac57e7d8f0981df27d0fa1c574a0b64b2e7fb9d0f0799a`  
		Last Modified: Mon, 22 Jun 2026 20:47:42 GMT  
		Size: 31.4 KB (31358 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; riscv64

```console
$ docker pull redis@sha256:a3dd959057db744406c6078f1068e4cdce436e1c519b682e032bcb5468d388a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19313615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e098156236530306361a8334b3786d288516023eaabb19fdeb38344d6b9fb51`
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
# Thu, 28 May 2026 09:41:39 GMT
ENV REDIS_VERSION=8.8.0
# Thu, 28 May 2026 09:41:39 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Thu, 28 May 2026 09:41:39 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Thu, 28 May 2026 09:41:39 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 28 May 2026 09:41:39 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 28 May 2026 09:41:39 GMT
WORKDIR /data
# Thu, 28 May 2026 09:41:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 May 2026 09:41:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 May 2026 09:41:40 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 28 May 2026 09:41:40 GMT
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
	-	`sha256:7c4d82e3621801d4e27f8ac69f3a199e2b803164fe848d212b27bcdbc1442405`  
		Last Modified: Thu, 28 May 2026 09:43:01 GMT  
		Size: 15.5 MB (15525037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65389cdb3fac85ba5190b6af83790be4c41ac418f544c8dc9eb1778e8aede2e`  
		Last Modified: Thu, 28 May 2026 09:42:59 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c900274952046633b749ee85be0a1a164ad52aeb69eed009cfd21fa439a671`  
		Last Modified: Thu, 28 May 2026 09:42:59 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:927560c57e709ae2dc05db1a6662e9ef91355b39459171c119e6fc2dd220927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8972da4c91692e3b857e32d5b390934623e63211e5fc3b47b3ccb0d0dde27413`

```dockerfile
```

-	Layers:
	-	`sha256:85ce748aa61840c92739bf1a2c1b60bb7fcb1a283a6c583378e22a90c8831c63`  
		Last Modified: Thu, 28 May 2026 09:42:59 GMT  
		Size: 462.1 KB (462084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d7a56f9d7008d103def814bd9e0f9950ec3eb68a932257b0ad38808957e5758`  
		Last Modified: Thu, 28 May 2026 09:42:58 GMT  
		Size: 31.4 KB (31355 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.23` - linux; s390x

```console
$ docker pull redis@sha256:e6947bc9f7028d4e1392bf4c30e429a678587f76c109285f74e5b21120871f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18297106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542015f46585cd0547d28764bfb3f79b0b383a094bfca7be4fdea20c643eb628`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:05 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Mon, 22 Jun 2026 20:08:06 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Mon, 22 Jun 2026 20:10:19 GMT
ENV REDIS_VERSION=8.8.0
# Mon, 22 Jun 2026 20:10:19 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Mon, 22 Jun 2026 20:10:19 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Mon, 22 Jun 2026 20:10:19 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		lld21 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Mon, 22 Jun 2026 20:10:19 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 22 Jun 2026 20:10:20 GMT
WORKDIR /data
# Mon, 22 Jun 2026 20:10:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:10:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:10:20 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 22 Jun 2026 20:10:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a86da4819386fa99c6175631c866c5b8c47c3ce85146378689c01bf51211c9`  
		Last Modified: Mon, 22 Jun 2026 20:10:30 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a5426a64479e696fde78bff67ee364db0cd0c1a52dd459b7d9af29e1ad304d`  
		Last Modified: Mon, 22 Jun 2026 20:10:30 GMT  
		Size: 199.7 KB (199740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dda12e8e0c6537bc319627f57d7113c80a066494da195f99b52e265b4a394ed`  
		Last Modified: Mon, 22 Jun 2026 20:10:31 GMT  
		Size: 14.4 MB (14386931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43f67c735af94a391a063e030e4b2c929c323019c5fc4546c62cff671b6335d`  
		Last Modified: Mon, 22 Jun 2026 20:10:30 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321de37f42e50c1505c5d02c2e8449c38bd588626c770f707fcf9f24a13d95d1`  
		Last Modified: Mon, 22 Jun 2026 20:10:31 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:e1d02fa9427fd0272187e3626777285bdce8cb8196a99b019ebe60a2c079e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 KB (493314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9b75dd4c66ded955390e15492a057de8c61216f634a1a5d91d6fd16fb55cd2`

```dockerfile
```

-	Layers:
	-	`sha256:b5e46349b5377490fd59693375ec8cbc64013a6c330f9c228e22feef17c8dae3`  
		Last Modified: Mon, 22 Jun 2026 20:10:30 GMT  
		Size: 462.0 KB (462030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c0abaa00507d7369e4528c67750f31131977ee25cdc19419a7fd5615b7d9ee`  
		Last Modified: Mon, 22 Jun 2026 20:10:30 GMT  
		Size: 31.3 KB (31284 bytes)  
		MIME: application/vnd.in-toto+json
