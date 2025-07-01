## `redis:bookworm`

```console
$ docker pull redis@sha256:b43d2dcbbdb1f9e1582e3a0f37e53bf79038522ccffb56a25858969d7a9b6c11
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

### `redis:bookworm` - unknown; unknown

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

### `redis:bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:c98927ee9320e1945c5684f23f404e75bb3c124b947d1b290bdc5ecd81792032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40926606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec6684980fb92aae23ef2cb182060b2580c25dd2f9bbcd2f663931574d276e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50a51d92499791a8ca42a200f0d9b59a7ab508957a83c9fedcb3f403ea5dcc3`  
		Last Modified: Tue, 01 Jul 2025 06:00:28 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff568ee2b31416de24bda33d4d1bb8c21e2ac9a309c9b649d3730f6e65597d6`  
		Last Modified: Tue, 01 Jul 2025 06:00:28 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c06ef8600aaf7f7db086592cb051485c153b17e46280e00ce38f0129e1e8f`  
		Last Modified: Tue, 01 Jul 2025 06:01:44 GMT  
		Size: 15.2 MB (15159932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9750e2d112dd65f58eed2ad5f8b47d50bc5b31d99c96da0de159b4cf02540d55`  
		Last Modified: Tue, 01 Jul 2025 06:01:39 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc46b563923bcec4d24c23dc6d47412a3282645254783b43ed479c93ac05e13`  
		Last Modified: Tue, 01 Jul 2025 06:01:39 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:6c7b69b3ca3acf16e62a1696b7e1dfed20507a705ea30df30ae6647635b0b940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afcc665b662bc03101bdaffad1a1ca121e15c4f9593ab94ac11b294c111bd38`

```dockerfile
```

