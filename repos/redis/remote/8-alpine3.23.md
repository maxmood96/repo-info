## `redis:8-alpine3.23`

```console
$ docker pull redis@sha256:b9646e7cdf8165d985b88bb3e61b3f2f7625db7f6c98af79def91997d04f26b9
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

### `redis:8-alpine3.23` - linux; amd64

```console
$ docker pull redis@sha256:02c2454cd3b6277389101b9d42d009f8518255930f8b06ae33624e324f8c6455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34482694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5068a1b35387fae8c8d5c2b30da50eacbb519b45e97a2524ae4758078fbc77a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:33:45 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:33:45 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:41:42 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 17:41:42 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 17:41:42 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 17:41:42 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:41:42 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:41:42 GMT
WORKDIR /data
# Thu, 07 May 2026 17:41:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:41:42 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:41:42 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fba6c0845a7a2ad0378dee0a019003496c6cd38baf2f2f382b00bb2c3f8bc87`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668659e960cb5a5df8757d495d829a0f8a853d84a4fa8ec10cd6e28757fa3c2`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 197.5 KB (197502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2156d2090f3d9a227b33aa143e540d6dfe3aad109711b0cc8c9766625ee5d94c`  
		Last Modified: Thu, 07 May 2026 17:41:52 GMT  
		Size: 30.4 MB (30417820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df16ec49200a2c17341c5561aeba491bea7baebb9af09e6aea4ecb4f713730ef`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111abd5c7b8c803af86929d10236b2be2747714e9a465de3bdb762f24eac77c3`  
		Last Modified: Thu, 07 May 2026 17:41:52 GMT  
		Size: 2.1 KB (2102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:362fa40a7a12112af5d77fdee7103497fe7950a93206935a912a4a501c8bd8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.8 KB (498793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d55d8b3a9d6a122ec48be16ac17efad241b011e42f3dd73e1bc815b715cc213`

```dockerfile
```

-	Layers:
	-	`sha256:a40d8a0d72873246c3bbd0cd09ce6f9f43e455668b3e3493382fd85939cf162e`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 467.7 KB (467661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85167027a9fad005dd3a08d0f972f08793b7a912d5cd0193b7efec4558ba83f1`  
		Last Modified: Thu, 07 May 2026 17:41:51 GMT  
		Size: 31.1 KB (31132 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm variant v6

```console
$ docker pull redis@sha256:31a87e216ac6c39f431a80c47cf35cbc666fe93c4483f3fd80af9e660ab5e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18682797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3139c87dd1adc3f1f665239b78af82f7e768ef84c8bf15bd17fa3355120ec2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:55:28 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:55:29 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:56:27 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 17:56:27 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 17:56:27 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 17:56:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:56:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:56:27 GMT
WORKDIR /data
# Thu, 07 May 2026 17:56:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:56:27 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:56:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8505a83ddf467e68cbcb3c6231352ace870a64facc1a1b30dbf7c4e938e2d79`  
		Last Modified: Thu, 07 May 2026 17:56:32 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1179cc050c5ab00690a8cbbe3a5162a0dc163ff02bb4f2bdcb5ea2ea4576308`  
		Last Modified: Thu, 07 May 2026 17:56:32 GMT  
		Size: 197.8 KB (197829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e70152b7741d0c47907eb5f821826cdda2c7ba8eab417fd944438739200496b`  
		Last Modified: Thu, 07 May 2026 17:56:33 GMT  
		Size: 14.9 MB (14909918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b43af4cca1f890a5d92c7b84050a2815b3d7622c800c5f0746a642ec1f0c41`  
		Last Modified: Thu, 07 May 2026 17:56:32 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a24a769df19e4f98636cc15c49eabad52655a0c72b671ca5e8c99c1ff6a826`  
		Last Modified: Thu, 07 May 2026 17:56:33 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:7960d6f5ed04c0d00f035f79d39f03c32299fa68fafd00be8494fa6ca9b44efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 KB (31068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaa081dea53d690c4e4702829c485a66a3c53fae0af63847ca10247c3e4fd06`

```dockerfile
```

-	Layers:
	-	`sha256:2f80d4a8fe1f4b331599b747c35bf4c3b20fff94f7d4af20e47e70a7216fb6c4`  
		Last Modified: Thu, 07 May 2026 17:56:32 GMT  
		Size: 31.1 KB (31068 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm variant v7

```console
$ docker pull redis@sha256:5ae2a329f9c9f2b2731181940f456150f272d28be0a6d31549a19d4338cc7c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56128607980846d9c6e752bad5c0bc09ff4bedc1e4c06ab640ad90dd582e54e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:59:40 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:59:40 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 18:00:38 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 18:00:38 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 18:00:38 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 18:00:38 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 18:00:38 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 18:00:38 GMT
WORKDIR /data
# Thu, 07 May 2026 18:00:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 18:00:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 18:00:38 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 18:00:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcd54cfe87a553efdfc4606e56bef088dd37e5dd6dcf7d4d30a930fbb44cb5a`  
		Last Modified: Thu, 07 May 2026 18:00:45 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f412849a883796f75f94dd00dfa953805517204f19c2de95f4410849c2adad5`  
		Last Modified: Thu, 07 May 2026 18:00:45 GMT  
		Size: 196.1 KB (196064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852dec8fe2c0a97858413c74b01f7de30716b5ed0118710828676fdc2d7ee41`  
		Last Modified: Thu, 07 May 2026 18:00:45 GMT  
		Size: 14.7 MB (14693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6c5195d31cf32e568580dd1cf7dc47dcddbd8abf38919879b43431f66fcbe`  
		Last Modified: Thu, 07 May 2026 18:00:45 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f2a740be9c397af33ecb790fd51417bed1ac47cd88e13a15e3ebe0d620f1cf`  
		Last Modified: Thu, 07 May 2026 18:00:46 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:34508c7a686f2e158b9c3fa7002cb684ec7075d07d6c9eda6c252f4dfbcb610b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.4 KB (498359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d304018ffd50c9e978619f54907e2fb9763fcf0a4e63b49217c2bba43e1765`

```dockerfile
```

-	Layers:
	-	`sha256:b9af39adf55850af2dde7f62463de5487bb08705a76aca44139ad6fd6afe0632`  
		Last Modified: Thu, 07 May 2026 18:00:44 GMT  
		Size: 467.1 KB (467079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:394d277a9a033db09e24660645ef1ee449222717d96e8de5abc03cab7dacc778`  
		Last Modified: Thu, 07 May 2026 18:00:44 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:9da178dde0aa239dbe55e9d1c2a9f13db8c990fd17bd6e9019baf6b4e9c902ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34365195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44091f51e9400804738d2d87161358f317d80f392ac21964f6054498a8b4bf39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:38:59 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:38:59 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:46:48 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 17:46:48 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 17:46:48 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 17:46:48 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:46:48 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:46:48 GMT
WORKDIR /data
# Thu, 07 May 2026 17:46:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:46:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:46:48 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:46:48 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aac07753e81896239cc495535859aeaf881b19127aa2f6c94582bc6fcac9de2`  
		Last Modified: Thu, 07 May 2026 17:46:56 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5825252f54049cba1ad2d5ea15a3e1c34547c4fc61f23503865ea0d6e3a5239a`  
		Last Modified: Thu, 07 May 2026 17:46:56 GMT  
		Size: 199.6 KB (199556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb5819b4eff7d56b015bdc97297a6e9e6570b864c04e255057ac31b47ac52b`  
		Last Modified: Thu, 07 May 2026 17:47:00 GMT  
		Size: 30.0 MB (29962589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763f9ac970db73db58c0238d3f94fd3972d8b1f23cecb5ae00bf0eb740ea959e`  
		Last Modified: Thu, 07 May 2026 17:46:56 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce11fa6b13e2a172b3c37aabdc074801ef6dcad38eebb9d428b6e82e017198a`  
		Last Modified: Thu, 07 May 2026 17:46:57 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:f37cb2dacfbf3411e97e7ddff5660d158d8e4c9c38d8d9879ebb10286632f742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.4 KB (498441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adcc00bc74b8f9402131fe5251c1e19a4aa28d30555e9814d4303be6fd03624`

```dockerfile
```

-	Layers:
	-	`sha256:5cc21295c2161f8420252180451985b28eec218163b9883790f61c17705b3e54`  
		Last Modified: Thu, 07 May 2026 17:46:56 GMT  
		Size: 467.1 KB (467115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932ec00e74e38be937c5dd8d802fdae27b6d674853df09b79a76b32f005549b5`  
		Last Modified: Thu, 07 May 2026 17:46:56 GMT  
		Size: 31.3 KB (31326 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; 386

```console
$ docker pull redis@sha256:59102ee1cdb56536acf17611b73cffe00cee1bfd039bfbe1812aac3fe063b563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18608746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c4a9f549144ee18feb7772f41eb04c31da9968995ed6a4c9686e3786138bbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:36:27 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 07 May 2026 17:36:27 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 17:37:33 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 17:37:33 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 17:37:33 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 17:37:33 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 17:37:34 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 17:37:34 GMT
WORKDIR /data
# Thu, 07 May 2026 17:37:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:37:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 17:37:34 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 17:37:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5730e3fa737c6bebac4c56290ec58b3f7bc577d6c21f5dd1569e512efe27bd5`  
		Last Modified: Thu, 07 May 2026 17:37:40 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4054c37c5c4bf2db4b61579c95d16e59be02d685e2baae78f207d657d617c089`  
		Last Modified: Thu, 07 May 2026 17:37:40 GMT  
		Size: 198.1 KB (198096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d24c7ddc9ede6fbccea09f7896a5e492cff0de832ba60f4e0c778fb4086513`  
		Last Modified: Thu, 07 May 2026 17:37:41 GMT  
		Size: 14.7 MB (14717014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fdbf1b0ce52aefe4db26372a40332b5a8a191b7b08448a87f09871639cc941`  
		Last Modified: Thu, 07 May 2026 17:37:40 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79429c828d82cb6859711375da427270308faab72f3a77062a52a001cdd201cb`  
		Last Modified: Thu, 07 May 2026 17:37:42 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:7861e71b8323500e08a5e927fa0a970e760597fa4684bda5346b2132d267da69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 KB (498690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480e4f6dbe928c7f36392aa8b901ba834881aaa852b1148cb43aba5adf1f7c02`

```dockerfile
```

-	Layers:
	-	`sha256:255d8699b141ab66aed9db615be8717d441264277811e9e3b102c2a7277decdc`  
		Last Modified: Thu, 07 May 2026 17:37:41 GMT  
		Size: 467.6 KB (467616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7bbf73afe6685a74f9dacb29809a5ecd10a5f2ba73e723f8d8dacdf9853607`  
		Last Modified: Thu, 07 May 2026 17:37:40 GMT  
		Size: 31.1 KB (31074 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; ppc64le

```console
$ docker pull redis@sha256:38d45f56b64fd5a4c6aaa72f069bba2af1a365a01b43d8bd5dcb8580657db00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20179832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d7e141531377335b99e27c46743da955eca185a7ebc4313bb59e33be6f3ac9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 21:25:09 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 29 Apr 2026 21:25:11 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 18:17:18 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 18:17:18 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 18:17:18 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 18:17:18 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 18:17:19 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 18:17:19 GMT
WORKDIR /data
# Thu, 07 May 2026 18:17:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 18:17:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 18:17:20 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 18:17:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ebf0420270d8ede8034d25245b718f9976e2cb34af38a1008a29de0bcc43`  
		Last Modified: Wed, 29 Apr 2026 21:26:43 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6c44d9fed74404736e252ab35d40dffae506ff75cca88be672d6156c04cac2`  
		Last Modified: Wed, 29 Apr 2026 21:26:43 GMT  
		Size: 200.7 KB (200671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46391ba7e5a6bd64098b25b71b8cad7629ef9025f1f0a06f4537bbcbcde7549`  
		Last Modified: Thu, 07 May 2026 18:17:33 GMT  
		Size: 16.1 MB (16145038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4f84a9e6f41abf76384b4ecc6778f03c3e3391d12fd529a8b1a5d644714f1c`  
		Last Modified: Thu, 07 May 2026 18:17:33 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc672f0b0a4fe21a97c213ef5c75044322bdeeb674411f24bcc38b75bb44cf3`  
		Last Modified: Thu, 07 May 2026 18:17:32 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:a2cf582dc9a0c62e5253b0a1075faa0c7b4f9150ae08bf60ceb810501bc96a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.3 KB (498273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bb24e93138d3c7e03274e4956d8f72f32950a98362b631265ff7b32c564c8c`

```dockerfile
```

-	Layers:
	-	`sha256:7c997f0bb98923848af8e84bbadb3d832085598075c111a207417095d54d5fda`  
		Last Modified: Thu, 07 May 2026 18:17:33 GMT  
		Size: 467.1 KB (467068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c08dc8061cd3c71384e0aa6f509c7503bf9df19922fba3b60658f1941aafdc`  
		Last Modified: Thu, 07 May 2026 18:17:32 GMT  
		Size: 31.2 KB (31205 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; riscv64

```console
$ docker pull redis@sha256:085e6034fb8c46aef5ed2a1a40ca7d9b07c805e52d892e35bf3f1bbf1e81f51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20246673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd4200b03b8403cd9d65a81afa6b88f310ddc178ef34d2483482cb64e5690ad`
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
# Tue, 05 May 2026 18:52:01 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 18:52:01 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 18:52:01 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:52:02 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:52:02 GMT
WORKDIR /data
# Tue, 05 May 2026 18:52:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:52:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:52:02 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:52:02 GMT
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
	-	`sha256:cf40683bac4bf5ad410947d69d23a35a50f5a09e0249f8c0b9909bb64f623518`  
		Last Modified: Tue, 05 May 2026 18:52:55 GMT  
		Size: 16.5 MB (16458095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0c13208b09564c4d39c41f1341319b9a4e8fb65e6e1e4c0002f4ec36e5cead`  
		Last Modified: Tue, 05 May 2026 18:52:53 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a9bab970e30a0c0835f44c6735c783bf7eacc3f93085745160b98afa606870`  
		Last Modified: Tue, 05 May 2026 18:52:53 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:b1d12b72acf0e4873fa05eab52a0a698f24d14578b3ec816b668158b31807c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 KB (498192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83fa67562ae705fb1ad0eed97ac5653870286045918e3fee239362a4805c979`

```dockerfile
```

-	Layers:
	-	`sha256:bf7411486c6042553958e1345ad43da3e88c12ae0df581d1a4322f5226e7653c`  
		Last Modified: Tue, 05 May 2026 18:52:53 GMT  
		Size: 467.1 KB (467064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bafa54fa7163439e766e6db829c377687a083a1970ad9209ade1ae9df4d29d0`  
		Last Modified: Tue, 05 May 2026 18:52:53 GMT  
		Size: 31.1 KB (31128 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; s390x

```console
$ docker pull redis@sha256:246ee555295c04b82d7a587259cf2e7066280ec751d8181f4dca3ee550405852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19564091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9949cec90e9b652246d64394f8b457e6e458cce32f541fec7d156cc5605c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 21:25:46 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Wed, 29 Apr 2026 21:25:47 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 07 May 2026 19:22:56 GMT
ENV REDIS_VERSION=8.6.3
# Thu, 07 May 2026 19:22:56 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Thu, 07 May 2026 19:22:56 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Thu, 07 May 2026 19:22:56 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Thu, 07 May 2026 19:22:57 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 19:22:58 GMT
WORKDIR /data
# Thu, 07 May 2026 19:22:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 19:22:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 19:22:58 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 19:22:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275c9cccad5fd51db2986bc1f5a7a87e0c1279c88a7404cc96773d20a20307dc`  
		Last Modified: Wed, 29 Apr 2026 21:27:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d0f4fb1dbaa436e97f4fdcced24e5de2ee2d79b035597b89757ac39d7a1ec2`  
		Last Modified: Wed, 29 Apr 2026 21:27:03 GMT  
		Size: 199.7 KB (199732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7ab79456b162ca60ac5ba155939b1b7b75c85f249cd69869f9efb034b4e949`  
		Last Modified: Thu, 07 May 2026 19:23:23 GMT  
		Size: 15.6 MB (15634637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16caf01029852da98790d667602f7acc2260f85f8de3f882ce41f5f46f7dcbe6`  
		Last Modified: Thu, 07 May 2026 19:23:22 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac687b3cceca49f3bef024ff454ee5fe11f9345ac9e8e89a7f27e58dcdbf87`  
		Last Modified: Thu, 07 May 2026 19:23:23 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:b228a006037f528ffc10484a6c3fd9c197885f8d2f924487919f74635c15a290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.1 KB (498142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf7a4dd3464dbcb82684b5a50989441a277a695c3a3de6a9c90aa783e2cd550`

```dockerfile
```

-	Layers:
	-	`sha256:27951de6187a67879500a852267db17659429d04c92ad9bf53ea790b5c94a4a2`  
		Last Modified: Thu, 07 May 2026 19:23:23 GMT  
		Size: 467.0 KB (467010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adeffd3aafbc512a93eac6526e285b908c2d1ec9e988a0f979eef62aa8de3a5`  
		Last Modified: Thu, 07 May 2026 19:23:23 GMT  
		Size: 31.1 KB (31132 bytes)  
		MIME: application/vnd.in-toto+json
