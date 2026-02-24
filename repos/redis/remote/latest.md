## `redis:latest`

```console
$ docker pull redis@sha256:db01931cfb4f86d0bb076f0744dae4ebe50f6b1cabcacaa0c6da685b8ad037e5
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

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:9bb8e98889679d1dcd42794248b5c7d480e69b7f08906bdd872981bf2c8f232f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53234809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c234a24851ba3f2089a7c7556f22bd5e889cc082b8d19a60d1544e5df651e60b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:16:49 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 24 Feb 2026 19:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:06 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Tue, 24 Feb 2026 19:23:06 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Tue, 24 Feb 2026 19:23:06 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 24 Feb 2026 19:23:06 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 24 Feb 2026 19:23:06 GMT
WORKDIR /data
# Tue, 24 Feb 2026 19:23:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:23:06 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 24 Feb 2026 19:23:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214ecf6e5c87b8c05b527ae904bab4bd32631c35951e69aa74f6b82cb2a3a02f`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b1b12d71095bb33e00db551da5d25556eacf6925feb4fcd104528e51b0bb6b`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f5c85b90de345b6ebe490560f7831c046853f1977daf7b27d754b35a2e792`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 23.5 MB (23452014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae77945b0371c0cf2e0d017db359d17b0645b1df997621100c449adfa5a38d21`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141e1fc22067fbe33bef9c743a0440fc9b940b6dece3152acbbce9e1c841b86a`  
		Last Modified: Tue, 24 Feb 2026 19:23:16 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:fa85b06ba4594b4f0e5c424c7a4c64f8c6d7fd34b65bce19745a4459b7b8ee67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f43142c92917556193da68595b89a67985720c9dfd72b8e72b6c18c9954a0e`

```dockerfile
```

-	Layers:
	-	`sha256:4a4db1a35d5b3ba1fd2a8ba6bd9f1a243c718fb119f0edf8dbdeabe002d2fbca`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 2.0 MB (1979801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e798a26a6510bdeab1ab192bf756cd003edddc951e55cf13146b689b82a002ad`  
		Last Modified: Tue, 24 Feb 2026 19:23:15 GMT  
		Size: 29.7 KB (29678 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:760707c5b760b9a2e41e83f15a1a0ed430f264ed241a9569f8d9a2d0a6e9767a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42182055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a07d47ccc74477999bb5ea5464dacf178a12c70e343dc23f88967fe71eb691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:43:49 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 24 Feb 2026 19:43:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:45:04 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Tue, 24 Feb 2026 19:45:04 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Tue, 24 Feb 2026 19:45:04 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 24 Feb 2026 19:45:04 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 24 Feb 2026 19:45:04 GMT
WORKDIR /data
# Tue, 24 Feb 2026 19:45:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:45:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:45:04 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 24 Feb 2026 19:45:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db909375714c3fac810e76fa9ad54663bde76d890422f15c46fb850bbb42ee`  
		Last Modified: Tue, 24 Feb 2026 19:45:11 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a5ec41df531f11350411e2430f4d1a74ac3ddecc6108b291ca06e2fc4170cd`  
		Last Modified: Tue, 24 Feb 2026 19:45:11 GMT  
		Size: 832.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084f8758e3e2b9f7eb896adc43643b6e51cefeeea2d11e7afeed588704b9881c`  
		Last Modified: Tue, 24 Feb 2026 19:45:12 GMT  
		Size: 14.2 MB (14230276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a193486584940d9010b413b5d6b7e351c41fd9090b30a8baed109ac2b7502a1c`  
		Last Modified: Tue, 24 Feb 2026 19:45:11 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68f5a8c746bd28e3471b64a0046fa30a223ccee36f835edd64ac4696af0e14`  
		Last Modified: Tue, 24 Feb 2026 19:45:12 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:08e9449a030e4e6c2026158d7469cccaea67d8992d61ba3fbd4bc3e234080301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2012623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2188cd9f74e57f8227130e2bc00f75095baed8aa9f48fbe6d19dfd169f3e3cf`

```dockerfile
```

-	Layers:
	-	`sha256:690282e71c12d19fc20cbd3e2facf4ec84fa27c6464e3af03c138c6c1ec2addd`  
		Last Modified: Tue, 24 Feb 2026 19:45:11 GMT  
		Size: 2.0 MB (1982794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e010cc8a1153d7ebaeacc3eafcbfd99444f7ee44c9e0efd017a9dc16d20985c9`  
		Last Modified: Tue, 24 Feb 2026 19:45:11 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:6ec1d6c1ee1213aaf6d1732e65a6791bcda0e742eb759c014eca4facbc669b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40209357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e055a36f2d150d4181463ccee6ab49e92c7ffa1e920a1ee950431d815d9e4bc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 24 Feb 2026 19:51:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:52:53 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Tue, 24 Feb 2026 19:52:53 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Tue, 24 Feb 2026 19:52:53 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 24 Feb 2026 19:52:53 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 24 Feb 2026 19:52:53 GMT
WORKDIR /data
# Tue, 24 Feb 2026 19:52:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:52:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:52:53 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 24 Feb 2026 19:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68f9fff9d29e58f69378a7a60c968efa95bd5dbef403e4c88cd1413f4c90af3`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ceb2811691bdc37f7f5e7c88c5869b390271c05b794ea0f04a1a21c27a20f`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fff1544a2b09139306a30bc805b2e4a46670d8b225196bdece2d4a257f3f5b`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 14.0 MB (13991445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306d857d9976af2ac8eda60e1d3736b3b0b31f6580f4d4c96a25fb7e0f46a703`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ca1612e451662ce1c7db545d5b83a2fe33a4833363c284dbb635d067d4f1f4`  
		Last Modified: Tue, 24 Feb 2026 19:53:01 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:bf5dfa65c08c0a38bdaaf59a7c469080a2e5c473d8322b9a4751d6cab894cba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2011060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560bf54d259ee30a39c21f670dc1c056785a76010500706b81eb4f0dabc68827`

```dockerfile
```

-	Layers:
	-	`sha256:0f1cc8b081da6fd39e5ae77b0bb146469a588712ee2025d83128a88684822e8d`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 2.0 MB (1981231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1cd88fedaf3b837e82915af0ec51ae31a713afd7398dcc7093adddfe41256f`  
		Last Modified: Tue, 24 Feb 2026 19:53:00 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b7e0bf9f5642e27acc72c1f031aa452c29f96f47ec89cf045df14918add7e836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53331872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35267b49b0841029c5168ff138d4ea5e820a868ff87c07c1972cc674c41677c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:57 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 24 Feb 2026 19:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:52 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Tue, 24 Feb 2026 19:27:52 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Tue, 24 Feb 2026 19:27:52 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 24 Feb 2026 19:27:52 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 24 Feb 2026 19:27:52 GMT
WORKDIR /data
# Tue, 24 Feb 2026 19:27:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:27:52 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 24 Feb 2026 19:27:52 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fb95a872ea7654fae0db624c661bf164d0f71d45de4ca7ea3ea108975b1fd`  
		Last Modified: Tue, 24 Feb 2026 19:28:00 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d7426568fcf74e745c5f007bac8c515da66a6278e72d500b2f5ee3a4d48971`  
		Last Modified: Tue, 24 Feb 2026 19:28:00 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d7f1255eedd93de4e7f51eb43081b18bf4257b104ac516ebedd9379eb99690`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 23.2 MB (23187612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83426d9267bceefd375a81f083a9adea4313817b5e480704eb5980ad8d313a33`  
		Last Modified: Tue, 24 Feb 2026 19:28:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee39f16a53f159e60e1738c682f6f2af61894b80382ecf5eb4e2116fca60775`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:7e48fe9d82c68b59dc2aec9400e5eb7ddc740c6b60c65ebc3f2b230ac22469f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2009982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67452cd7c448339368ccb57da4d831125d455ca8ed884c65b5bc5cc847a5cb`

```dockerfile
```

-	Layers:
	-	`sha256:4bb7e66c93a3e7057c938d36d084803ceb246f8a58438eae10c2eef3b275d114`  
		Last Modified: Tue, 24 Feb 2026 19:28:01 GMT  
		Size: 2.0 MB (1980107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4119f85571323aea57967b0a5b4ecb30c29b6f3b4b2beda6bc4fb4250cfe9308`  
		Last Modified: Tue, 24 Feb 2026 19:28:00 GMT  
		Size: 29.9 KB (29875 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:1b0c7eebcc9744423686a62fcc8bb1a3e9e3e1ae411288d5061539710a6be0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45057420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c8bcb09dd9b3855911b234c776755474f92a7b195593bf5cfbfedde665f6ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:56 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 24 Feb 2026 19:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:22:02 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Tue, 24 Feb 2026 19:22:02 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Tue, 24 Feb 2026 19:22:02 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 24 Feb 2026 19:22:02 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 24 Feb 2026 19:22:02 GMT
WORKDIR /data
# Tue, 24 Feb 2026 19:22:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:22:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:22:02 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 24 Feb 2026 19:22:02 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42bf1cae7551ca687cf0615de45b1429e405f0cd754430d9a1cc9ca269deca5`  
		Last Modified: Tue, 24 Feb 2026 19:22:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4b3398e4d8d475f5be2ee38d9a9a18bfbba48c8c951358fa9e7fec2424eda0`  
		Last Modified: Tue, 24 Feb 2026 19:22:09 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218e71ff9f2d541fc3813c85e78ea10947ba5f23752154cb61a11a81787c40f1`  
		Last Modified: Tue, 24 Feb 2026 19:22:10 GMT  
		Size: 13.8 MB (13759338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32660e66563be96146c021a140f3c4b39023e9cff19b44de2384222fdad33a6`  
		Last Modified: Tue, 24 Feb 2026 19:22:09 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098472785f9cecea0353e64a9934d2211be871a8caf35b5918053de7da11184e`  
		Last Modified: Tue, 24 Feb 2026 19:22:10 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:35c3a752f667ae7ad1cdc42911d3a2e4c312f459cf7b56dc6ece26ebe8a52295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480db6a20f76d158b72f3f953fca0c8c4e042b344239d2a5ad652eb8cb6120e8`

```dockerfile
```

-	Layers:
	-	`sha256:a2e7c37b6f0967a12a90fab42951be449b42b8e7585df0ba8a8bb675d71fc1d6`  
		Last Modified: Tue, 24 Feb 2026 19:22:09 GMT  
		Size: 2.0 MB (1976978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1986efee98f8050d6690b65ded91c366c45cf5d0949127e923a91dce485d2ac`  
		Last Modified: Tue, 24 Feb 2026 19:22:09 GMT  
		Size: 29.6 KB (29620 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:e7b3083951d50df6056d625b81b46ded1a32fd8ac5ecf0ea2ace327fae8bf97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48827336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13758a1a5b64ad28eac0f0e6668159a85d150bacebbba5785e1711d2d0525ea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 10 Feb 2026 19:03:46 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 10 Feb 2026 19:03:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 17:33:31 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Mon, 23 Feb 2026 17:33:31 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Mon, 23 Feb 2026 17:33:31 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 23 Feb 2026 17:33:31 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 23 Feb 2026 17:33:32 GMT
WORKDIR /data
# Mon, 23 Feb 2026 17:33:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Feb 2026 17:33:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 17:33:32 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 23 Feb 2026 17:33:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e15f524567fd84c65a1882209b262142d489a5cfc2fe5c6fb7899016a6c848`  
		Last Modified: Tue, 10 Feb 2026 19:06:12 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e28724f2ee579fe71f1089b38ad4635b03b42e6ac6642e3b20cd6de546e77e`  
		Last Modified: Tue, 10 Feb 2026 19:06:12 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e20c2e388b1db686073e1d6ce3dab4b4e643b2f2648b09e2477576884646b44`  
		Last Modified: Mon, 23 Feb 2026 17:33:49 GMT  
		Size: 15.2 MB (15222987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ea98e645cf0d6f9b813ed813f75ed89bb38813c947c95524ed1402781960e`  
		Last Modified: Mon, 23 Feb 2026 17:33:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aca87297c792a25f65f560f85681e47c04faadbe7a9a396ae6da6a09e8be83`  
		Last Modified: Mon, 23 Feb 2026 17:33:49 GMT  
		Size: 2.1 KB (2104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:71cc78273689ee8a5b0dd1ab7ad0e0f7443188f9321fd88dc851297f267e9b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2013088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e490af2abddc3c8982bbf858b3a277761129630ab864b696f852a92fb9c36476`

```dockerfile
```

-	Layers:
	-	`sha256:a98dd727f38ea5d9733460129430b1d316bfea12ed4c228216641da64db7c33c`  
		Last Modified: Mon, 23 Feb 2026 17:33:49 GMT  
		Size: 2.0 MB (1983336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f1c2b9de6af8fd25e7070e974463541d659f9772d1d00189318ba6e1c4dbce`  
		Last Modified: Mon, 23 Feb 2026 17:33:48 GMT  
		Size: 29.8 KB (29752 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; riscv64

```console
$ docker pull redis@sha256:494a8e614ca7e06e536398d91c55390045460f217555592f0fd9f051c2783592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41791776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2186165dcf78226a822eac19173fc7b428606fb4db8aac18712f333613ba436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 02:45:23 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 23 Feb 2026 17:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 17:49:54 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Mon, 23 Feb 2026 17:49:54 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Mon, 23 Feb 2026 17:49:54 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 23 Feb 2026 17:49:54 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 23 Feb 2026 17:49:55 GMT
WORKDIR /data
# Mon, 23 Feb 2026 17:49:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Feb 2026 17:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 17:49:55 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 23 Feb 2026 17:49:55 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2a1a3f6a1a1e5156270a50f9575d68a42cf3b8eb587ff9352d2c2e83082ac`  
		Last Modified: Thu, 05 Feb 2026 03:03:46 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c5bff277e53bb02abc5ce1542b0e84db74175ada1558a98ff8e6ce2b89da47`  
		Last Modified: Mon, 23 Feb 2026 17:50:58 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d10ab0b56b739999fd9f28b6185b00bd176b2a740796a571efa7ab0d4a88f`  
		Last Modified: Mon, 23 Feb 2026 17:51:00 GMT  
		Size: 13.5 MB (13511224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4111de6232f98595dd77ad6d82563b9db8b8cc2c50a0d9fa98f19e8ef0c4e321`  
		Last Modified: Mon, 23 Feb 2026 17:50:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0086028ae1507d099f62e4bc5679af0095dd17ff2ba975c475fcf5008e18db9`  
		Last Modified: Mon, 23 Feb 2026 17:50:59 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:6ae7533a77a051df7650ff6e4c1ae839758f4248aa70b31671848ac4bb9ffec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2aa6053d025efe66e2d531196afeb2eb2ffc5af70ca5b431f35b6df4a58361`

```dockerfile
```

-	Layers:
	-	`sha256:7c42c4298042fc2d6f298968f6c5393f0571422e098c2a1b50b71f2e8ec32a6d`  
		Last Modified: Mon, 23 Feb 2026 17:50:59 GMT  
		Size: 2.0 MB (1973739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140a8bebafd99f6f048376b9fa387ad80518d2592a58646e827f3bee883328e4`  
		Last Modified: Mon, 23 Feb 2026 17:50:58 GMT  
		Size: 29.8 KB (29752 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:8330dfb87e8dce8e943fc6d8522bccf4cd9064a09941765b672568239bed1adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44674454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf6273dd1c04925a0908557d72544c574a128b7f56a5a18c88ecb36274047d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Mon, 23 Feb 2026 17:31:34 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 23 Feb 2026 17:31:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 17:34:16 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz
# Mon, 23 Feb 2026 17:34:16 GMT
ARG REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
# Mon, 23 Feb 2026 17:34:16 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get update; 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 23 Feb 2026 17:34:17 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.6.1.tar.gz REDIS_DOWNLOAD_SHA=88ff5661160bf4b12aba2dfc579b131c202e75a3ac1f0b1d06db05a9929d5a89
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 23 Feb 2026 17:34:18 GMT
WORKDIR /data
# Mon, 23 Feb 2026 17:34:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Feb 2026 17:34:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 17:34:19 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 23 Feb 2026 17:34:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1291cb8a0ecdcdaeeae344992a3e3ee0611216c0697864abf336d9d65dd2a2`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a522b64d1892bfb1d844dbebb4ea19402e71021bf0728437b120ba6f1f898a21`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6323f0406f9b85445e2ab4d679affbdc6ab5d698ba5b0d47749138422d1d4073`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 14.8 MB (14832136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d70ffeddd6c4929e87c949b257bbb040eb1dac03432757ccd4b25fa80c7766b`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fad2f9b1592662b4b7d4c4f56087c2672dfb32f0d108bf8d3443a1de30da88`  
		Last Modified: Mon, 23 Feb 2026 17:34:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:dfa30c7201772ece8df10d5fdbb02dfc4ea773fd64e0c5d9d9ae5d186b135022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2010925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b49f108d6510a76d7f7d4e00e00e42beb30680170dc4c2df8f70e28e8e515f`

```dockerfile
```

-	Layers:
	-	`sha256:00f00c9cee21a5299cc43937fcc638bb1d9640f6f0b85a5fe85fda379f0eeae7`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 2.0 MB (1981248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb464db3d3d78edbbd63403d355b2b27d979b31406364705e6924d009796cc6`  
		Last Modified: Mon, 23 Feb 2026 17:34:35 GMT  
		Size: 29.7 KB (29677 bytes)  
		MIME: application/vnd.in-toto+json