-	Layers:
	-	`sha256:d449af0aac550c011e1e19b070e1799a9f0cf831b12c3f798b4f974e0ea62555`  
		Last Modified: Tue, 01 Jul 2025 07:06:00 GMT  
		Size: 2.4 MB (2375347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c379ba2de0a6c561543b873bfc4a2a9bdd6f46cb6e9810ce89737bdd691c0d`  
		Last Modified: Tue, 01 Jul 2025 07:06:01 GMT  
		Size: 29.9 KB (29862 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:d62768eea80901d4859d20c3ffd561348d0bdb18042b83c103ae7ad4deb48527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8ea7660e24894f5e147626135385827a4993de1c5ae01eca3007bc7a77aaee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df362a4c9a4a4d763f3fee01d03fedb9ecfb2539441fbf7bd412c275b15d2e6`  
		Last Modified: Tue, 01 Jul 2025 08:35:02 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fbbfff90eb5a817b534463d14394db5521da9321c369d4047dbfcfc65292cf`  
		Last Modified: Tue, 01 Jul 2025 08:35:01 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ed0bfcf4c3f636af5a99e52cfea935362e4a9fa5f34c262c563460089624e2`  
		Last Modified: Tue, 01 Jul 2025 08:36:27 GMT  
		Size: 14.8 MB (14811852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f18de188a6d0290bf0aab852f022c99f7ab6557c31aa244fe862cadc133e641`  
		Last Modified: Tue, 01 Jul 2025 08:36:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08052736750f3164775783a2a5d207d65dfe2d4fbfd35e43a8fe20b5106c6b73`  
		Last Modified: Tue, 01 Jul 2025 08:36:25 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0b02108df03630c94e7ac1f1bef2af2170a95a2bfe78c3de3b7d3561a2a32534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f258d07ab2c7634f6312f99385f1c00931c06168853bddcd7fa26849646b90c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb40c78ccd402bb17755fcfcc08ceac28643243319dce7ba41859e326148c73`  
		Last Modified: Tue, 01 Jul 2025 10:07:56 GMT  
		Size: 2.4 MB (2373764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4d9b894ac579d51ca8e6aaea71d70a723275b6b5af6462278df0bd8fe5078d`  
		Last Modified: Tue, 01 Jul 2025 10:07:57 GMT  
		Size: 29.9 KB (29862 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:827c22a04103d6b331b5cf2703cb1097741a34d9220bf0b40a40ac8caaf31cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49205990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c7b493895df800429b34c0f940a28aefa66aac4e1f70949659c697a22e66a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929c063e7c678d0070c8493f4f1adb7bd4bf19ffacb39bbc25004dc5d6904ae0`  
		Last Modified: Tue, 01 Jul 2025 06:24:54 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6487d14aef1cecb8c12701fd57ce78d14504facc295b130fb158398d64982ed3`  
		Last Modified: Tue, 01 Jul 2025 06:24:55 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1951cc36241a5a237e70a37ae2c1692daddcf250ad1d5cbcc614e9a84d3ebfef`  
		Last Modified: Tue, 01 Jul 2025 06:30:14 GMT  
		Size: 21.1 MB (21124096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bcecec106d3a0d1ba33a99dc2117f275b19f1cf8558ca06b8148e218415d4`  
		Last Modified: Tue, 01 Jul 2025 06:30:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbd38be072595d16d8096e4239add78348987209ec0adf490acc372f7d8b2d`  
		Last Modified: Tue, 01 Jul 2025 06:30:11 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e02d10cf25a8488b62cff6c795106e6bcf95f9ebaf8fe4a113488bff13fa3991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511b27761f0021da3e3b9d4ff3e4972dbf959a92a85ee4126ab5a40d3b064e94`

```dockerfile
```

-	Layers:
	-	`sha256:ee4090426aff95e06727386f1cd64b6bb9c483c6b65195add804b4f433d52756`  
		Last Modified: Tue, 01 Jul 2025 10:08:01 GMT  
		Size: 2.4 MB (2371816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e70b4a76c68be6220cb789ff2f474a49460e7bbcb6196719c2cc4061ee689ab`  
		Last Modified: Tue, 01 Jul 2025 10:08:02 GMT  
		Size: 29.9 KB (29912 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; 386

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

### `redis:bookworm` - unknown; unknown

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

### `redis:bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:1b301e2cc8e43b795fdbd305bf2db0dec2869abb818e83e20d45063528553302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44054610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1843caf7fe148ce7ce9646ffc2899a4b5d95378d6a6ff18301c28f38f850c954`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8f7ba97df6bad056141dc892e32c722489666c26ed556d23f8e5ac35d05db`  
		Last Modified: Tue, 01 Jul 2025 18:18:25 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9d9fff6c8eb93533d24a4425f9cb5c35d753d4ef53b69e1769245d5a9e1c9`  
		Last Modified: Tue, 01 Jul 2025 18:18:24 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dc21d1cdc0908136c272a4a70b364d2c5c872030f7dead738f6afe131f06c0`  
		Last Modified: Tue, 01 Jul 2025 18:25:39 GMT  
		Size: 15.5 MB (15533658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee727d1199603a44c01f240c45480c92f37d1645b87c02df58befbe5e7419b89`  
		Last Modified: Tue, 01 Jul 2025 18:25:30 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a554c3c60b3438e401f256a407abff0a6312dae4ea892601b1a3dadb7da549`  
		Last Modified: Tue, 01 Jul 2025 18:25:30 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:7ed7462c991245ce770115316706eba41bcb27f7af016935ae61825ea842d4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 KB (29611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428645b71edb6909fcad68b2e524ab815c3dc2701fd1d57a2555b5c82769c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:5d0519fbf65001c3d7f380e1efae66a7e1ca5dc4bf83c58381901302dac15753`  
		Last Modified: Tue, 01 Jul 2025 19:05:44 GMT  
		Size: 29.6 KB (29611 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:75ecabddb21a6e2b2a8c85fff2d6a40ca989f865074ae811036e7ae759866c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48696986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defe3c7a48c6aa78246f27e46209c42f584dcb3f6782bbfe3cd94a0537396b82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da01b466b4c61a0f0a36b1d7ae484058884b888f05d757dc367939cb0966b0bc`  
		Last Modified: Tue, 01 Jul 2025 04:43:53 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1cde8f812c6d4542c61e8cacdd26cf2bef07cac40f1500a7ad394ef001eb3b`  
		Last Modified: Tue, 01 Jul 2025 04:43:53 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409d4c373168f071c655d22ebe3caab84a7feb3d4342836c95df44c09a76d2a`  
		Last Modified: Tue, 01 Jul 2025 04:46:07 GMT  
		Size: 16.6 MB (16619958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b921e1d6f8c96d77ce1e3af73dc081b0691229e111d0f0668613e3f5e62d4d`  
		Last Modified: Tue, 01 Jul 2025 04:45:55 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6180725f8ad41dfa22c7153deb7310463c8ac985a2424f6ceaad4ebf3747ce8`  
		Last Modified: Tue, 01 Jul 2025 04:45:55 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:27899b8c69807d5cb277390986f6ead6cece5c63475a91e02080c87e1a3da4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d78578b4cf8b4b4deeb9bd9f5fd719235434c6733794d8374427af746f197`

```dockerfile
```

-	Layers:
	-	`sha256:7462b7e2689631657bc0cd7d00086a65438f73af122bbc88b77fbb350d7ce705`  
		Last Modified: Tue, 01 Jul 2025 07:06:14 GMT  
		Size: 2.4 MB (2375917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d1c149f09c0b0ef7b73f571cc8b8415a8f55c34d9798f8a04395d91b15f010`  
		Last Modified: Tue, 01 Jul 2025 07:06:14 GMT  
		Size: 29.8 KB (29789 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:bookworm` - linux; s390x

```console
$ docker pull redis@sha256:7ec4decb0ced62ee6f1c20ebb10c6a6326b822defe828907cf57765c6f3a8c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42363166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73808e301fe3f506a1d86c53b057ebcae9f8a5d7156ae606ef6949b6ea9615ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 29 May 2025 16:02:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05909171b96e95496b1eac42fa8a7da392cf5e9c299c427130af7dae159a06f`  
		Last Modified: Tue, 01 Jul 2025 05:15:53 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4c5773ebeb8e7989a4fc1227ed4e2e6e2cba45557730b46c836f1e3107eef4`  
		Last Modified: Tue, 01 Jul 2025 05:15:54 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d22a9ce0dcd955d80576745a867585b669dd6cf61ac813fbaaf9264015272c3`  
		Last Modified: Tue, 01 Jul 2025 05:17:31 GMT  
		Size: 15.5 MB (15471145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9d9c2910227832faa4cf0b4ae44721fad7395a9cb0558faca306d3c4cce3dc`  
		Last Modified: Tue, 01 Jul 2025 05:17:29 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733a43cbaee638435f5371a58200559553d52eb5a4d6f0100a7574dde44b2322`  
		Last Modified: Tue, 01 Jul 2025 05:17:30 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:f335dd15ac4dc05d87cdde0d56db709204dbcd45a33027d4537f8424f8d8f57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1017362fdb04043f8bee57c570e769ca8207ba0ffb2a78e680f4bfbd112bc8`

```dockerfile
```

-	Layers:
	-	`sha256:6c03145130a9ec96f8bfa9b854b28011f922a2d7055e0c8e5c52d1ee4f858fa7`  
		Last Modified: Tue, 01 Jul 2025 07:06:19 GMT  
		Size: 2.4 MB (2368343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620fc52f74c70a8e89dea52187f8a03dcb6d73fc81d45da4b19d2f40821d7ce8`  
		Last Modified: Tue, 01 Jul 2025 07:06:19 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
