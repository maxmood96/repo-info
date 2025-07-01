## `redis:latest`

```console
$ docker pull redis@sha256:dac8ab0340cef636bf80c4d771e338733c694885567aaabd15fe1368d6bf7c13
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

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:07c689dad77c543eee9c4e98563c021a7b531d0f87d982aa109414492b5483e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49504906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3a2af6d0d46ba343b13c99d5f410d5b5db5470712ec6f404fb3442665f7490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db655ba2dccac7370017b76972e0a959952eff9c42208411f50ec89b61dfa456`  
		Last Modified: Tue, 01 Jul 2025 02:31:18 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef8fa7693bb0aa715e32e2958d4c32b55fa2446e698a0507ac6fa12d31663e8`  
		Last Modified: Tue, 01 Jul 2025 02:31:18 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881b4a6fb2ec7b0fea2fa42ed70ebdaab5e37441f930f3ff494713c9e37b2eac`  
		Last Modified: Tue, 01 Jul 2025 02:31:21 GMT  
		Size: 21.3 MB (21270547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7393f5b31015fa64d278f6e97a4149c516a24deb31b97b3c48155994a1cfa5`  
		Last Modified: Tue, 01 Jul 2025 02:31:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab22bb3606caf16e94bbaebd0734de400b7a51826acd1adc41e97d66fc937500`  
		Last Modified: Tue, 01 Jul 2025 02:31:19 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:91c20a6180c2e60d199dd123717ae2d9da8ec198238d98ac7e0809a3fefeaedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908dcc96ec34c2b8fec72e2141dd97a35862e4c8907b30cd7a0f6db98a95e3fe`

```dockerfile
```

-	Layers:
	-	`sha256:04bb8e6f163ca65cea030787aa962a8c1460f3b3702eeb09d4a290975dc67982`  
		Last Modified: Tue, 01 Jul 2025 04:05:44 GMT  
		Size: 2.4 MB (2371511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187477f4ab5e2d5e51400d9b63a9057dbf658dc365c0288f27598cb3177af204`  
		Last Modified: Tue, 01 Jul 2025 04:05:44 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:cd3e4a389e9918f5ac37020320909e6169d0b50f54b221f7431aab12701558b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40926533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca95c492fc8c88cad921127c1d1572359aca24e1676b440286b3cdb4153cf36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a63d5c6e5006331ee40b5e94e8ee1f4a7bc4dce5000e15c8843f71c18b54f9`  
		Last Modified: Wed, 11 Jun 2025 03:19:45 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae2ff42ff96c06ac612702069a6f0cc339d27ca481f32ac0c3896f21061e63`  
		Last Modified: Wed, 11 Jun 2025 03:19:49 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d173b37f6022b236b7e3d71437617880f201259e73006d02648e3dd64d32a`  
		Last Modified: Wed, 11 Jun 2025 07:13:57 GMT  
		Size: 15.2 MB (15159926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee52c7a7edc4cf2b789d475310bbafd0b0888180ae4e8fb27a8fcd458d8fa1d`  
		Last Modified: Wed, 11 Jun 2025 07:14:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b1572b6c575c8a59fe8118853921b29796b17403d94e2cb4e37a617562e32e`  
		Last Modified: Wed, 11 Jun 2025 07:14:09 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:25d3535cb2bc7c0686ce199035db228d7fef5877aea9dda3e8e628abbccd9917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bb30c6c534a4d96a9bc5af28eafd8910493d0d7a3b55cebcc42e8e712e4b5d`

```dockerfile
```

-	Layers:
	-	`sha256:c57e449883e579c9969daede27c0a2443acc0816143f0d567cdd4d4e3d0b7571`  
		Last Modified: Wed, 11 Jun 2025 07:05:49 GMT  
		Size: 2.4 MB (2375347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb76cd23db14b1153b36ec48d18df7431c3059cdf6c102f147233e5d2eedaca`  
		Last Modified: Wed, 11 Jun 2025 07:05:50 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:9c9e8dab648e0450adfa61d6ffc5b5ea08d44e18d0d0d25814a364deab7ae7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee24899a6b3b2751ef1c6deee9ff3901ed02ec59921365c4520d95cced36c9ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d36808f93f90ca9de6377080dbc9d725c42571aea21eb73bc8ec52e936dd4`  
		Last Modified: Wed, 11 Jun 2025 04:47:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac1456d3c8cd325711d738005e087c2d583d46e3a18a744c389fce904e0b558`  
		Last Modified: Wed, 11 Jun 2025 04:47:56 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4e5fb0496698e468a3338c91d4b53326d249e1783d26d9f4585f9086d85aa`  
		Last Modified: Wed, 11 Jun 2025 07:02:17 GMT  
		Size: 14.8 MB (14811819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234721f7d9d577a5ec437c1564b1f44ca8a175aae985f3c817f8b15859659b25`  
		Last Modified: Wed, 11 Jun 2025 04:49:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d7cc6f932ba2b7cf8ecbde7f593b8307076cfcce4ddd4b7833028196d7fde`  
		Last Modified: Wed, 11 Jun 2025 04:49:28 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:7e6b539e5b79e1f44a3e3ffe05fc10557dbe7e3d52e392e5a6f8584b17a69f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6552867a4f95099be74edf6169c1dab4ef5ff39684f14f15cadcab3eafdbf57b`

```dockerfile
```

-	Layers:
	-	`sha256:3f13c3bf96182057dd74d622e18e270b7184803bcd136a3f710f5d3b2dcd685d`  
		Last Modified: Wed, 11 Jun 2025 07:05:54 GMT  
		Size: 2.4 MB (2373764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e81bfe9a103ee3be7e7f9d205984b585b4434cde8597b156f37aba4cdc73437`  
		Last Modified: Wed, 11 Jun 2025 07:05:54 GMT  
		Size: 29.9 KB (29862 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:4d8a53a649e5ddec984e618209aae3261dabd02048c535e39ced9e7fd775f3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49205972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ae424e8e63f698a382358b0fb25999514601acedd945590322b7dc82029d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2044fe96c79cdd0a6e50acd4e38abe88868ee837e268354673abf6ae8bf882f`  
		Last Modified: Wed, 11 Jun 2025 02:32:55 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69ad4fae421f119416cbecfd830d5bbbb26c77a1f78be556d6e7e42958601e`  
		Last Modified: Wed, 11 Jun 2025 02:32:59 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f73e9b67c7becd722193f71d7f86936d52f12a7dc3970e7fd08406194c56ac`  
		Last Modified: Wed, 11 Jun 2025 04:06:01 GMT  
		Size: 21.1 MB (21124082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34be6f5e68604a2fead17414896fad604fadb8ca2612bfd8f7447d0986b24a8`  
		Last Modified: Wed, 11 Jun 2025 02:33:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41084bef585a2b9af96ecee69245b0080d49037cd57e83dc8a950efd32ade174`  
		Last Modified: Wed, 11 Jun 2025 02:30:54 GMT  
		Size: 2.1 KB (2113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:883e1145c3d5de276275c6c676a1535c671eae010c47c4443b427142f414a3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7203e965ebc9336bb1145aa9032301ab8a6d2d645d292dbfaf236e0690d93ae3`

```dockerfile
```

-	Layers:
	-	`sha256:929d03243da55a7105d61881f930c1e9c955c2fd762ad2db65b999d708268a8c`  
		Last Modified: Wed, 11 Jun 2025 04:05:44 GMT  
		Size: 2.4 MB (2371816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc023a908396549cf11e14947f7b9caac07cd82a05919b08864ebb12ec3f583`  
		Last Modified: Wed, 11 Jun 2025 04:05:45 GMT  
		Size: 29.9 KB (29912 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:54668b67c87508557d8e81485ab2cafea23e0ef8fd34251986d73af633b0169a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44166837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6cf0fa8e808e9261ea1033c835e0c3c4974d29da7e46abd87cb57f7405af3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c25380c01545cf93b336fc543d92f50fc0ee5996516c6e9c094f96bd8b7d33`  
		Last Modified: Tue, 01 Jul 2025 02:23:26 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0888a84887f4181d6c15d36e63b55c86f98992a7df7ff6477030c5f5b60fe7f`  
		Last Modified: Tue, 01 Jul 2025 02:23:26 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d4549ceeff85897a0f263b60f9be2bda15a6271ff64bb70504250e66dfc065`  
		Last Modified: Tue, 01 Jul 2025 02:23:39 GMT  
		Size: 15.0 MB (14950196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc627cf76914dbb85e1ab5444b874de2d9a622427d2470baee0a6d7dac498dfc`  
		Last Modified: Tue, 01 Jul 2025 02:23:27 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6fd9f77f2e0a933525a951d63a4e1f5fd047128ccae5b8112ec7d003849a46`  
		Last Modified: Tue, 01 Jul 2025 02:23:26 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:d78c7993d652d94acfdbea2a2e6a1ddc2c597855b0f05e7277d4aae7ac3f0c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4735d8e66f00e37f2bccfe3fcc17a3816250ce993053aeac0cc77b50fd5c375e`

```dockerfile
```

-	Layers:
	-	`sha256:d1e2c1feebfb5227e20541aded5faa9361771d40152b44289fa5f7f7c12bd46e`  
		Last Modified: Tue, 01 Jul 2025 04:05:56 GMT  
		Size: 2.4 MB (2368674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c63fb87f706fe66842f2aec739e1af3d55a45962bc596a5df6d8fab848442d3`  
		Last Modified: Tue, 01 Jul 2025 04:05:57 GMT  
		Size: 29.7 KB (29656 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:4cfbc4a694032947bbd5fb32dbaf06b0b01f1858f6dc92461bdb3f33e0319718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44054576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90815c95d7f6c3ef9e447fcebf468cfe192349aeebb82af28f357e9830861a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305356bcf0eff77ff512f753ccedfdddba676f75172f11e5a66752aec884073c`  
		Last Modified: Wed, 11 Jun 2025 12:38:08 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7c0097ed51329319816890b742d4176dee7daad828d2281e4495c236d536e8`  
		Last Modified: Wed, 11 Jun 2025 12:38:08 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107f3793f8d250f092acc76cf1ef2c23ddd1aaaaae30899315141d27bf41e95b`  
		Last Modified: Wed, 11 Jun 2025 12:38:12 GMT  
		Size: 15.5 MB (15533641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae9aa6e19ecf3a9f37c75c9d2ecf70798f0cad7e0333ceb3261efc360a5121`  
		Last Modified: Wed, 11 Jun 2025 12:38:09 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff379f358648ad5d90534457c8dcfb7b05847d19e95b4245a244faec0c8c6765`  
		Last Modified: Wed, 11 Jun 2025 12:38:08 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:0f7f0705f560722547393b7cd513c44d1dce5e8bbf8285c9a680a68b768bce97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670f18915d8ada98805005b4691a064c7a6f1a2aa11edfff0adf45495d5bf322`

```dockerfile
```

-	Layers:
	-	`sha256:795bde474fa367982d773a429f2bbabe5277a7276331574fd7d762ce6a5df6e0`  
		Last Modified: Wed, 11 Jun 2025 16:05:40 GMT  
		Size: 29.6 KB (29610 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:05a29e844647ba66ff3df92c5cfe5bb951853e4d8239bcfbf2f5543b6b4f6071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48696984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693c46d191395084686103d0dbeae6c1e286de97380e96ad38b1bb9023d37ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ac5959c70fab1d000c93e8d913d16ed781ab8f83bd4eff9e253fea19cdca83`  
		Last Modified: Wed, 11 Jun 2025 04:37:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536e3a025311e951f3d3f8c408e7ccac6415a5c830ff9a8bc80dfbce8313aba`  
		Last Modified: Wed, 11 Jun 2025 04:37:10 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127e9e400d97e97cd42bc6cf2e3b58dd2cff77f9583844fd4100fc7889bd9ad6`  
		Last Modified: Wed, 11 Jun 2025 04:24:11 GMT  
		Size: 16.6 MB (16619975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f90ff29a99b078a6ec182d66d0e4765c8b91cc2b442fdb0d1f4f02f0753d962`  
		Last Modified: Wed, 11 Jun 2025 04:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c401efe58e4743623b59e55d88fc796319c2bcada2c5898072cea1cc7db157fa`  
		Last Modified: Wed, 11 Jun 2025 04:24:09 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:c6a4cba773ff8e6af611976a180548ad49b30b6441e614747625b7ef6388f2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f60f501497febfba413ad6fe5518ddcf28a46fa74db5d85cf075114952a7406`

```dockerfile
```

-	Layers:
	-	`sha256:a4f911594d2806901530ed639fadabf11627a7b76053e27cfff6e3e646118875`  
		Last Modified: Wed, 11 Jun 2025 07:06:05 GMT  
		Size: 2.4 MB (2375917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9112cde71c640799d9430f7954ad46a33beeeef17af4c1f7b758c5296dc14b5b`  
		Last Modified: Wed, 11 Jun 2025 07:06:06 GMT  
		Size: 29.8 KB (29789 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:501faa9ab96ee9826638653910618ef353b5c94f42531f95ff5205e09135ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42363221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e399ee1a14c1b7f85c4c78a750595c2da81cfc61be2fb7901de4c6adfd66ec06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		g++ 		libc6-dev 		libssl-dev 		make; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apt-get install -y --no-install-recommends 			git 			cmake 			python3 			python3-pip 			python3-venv 			python3-dev 			unzip 			rsync 			clang 			automake 			autoconf 			libtool 			g++; 	fi; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	case "${arch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/cache/debconf/*; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 29 May 2025 16:02:07 GMT
VOLUME [/data]
# Thu, 29 May 2025 16:02:07 GMT
WORKDIR /data
# Thu, 29 May 2025 16:02:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 16:02:07 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 29 May 2025 16:02:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceab5f0ec081b2d586056d0fceb1df560187573884616afb778ebab996179dc5`  
		Last Modified: Wed, 11 Jun 2025 02:51:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c69ef924295878769bf9d052f83acc25663b94fa5d990f5fe5641de3f677a6`  
		Last Modified: Wed, 11 Jun 2025 02:51:15 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091540b6148a4dd8aa46338d70b4df552d9b06b09516c202cd2ebec3c42a3b9d`  
		Last Modified: Wed, 11 Jun 2025 04:08:32 GMT  
		Size: 15.5 MB (15471156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35b761aa4de48f2ba5c12659e6856dd2b2c7267a9baf7faee04b931955d438`  
		Last Modified: Wed, 11 Jun 2025 03:15:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6c52b81be55a0e0a22e8f953eb547bb43da05a25cfcdbb48f017b35929243`  
		Last Modified: Wed, 11 Jun 2025 03:15:08 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:147378d8226ca1ab91c9a2cff4b8abf65e50a43ed0305aa18ca68fa87c3abd97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c75ed68a1e032bf319dbf1cf3c2466dfaebf6b7148d6c9dc82b0b53bcc9bc`

```dockerfile
```

-	Layers:
	-	`sha256:07a89afd9dfa0004590565563b9cedcc2479985cd226fba89a8027f717b34c7a`  
		Last Modified: Wed, 11 Jun 2025 04:05:56 GMT  
		Size: 2.4 MB (2368343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b139cd89404bb0e265094938dca4b1a14d516fd7cbce8fee208edb2207cf3bf8`  
		Last Modified: Wed, 11 Jun 2025 04:05:57 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
