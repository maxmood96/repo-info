## `redis:trixie`

```console
$ docker pull redis@sha256:0c341492924cad6f5483f9133e43bd6c51ecdecbcadfac5b51657393b6a7936c
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
$ docker pull redis@sha256:94ea4f5ccdaa6b154df99a792986ecb3ffbb3fe7722a197220477f1f3e65f9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53283054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56937f91b9b70e81874773ebaa8f72300f2f59e5e0a27a9c56bed841f142c244`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:34:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:40:11 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 19:40:11 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 19:40:11 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 19:40:11 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:40:11 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:40:11 GMT
WORKDIR /data
# Fri, 08 May 2026 19:40:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:40:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:40:11 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:40:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c3033571c54f9b212794f6ccebb87f3b96b8770e9d9f394cf5cc7fcc68ccd9`  
		Last Modified: Fri, 08 May 2026 19:40:20 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39932f0416f73157004ccc003b42146b3038adb9b901a370077b8ee811e12919`  
		Last Modified: Fri, 08 May 2026 19:40:20 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188c6fff82e6c660facedbec30438ab7e6d929c6fb1b48f587d13b20eb4a5228`  
		Last Modified: Fri, 08 May 2026 19:40:21 GMT  
		Size: 23.5 MB (23498657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e422956e4a5a81064fefe608584b3173c853e25ea62111f1d89e868359b168d`  
		Last Modified: Fri, 08 May 2026 19:40:21 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb1988805dfdadb51e917faa670537c8357fa3983b884a7141af789772ab97`  
		Last Modified: Fri, 08 May 2026 19:40:21 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:68968b74bd96d4e2db262b383f0dd4d1fa47ccbe3e93e1020018299abcc10e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2008183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c1ee46b4d9a494d9f40de6f6179f9dd776a449de59a43b4b4739db9e66c8bb`

```dockerfile
```

-	Layers:
	-	`sha256:f62aa748d96dcf9b9740f656d539c13446dcc90c308411094fcfe7ce04243f80`  
		Last Modified: Fri, 08 May 2026 19:40:21 GMT  
		Size: 2.0 MB (1979837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c6b874f46d84836dc92c0b044af1a13e057ef4a865656f0619fb5d8c38223f`  
		Last Modified: Fri, 08 May 2026 19:40:21 GMT  
		Size: 28.3 KB (28346 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm variant v5

```console
$ docker pull redis@sha256:653518ce11b63ef2bc13fe48832325a677431f16a7a848c864414eb9c23fcd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42195604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c395ec7eea71da03c4e77e39bed5a1596d03b619f8adf0390ea37c547d6ff04c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:52:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 20:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:54:13 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 20:54:13 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 20:54:13 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 20:54:13 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 20:54:13 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 20:54:13 GMT
WORKDIR /data
# Fri, 08 May 2026 20:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:54:13 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 20:54:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04fc79dea02365634bb2b86f59058cd2e89cbf5826b8cf36205d0e78a822ca8`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7453f894e0ff3bc1a7366239d25ff7ac5b2e15386f9cf70d6975aac79fa0c3`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a54b349950410ae90864dc307b625e5a9f2d5598382455f288bfa93c4eabb84`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 14.2 MB (14243229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52294367f4b8199146755a7c490ac5b55d0f7ae5eef5b07916db6a59bc6a592`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b0f17cc6a15aefed93d775cc1654fe908d98ed36fc8f331385bdfb898016e3`  
		Last Modified: Fri, 08 May 2026 20:54:22 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:b50a7de2cd4489bef92492581f5be1b3a99e0e890a9d720bd32e32898156e2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2011326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234d7e9280d00aec4b7b39cdff88b5d9f9e7fc1153574f22f9967a70a034a5dd`

```dockerfile
```

-	Layers:
	-	`sha256:53e355f338eea6f9510c2e6ba8019675b8fe85b0267440c05aad6a86d8b90463`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 2.0 MB (1982830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de07f51dfc04226323df8a54061948b5f2aadfa44d72cadca530d00a36b9ae2`  
		Last Modified: Fri, 08 May 2026 20:54:21 GMT  
		Size: 28.5 KB (28496 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm variant v7

```console
$ docker pull redis@sha256:9769bb99b59fa4d75d83bd63184c5bc0d21751320862b03b5d8630fc85ce7f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40219462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53577b5911805658f02d789151f1aca991e6c809f8b60672ecf15700c51f9421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:14 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:40:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:20 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 19:41:20 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 19:41:20 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 19:41:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:41:20 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:41:20 GMT
WORKDIR /data
# Fri, 08 May 2026 19:41:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:20 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:41:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81709f75a0a450f1a2c57cf056e4db4e3919bde162575123a6d6db6d4c171f32`  
		Last Modified: Fri, 08 May 2026 19:41:27 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd4c25d4d78f057b5df4f8e27385afbeb699d6dbbd012568160c081eea8be5c`  
		Last Modified: Fri, 08 May 2026 19:41:27 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41b0bd04921ccecfbbb3c21d3f829b3bb1773690641541e843090e904393ed`  
		Last Modified: Fri, 08 May 2026 19:41:28 GMT  
		Size: 14.0 MB (14000383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9929159a029470f8ca544501afe65f0e3a302e3aef135b05b21ba26e9018f6b2`  
		Last Modified: Fri, 08 May 2026 19:41:28 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a38d23eacc906f0c1cbe14c8c1528a5ea09d556c9bef1546d7bb645b0bbba5`  
		Last Modified: Fri, 08 May 2026 19:41:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:5489399d394594c9fd799ce043c247984cfdca8b40d8dc0600564d247e44da9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50289a0e0df0dc2da94228a14c80713dc3844514fbb0689f626bd6eb7c8ee21d`

```dockerfile
```

-	Layers:
	-	`sha256:0bd5c30951b522556d2216bf725c7d533a465cc9c73d653f5b7d10b104754fae`  
		Last Modified: Fri, 08 May 2026 19:41:27 GMT  
		Size: 2.0 MB (1981267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fb4de43aac8df096c37795ebf38c2d84153630a26530076da645825db5a04c`  
		Last Modified: Fri, 08 May 2026 19:41:27 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:f2394cd907d952450d3c9235bd626070db93e898274df9c840864131faecd6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53386217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d78b72d2fbbcaf9fbe82189409310b05cc588a82312e3a84398ba19b809d98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:35:22 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:03 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 19:41:03 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 19:41:03 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 19:41:03 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:41:03 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:41:03 GMT
WORKDIR /data
# Fri, 08 May 2026 19:41:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:03 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:41:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0223ff68dd48a77fe168f26c0a46068ba87cded5a44e7cfefbe23bc14580998b`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17700a48c5e5f24a537a52b2a81a40a4f37caff8fd3f1936d79b5a27b2265aa`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4d17099fa1dcd84b639ad4275475703088fc5aa9d2d4830fdb48ae8090b895`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 23.2 MB (23238408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdbb90f87d388abaef266b73dd37dfe738eb86b8d20d80c1dd777e557820ed3`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3533fe182a5f4135c37b14c5b235332fe40b9c6ad9ec41f3fe18e652ecd4fd50`  
		Last Modified: Fri, 08 May 2026 19:41:14 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:08e571f5775d70364b471e879f336834308ac0a690aa069ac53f6601083c7bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2008686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611ecd40bef3a09bde59a38345bb575c6cbe89c6e4f60fab5b5ef5bbfdddb93`

```dockerfile
```

-	Layers:
	-	`sha256:2d4b196249e8ab0ad2adf35e79825b1b508299122e2e3a6cc707804619f1447e`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 2.0 MB (1980143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b9aa8e4153731532a8f01c8176e13067b1f7efc343c40652fc03758db0fe6c`  
		Last Modified: Fri, 08 May 2026 19:41:13 GMT  
		Size: 28.5 KB (28543 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; 386

```console
$ docker pull redis@sha256:95fab50661ead62f3c5d05b552e1a815f697038fe133efc4ec0a68a46168d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45074479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c1504f6cbfaa13ec02857140fc578a19acedb6f46dfb453d67cdf1ff8ddf98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:12 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:23 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 19:41:23 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 19:41:23 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 19:41:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:41:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:41:24 GMT
WORKDIR /data
# Fri, 08 May 2026 19:41:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:41:24 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:41:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3f272128b80ccfa084632c4eaa1cb3b55e73aa45a2374eae68f9b24e292621`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0238652c960ea673f7703d909f5d761ed647e4a0f7fb401995151af6246ab8a6`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c707871d96795ad9d2caca2ffc28c33d4a69f7938994a7b10f5b4c4212d2c9`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 13.8 MB (13773911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbec9f3b28313750fef76eb4a7226ff8508cc874d6f74ae24c158fa4f129f87`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cbe7b38c4a61dc5834677c9d53adfd62d9ba434473daaa9e2b67caf947a57e`  
		Last Modified: Fri, 08 May 2026 19:41:32 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:227dc2c2014a064f510df01cf10fad7db113eb2ac8359e811af1f73fee572087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a3bfbc51f4155d088a513f75aac1fe465fb7d49c69ef696142b7e92565083b`

```dockerfile
```

-	Layers:
	-	`sha256:382fd020ccffd2de8cf0b566832c0f3d714d4a5f24f8d785af92e3b5a2b259f4`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 2.0 MB (1977014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15749208bfdf3a6deffbd6c1732ed340178791e8530e46de0531a8e5a072dbd2`  
		Last Modified: Fri, 08 May 2026 19:41:31 GMT  
		Size: 28.3 KB (28288 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; ppc64le

```console
$ docker pull redis@sha256:95c4f80b6fbfd983a613cb9bbf4c687957e321c641fdb5efc0b29b93f94b503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48840664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09be3d16555860f07591657c40e6243e13493a6d937f3b90ea7f3f788193059`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:45 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 22:15:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:19:17 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 22:19:17 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 22:19:17 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 22:19:17 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 22:19:17 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 22:19:17 GMT
WORKDIR /data
# Fri, 08 May 2026 22:19:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:19:17 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 22:19:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abeb7db92f9c001276b72d8f345f5e5746b1368cf3586d5f92b0e73b8801daa`  
		Last Modified: Fri, 08 May 2026 22:17:39 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d466c95b650ca7292b8f4a460d224eb49608d34afff17b62f5ecad52bd0253`  
		Last Modified: Fri, 08 May 2026 22:17:38 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03896c01d933245ba3b45238510528681f55fc09601947ce3c3f67842a004c8`  
		Last Modified: Fri, 08 May 2026 22:19:32 GMT  
		Size: 15.2 MB (15238411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e7c2c7e0dceb34cae47ffd0ecde992c411107bb68fcdc2d83c66799d9040`  
		Last Modified: Fri, 08 May 2026 22:19:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a158d514aa04d3fc1e7573790908d4f1a3bf26b71cb7644886e32e456327aa42`  
		Last Modified: Fri, 08 May 2026 22:19:30 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:757c0ce5da4af9e1b04120ad67f01b7a93aa4fa565d705fe69bfa68d82ff8633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2011792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497e7e7c0b10fd03f7dcd0f7c727f6398a70e7df2259f54e4480b9eecde05467`

```dockerfile
```

-	Layers:
	-	`sha256:f8abd84ecc2e71e6223ffda1659d37b40cb5482c8d0e45c73e3c9bc9a23ac3ca`  
		Last Modified: Fri, 08 May 2026 22:19:31 GMT  
		Size: 2.0 MB (1983372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6ea0fc8a2bec7d992bbfc09d057fe46ad75dd1dbbf22a45de364d2002fc5dd`  
		Last Modified: Fri, 08 May 2026 22:19:30 GMT  
		Size: 28.4 KB (28420 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; riscv64

```console
$ docker pull redis@sha256:2f9c93c94de5a71081add7568a7a0eba577527e425d1462911755e949a260ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41811611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7484f4e7b6d773ea623a288517b571c0058ed0b775e0062c9a1bfde7a9cc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sun, 10 May 2026 22:40:54 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 10 May 2026 22:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 23:16:25 GMT
ENV REDIS_VERSION=8.6.3
# Sun, 10 May 2026 23:16:25 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Sun, 10 May 2026 23:16:25 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Sun, 10 May 2026 23:16:25 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 10 May 2026 23:16:26 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 10 May 2026 23:16:26 GMT
WORKDIR /data
# Sun, 10 May 2026 23:16:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 May 2026 23:16:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 May 2026 23:16:26 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 10 May 2026 23:16:26 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17444fdc2dfba18829753a41034f2a971a21bd37149b5efac87d130399a3e0fd`  
		Last Modified: Sun, 10 May 2026 22:59:26 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce9e1f11023489f41b9f55287fe99fe4c7e49dff7dc8c8642acd9f652bb4fc`  
		Last Modified: Sun, 10 May 2026 22:59:26 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f91f392575e7079feadedea0ac0df7c45d06c86a964d58c214583a276ae5e91`  
		Last Modified: Sun, 10 May 2026 23:17:32 GMT  
		Size: 13.5 MB (13527212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2dbf7f3206807fa3968f02e44577ed4e2cf26e48ff7659513344ee3ee6dc87`  
		Last Modified: Sun, 10 May 2026 23:17:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa4562d72d85bc22f67095bba861779618aeb54fca374d5cb25cb1c918690ea`  
		Last Modified: Sun, 10 May 2026 23:17:29 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:a8ddeebcde78602638891bf2351b49419dcf60d57acbf70cb7771158e37cd8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11d924d63ab26628fc7c28a968480d845051ca451fbf26a502539fde1923d9f`

```dockerfile
```

-	Layers:
	-	`sha256:6a4170193dbc0e4a09301b8c4c0f7fd3e33afc9c029ed6710eab37a24bc26b21`  
		Last Modified: Sun, 10 May 2026 23:17:30 GMT  
		Size: 2.0 MB (1973775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd453a98e93917f541478a75bb7de864c3b53caac3dc0abd4167b7e91448cc7`  
		Last Modified: Sun, 10 May 2026 23:17:29 GMT  
		Size: 28.4 KB (28420 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:trixie` - linux; s390x

```console
$ docker pull redis@sha256:f29fccd53b969666f3467dfdc7ccfa3cf475f90ca5048ecb06086944e4aeba40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44689631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d2783e09c856c81d3b5eebb6ed93d8d47923706178fb33f88d5b38ddf8793f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:44:44 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 20:44:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:47:43 GMT
ENV REDIS_VERSION=8.6.3
# Fri, 08 May 2026 20:47:43 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz
# Fri, 08 May 2026 20:47:43 GMT
ARG REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
# Fri, 08 May 2026 20:47:43 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 	make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 20:47:43 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.3.tar.gz REDIS_DOWNLOAD_SHA=58d0d1eb49a1ea6c2179659707fec171b1e2e2b8d5157ed2ec59d1d66ad5a654
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 20:47:43 GMT
WORKDIR /data
# Fri, 08 May 2026 20:47:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:47:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:47:43 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 20:47:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a58c57fdb282ab1a973bff527b6a721449b94cb6d99008d8183c13e2689b6d`  
		Last Modified: Fri, 08 May 2026 20:46:12 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3e9fb35e032a8955d5459a42384784baa600bf0e26e5e308c6491dea6ade73`  
		Last Modified: Fri, 08 May 2026 20:46:12 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26513b326a94c2fdbbd08fa7971a7f95a317f212a18610f25909f535d2cca48a`  
		Last Modified: Fri, 08 May 2026 20:47:56 GMT  
		Size: 14.8 MB (14845116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c309ab290a18373ab2c69cd939c2e79df4c847837299365d04a8318331ef5b`  
		Last Modified: Fri, 08 May 2026 20:47:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ea8a8e9982cd19ebb1b34b5664e46c401dba4fd351e57bb0a3c548d75f0bdd`  
		Last Modified: Fri, 08 May 2026 20:47:55 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:trixie` - unknown; unknown

```console
$ docker pull redis@sha256:79d833cf83a57dea42f7b208b376f8148df659bb68eae5aa1b91a01ccd87dcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0ee3bd8f73373ed604e161de2d5284fa12c6e27bfe8e5bc637261818b2e415`

```dockerfile
```

-	Layers:
	-	`sha256:e5467aada87a0040000564ef943ec9757486f37c103ec721046e41986ab5accb`  
		Last Modified: Fri, 08 May 2026 20:47:55 GMT  
		Size: 2.0 MB (1981284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9743a70457de18dadb079d70f0ea19d03fe8d4a0c6811c30dd59aa7518028a8d`  
		Last Modified: Fri, 08 May 2026 20:47:55 GMT  
		Size: 28.3 KB (28346 bytes)  
		MIME: application/vnd.in-toto+json
