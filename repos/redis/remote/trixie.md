## `redis:trixie`

```console
$ docker pull redis@sha256:aa049e689e141a4358ad1d4562dc49c88a89fbab711fd8fcc33f684c80b26301
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redis:trixie` - linux; amd64

```console
$ docker pull redis@sha256:e74c9b933d78e2829583d88f92793f4524752a15ac59c8baff2dd5ed000b7432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54269113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128bbe5f7793f7e955a5eab7d492b1de001e182462c694f03362f4704cfb1a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:00:52 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 26 May 2026 20:00:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:08:57 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:08:57 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:08:57 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:08:57 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:08:57 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:08:57 GMT
WORKDIR /data
# Tue, 26 May 2026 20:08:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:08:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:08:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:08:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fabda3f1df5dfadbc1ebf1d633a639961237e658225eadd33699a002c60fd80`  
		Last Modified: Tue, 26 May 2026 20:09:05 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eb956baa11f601b3bbb34856edca8595cad61ea5a93003d7c944285c012b50`  
		Last Modified: Tue, 26 May 2026 20:09:05 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b607e46fa9d6ed4aff0e20cd947ddd2c8ccfa3cae6d138dd13610da88c9a8f73`  
		Last Modified: Tue, 26 May 2026 20:09:06 GMT  
		Size: 24.5 MB (24485024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad395060b0aa60020c651ad9d61e5d9f8692e20803aa0a69e88059953f367106`  
		Last Modified: Tue, 26 May 2026 20:09:05 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade30136b2f2af4db7e3f67b7ec5c96b8497e402e43537aabacacc1dc398b09b`  
		Last Modified: Tue, 26 May 2026 20:09:06 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:c1523d5408bb4c55a2601b661e8e144f3148ad386d6a20e842c90e438d61d055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91c46f8557fdec2615f6a36b37e9ecaf138d9e0d2bf02e9ef81ad8708a0e1a`

```dockerfile
```

-	Layers:
	-	`sha256:24afe2cc963a220f7d7ff6755e20d7ee8a92937736de82fad32e7c15dabe5a0c`  
		Last Modified: Tue, 26 May 2026 20:09:05 GMT  
		Size: 2.0 MB (1979879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69ffaa3ebfe67c346eb2a8e33c94ff93bde58ab5a60f9ccfb2c6cc1442e1dfb`  
		Last Modified: Tue, 26 May 2026 20:09:05 GMT  
		Size: 29.4 KB (29384 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm variant v5

```console
$ docker pull redis@sha256:dfaad941fdc7de7ed16762cfb1cd109311b57c2aba7375088d39c905246a3a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42069999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db18f4f71450b3c91ae80368018ac059f12bc048bc95010400f7a7f9446ffa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:59:51 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 26 May 2026 19:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:01:28 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:01:28 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:01:28 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:01:28 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:01:29 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:01:29 GMT
WORKDIR /data
# Tue, 26 May 2026 20:01:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:01:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:01:29 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:01:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547a82a002873ece1bdae80ed9c381b2053a280b406e702f112943556ba6ab8f`  
		Last Modified: Tue, 26 May 2026 20:01:36 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28329c69eadc8eb5d24fc9a9195074d9d932378df05cab221b123aeffe6c8745`  
		Last Modified: Tue, 26 May 2026 20:01:36 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d9f9d84bd98dad44637bb2da16ab8c7a4a4278d508eb6a37228254af61608`  
		Last Modified: Tue, 26 May 2026 20:01:37 GMT  
		Size: 14.1 MB (14111962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc04fc7a1021695553fdcd3853cf536a29a47358f7db8dd55eebf34dad33eb09`  
		Last Modified: Tue, 26 May 2026 20:01:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ec6da529ca0f81688f9a37a50707506fe8dd2480e6ebfec15641e3ede015bb`  
		Last Modified: Tue, 26 May 2026 20:01:38 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:cec66c052f388c0390a10ab6a71c5de6053d2255fb37aab773e9a5009a11f888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2012407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f7596e60f9e10a5acaa2c63fb741e7210a83dda2cc36aead253a9120fbee`

```dockerfile
```

-	Layers:
	-	`sha256:18af05586efc3d53af7e6e3f0a879db8440347e484fd9e52104c49b1f160bc4d`  
		Last Modified: Tue, 26 May 2026 20:01:37 GMT  
		Size: 2.0 MB (1982872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21627de213904c135f81d0638a5fc22e01ffa7a4e9a97446815eb1ceb978c579`  
		Last Modified: Tue, 26 May 2026 20:01:36 GMT  
		Size: 29.5 KB (29535 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm variant v7

```console
$ docker pull redis@sha256:5460563fd16e88cd616efa206dcce9b90c7c42c5d182da7c8a5186e6641d7b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40070690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe6670f58ad1cda11559bb0291eae7de10e1aca3dd0d768e79a6265a8d847ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:59:22 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 26 May 2026 19:59:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:00:51 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:00:51 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:00:51 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:00:51 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:00:51 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:00:51 GMT
WORKDIR /data
# Tue, 26 May 2026 20:00:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:00:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:00:51 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:00:51 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beb3d1810d09583eef6913620d2d76bd44448e5a19d693ea616c5d655fe8f95`  
		Last Modified: Tue, 26 May 2026 20:01:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6667a75f442d778f8d787d7794316ce71e7854c5b3437ece25a46d1f7edd8a8`  
		Last Modified: Tue, 26 May 2026 20:00:59 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae45c6c2e710faaecb8222aa51198298a71e6dbd28170a18b09c993096a6fdb`  
		Last Modified: Tue, 26 May 2026 20:00:59 GMT  
		Size: 13.9 MB (13860689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edd04ab6eddfea787aaa9883286979e473c8fdc69b8ec55360d6f3e8ebddce9`  
		Last Modified: Tue, 26 May 2026 20:00:58 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b85af9685ead014615a88fc4e677a1e09796bc3dc7751209cd343f3ecf15028`  
		Last Modified: Tue, 26 May 2026 20:01:00 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:a56c37cd649f49503b712f43b54318c598c8b4dd26e0eaf9437d99dc5035b458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2010844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c987d6d3a02351e6e87aef20431b4480476db6ceb90c83660f38202ee8e2ae6b`

```dockerfile
```

-	Layers:
	-	`sha256:041666f1d402712d595e8f4cf0675cbd9516220058a04f499ea7468cae3cd100`  
		Last Modified: Tue, 26 May 2026 20:00:58 GMT  
		Size: 2.0 MB (1981309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57715eb0a82d5b74987e99dcdc3f9de00bac6bebfd3aafd27c6bde91a28cb7d2`  
		Last Modified: Tue, 26 May 2026 20:00:59 GMT  
		Size: 29.5 KB (29535 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:be3df1db92a5386405a468838dd697ef6c817ccd247ccf971c9555163daa7d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54127284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be14cbb98e70d06d9c0c945aef86f13004316c3193453b468ea360ea34dc1861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:00:28 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 26 May 2026 20:00:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:08:23 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:08:23 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:08:23 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:08:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:08:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:08:23 GMT
WORKDIR /data
# Tue, 26 May 2026 20:08:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:08:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:08:24 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:08:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477789fa60bf5cb3107af7f02f72eed007abf5ebb9585010a0ff02f339e830ee`  
		Last Modified: Tue, 26 May 2026 20:08:32 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1918c1f6bd780c725b723cf29ebb3d71f0ddab1d4abb4d759602d810dd3815`  
		Last Modified: Tue, 26 May 2026 20:08:32 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9bd87837499fb4db1179ff5dc102ae74447ffc113fcbc0bd1c43707ac8b962`  
		Last Modified: Tue, 26 May 2026 20:08:33 GMT  
		Size: 24.0 MB (23981206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1967d99066d4d0bc6d21b31bd828bfd40e5c36e6ca9c6a9b422f67c937708c7a`  
		Last Modified: Tue, 26 May 2026 20:08:32 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80384ca85e40804ff8d2879ed68bc0cebff64974c212f3898634825e36fe9ef`  
		Last Modified: Tue, 26 May 2026 20:08:33 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:2ca5ba92f0c6fab2df5fa8907686cef5ad2adc0733b1357caa28beaf2e89f627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56e5c683efb0ca7197eadaa634d93c51c9c81d7968c87dcc32521947fd7c31b`

```dockerfile
```

-	Layers:
	-	`sha256:00022ce2a3d6cace82db0c1e6ef5a6236979a50b1b1f9b2220034c061f894478`  
		Last Modified: Tue, 26 May 2026 20:08:32 GMT  
		Size: 2.0 MB (1980177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63d6921dfbe17ded0100195093da2174d496fcda64d34c94b58f082b586ffc2`  
		Last Modified: Tue, 26 May 2026 20:08:32 GMT  
		Size: 29.6 KB (29581 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; 386

```console
$ docker pull redis@sha256:a4d0f8e4181735effd3dc97a8229be4088c0207178bfc84d831988ced0b41cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45133002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3a26354185ed1aa1619da07aeb560be04f5093381fbe4ae7bce1abd66c94f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 21:41:51 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 26 May 2026 21:41:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 21:43:26 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 21:43:26 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 21:43:26 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 21:43:26 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 21:43:26 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 21:43:26 GMT
WORKDIR /data
# Tue, 26 May 2026 21:43:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 21:43:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 21:43:26 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 21:43:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9e8cbc4dcd084a00764a0852727678d10bbf23153f24fe4089a94804b75593`  
		Last Modified: Tue, 26 May 2026 21:43:33 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f886905b95e3f6ae3eb8f97038bab0ac562bfd2aac1ca034a3c5e5e2633a1e85`  
		Last Modified: Tue, 26 May 2026 21:43:33 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a303fadeb516569171dbae5f2e9fe71d1b30f04a9a067c541a06623c47d30f`  
		Last Modified: Tue, 26 May 2026 21:43:34 GMT  
		Size: 13.8 MB (13833501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad2b5038f212d7496389871483a4063657e4ff40d417574fec841a1c785e7ff`  
		Last Modified: Tue, 26 May 2026 21:43:34 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4f6259805b804cbdd484267f3f2de6965d7530ac98bbe924acc73eb5b3b30a`  
		Last Modified: Tue, 26 May 2026 21:43:34 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:ecad3056f4b07750608c517bb61e6736af8f4f834a12c21637f5386b943b26c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99468b3f85bdae3dabeb81a197dd22f49162e02af88752837abffa516c80a588`

```dockerfile
```

-	Layers:
	-	`sha256:2047ed655fc5ffbd59608674499b3598e12d12f5ac17e4ca3e04223768a750ee`  
		Last Modified: Tue, 26 May 2026 21:43:34 GMT  
		Size: 2.0 MB (1977056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc166c723729a712921adb4c0b79aefee00c84edeaf43d05ec030d60010cb15`  
		Last Modified: Tue, 26 May 2026 21:43:33 GMT  
		Size: 29.3 KB (29326 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; ppc64le

```console
$ docker pull redis@sha256:1ef0a08a2c0434f6255d8fe668469b77ebb1faecee34fc3b319eea8fc8632bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48700598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4686aed452b9429c5c3b7a8aeafbb90111499f6ae2e961663685aba997b168`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:03:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 20 May 2026 01:03:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:20:35 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:20:35 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:20:35 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:20:35 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:20:36 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:20:36 GMT
WORKDIR /data
# Tue, 26 May 2026 20:20:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:20:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:20:36 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:20:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a51445a050c144dd59f3db8b8f64b039d6abcc90ed4727456e52c0941fa44a8`  
		Last Modified: Wed, 20 May 2026 01:05:17 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09a221856fe40babf6db331030d1023c45825a84ac76d0ac58f9985d37a272f`  
		Last Modified: Wed, 20 May 2026 01:05:17 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a04602c62b4d2800b25008aad16c6a2b344bcfbbb8e08ab7f0ace84bb1da7`  
		Last Modified: Tue, 26 May 2026 20:20:52 GMT  
		Size: 15.1 MB (15095978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe14c1d8d3bfaadd9c9da1b48e1cd308d0741fc3a24bd861418e88a59cf4c11a`  
		Last Modified: Tue, 26 May 2026 20:20:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af083f31d0d41c920173a238e992d4987319e4a30b21676514eb9f52528efe`  
		Last Modified: Tue, 26 May 2026 20:20:51 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:3f112e7b4f87c7a72b4a953de0cff00da7c15e3336a09fe76aec4f110cc041e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2012872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530640974fa9dba40e30683fc5b7749fc3a205624c7e656476427253f53c983a`

```dockerfile
```

-	Layers:
	-	`sha256:7ca72fe4154b7b7e595dedb6477db4b68491fc042b881ad2f433c558c8b250b7`  
		Last Modified: Tue, 26 May 2026 20:20:51 GMT  
		Size: 2.0 MB (1983414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329d7f2e738ca210bb935190bc7154b22494cf0ee9bf11fba84eba239e91556c`  
		Last Modified: Tue, 26 May 2026 20:20:51 GMT  
		Size: 29.5 KB (29458 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; riscv64

```console
$ docker pull redis@sha256:54177c3d26be482a012509fd9bcfd825c4836b404fad2222f3f62826a4d4b842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42036137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378b1f136d4b73fb379fba30c948bc56dd533fd620e8f390242bd84c652f4e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 13:11:25 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 21 May 2026 13:11:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:00 GMT
ENV REDIS_VERSION=8.8.0
# Thu, 28 May 2026 18:28:00 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Thu, 28 May 2026 18:28:00 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Thu, 28 May 2026 18:28:00 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 28 May 2026 18:28:00 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 28 May 2026 18:28:01 GMT
WORKDIR /data
# Thu, 28 May 2026 18:28:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 May 2026 18:28:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 May 2026 18:28:01 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 28 May 2026 18:28:01 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0b9f00c2cde78d2247debb5d964c002ea9018c172e7e4a60fae9a713a8fdc1`  
		Last Modified: Thu, 21 May 2026 13:29:22 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df001a8c17ecf4485339fa25adbae42d8991547b7a2e07905565f21456337424`  
		Last Modified: Thu, 21 May 2026 13:29:22 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2cf9d994a360e91fccb0248577dd0edaedffd479d43cba3eb33f5c3dba0c8b`  
		Last Modified: Thu, 28 May 2026 18:29:42 GMT  
		Size: 13.8 MB (13754384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76dd201ca409d89a90b6c4ae390e08fe1ca03a113fb2b9e38566de7be78e9e6`  
		Last Modified: Thu, 28 May 2026 18:29:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944780a72d737389e1c49c88af87d432f0bbaee0a19550bc56bcf4007425ce9e`  
		Last Modified: Thu, 28 May 2026 18:29:40 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:4d9da7c04b96d1bf4b8aabba55a35ad2b7930d8cf4e2ae86505d47ffd2a4d1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa1c19cff9484440b96eb878a5402ef57209b934acbdd504c4401e6464617ea`

```dockerfile
```

-	Layers:
	-	`sha256:eaa9b75a0fa1d5b1f8a9a9bdd103656aa4d6bf5659dec1bbfe927625f82c1a7c`  
		Last Modified: Thu, 28 May 2026 18:29:40 GMT  
		Size: 2.0 MB (1973817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93a22b57a8e8917957e7418bedfcae2c2f49c9b35442f7c4b5753757026636a`  
		Last Modified: Thu, 28 May 2026 18:29:39 GMT  
		Size: 29.5 KB (29457 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; s390x

```console
$ docker pull redis@sha256:d62a88c0285769190f55d24a591a670f8448dcc758e91200bcf1c3106a5e277d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44580078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14432714fe15232671ce95ed55e54a05c66912875d23289cbad929199b6015ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:12:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 20 May 2026 00:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:03:57 GMT
ENV REDIS_VERSION=8.8.0
# Tue, 26 May 2026 20:03:57 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz
# Tue, 26 May 2026 20:03:57 GMT
ARG REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
# Tue, 26 May 2026 20:03:57 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list; 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			automake 			autoconf 			libtool 			g++; 		apt-get install -y --no-install-recommends clang-21 lld-21 llvm-21; 		export PATH="/usr/lib/llvm-21/bin:$PATH"; 	fi; 		rm -f /etc/apt/sources.list.d/backports.list; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		export LTO=1; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 26 May 2026 20:03:57 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.8.0.tar.gz REDIS_DOWNLOAD_SHA=19736ce6117d90b3df032504c6e5c1ce41667ae47f073281b40d2f274c200a74
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 26 May 2026 20:03:57 GMT
WORKDIR /data
# Tue, 26 May 2026 20:03:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 May 2026 20:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 May 2026 20:03:57 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 26 May 2026 20:03:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30efef771b60229b0a8ca1a6810fff32a9856e4d0da16ef66fe8c61cf5925da4`  
		Last Modified: Wed, 20 May 2026 00:13:57 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd642b270b5561badb1d9b778fbd71bcf6ef4d6651e84b5e2aedb357848de020`  
		Last Modified: Wed, 20 May 2026 00:13:57 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447084278aefa2eba02c1f9935493aa12c445007b39173cd8002eb5f7ee6d490`  
		Last Modified: Tue, 26 May 2026 20:04:10 GMT  
		Size: 14.7 MB (14729991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7940fc3ee8d08c4dceb63e760fd8f55b84f18e87005526b40fdd1a057c767a`  
		Last Modified: Tue, 26 May 2026 20:04:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9256d5a04499b56d1384f3cf03d9816f113cf8a884de549bc7134014d86bd7e`  
		Last Modified: Tue, 26 May 2026 20:04:10 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:27d3be30d1aa52de96228eecff42f35d5b67565b7f146ad3eea43d92003fdf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2010710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886ff471a4c71d34907d146521be25643766ec562a6c4f48cfcddaf12c06a17e`

```dockerfile
```

-	Layers:
	-	`sha256:19628e8a7a998a62bd5db10bf8233e6edf486e47949af3b379623d317365629c`  
		Last Modified: Tue, 26 May 2026 20:04:10 GMT  
		Size: 2.0 MB (1981326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b039499fd3a46e0866d4b185e9fba9a887e24eecea7b0613d30c8d1562123fa2`  
		Last Modified: Tue, 26 May 2026 20:04:10 GMT  
		Size: 29.4 KB (29384 bytes)  
		MIME: application/vnd.in-toto+json
