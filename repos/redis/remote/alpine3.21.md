## `redis:alpine3.21`

```console
$ docker pull redis@sha256:f33f899662cc7e2f2508e760be153dad1168f6c966ca416e0f507ea7effb3342
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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826632aa5dd8df6206034a82fe85493f1b7c96691d94fe4abec5ab08a187345`  
		Last Modified: Mon, 05 May 2025 17:26:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7279224f08c0d30578f4dbef204f0d766afabbd04daf59490323251b558dae`  
		Last Modified: Mon, 05 May 2025 17:26:44 GMT  
		Size: 195.2 KB (195239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b782747b1d523d78e2eccdc898011eb18b9e831309cefc10bb6601fcfe3aa1d0`  
		Last Modified: Mon, 05 May 2025 17:26:45 GMT  
		Size: 20.5 MB (20508439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a566114717809f918a100e6a2d5745e2b81ecbb378f3e5908df3026920199`  
		Last Modified: Mon, 05 May 2025 17:26:44 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64136cebabc3fd206a2e54d36143516c9e9dd18c1a4a6d11d2f12850920bd35e`  
		Last Modified: Mon, 05 May 2025 17:26:45 GMT  
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
		Last Modified: Mon, 05 May 2025 17:26:44 GMT  
		Size: 5.9 KB (5896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265b70a6a50cf838d71f68898a8b2bbd32e9f0c56301502e231a50f0912be8c1`  
		Last Modified: Mon, 05 May 2025 17:26:44 GMT  
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
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306bc7f3cd8273ca2f216836302ad21df95fa6a35edc08f6d45e13364a9fd5`  
		Last Modified: Fri, 14 Feb 2025 22:05:40 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbe3dd27371f1c37af36d90cf012f849a0806aeabd01177d0dd5e1f05b2685`  
		Last Modified: Mon, 07 Apr 2025 19:59:04 GMT  
		Size: 195.7 KB (195696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e5c38d3252b6acc3a973779a2961e0cf93a74e74d647dd5b0a4581705b29f`  
		Last Modified: Mon, 05 May 2025 17:17:44 GMT  
		Size: 14.0 MB (14023126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568cf143d108dcce5c6bb165b01c719b75ae6dcb0017e84772613704aa8ebf75`  
		Last Modified: Mon, 05 May 2025 17:17:43 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3bc1f6e40633000e515c117c76b86a4748ee69900ec68edcd21e4bc675a10`  
		Last Modified: Mon, 05 May 2025 17:17:43 GMT  
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
		Last Modified: Mon, 05 May 2025 17:17:43 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38de7eb7132bf24de27447f0d6330d4299fe0264ac584c5f44fa45bfb8da0f3`  
		Last Modified: Thu, 24 Apr 2025 17:00:55 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075129f30b31cbb1654653588b25f41fd5d899285e15d6fee8739cc39c609ede`  
		Last Modified: Mon, 05 May 2025 17:46:13 GMT  
		Size: 194.0 KB (194040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a003ad8d70e3afeb6558df4644ea31203ab133164940c38829c4397af22a3b`  
		Last Modified: Mon, 05 May 2025 17:46:14 GMT  
		Size: 13.8 MB (13811429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b490790304f175a292805f9ecc5d125e166eb2123162b16799c043b40349fef2`  
		Last Modified: Mon, 05 May 2025 17:46:13 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca3626dc272a208b340786413012f8e96082886ec9e99777808c335a9a0f5f9`  
		Last Modified: Mon, 05 May 2025 17:46:13 GMT  
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
		Last Modified: Mon, 05 May 2025 17:46:13 GMT  
		Size: 6.0 KB (5965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72dc04a8ada6455ecf6e924402cfb03e36799731babee535461d6a041f0f6779`  
		Last Modified: Mon, 05 May 2025 17:46:13 GMT  
		Size: 32.5 KB (32492 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d4690cb02e70c8b8a530134722e33b47e02ca1a4ca3f70386b117574e54e18ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17667517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4b148eff3106317059e5cb92b379e3449491cf05da6fafad08d603be9e551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV GOSU_VERSION=1.17
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_VERSION=7.4.3
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.3.tar.gz
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_SHA=e1807d7c0f824f4c5450244ef50c1e596b8d09b35d03a83f4e018fb7316acf45
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
VOLUME [/data]
# Thu, 24 Apr 2025 08:18:49 GMT
WORKDIR /data
# Thu, 24 Apr 2025 08:18:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 24 Apr 2025 08:18:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c125e7fc044f208a7f4c40121d44812b8d4d877c9684859bd42f1c3653041685`  
		Last Modified: Thu, 24 Apr 2025 16:59:11 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e7d4e0afcc013800e6e193a01ed22d545de1f6139c8ab1c0b820bd78b13f7f`  
		Last Modified: Thu, 24 Apr 2025 16:59:11 GMT  
		Size: 173.2 KB (173226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab7de54d08bd3d1f06a010b6b42a9876f39ef6e4bfd1f115052e2fb8441ea9d`  
		Last Modified: Thu, 24 Apr 2025 16:59:12 GMT  
		Size: 934.7 KB (934718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff564f4799eca04adf8f03e027c76a9f40a5400f95b848e5a3fa163cf3f878fe`  
		Last Modified: Thu, 24 Apr 2025 16:59:12 GMT  
		Size: 12.6 MB (12564884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf79882350efa15a0a28ab925f74b8bd386e44366a3103e6ff01a30b34c02bc`  
		Last Modified: Thu, 24 Apr 2025 16:59:12 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d7bc2c144e06d32f3b37ccced778621158a619a5dd8980de97c0c15ebb4c52`  
		Last Modified: Thu, 24 Apr 2025 16:59:13 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:395fc04bd8fe98e48cba84e10fd8ab9ff1a453b15609c0bbbebab5f9b5e9d5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 KB (494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1542b970fd2d0114b68a2e30e1e9cdc1de044d0b354c4ba556309045f9a803c4`

```dockerfile
```

-	Layers:
	-	`sha256:6afbc8c7a07d2b6d039618d633b85e1351ee7f043a67981e8c7ec44996b673dc`  
		Last Modified: Thu, 24 Apr 2025 16:59:12 GMT  
		Size: 459.9 KB (459930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4222e61cdb829113715881b3a00ee7ddb0571eb6326485470aae676308d498`  
		Last Modified: Thu, 24 Apr 2025 16:59:11 GMT  
		Size: 34.6 KB (34627 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc03c307c042b0019919be4aca7c5db8571469a1970bbca53c2125d9eaf35f`  
		Last Modified: Mon, 05 May 2025 17:19:09 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10234629e49fd6134d9fcab3db5c1ef67f666879ebeb399d25ef4639f433dc`  
		Last Modified: Mon, 05 May 2025 17:19:09 GMT  
		Size: 195.3 KB (195265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f262b87977f78b0ee89f9c4ded66b6dc502aae2136cd6f8d5c720994a377ef6`  
		Last Modified: Mon, 05 May 2025 17:19:10 GMT  
		Size: 13.8 MB (13798512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e98aaf59b67d32794055b335cfdcdb0c4fce301ebb58612a7ff09c11dde1dce`  
		Last Modified: Mon, 05 May 2025 17:19:09 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddea5b1619a1f8fd36f2c4a9dc8742e5fc66b38fc3cc43c657bc3b7abc4adc86`  
		Last Modified: Mon, 05 May 2025 17:19:10 GMT  
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
		Last Modified: Mon, 05 May 2025 17:19:09 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4357a7180c29461854a2f4c3ca595e376174df34d176ac0a0e44a55e51f8cfe`  
		Last Modified: Mon, 05 May 2025 17:19:09 GMT  
		Size: 32.3 KB (32287 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; ppc64le

```console
$ docker pull redis@sha256:76525fd7f2c6a73da35f2e2b176972a56e0033574d56fec5f59bcf22dcc28057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18015501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934f6db236c7abb622acfb6267cfcc92283f0ad46ed6c9f703a6ce105da07333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV GOSU_VERSION=1.17
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_VERSION=7.4.3
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.3.tar.gz
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_SHA=e1807d7c0f824f4c5450244ef50c1e596b8d09b35d03a83f4e018fb7316acf45
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
VOLUME [/data]
# Thu, 24 Apr 2025 08:18:49 GMT
WORKDIR /data
# Thu, 24 Apr 2025 08:18:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 24 Apr 2025 08:18:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11623b35463c76a5fb599f0a8f5fe558186f8d35f1227ab9117b9745236ca7e6`  
		Last Modified: Thu, 24 Apr 2025 17:00:57 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddaff3d60c9b703d387e673fe252b1da25ef301e3572bd6ab2f85c0fa650e80`  
		Last Modified: Thu, 24 Apr 2025 17:00:57 GMT  
		Size: 173.2 KB (173244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb21bc8214a1fae54e4a25a370d82b2e9c553ed814979e92a091bb4f549f2cc`  
		Last Modified: Thu, 24 Apr 2025 17:00:57 GMT  
		Size: 923.0 KB (922964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc1a0fdbf1bb49551c4ba3dc79c7867624562888a1c8f6c15a938ba20551696`  
		Last Modified: Thu, 24 Apr 2025 17:00:57 GMT  
		Size: 13.3 MB (13343288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721f8d372f7c5439a29dd7d6cde5e5056c870689d2bfbd1a563988a9acf9e959`  
		Last Modified: Thu, 24 Apr 2025 17:00:58 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f2ee61e7ed1564209f09566cdd6278f68469f6bbd74b9e50e463be11d00f57`  
		Last Modified: Thu, 24 Apr 2025 17:01:00 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:1944f8ba1762abfef9d8be1bb24fceaae02836308ff58c880a8e08736ce31671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.4 KB (492421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5a0b9b7d04e5ba3be1717512c1bc5199dec2eadb57b74ffaa72713f0e6537f`

```dockerfile
```

-	Layers:
	-	`sha256:774b39549b94ae67a0d1bb3b8da98119905720e5586bda9fe118c120b5f9172e`  
		Last Modified: Thu, 24 Apr 2025 17:00:59 GMT  
		Size: 457.9 KB (457933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64551f3c63d31b0e6c5bad27a47d1b546ba74e3fd42d6ee3b1c0812707dba94`  
		Last Modified: Thu, 24 Apr 2025 17:00:57 GMT  
		Size: 34.5 KB (34488 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:alpine3.21` - linux; riscv64

```console
$ docker pull redis@sha256:1f37a046d0c0858b044f6ec411ccc7ebab8972560caaa8e7dda848fba55ab56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16459741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d49d64bbbc72b3fbb018aa57d67b78dcbe54e3835c5943a510bd0e1153f3128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 	; # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV GOSU_VERSION=1.17
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .gosu-fetch gnupg; 	arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'aarch64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		'x86') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'ppc64le') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armv7') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apk del --no-network .gosu-fetch; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_VERSION=7.4.3
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.3.tar.gz
# Thu, 24 Apr 2025 08:18:49 GMT
ENV REDIS_DOWNLOAD_SHA=e1807d7c0f824f4c5450244ef50c1e596b8d09b35d03a83f4e018fb7316acf45
# Thu, 24 Apr 2025 08:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		wget 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
VOLUME [/data]
# Thu, 24 Apr 2025 08:18:49 GMT
WORKDIR /data
# Thu, 24 Apr 2025 08:18:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Apr 2025 08:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Apr 2025 08:18:49 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 24 Apr 2025 08:18:49 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a324ded8895b39df9977bfe580708e3ff9c28d3a7b4fb788f16b001563006f`  
		Last Modified: Sun, 16 Feb 2025 05:07:12 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce95c03e4bdd147987ed384886f65414bd526299fe188331037c1e389c34024`  
		Last Modified: Sun, 16 Feb 2025 05:07:13 GMT  
		Size: 171.6 KB (171567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614203cf3ba3b4bccf25a43e3bcffa4e07f09db3b61d4c0179d526f583e3d0f5`  
		Last Modified: Sun, 16 Feb 2025 05:07:13 GMT  
		Size: 975.0 KB (975017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce216dcb360aebaa5fe5ed98d4ef7708288b64320945b1f86da230b1db35f3e`  
		Last Modified: Thu, 24 Apr 2025 17:13:35 GMT  
		Size: 12.0 MB (11960059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41807a4cbd8c2677b30d2281b2d189d88f0196fa04ff58c095d1e5774d1d1e17`  
		Last Modified: Thu, 24 Apr 2025 17:13:33 GMT  
		Size: 98.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea16181755e087509b59e07367595e663596d3e88f93be57eb1849f56c4d5bf`  
		Last Modified: Thu, 24 Apr 2025 17:13:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:alpine3.21` - unknown; unknown

```console
$ docker pull redis@sha256:ef3ae94d12b5df169f9e0038b291737da0ebcabddb8d40d062888bc3248ab638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.8 KB (491795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb407b2b0ec5d0ff99f910f8d443e63f43074bee1bf424ee9eebb6e042434173`

```dockerfile
```

-	Layers:
	-	`sha256:8985b608b3ad80de491b4c80800bbbeb4cc9fa63368c0d5531ecc36fba07c47d`  
		Last Modified: Thu, 24 Apr 2025 17:13:33 GMT  
		Size: 457.3 KB (457307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70e700f7cfd594f52b5a8ac32a67e1b3105f79b55f21f5c06ce18d61e21e68b`  
		Last Modified: Thu, 24 Apr 2025 17:13:33 GMT  
		Size: 34.5 KB (34488 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32617ca14c22b7a6e74fd0287233c89cd82724992d76be7572bfd6d20b50c651`  
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017239f40fa06f59a01941964103b2a9f1cfa98c18f10c31292fb974d520453`  
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 197.8 KB (197757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a524ea8c131a508928d9c19a6f2d460890d24e9fb1476fa3ca15d4830feac2`  
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 14.7 MB (14734323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2def0c28cea214ac0f47ba9db57dbe5ee2740220e96275503c403de29fd283e4`  
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cad2c79c250951a6e34664a13fbeaa39e870b4c2b68527440877befffb4e56`  
		Last Modified: Mon, 05 May 2025 17:45:00 GMT  
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
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 5.9 KB (5896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fbe29e13a4c32035f01cd1d60095be3fac93fb1b1b8171a6ebcb1a28a44a1f`  
		Last Modified: Mon, 05 May 2025 17:44:59 GMT  
		Size: 32.3 KB (32342 bytes)  
		MIME: application/vnd.in-toto+json
