## `redis:8-bookworm`

```console
$ docker pull redis@sha256:cc2dfb8f5151da2684b4a09bd04b567f92d07591d91980eb3eca21df07e12760
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
$ docker pull redis@sha256:a240ca6b723fb655f76edd7fbba67282eeb73e4b87462629c01083d620d8e3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52422223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1fe3a9a889c69d0b4febf6affb4a8d90213cc35196e11d379c87a753658ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f60c71d8e10e0555ce03c32fd4407a9dd7090df812c98efb325a91f820a35`  
		Last Modified: Mon, 18 Aug 2025 18:20:38 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d9cf20af57b45fca01f6e264cac4a6e2e213067a5593eb4d38a3c8b5c3f36`  
		Last Modified: Mon, 18 Aug 2025 18:20:38 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22261c94fe4aaa2fc0818ade274d1b988a83d48bf2af24ce719b4f9c97ad8cb`  
		Last Modified: Mon, 18 Aug 2025 19:21:04 GMT  
		Size: 24.2 MB (24187743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f34ca96de3ff70793fb163e4f3b823438504df5004d00b4bac5c0a61a87b333`  
		Last Modified: Mon, 18 Aug 2025 18:20:37 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63edde0222ea5d1f451341c589856bd7a648df0d06c22e8c459a743a727e93d9`  
		Last Modified: Mon, 18 Aug 2025 18:20:37 GMT  
		Size: 2.1 KB (2117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:ece8d05f808ff97871582a9027f131c9054322c6bab5275a4f2bcfa2776012d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91f94adb8e851a4e80ee8f9e97f72f21529a408c5667a9e276720f3f40c607`

```dockerfile
```

-	Layers:
	-	`sha256:9c586556e0736816ae56d43b0bc1e4ca1bd531d042192181b80234b633378e14`  
		Last Modified: Mon, 18 Aug 2025 22:05:08 GMT  
		Size: 2.4 MB (2371511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca12f7e6020df45a22ee0b862d2c97a19182087b689f601029014babebdfd930`  
		Last Modified: Mon, 18 Aug 2025 22:05:09 GMT  
		Size: 29.7 KB (29685 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:118872825c66ae7cdca85d0aa39fce863173200197c70ad5466a31afcf656d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cfb65332d16b10da3e7a5c9a9b59287ec17422f541c3635e1ab3585874b450`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490d6ff4174c70151b82cc7df62ad555ff7a4f51fb18acdd612018cb29149562`  
		Last Modified: Tue, 12 Aug 2025 23:55:33 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c34effacdf4844b196a4b3be2e7b0e39aa56432701a30b1a2101fcdb4ff550b`  
		Last Modified: Tue, 12 Aug 2025 23:55:34 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa029b87bb0ec123ff2ecaa8e8d5c2e2d1279d0611d1eda1671f9521246dff`  
		Last Modified: Mon, 18 Aug 2025 21:40:46 GMT  
		Size: 15.3 MB (15332848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34982aef27cdb2f3c8897ece7c65107a5d820a3204c922aff6da0cae47dacfa9`  
		Last Modified: Mon, 18 Aug 2025 21:40:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7e4088000658416b0f645b9b60cd39bba7c4c49c8f2ea0051bfe501135242a`  
		Last Modified: Mon, 18 Aug 2025 21:40:46 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:4d958b57497fa70e08e119bdcb2164fc8b1413855d9534e1e01a8ec685ae7177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa2e994fbd3e008b3929a9eda9010fc9da5b32faedc26e4cc137337fcd2428a`

```dockerfile
```

-	Layers:
	-	`sha256:504f1c2ba4cb67532b316a704a3f540d556e89cf0e9d6bfe01ac76f11623143a`  
		Last Modified: Tue, 19 Aug 2025 01:05:19 GMT  
		Size: 2.4 MB (2375347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1ae9a0794953af8f6607639f4a00a75bbb394c7cce36ed80e352c1af3c7c41`  
		Last Modified: Tue, 19 Aug 2025 01:05:20 GMT  
		Size: 29.8 KB (29831 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:79acd689731d1a58e88f04d97ebc2aa00afffe534bac66ba54428b4ed41121a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38920766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6015d38489099a2ebe8d6ce1b94092faee26935fed61a79254dc3eebbfd944f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33377d9e572c19d254e3976bcc634a9bdfba42ff8858a74c04a41c0ea79cc522`  
		Last Modified: Tue, 12 Aug 2025 23:54:59 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e51a68161c03437d230e01235b378054af502fb6143aa8e691664d326cc6cb3`  
		Last Modified: Tue, 12 Aug 2025 23:54:59 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75af4f04ba757b8bd7e8f55036b6d506e3b03ed811b2ae49e59eef373b123bc2`  
		Last Modified: Mon, 18 Aug 2025 23:08:15 GMT  
		Size: 15.0 MB (14977628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca5299b9b6fe527533d7bf6e7de620afae17bf506ee08802765e2600a217942`  
		Last Modified: Mon, 18 Aug 2025 23:08:14 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd689bc00c50476145a6974f4384382b6e827b52079bc9bd8242bc15e1af665`  
		Last Modified: Mon, 18 Aug 2025 23:08:16 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:957e09e45838ea16625351ee9a693da20b7858a673ba0f54327980d5b6104e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6785df63718920b20fec03d445c7489dd91fb77853de7ab9f31a715d9452f6e0`

```dockerfile
```

-	Layers:
	-	`sha256:fb5ef3d1ada4618b7d1f1330fa79af05dd7984c38f4a4fd5a39b10c31067ce11`  
		Last Modified: Tue, 19 Aug 2025 01:05:24 GMT  
		Size: 2.4 MB (2373764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ece5215708391907b28fd73cadfae1cacb96d266246175d0cddbee904fa927a`  
		Last Modified: Tue, 19 Aug 2025 01:05:25 GMT  
		Size: 29.8 KB (29832 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:98d9e046d70bdcf297a0ba981c6557918efd02d53035525cf23482ee8e1a832a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51864236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742fe6f4da2f9d27ef93e59754ed04b5e1e24a3cf4b5a6b715939e62baca9e03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea3a4ff9abc7870c4f495bcbe75caf41f9963a82260015a16164315ca679eea`  
		Last Modified: Mon, 18 Aug 2025 22:02:45 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ca5bfacb225bbac607a3f27334b5f2765357fe297c0483f4796be3967c65be`  
		Last Modified: Mon, 18 Aug 2025 22:02:46 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d137d914b5acd7fe6bed95680feef74624ff52256d3b365f1e5ddcc995843`  
		Last Modified: Mon, 18 Aug 2025 22:02:48 GMT  
		Size: 23.8 MB (23778021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb088ca8d581489546ed84b775cd6aaf06964cd6a9f445c5a8bae08404543c95`  
		Last Modified: Mon, 18 Aug 2025 22:02:47 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f98ec3ea3c32130effef245ddf3d8a53edd1290e45d6ab978698ba17fbcabc`  
		Last Modified: Mon, 18 Aug 2025 22:02:47 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:78edf2844283969a250f0544c2453ecb2d068b45c5e48ab0487386753fcd5ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2c4d50cdd8f69af6d08a38e4a858ee0bbcbaa3d65612c6c54e3caa4130c3d1`

```dockerfile
```

-	Layers:
	-	`sha256:fae17f5a579e85dc90a397213a062a46473a3231dc5d5ad83d142d8d2a476b96`  
		Last Modified: Tue, 19 Aug 2025 01:05:30 GMT  
		Size: 2.4 MB (2371816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d8acfd5526c98e6a1b6679f7ae2182c8764899a856bcac44e1a9c7c38999a3`  
		Last Modified: Tue, 19 Aug 2025 01:05:31 GMT  
		Size: 29.9 KB (29882 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; 386

```console
$ docker pull redis@sha256:54b089269295cf65bf47b9621c99828d9e376c5d71eae4aa74873c8b6434a051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44386327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a8731189bc89faf73b09eba87f4c89facab102d81cfb564fcf13d9d7094d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac1c32adf45c18b5ce3614449151fdaf3a1104098cc8754352f0c7d8774ac3`  
		Last Modified: Mon, 18 Aug 2025 18:13:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb37daaa221045bb560e090da6c9861bb038c925564e29b78e95ba0a750b26a`  
		Last Modified: Mon, 18 Aug 2025 18:13:00 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea257234f024eeedd955b250e84e61cddf19ffd02e3f9cd87305bfb5d14d4b42`  
		Last Modified: Mon, 18 Aug 2025 18:13:04 GMT  
		Size: 15.2 MB (15169509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b14ecc59ce389cd8182964b2d4a2afee73e253c4f4742a7d03b7529e5da9a9`  
		Last Modified: Mon, 18 Aug 2025 18:13:01 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a7e3b0c235952759d4aa1bbb8d090a58db8be57ab6889945ddc1c72b4d226`  
		Last Modified: Mon, 18 Aug 2025 18:13:02 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0d4434e48ea186af88fe09543fbe354fcd2c8d647175813db29517ae0b90536f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d55a1c3f523f558919d63584109de2a0cfcd155b63ecaaf8884e4ff7ce87670`

```dockerfile
```

-	Layers:
	-	`sha256:b3256e1ebaf5e4262583cd6a9f4fe9b058699ffad1b795ed2e867e9ac95c755b`  
		Last Modified: Mon, 18 Aug 2025 19:05:17 GMT  
		Size: 2.4 MB (2368674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bbd7e4109661708d35f08d2e24415b21b62f3dde1fc268b4b2ad7f5fd75a36d`  
		Last Modified: Mon, 18 Aug 2025 19:05:18 GMT  
		Size: 29.6 KB (29627 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:13d276b90d4aee6c2015e9b8f32a7d6cfb9995b8bb8a91f1e75777b5ff0ed49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44280715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93996d9b1c0d6229d984dff4d366ebaf2f104fa87abd41ef12b14365bcf3bcf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ac78d5c0e47b4d9929037271677f85f677dffecdcc81971680b6c8fff0991`  
		Last Modified: Mon, 18 Aug 2025 23:56:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e37f32bebbd78e3c4d80f5eb52bbd51bb59c6af0635bed8b4069ffcb05ab58`  
		Last Modified: Mon, 18 Aug 2025 23:56:52 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7b7d7b34c20aa828985b3995e558e7445983563c4c50177042d8258f0bee95`  
		Last Modified: Mon, 18 Aug 2025 23:56:54 GMT  
		Size: 15.8 MB (15759570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf6335301f3a0a6acab9fcafde5c46bb7221a9c666b43915385e085cc696bb5`  
		Last Modified: Mon, 18 Aug 2025 23:56:52 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb34b6d41149c7e6d4ffee0a0446a4f490f0f33ac2ec510dbb90233f2be1a72`  
		Last Modified: Mon, 18 Aug 2025 23:56:52 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:a31643f1cfe92a62f60697cd85efba8c2e4725f90a6c53062eff758ff977d31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939216176628b9908863aa4ebda9c570bd18d27827f2e5ae0d90731cbf5ea84e`

```dockerfile
```

-	Layers:
	-	`sha256:903c426a72a798ebe16a1596ea0fe173522b1dfdd388d985aa5af2daa87c7ca8`  
		Last Modified: Tue, 19 Aug 2025 01:05:37 GMT  
		Size: 29.6 KB (29578 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:b05b730c92abb8600cd7e8dc086725e04696994d19c9c82d0e3b687fc11db16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48919696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f9dd292fb9bd6ee859ca687629853864a8a323b93ef5ea7d28a0d8e1c08bc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024965d4fe419cba89e360ef432c876de683a456113f97d6ddaa2ee5f9a8ddf7`  
		Last Modified: Wed, 13 Aug 2025 11:45:56 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7152a3689596cb1ed68ff297635030e5d5ac35a1e7c83bb3b89b8aa0bde66f6`  
		Last Modified: Mon, 18 Aug 2025 21:51:36 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fa82471ad4a276105d5815fc74c11c391964249795e9fba625ea046687ab48`  
		Last Modified: Mon, 18 Aug 2025 21:51:39 GMT  
		Size: 16.8 MB (16842063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ec7df57a4371e3390fef3ec52e05558ba2218cdb5e1e5dab33f3291c1c851`  
		Last Modified: Mon, 18 Aug 2025 21:51:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12f2f9e81255dc9b1f9976b2d5094f6ae47f961aa76644818c8019d2491b5d3`  
		Last Modified: Mon, 18 Aug 2025 21:51:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:6c2725b82649ede763c5eb43460ed5e7447637378664c3d57e97d8cad13d3e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edf6fd29272a84d3077f86762ac9f2921716f265134f7cfda7dbcddbeb29994`

```dockerfile
```

-	Layers:
	-	`sha256:870974805376bd0940d9aa6f27b9fcecd2795c89022cab12770162863389a5ec`  
		Last Modified: Tue, 19 Aug 2025 01:05:41 GMT  
		Size: 2.4 MB (2375917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31db4beed049e02d89e7f26a13b94e4030ae5238332632fe59171c5c10bb18ff`  
		Last Modified: Tue, 19 Aug 2025 01:05:42 GMT  
		Size: 29.8 KB (29759 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:b0b37459e1bc4e585ff955075fcc26c30b079c4e6d3c39de89dbc12f2d61ce43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42559142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96933808f9e01024fbc8bb0108fbe06acb0c1ef81ccba225c89435aad4b5ac38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-8.2.1.tar.gz
# Mon, 18 Aug 2025 16:44:26 GMT
ENV REDIS_DOWNLOAD_SHA=e2c1cb9dd4180a35b943b85dfc7dcdd42566cdbceca37d0d0b14c21731582d3e
# Mon, 18 Aug 2025 16:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
VOLUME [/data]
# Mon, 18 Aug 2025 16:44:26 GMT
WORKDIR /data
# Mon, 18 Aug 2025 16:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Aug 2025 16:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Aug 2025 16:44:26 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 18 Aug 2025 16:44:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2313d99ed8d1567d73e0d886019d31f1cbc454fe0ddad43087707cda034ca4`  
		Last Modified: Mon, 18 Aug 2025 18:35:59 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b5cce5e584ac800acfa33ccb8f5703a347a5611a0c4e2ca5fa7b887c2d677`  
		Last Modified: Mon, 18 Aug 2025 18:35:59 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f18ecc629597a2acc0930b1a654593133e12ea070da166dc24746f67fb266a`  
		Last Modified: Mon, 18 Aug 2025 22:05:19 GMT  
		Size: 15.7 MB (15667084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8beff59bfee3828325b932e10a924b2d47ed948b8b38c6594d3e5475a05a26`  
		Last Modified: Mon, 18 Aug 2025 18:36:09 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11554808b59ea756a6fac2edf6fb05f9ec25c196c8de654e3cd850080e128cd4`  
		Last Modified: Mon, 18 Aug 2025 18:36:04 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:294c69ced8f5c1dfa0a1e87cf989b51aca0f1302c42ff68ef6976b2bab267dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91340c284c810e8f73f03b9845b4789da6b70c4d51885a88dea29dbdf08185c`

```dockerfile
```

-	Layers:
	-	`sha256:774d1ab23d187ee70ace029e953041b6d51479c22e4ee1bcf86b27d17406ff0a`  
		Last Modified: Mon, 18 Aug 2025 22:05:28 GMT  
		Size: 2.4 MB (2368343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f47e1da8921123e05c601d6296dcdd4b5a4c2a810c9cfcf082c74fc2b19ed0`  
		Last Modified: Mon, 18 Aug 2025 22:05:29 GMT  
		Size: 29.7 KB (29682 bytes)  
		MIME: application/vnd.in-toto+json
