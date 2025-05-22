## `redis:bookworm`

```console
$ docker pull redis@sha256:c49bdcc516aa4b2d66d8a46526afd7d38f2e53d069c5a2c1cb0efe76ebffa737
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
$ docker pull redis@sha256:5ccc8af4cdb4f8fe6fe87eb71f7cf8ea41517a6fd26a18965fe904cf776ec47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49492090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b270fb6df331ff456014744f4fd3de812584386de75e762dc73add32533311`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 13 May 2025 16:54:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9e5369fdd31f94d945e37f1eda5d234645d0015737905d72f58cf7a72979f`  
		Last Modified: Wed, 21 May 2025 23:20:59 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f8315b617aca47a4147192ba0f21c1bfe2e76323d6c08f8b1842829bb129f7`  
		Last Modified: Wed, 21 May 2025 23:26:13 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61abf5b1052a4c81a7c15ea930c776348fe4146096fd172cf727515ab7fb9c`  
		Last Modified: Wed, 21 May 2025 23:26:14 GMT  
		Size: 21.3 MB (21263473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc4ee78aa861cb00278c75b783cf4a1f682a6d283da5e9f000b4695720f6f6`  
		Last Modified: Wed, 21 May 2025 23:26:13 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cd3c5153abd3ee5674c4d7cd2d1ff6648316ccb0a99387286cd3121997759b`  
		Last Modified: Wed, 21 May 2025 23:26:13 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e9b56cf9c41bf34d502025177cc9ab1f79205c2727f5794afbfc970477f2c433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67df9173a049d67dac540167e8f667eef9ca1a86c9a94840c5ca886926a6f8e`

```dockerfile
```

