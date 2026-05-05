## `redis:8-alpine3.23`

```console
$ docker pull redis@sha256:69f2c586c8a7e9cce4ae1ee9bbaf60bc4bb5f4bb3880e4ed022b1fd758a7cab9
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
$ docker pull redis@sha256:576ad98202c05a581de1209cd63bf3dcd19c853ea6dae89738b248c52bc750f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34482689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d00c3c4aaf2bfe0d5eaf6303366c18fb3255e9af0cf63cd5299b68425f94431`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:55:36 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:55:36 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 18:02:40 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 18:02:40 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 18:02:40 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:02:40 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:02:41 GMT
WORKDIR /data
# Tue, 05 May 2026 18:02:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:02:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:02:41 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:02:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21d49ce200048d25fbc9f80b69299abf08ad4203ed58e30b4e678241635e6a`  
		Last Modified: Tue, 05 May 2026 18:02:50 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f647393b837cf120f3059021b056e85eee2fc6e4529d482168a20f1c0be9eda`  
		Last Modified: Tue, 05 May 2026 18:02:50 GMT  
		Size: 197.5 KB (197497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0305d994255ad992b7fb4131f1feef1c95c154249d2ecc104f0157348ea0139`  
		Last Modified: Tue, 05 May 2026 18:02:51 GMT  
		Size: 30.4 MB (30417819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fa0f64c0fee9c8ec264baf1c88d5a8c4226906036419ecbc8f2416649580a6`  
		Last Modified: Tue, 05 May 2026 18:02:50 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f745ed1fa982c3fc93e8e4857b1540351b21e8ee40bb9483bcfed72137fe223`  
		Last Modified: Tue, 05 May 2026 18:02:51 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:fda058becc8a2fd647e7a5ebc4131cba18f2080f1b6bbb80364dac8967aca0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.7 KB (498712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a55232c4032c77946f9d1af6f2f50f20267f31e197e2639d740f34e4312e14`

```dockerfile
```

-	Layers:
	-	`sha256:71d73e95ed99f1d9b0f0ff31520054662b9c39f3a69a322f0d78b371c492d1e5`  
		Last Modified: Tue, 05 May 2026 18:02:50 GMT  
		Size: 467.7 KB (467661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef0b4b28b4df99516f1b9b1fc19a6fe9244dab87c9149546f98fecc84246fdd`  
		Last Modified: Tue, 05 May 2026 18:02:50 GMT  
		Size: 31.1 KB (31051 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm variant v6

```console
$ docker pull redis@sha256:a0f7d97bb6e0ec85e9353301923d73f7387fbbda42e94177e0a0b751fa2ad658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18682771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4a97289e4619b3074cab55db96e8394d14e856ba2c8423bc056b276b33127f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:51:38 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:51:39 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 17:52:39 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 17:52:39 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 17:52:39 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:52:39 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:52:39 GMT
WORKDIR /data
# Tue, 05 May 2026 17:52:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:52:39 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:52:39 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1cbd79bc678445b03a360bd66c2c857b60205a1b5077995b189200806b3aef`  
		Last Modified: Tue, 05 May 2026 17:52:44 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b294e1cf222dac46b3075beb547fbbcb68e06e20ae80b172ccb229dda56e7361`  
		Last Modified: Tue, 05 May 2026 17:52:44 GMT  
		Size: 197.8 KB (197824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd2b584f214091da665ee1b8172fe58b584f12c7ccc723aafaae2659e1b3da1`  
		Last Modified: Tue, 05 May 2026 17:52:45 GMT  
		Size: 14.9 MB (14909896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59331ff4229991989a3ce3dfbe178a53200a06b0123481dd4a916d51cbdde8e`  
		Last Modified: Tue, 05 May 2026 17:52:44 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2431a4bd3f597827b547bee6b1a71ef7ffeaaba908b85441b189794040eea4f3`  
		Last Modified: Tue, 05 May 2026 17:52:46 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:2d28b8c72dea317ce3e08f3da52f3ebe6c1b11c13e897c982a8799678d3f3afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aeca2e5b8f228d8f962d92913a66a688caafd36d8be01d023979fd6f443367`

```dockerfile
```

-	Layers:
	-	`sha256:77d06c5ed84613e6389df9d9e3d0b6a2e1b31b9f135cd8b47bc03be7079a34d5`  
		Last Modified: Tue, 05 May 2026 17:52:44 GMT  
		Size: 31.0 KB (30987 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm variant v7

```console
$ docker pull redis@sha256:4b378237690eecdbac3196ea829b40cc5f756e88b80f3afa9407fb337d6b8013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f61c406d94800a2c3393f8e70c4aa3eebb78e58a275d215cef83f90f484543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:53:13 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:53:14 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 17:54:12 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 17:54:12 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 17:54:12 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:54:12 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:54:12 GMT
WORKDIR /data
# Tue, 05 May 2026 17:54:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:54:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:54:12 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:54:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7243b8c7653498ac0a4e829d88b6895fa2ca1536abf67300cd9661a221e744aa`  
		Last Modified: Tue, 05 May 2026 17:54:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ba5256b41aefbf2fa2ed189a103bd5353654c916ac88a137fa18fccaccdab`  
		Last Modified: Tue, 05 May 2026 17:54:19 GMT  
		Size: 196.1 KB (196081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa38f596fe331a5bb6ed5ff77b09a5915d13ae13998c3dc7a56c077ee8d02f9`  
		Last Modified: Tue, 05 May 2026 17:54:20 GMT  
		Size: 14.7 MB (14693064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19d7a7db0c5db317bc88cd339f56c869cd7570140bf9bbbdc9e14899710380`  
		Last Modified: Tue, 05 May 2026 17:54:19 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec19b9ef93b3921ecdbda052da19a1acea1e157c57da90268f70944b3afee95f`  
		Last Modified: Tue, 05 May 2026 17:54:20 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:6bec70af558df908c7d56d13ebefda50f3532802871ca8a2ef3ee1d9bacc8a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.3 KB (498284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcd2784b13f0de1819af5ac9c33da30cc36f18d9918a3534e936821952bde60`

```dockerfile
```

-	Layers:
	-	`sha256:da18a730abdcb6e77f413450dc79ebc41b589490c76d0beac8623e97025cd8ff`  
		Last Modified: Tue, 05 May 2026 17:54:19 GMT  
		Size: 467.1 KB (467079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7944b942fbe6cbf6e28c7e7a09fd540cd2c287a05b8d6a9448a231b14f5009f7`  
		Last Modified: Tue, 05 May 2026 17:54:19 GMT  
		Size: 31.2 KB (31205 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:0be0cbdca96a8727ba362575cad64f01bfe8a3929d239c8bea5a3f4d79e2e06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34365184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba270f39d13c052464b08266e5005a8d9e62ac9bd83c715b681909282ad550b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:54:16 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:54:16 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 18:02:07 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 18:02:07 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 18:02:07 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:02:07 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:02:07 GMT
WORKDIR /data
# Tue, 05 May 2026 18:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ee89976ab798941ea78b4bbba9eac341b067b012c2f9e4f8abc03733328a80`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecd5b0ded7d1444f92f478482d0daf653187ec96efd4a8f45822e3d240594d5`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 199.6 KB (199565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba1b4cabb0135e5aa77116c5e0325dbffca5dd53cf69390f6cce9059e07685b`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 30.0 MB (29962562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ec21c8ab8b8c8f5f25853d7e9ec0b64055b32053d7b4559423c9721e46007`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b0407e31c57508773f0de550ddf756cce725193c2eff8a755d398965dfb4e4`  
		Last Modified: Tue, 05 May 2026 18:02:18 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:60d07bc7a526d866e73a598887f85a7643028237548ffba0448c5aeb156282ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.4 KB (498366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10cc9bbafb316c0f4b311afcc4cce826fa658d3868873371942a0aa766dc059`

```dockerfile
```

-	Layers:
	-	`sha256:aa392b91bc30cbcf4fca313f8a6aa99772593a5ef24d240e02f991bf6cef9618`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 467.1 KB (467115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2d82dd274f638defd358eb11a4b3b5e68668c68c64e12ace30ba03b986fb42`  
		Last Modified: Tue, 05 May 2026 18:02:17 GMT  
		Size: 31.3 KB (31251 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; 386

```console
$ docker pull redis@sha256:4e6839f96d05e0af67b0992225c6c9a1e6beb499d3a60f1dc4b56504c723183b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18608776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8739894651fb581b6876985d04c2ec6b50ae71747b3a813fb1f44b4c9093cc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 17:53:44 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:53:45 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Tue, 05 May 2026 17:54:49 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 17:54:49 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 17:54:49 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:54:49 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:54:49 GMT
WORKDIR /data
# Tue, 05 May 2026 17:54:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:54:49 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:54:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bab64242bf99a54201a19c2c2f6951501bf465487b94a5215f7a5ddfb9b97f2`  
		Last Modified: Tue, 05 May 2026 17:54:56 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8d0f10e39abfb86380d49314fbb322514394f0d71bbb9b8b912fc2947611a5`  
		Last Modified: Tue, 05 May 2026 17:54:56 GMT  
		Size: 198.1 KB (198113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c855bc1b8d7541a72109157b7ee4051bc40b7096c34058fdb13065dd1d0da7`  
		Last Modified: Tue, 05 May 2026 17:54:57 GMT  
		Size: 14.7 MB (14717028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd0899e97ec1c752d871e94f073d879e5c6c7005a129733e5ffa52cce75e8f3`  
		Last Modified: Tue, 05 May 2026 17:54:56 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e306de2125388f9a679ad8f8cfa665f59e74772a38273b305ea3ac0fcf4285`  
		Last Modified: Tue, 05 May 2026 17:54:57 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:929c1970801f8a89a21c80b7004fa6af92f15e038583e6127744257aebd2e0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.6 KB (498612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29704d2de924a9a7427990302e657fb3dc4ec4fa77de38f63aaf4504fc4337fc`

```dockerfile
```

-	Layers:
	-	`sha256:4f2bdcb93359f7f4fe2bd9d1ab1d6fb62c2c9c3ca25fff32635ff54d14bb0208`  
		Last Modified: Tue, 05 May 2026 17:54:56 GMT  
		Size: 467.6 KB (467616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3df6fb4fad744b69c3845dfc64639e48ab979a7c535c6f57776e1f92699b05`  
		Last Modified: Tue, 05 May 2026 17:54:56 GMT  
		Size: 31.0 KB (30996 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine3.23` - linux; ppc64le

```console
$ docker pull redis@sha256:716e853379a26e51a9b453fb6a54ed91449038e102a77621efcda6e7399f3567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20179926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea50d71e7ba8873ac3ac8e8db361e6d9257f471ec7e121df2af3693cd608a412`
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
# Tue, 05 May 2026 17:51:45 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 17:51:45 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 17:51:45 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 17:51:47 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:51:47 GMT
WORKDIR /data
# Tue, 05 May 2026 17:51:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:51:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:51:48 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:51:48 GMT
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
	-	`sha256:c72c2e1d526763dc78721951ed8575e6fe7610c646185bd02ccb24e02584db10`  
		Last Modified: Tue, 05 May 2026 17:52:03 GMT  
		Size: 16.1 MB (16145131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67709d2659b71b1e0ab0908156b9b7fa754e7b490773d6f2cffbfbc3a07fe0b`  
		Last Modified: Tue, 05 May 2026 17:52:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e4a312cb26d30a83599da1cbc47db4d98551c6080f3ce4d23e98e1f416405`  
		Last Modified: Tue, 05 May 2026 17:52:02 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:7d40d17ce74c2d1db04e99802ec56cddf9ad5622206ebe4c88ebf63e63d7a648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 KB (498195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5344f7f44262f8776082f2d62711e0b3bf513b03b8ee8baadbddf48eb880ef9d`

```dockerfile
```

-	Layers:
	-	`sha256:b44acec558d16fade88ca1cf08171b2de96ce5483fc5f21bb89469c8251f750c`  
		Last Modified: Tue, 05 May 2026 17:52:02 GMT  
		Size: 467.1 KB (467068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b99cba6c209339f7e05211ff53f454868b558b0b84ce6a65f4f2d181cacaa5f`  
		Last Modified: Tue, 05 May 2026 17:52:02 GMT  
		Size: 31.1 KB (31127 bytes)  
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
$ docker pull redis@sha256:ed22063d730607e71d92a08aa8a2767ca8cbe6746debf99ebf1a3690ba20c380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19564170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbcd2e609ae6a6d454b25063f0ff8eb6b4cd9f94b482797f20762a0b6b4ed22`
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
# Tue, 05 May 2026 18:03:16 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Tue, 05 May 2026 18:03:16 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Tue, 05 May 2026 18:03:16 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang21 		clang21-static 		clang21-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		llvm21-dev 		ncurses-dev 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export RUST_DYN_CRT=1; 	export PATH="/usr/lib/llvm21/bin:$PATH"; 	export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
# Tue, 05 May 2026 18:03:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:03:23 GMT
WORKDIR /data
# Tue, 05 May 2026 18:03:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:03:27 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:03:27 GMT
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
	-	`sha256:fa6451db5d6cfb6dc74263620ffe779dbb68aea3c777a818b5fa0bbc523d4594`  
		Last Modified: Tue, 05 May 2026 18:04:55 GMT  
		Size: 15.6 MB (15634712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f424866df1ec6c959845bdf3a01424faa0fc327818b4a1653cc539a39ae61d5`  
		Last Modified: Tue, 05 May 2026 18:04:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c57b3d309ad04b89a083eaaafb5859701c9b34bf642f9f7bae47221317694b7`  
		Last Modified: Tue, 05 May 2026 18:04:52 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine3.23` - unknown; unknown

```console
$ docker pull redis@sha256:8f95f5d7a2a5fe8ea88b651299fab095c4c61a7e94d79dc0c4f9b13e8df2a2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.1 KB (498060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9c337019e69686fd8211919a147ac98bc7b55bd1a8f07d42e887b8db3c4b17`

```dockerfile
```

-	Layers:
	-	`sha256:a8ede6ff5fb472ee107459fb3073b5addeda45cad2c7320287e09547be83a10e`  
		Last Modified: Tue, 05 May 2026 18:04:52 GMT  
		Size: 467.0 KB (467010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe78f38627dff700faf4e8adc0aa26a5a24a86d3b82ea6f8359b98b3915f20a`  
		Last Modified: Tue, 05 May 2026 18:04:52 GMT  
		Size: 31.1 KB (31050 bytes)  
		MIME: application/vnd.in-toto+json
