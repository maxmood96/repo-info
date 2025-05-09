## `redis:alpine3.21`

```console
$ docker pull redis@sha256:0779069b3c24a47a2f681855c1c01d046793e7c5f7d2b079c2aa0652c42eaf0e
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

### `redis:alpine3.21` - linux; amd64

```console
$ docker pull redis@sha256:f379f1432fb8d7fc6ade9ffd313a815f9bf5e358fe131ca30b573bbe33cba7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24348180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ae465a41237dd99c408c760e5e59a39e8ee00c2bd93095811b699554fab2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826632aa5dd8df6206034a82fe85493f1b7c96691d94fe4abec5ab08a187345`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7279224f08c0d30578f4dbef204f0d766afabbd04daf59490323251b558dae`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 195.2 KB (195239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b782747b1d523d78e2eccdc898011eb18b9e831309cefc10bb6601fcfe3aa1d0`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 20.5 MB (20508439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a566114717809f918a100e6a2d5745e2b81ecbb378f3e5908df3026920199`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64136cebabc3fd206a2e54d36143516c9e9dd18c1a4a6d11d2f12850920bd35e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:f81eaeb0a6858e7b88c1a87176d77b44d7088190fa4ee448ef45e66b291464a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ab96cd6fe50966bcb7c5b5d9d83b5580846b9ad1108446c3f861e0d0b779a0`

```dockerfile
```

-	Layers:
	-	`sha256:c5fadbba349c83adda1c960d3c66dc38fa8ec73e373d71a790ecd5ee458bc7c6`  
		Last Modified: Thu, 08 May 2025 19:17:17 GMT  
		Size: 5.9 KB (5896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265b70a6a50cf838d71f68898a8b2bbd32e9f0c56301502e231a50f0912be8c1`  
		Last Modified: Thu, 08 May 2025 19:17:03 GMT  
		Size: 32.3 KB (32345 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; arm variant v6

```console
$ docker pull redis@sha256:5893922c7f5f5fe86cdf4e3bd7b93d506d438daad7c8499c89c126e36dda36df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17585815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688acd24afff8c6a34e62a7d293ae6202c6ee103c9b6e2a66dde643f2ee97877`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306bc7f3cd8273ca2f216836302ad21df95fa6a35edc08f6d45e13364a9fd5`  
		Last Modified: Fri, 14 Feb 2025 23:04:56 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbe3dd27371f1c37af36d90cf012f849a0806aeabd01177d0dd5e1f05b2685`  
		Last Modified: Fri, 09 May 2025 00:21:37 GMT  
		Size: 195.7 KB (195696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e5c38d3252b6acc3a973779a2961e0cf93a74e74d647dd5b0a4581705b29f`  
		Last Modified: Fri, 09 May 2025 02:00:24 GMT  
		Size: 14.0 MB (14023126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568cf143d108dcce5c6bb165b01c719b75ae6dcb0017e84772613704aa8ebf75`  
		Last Modified: Fri, 09 May 2025 00:21:36 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3bc1f6e40633000e515c117c76b86a4748ee69900ec68edcd21e4bc675a10`  
		Last Modified: Fri, 09 May 2025 00:21:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:934b8acf74028fcc708b93a7eee03aa1a942c2f4ca253adffd37fc2db81c95c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118acb02c3aa22b46c49d286aa40994e39fcd2837d64d7a70d25e0f27f6b7de2`

```dockerfile
```

-	Layers:
	-	`sha256:5b76309b82104ecca37e6a88ff2c4edcbc468b1cf6072a2bb9ea404f9cf3a185`  
		Last Modified: Thu, 08 May 2025 19:17:05 GMT  
		Size: 32.3 KB (32275 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; arm variant v7

```console
$ docker pull redis@sha256:b44ee6012d6a7cc608efbed25408d09a4e89f2b9ee37955fc6ed6e053127e995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17105854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d976a2b94d83a7fffe127b2e70d72ab58d48f1facd3bacbdcdc2cb62d0ab00f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38de7eb7132bf24de27447f0d6330d4299fe0264ac584c5f44fa45bfb8da0f3`  
		Last Modified: Thu, 08 May 2025 19:09:52 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075129f30b31cbb1654653588b25f41fd5d899285e15d6fee8739cc39c609ede`  
		Last Modified: Thu, 08 May 2025 19:09:53 GMT  
		Size: 194.0 KB (194040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a003ad8d70e3afeb6558df4644ea31203ab133164940c38829c4397af22a3b`  
		Last Modified: Thu, 08 May 2025 19:09:57 GMT  
		Size: 13.8 MB (13811429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490790304f175a292805f9ecc5d125e166eb2123162b16799c043b40349fef2`  
		Last Modified: Thu, 08 May 2025 19:09:54 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca3626dc272a208b340786413012f8e96082886ec9e99777808c335a9a0f5f9`  
		Last Modified: Thu, 08 May 2025 19:09:55 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:4ac60eab76db96ad4081a0e048bf47468c64afb338fb56bb1e27717eee991e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 KB (38457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f77983755a40c06044fb0ff24a8d29a17ad8cc9e6663ca09c0451c227062431`

```dockerfile
```

-	Layers:
	-	`sha256:20e95b3ff21102449c8d14a00c5169a31466f0d489ad365fcb0c8440f8aff132`  
		Last Modified: Fri, 09 May 2025 02:00:28 GMT  
		Size: 6.0 KB (5965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72dc04a8ada6455ecf6e924402cfb03e36799731babee535461d6a041f0f6779`  
		Last Modified: Thu, 08 May 2025 19:17:07 GMT  
		Size: 32.5 KB (32492 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:728448f12cef72ce342090283f5faf78c28c1cc3241faac0be72b04f3c0c5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24618861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd57cd1723155c05b9cb459e08a9d8db376d3046c2eabe2dfa1a7d1985edd40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a37282d43d3092d42cc7aafd345de189dcb8dc97f7c0c44663ffdbe107dfce4`  
		Last Modified: Thu, 08 May 2025 17:05:40 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44a25f41bb21e5989391abaeedee4cc0e0680f2370fc86e0cf01c8939d4b662`  
		Last Modified: Thu, 08 May 2025 17:05:40 GMT  
		Size: 198.1 KB (198057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68676f3e0357f3cea9d33f03ccb30049845def061097badd6c82664c598c26`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 20.4 MB (20425521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec361d6f6cf728cf599dd5cbb84a3b43822d164c184534d4650f91ac9cea36f`  
		Last Modified: Thu, 08 May 2025 17:05:40 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af58ecfedf0a2327f6d3e09044dff7f47b322963e8a6d6fa2d504ca87179ed0`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:422612c7013285209859232bab25d5414434e8a3967b9aec59db08b06a8aa153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 KB (38538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50a7de4bad1fa6b9bba40b5ea43aa7c6e4495c9d81d35eec2ac39bd1de97003`

```dockerfile
```

-	Layers:
	-	`sha256:2a5df315caefaf9ab5cf296866100001986c3c0e0f2c32729dd2888d72c2bcb1`  
		Last Modified: Fri, 09 May 2025 00:04:32 GMT  
		Size: 6.0 KB (5999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee4d1d3b3dd0eb4a708a58c8fceca6394182b183061ac242dd50616b63e4d14`  
		Last Modified: Thu, 08 May 2025 19:16:53 GMT  
		Size: 32.5 KB (32539 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; 386

```console
$ docker pull redis@sha256:5b9f83c7ad78388f7124d412a2a56c3e53e939f4883dce069e0e9efe1e3ab5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17459663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16833c2b3afc4a98f91d049714833d5680aee109ce0d97a86cb00ca500c7e8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc03c307c042b0019919be4aca7c5db8571469a1970bbca53c2125d9eaf35f`  
		Last Modified: Fri, 09 May 2025 00:05:12 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10234629e49fd6134d9fcab3db5c1ef67f666879ebeb399d25ef4639f433dc`  
		Last Modified: Fri, 09 May 2025 00:05:17 GMT  
		Size: 195.3 KB (195265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f262b87977f78b0ee89f9c4ded66b6dc502aae2136cd6f8d5c720994a377ef6`  
		Last Modified: Fri, 09 May 2025 00:05:36 GMT  
		Size: 13.8 MB (13798512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e98aaf59b67d32794055b335cfdcdb0c4fce301ebb58612a7ff09c11dde1dce`  
		Last Modified: Fri, 09 May 2025 00:08:03 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddea5b1619a1f8fd36f2c4a9dc8742e5fc66b38fc3cc43c657bc3b7abc4adc86`  
		Last Modified: Fri, 09 May 2025 00:08:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:03545dd35f2e52f8914a55f98e65ed53b0f955d7130c063aebffceb9e0396e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e554eeb4cff83f7e976894de8f6dbca721e32411b614eb85656dbac98fe5ff`

```dockerfile
```

-	Layers:
	-	`sha256:ff498beb8e49e3ff3f0073e2804981508c61890ff30043d20123326980fc2b91`  
		Last Modified: Thu, 08 May 2025 19:17:09 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4357a7180c29461854a2f4c3ca595e376174df34d176ac0a0e44a55e51f8cfe`  
		Last Modified: Thu, 08 May 2025 19:16:55 GMT  
		Size: 32.3 KB (32287 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:08878f5fcadf4701f9218b2906b80d13f7a868c1e5aa1b43965a7c9dba3d8eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff9bb5afe54177db22a3cf347e63e1980cd46a66ecf33486a5943fda0fd4bbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b92922c442a61cfe54344354ebd3fbc995fa57fb8b78a500f20de74adb2c53f`  
		Last Modified: Fri, 09 May 2025 00:21:38 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36f2a7f82666649e1b57d6c77644c4f9c1b715872358446fd6f53a3efc7b2a`  
		Last Modified: Fri, 09 May 2025 00:21:38 GMT  
		Size: 199.1 KB (199050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79bc66df2694d9c2acf38a54dff61e7752ea57aa3cf5c6f105e09b33dec5c1c`  
		Last Modified: Fri, 09 May 2025 00:37:44 GMT  
		Size: 15.0 MB (14988555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a244728108ce0560ebcb807b30a26f93b9f6581d987e525f43c139f9d534b`  
		Last Modified: Fri, 09 May 2025 00:21:38 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7e93547ce2a5f3a71b44b5ee5dcc65a14ecd52046ad0ba4a1b239955f014ff`  
		Last Modified: Fri, 09 May 2025 00:21:38 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:5adc6bd8eb8317f367db9517e38a1203ea94fea6ba2f325c32e946da03ad9fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3898c89952e5ec9d4f5d6780d6f462555144bc24283b4b55309bfb0c526a8d4b`

```dockerfile
```

-	Layers:
	-	`sha256:bd1a50eec63ba2b3b3be1ef6a7ea6ced439d36095526c7a2400597f155ead99d`  
		Last Modified: Thu, 08 May 2025 19:17:11 GMT  
		Size: 6.7 KB (6700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1e0e1e90e84cfebc31cdc573d9079e858489245a69b701d744d09b8b1b3082`  
		Last Modified: Thu, 08 May 2025 19:16:57 GMT  
		Size: 32.4 KB (32419 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:5173180cae734ee8abab6fe919567b38bc9695762da5c3a68664e5552b8b57d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17075822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55399edb8b459036ec2080d205530a1ef29ffdee81128c3e1e8047d6bd8fda42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a324ded8895b39df9977bfe580708e3ff9c28d3a7b4fb788f16b001563006f`  
		Last Modified: Sun, 16 Feb 2025 08:05:19 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7181eaf68223ddcee59316abf0f05d2e2377dcd7187aae89549641c24390e2`  
		Last Modified: Fri, 09 May 2025 00:21:35 GMT  
		Size: 195.1 KB (195055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b308b7bf97cf1c9193f2017908eb1e5f91e062736541675f1c3b99242ed1c`  
		Last Modified: Fri, 09 May 2025 00:43:22 GMT  
		Size: 13.5 MB (13527065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec1e82cde0331011d3988f758fecb0e2648189163ac977c79eca78e86015ca3`  
		Last Modified: Fri, 09 May 2025 00:21:35 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f63f5840b3f089bf7d6373046ce1bb5b6e554adcf18738418e7379522becae`  
		Last Modified: Fri, 09 May 2025 00:21:35 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:648ff90fa6dbf2c7139db45869a0bbdc57c7599925f563d0b673ada042faefbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 KB (38363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb241b9b76bdb5e24ac8ce6fdbdcd1ea719fb67c0e0419a1c1b4f6bc90cd2610`

```dockerfile
```

-	Layers:
	-	`sha256:bdfcb27779d69273377b831d48570453cda54b53d1c852e9401fc770678f9367`  
		Last Modified: Thu, 08 May 2025 19:17:13 GMT  
		Size: 5.9 KB (5948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9982868d7815b44349ba70102e8e06f384f51e7d3fab0919347302b6666155c0`  
		Last Modified: Thu, 08 May 2025 19:16:59 GMT  
		Size: 32.4 KB (32415 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; s390x

```console
$ docker pull redis@sha256:a5976a18b2da21e7d01a8c8e310a5ec1c29d63591cc3f11a05f50f3575830c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18401911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3aaeb874b0092b066247eb046fa1930b9fe49b418a23b885c3210edb023851`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.0.tar.gz
# Sun, 04 May 2025 07:19:33 GMT
ENV REDIS_DOWNLOAD_SHA=6d1b428d289426b68cff933d61f2d5c0a44a316f17236c51fbb33bc9e5c5a385
# Sun, 04 May 2025 07:19:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	apk --purge del apk-tools ; 	rm -fr ~/.cache/pip*  rm -f /sbin/apk && rm -rf /etc/apk && rm -rf /lib/apk && rm -rf /usr/share/apk && rm -rf /var/lib/apk && rm -rf /usr/lib/python*; 		redis-cli --version; 	redis-server --version; # buildkit
# Sun, 04 May 2025 07:19:33 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 04 May 2025 07:19:33 GMT
VOLUME [/data]
# Sun, 04 May 2025 07:19:33 GMT
WORKDIR /data
# Sun, 04 May 2025 07:19:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 04 May 2025 07:19:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 May 2025 07:19:33 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 04 May 2025 07:19:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32617ca14c22b7a6e74fd0287233c89cd82724992d76be7572bfd6d20b50c651`  
		Last Modified: Fri, 09 May 2025 00:21:36 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017239f40fa06f59a01941964103b2a9f1cfa98c18f10c31292fb974d520453`  
		Last Modified: Fri, 09 May 2025 00:21:36 GMT  
		Size: 197.8 KB (197757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a524ea8c131a508928d9c19a6f2d460890d24e9fb1476fa3ca15d4830feac2`  
		Last Modified: Fri, 09 May 2025 02:00:49 GMT  
		Size: 14.7 MB (14734323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2def0c28cea214ac0f47ba9db57dbe5ee2740220e96275503c403de29fd283e4`  
		Last Modified: Fri, 09 May 2025 00:21:36 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cad2c79c250951a6e34664a13fbeaa39e870b4c2b68527440877befffb4e56`  
		Last Modified: Fri, 09 May 2025 00:21:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:27da07ede2a890084d4d165ebd8c5d631aed8c6849cc83196895bedcb947f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f6ee4656bdaeec48bd7e22f27e380c6ae4037d6f1b79dd60910ccaf06513e4`

```dockerfile
```

-	Layers:
	-	`sha256:8e9534382c8fa04dced4a92e7c1a5e9079047919921ed15d80c0f81a214f61b8`  
		Last Modified: Thu, 08 May 2025 19:17:15 GMT  
		Size: 5.9 KB (5896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fbe29e13a4c32035f01cd1d60095be3fac93fb1b1b8171a6ebcb1a28a44a1f`  
		Last Modified: Thu, 08 May 2025 19:17:01 GMT  
		Size: 32.3 KB (32342 bytes)  
		MIME: application/vnd.in-toto+json