-	Layers:
	-	`sha256:9034724d74be81346cd158e0c5df6fb309bea6fa0775c9c929f3e0a75807a908`  
		Last Modified: Wed, 21 May 2025 23:26:13 GMT  
		Size: 2.3 MB (2280517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5256a8f69eca663a9227159ff2c8dd3097a187ba89f6486cf8445b8260f8356b`  
		Last Modified: Wed, 21 May 2025 23:26:13 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:904f3d54aec32914fad45c44d175433d7125f383e1dd1365dea5e0add6f6b8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40914111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c0eb794ccd26bd7c7f4531247615f4ebff9e9c97828d5cba1c8c255c22ab44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84254828f2cdb11b5c05d484ee88b3ed4b137ac983f2750561120d3d705c122`  
		Last Modified: Tue, 29 Apr 2025 00:45:25 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4580e7c1a0569ed4ae1415bfd2506cd308cd2cb87a19ba768ded0cd623455bc1`  
		Last Modified: Tue, 29 Apr 2025 00:45:25 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698d27b2b8594a35b2294fca6f5b4c90ce1cf06ea63e325b8bd527d563249888`  
		Last Modified: Tue, 13 May 2025 19:03:16 GMT  
		Size: 15.2 MB (15152999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe60a3c9a55ac0e4621474061e84fae1da1e1296cbc79c532c7c4936d56447b`  
		Last Modified: Tue, 13 May 2025 19:03:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e80ce753f52e01b9906f8a4c434d4652e3046cef9d8a00505acffb530224cd`  
		Last Modified: Tue, 13 May 2025 19:03:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:fd7ae782c9887c62896513e2c92d348052341c9e97c24b360817862740403119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870f2c8143e6924ee664ee46d8196b4a96be9eab2c105190706310e5c08d5bf9`

```dockerfile
```

-	Layers:
	-	`sha256:e1be69ce0bd920508273d096289f3e86a4d68a492eb37373c50f699dd9749839`  
		Last Modified: Tue, 13 May 2025 19:03:15 GMT  
		Size: 2.3 MB (2266884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ecbca88a04a4bd600490b347fdb84444a7a595fc1edb9a49db2e244600abc6`  
		Last Modified: Tue, 13 May 2025 19:03:15 GMT  
		Size: 29.9 KB (29862 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:ed9bfb7c1d907e85ee35f087217c2ff11e84810289e067c05c99b050bd09798a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38742944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ab653997ef5364cf60a2e96f830146105ed18c9dc36698da534801a7c41b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5292de50ac263cfab0ad34121349c216c9c05b46736e868a033e9df6d5990a9a`  
		Last Modified: Tue, 29 Apr 2025 03:16:28 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e35bb1fc07e74a8f7b9a51ea784c60e63c1e34ab6f4664a84e1ec13bee20a5`  
		Last Modified: Tue, 29 Apr 2025 03:16:28 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab80d005fdd0dd58f09df59b9d34ba49cb897d56785b7cac5446ac157502502`  
		Last Modified: Tue, 13 May 2025 19:03:04 GMT  
		Size: 14.8 MB (14801591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633edd026c9fd125f025ef1a68354938547592032a4b298915a23b99799e6bf0`  
		Last Modified: Tue, 13 May 2025 19:03:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897e8c76c7780db4fb7fa455a1f0af991feb9d825018a99c89861d07a8c88584`  
		Last Modified: Tue, 13 May 2025 19:03:04 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c7ffa7780ebcc1d028be5e44744d7b5104713200efca0b34934706a8638a92ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee1179c58dff09fdc79ca6737f0297d5c03456b6646d1665dcdd0ab0a3798b7`

```dockerfile
```

-	Layers:
	-	`sha256:71af53801762d4ecfe328f0b7c2d69e3d322e2f90f4c4a717c7205ccc65f003d`  
		Last Modified: Tue, 13 May 2025 19:03:04 GMT  
		Size: 2.3 MB (2265609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abcf6a059c273dd4e9b7af46a81eee2123ff74b02cf24e61bb7d8155234e8657`  
		Last Modified: Tue, 13 May 2025 19:03:03 GMT  
		Size: 29.9 KB (29862 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:f2f76efcd07c3169d77ef941a1d45238105d777b9e3b5679ac908bee6c86727c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49183781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671ddaed9b1fbfffc5b0df24ac161101977968d2b9ab476cdd30667039b7345`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0938ddd3e8f7dd8c09258b1181db885d203ea5e07a72fb58fdcc82d3e65b17`  
		Last Modified: Mon, 05 May 2025 20:33:06 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06242992f6450c18cd851aea3d589b5ee74db39b25282b4d87fda06f10e14ca1`  
		Last Modified: Mon, 05 May 2025 20:33:06 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fccd451853206a09dc4efc3bb8bd76b29a21429ecd3e35a7107c99b93c4435`  
		Last Modified: Tue, 13 May 2025 19:06:36 GMT  
		Size: 21.1 MB (21113872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1d4ef16edefc90a21a330286408298b5fb63e6ea1f89af01851db2a3214e37`  
		Last Modified: Tue, 13 May 2025 19:06:35 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3595f9893a45a23433fa2c360589c2513fd8122bd0bfa924235f2987aeb0a8a2`  
		Last Modified: Tue, 13 May 2025 19:06:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:fa47c2f69cc2af4f5e5f86efeee28e1a8de95e6ef27076098485d29a9a281a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53971175e7a4122c67920b7acf2854b233c852d64eee83573022c77dd5bb773a`

```dockerfile
```

-	Layers:
	-	`sha256:75d5079656670fa1c2e05686b6eed22752f14f7ac306e26bf33fa5772b8a9540`  
		Last Modified: Tue, 13 May 2025 19:06:35 GMT  
		Size: 2.3 MB (2263661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72f8d0632f4571a5fd3606c5a7b9ce56f1069cfa97e0a0c2242ce45a9ea592c`  
		Last Modified: Tue, 13 May 2025 19:06:35 GMT  
		Size: 29.9 KB (29912 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; 386

```console
$ docker pull redis@sha256:93fd4d1ed471c2e573fa580cfb6bfe603ddd5ebbddb7e135195ec78b843f870f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44153432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e4656882c62040a04e97f2b827ddcd276a140c11bd223118abd833671cca0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 13 May 2025 16:54:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c56b23f677723ed94ee26141e78d2377b9b0553410b855f4f163b5c4efcbf7`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83171563b1bce559e1aacff10b1f65ba4cc5acd760bce8bd87151854183c8a9`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e91f47b4f4c509fbecdec1adda851b0a8c66edc0b718f1cfeb1dbd66c169f`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 14.9 MB (14942669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3001989407830080a88c80d1dde1cf66d31de06cf7ce8e7f1ebdda40a84191`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4641237cca68ad848eb1b85d0f44fab856a5251966ca247f9ebd4fed98a8151`  
		Last Modified: Wed, 21 May 2025 23:20:31 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:fc23b49fa18dd48ca736e61e94a7bf0f93551c54c492188212b53731355ff6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bc37258721a84ed38014bd6c84adfe33c19ef644c34cbc61e383b5d867470a`

```dockerfile
```

-	Layers:
	-	`sha256:3220e9946a0daf71a34fc404b19d21e114575cb4e1d441ab2e488ddc34e9eb0d`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 2.3 MB (2277680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3c24c526725f2f9090ffa7ea00c14f866376e40c3f14ffa60b68525d12e6fc`  
		Last Modified: Wed, 21 May 2025 23:20:30 GMT  
		Size: 29.7 KB (29657 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:2accc50d548fa732a70c4ab04ef232e5eba198275b8f0e68a1db96e766c50d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44039459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da3ad03e77a3636e9e7ad8bfe01808cb6a3749d4e273348b46c746370307994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98efccdb475d14a59d261d66426202f690e942410b68d31e0074023f7cb242`  
		Last Modified: Tue, 29 Apr 2025 12:19:49 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff9ffd1fb1bc3975eda7d63e506ec6882be2fee5cf65b1c4c007c5f9a3e1dfb`  
		Last Modified: Tue, 29 Apr 2025 12:19:49 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602a9a7374a483b79ab3b330368a0c3023f9a1067d1627652b9db2423bf2488`  
		Last Modified: Tue, 13 May 2025 19:08:12 GMT  
		Size: 15.5 MB (15522038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83f9deda446fba9c06cd7ba51d92d091e7b48d1d9f33c07a09c62d4a5ab9ec0`  
		Last Modified: Tue, 13 May 2025 19:08:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f3fd939063ff1c5f197d89483eae7384a5ede3548fd0ba1ae09bf396550ccd`  
		Last Modified: Tue, 13 May 2025 19:08:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:8b6743f2fa56e3c65c586fe9cb6ac75dc1cb545de54d0452274b893b4631920f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9ca99be69cb0a066b1c9a17cee92a0c4beba3abbaee9272a3504f1fe2bf3f7`

```dockerfile
```

-	Layers:
	-	`sha256:1c1d2cae9985a772d63390ffa172c3ae5546dadd97bd96b5302751f08424f204`  
		Last Modified: Tue, 13 May 2025 19:08:10 GMT  
		Size: 29.6 KB (29611 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:ff9bb4368b88c22a0f267fb3570d724071b2d416eb884a7531254c5fcafc3c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee22b9276e4c37a07feb82c9099116e22b07b884edfebc4f90526ab7cfc2517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06088c1879669f94d4784236f96b8153a5c878795a29054496a33f116577d809`  
		Last Modified: Mon, 05 May 2025 18:47:30 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589c0384a5d4cbf54e532211834d36fdc2ca320d2814e316c014d4b15ddd27dc`  
		Last Modified: Mon, 05 May 2025 18:47:30 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca1e56464c5d63a629ffe0cdb4b57cba3d3adaa05856a76f790833aab7bcf6e`  
		Last Modified: Tue, 13 May 2025 19:47:00 GMT  
		Size: 16.6 MB (16608788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e73e73f6f7944bb00d04e18f0233834dc537517f52d82e8f4a6e19b76e0bbb`  
		Last Modified: Tue, 13 May 2025 19:46:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affa61cba4db0a9374eb0826d53b4121c6d864cd66a739998ebf5006bf68a14d`  
		Last Modified: Tue, 13 May 2025 19:46:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:1c37fbf35f23a18acbd840f5af25764631948ec25b2268b964f8ac577da8c707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78ccaab0159e3d57133591c85a8c361e3858936a1d161b992b98c744a4c0c3a`

```dockerfile
```

-	Layers:
	-	`sha256:f1a663f2984b328c9ad347be582e72213546fdddaf205472a4b9e76c557a2470`  
		Last Modified: Tue, 13 May 2025 19:47:00 GMT  
		Size: 2.3 MB (2267670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6151d6fce3baeabc5bf8e35cbaf6f15c5598c2c38f7f01c1a6f184476f293760`  
		Last Modified: Tue, 13 May 2025 19:46:59 GMT  
		Size: 29.8 KB (29789 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; s390x

```console
$ docker pull redis@sha256:6beb608cc20245a4d276a4b64e33b9f40f57f3752e6f0aaadba33c31ed2ee1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42347770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe39af147434f75c8fb0e42a4c2a0dd77fdb8f4e341e93d0157426d142acf9bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.1.tar.gz
# Tue, 13 May 2025 16:54:20 GMT
ENV REDIS_DOWNLOAD_SHA=5e347d3532ff15bb888a78d851e87cf5cc1956edd32b5d4a0cac3220da0a5a0b
# Tue, 13 May 2025 16:54:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 13 May 2025 16:54:20 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 13 May 2025 16:54:20 GMT
VOLUME [/data]
# Tue, 13 May 2025 16:54:20 GMT
WORKDIR /data
# Tue, 13 May 2025 16:54:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 May 2025 16:54:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 May 2025 16:54:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 13 May 2025 16:54:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a0b97545203362ddc4bf4bb2915d68c283e47886e8f7ade8334b7ddcd53c3e`  
		Last Modified: Mon, 05 May 2025 17:43:34 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36ac850de3bf81b3f52412fcdeb4afaeb814643f92e86d6bb416865730626bf`  
		Last Modified: Mon, 05 May 2025 17:43:34 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d492e1a49fc1620e47b6f0e1f59fc0e163cbf9d8aaed93c2d18cf569dcd7d71`  
		Last Modified: Tue, 13 May 2025 19:03:09 GMT  
		Size: 15.5 MB (15459625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9e2d2be552d4c9410d41e689911eda0d3a27afdf57188b5e3e9b9fbe05f63d`  
		Last Modified: Tue, 13 May 2025 19:03:08 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225352625032b7c4a073889a71ace95b72d8c8254ac05133849e802999c0db0a`  
		Last Modified: Tue, 13 May 2025 19:03:08 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:fc0abfc670fccf7c847482e17e4fcff9b888cd5d338649a586d559a321563e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f12232585ec9a58231e1957b3550586843a8b6613a0ed1b44f583cb22418ecc`

```dockerfile
```

-	Layers:
	-	`sha256:f5c843dbe3223954b421dbf46c686cd9e1e450ea7fb7184459485dbd5ca9e9ca`  
		Last Modified: Tue, 13 May 2025 19:03:08 GMT  
		Size: 2.3 MB (2263080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4956c41d25a5219ad27561ab7a47547dda07fa260cd4e5181fd0e99e9ed5b0ba`  
		Last Modified: Tue, 13 May 2025 19:03:08 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
