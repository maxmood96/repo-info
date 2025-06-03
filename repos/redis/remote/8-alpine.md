## `redis:8-alpine`

```console
$ docker pull redis@sha256:48501c5ad00d5563bc30c075c7bcef41d7d98de3e9a1e6c752068c66f0a8463b
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

### `redis:8-alpine` - linux; amd64

```console
$ docker pull redis@sha256:791db4fefbec3fd6ba54690f2479554f2d7ef68dc786e87a7d1f5fc11caebea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24326461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74faa347ab0b6a3c1b040834a35ea5f20e3aa02460db4bb9d5b4685f3dd3baf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db14a52e194f7d4b3637f40569c1cfac85fe5be3cd2db1e6acda30061091088`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ac91e0937206f61f419e184bb158a10fb5e0ac6ae83a5db388f0e48feeb77`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 195.2 KB (195225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3535ba13b4da0af2f7b616050815f19caa89b8141b1f2416af44a8ab51cbf019`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 20.5 MB (20485805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ba5ae8d20db7c9dcbbec42a3c8b42c54bd48441d55ea3eeae679bbbca62ff9`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493ebef02b702bda0911b2f29bc7d42461a5d095594a728869619b96de9133a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:1f4b4a25dca1eb7d0dc82877ad49a091a36d5c60d87212ae2847a60bf8bc5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.1 KB (500061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22605a74d181c5a5fb3e87462697c108ed4a23c94c2d1dd456f1ef93307bfbd`

```dockerfile
```

-	Layers:
	-	`sha256:bfb83d875bd9d675d20f1225dbb3cc36619f5dd5457e94e62457c1cb6ae48acf`  
		Last Modified: Fri, 30 May 2025 00:21:30 GMT  
		Size: 468.2 KB (468167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e3386ba6ac3d92c0d1e8f497496710ae1862009b4303c072844c6494b10e53`  
		Last Modified: Fri, 30 May 2025 00:21:30 GMT  
		Size: 31.9 KB (31894 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:58082d57038edc8d63e83a4708b2d48e6c5f6facdc3846e8ddcd73dba7999f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17562329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2e807703fa2d8d1653734e4fcff2a4588498c58bf0b464b3510499ba50e183`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:282db186f1a7e7df8c33f1e94e8475a306e53ce93490a4b0846863973baf4e30`  
		Last Modified: Fri, 30 May 2025 00:30:23 GMT  
		Size: 14.0 MB (13998710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb7a2ecabb4a71b2e48703e8789181b0f16d17100e1392f1b55af3994bcbb8`  
		Last Modified: Fri, 30 May 2025 00:30:23 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4304e4111b084b514d4fec2af7a7cafbbe6f150900397b0aab18857f0a82272`  
		Last Modified: Fri, 30 May 2025 00:30:23 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:7c349c7eeef33ea2930b0d5413c19da87ff0061ffbccab2798af429745961a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca675e0ccbd2c7e975d804ed72c4e41373800826196afed46655755df26674e`

```dockerfile
```

-	Layers:
	-	`sha256:4877a5607c04ecd9838450b6a6f9e4f133fe8afbb83fe9761598ffb5c074dabb`  
		Last Modified: Fri, 30 May 2025 00:30:22 GMT  
		Size: 31.8 KB (31829 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1fd8640d4d9cae736e33a6a2fa54464f0fb0a8fb1752fde8b219306302f0ad06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17078701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77de4d8c84708e4517d253bad999f391cc20991d267af119f33e908d99e5db9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:1b5a62d507a24bfdf86301eee9a47cf842bb04ba81debfa6ad7103c4d6e36cfc`  
		Last Modified: Tue, 03 Jun 2025 13:33:00 GMT  
		Size: 13.8 MB (13783343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de39383f44d030fbd1f0ce84776e7d61f70e24fcd57d1fbb18223b05b63fb058`  
		Last Modified: Tue, 03 Jun 2025 13:30:55 GMT  
		Size: 101.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236ceb60a923ff37c126025af915ee269b9c377543f524cdab95cbae7a22773e`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 2.1 KB (2111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:a04a6cdc39c6bc3ebe6645a6d91eeddc3288f0dfa1ec741c667a174cb22aabaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.3 KB (500279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b50fe8ad2af236df09e76fc8e5c79f54483301b0e7771c8b1c87e5a57e2a31`

```dockerfile
```

-	Layers:
	-	`sha256:2b97cf587fd002454f583e6daf02fee0af315afb7dab473133be8921db113341`  
		Last Modified: Fri, 30 May 2025 00:15:05 GMT  
		Size: 468.2 KB (468235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a714a47808c442e033be55335b14d5ee65b514d323b75904b25a0fff77200893`  
		Last Modified: Fri, 30 May 2025 00:15:05 GMT  
		Size: 32.0 KB (32044 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:692903347ec4ba765e51ac71a899e77b763aca0311b1f220739c1d52585f9050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fdd1f7ada586be306a0f87861106d902f49aab742252c05903b76e926772bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ae3b7f17cdfe6a48ce5eba4c9d2bb1056bc39f6c4323d418033f1ce6c157ae`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1471fa3c8b312cb841f2ba58571f80f81b78e863b0f7573500fab2dbc3aef19`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 198.0 KB (198044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7c96abf22d3a52fc80a75589c527e0332394b2fcff7200eaf28ee75060a66`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 20.4 MB (20408832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52903a8199519bf0bfde92600071365f1a18af3551e48e0b746b826d13c0d2c`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07b81fc7e4d7434e5328259757651585c028843642256b604022f32507aa139`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:6a3bbeb52ed2d7841d87257ce43dc6ae5c60a089c0b74b1ba84956c4d9ba869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.4 KB (500361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5549c2aebae1db8222ad75fb617343a605b408d0194bcc7009bc064c36a1c04`

```dockerfile
```

-	Layers:
	-	`sha256:8f97b42216d04145d36c1091ff76585efdf3ab77f1bb962ea190a3722813599a`  
		Last Modified: Fri, 30 May 2025 00:22:38 GMT  
		Size: 468.3 KB (468271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a28fdc921cbbbd0f35cc5fcb9ff2425ec7f4e04fa16d5ce4e15cb7bac24b0f`  
		Last Modified: Fri, 30 May 2025 00:22:38 GMT  
		Size: 32.1 KB (32090 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; 386

```console
$ docker pull redis@sha256:9f79383109fe3fa72538d8532ffbbd1a3b4b155e7b6ca2df3dcf872fef2b6e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17436226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8b87505e533e0c4bc15482d80752c5feb59f3ac4e3f2ebd64f97500811f0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dd2a4c83a3c6a8cf2a9644ba8e5acad69362e75fb188dd5bbe4596042bcaa0`  
		Last Modified: Fri, 30 May 2025 00:14:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb2b500a56d7be03bc363b01fea869c3b85aadfb8b2e1ab8e05fecdb1d0de2`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 195.3 KB (195267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ee6053ad04a22b7c65a74a29d9798571a149b503c5e10752cecb113dd3dd5d`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 13.8 MB (13774141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6472ccd89c4f10bd5eb636b5d36f286abef1628254f66d08eb4352fdafccbbd6`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bafad5901e36409c55f8ba2e73049cca93e3ef7337912fc6ba3a89159ff89c`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:cfc76f42bc3a594b65595c43b809746f321e8157e9fb8927dc90783ea512f1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 KB (499961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022145c636e4e84c9b815aed40390f819b28ed3480cb33a680f0612796ff30c1`

```dockerfile
```

-	Layers:
	-	`sha256:765a330e01dd975f44ff7c86bc1f37d277d63487fc794ec8a163ebc644abcc8c`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 468.1 KB (468122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc6f5399106f6a7808e67eddeb2ab4e12f0e407fa21b46424d46fe6e43749e2`  
		Last Modified: Fri, 30 May 2025 00:14:15 GMT  
		Size: 31.8 KB (31839 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:ea0b0505fe8c57fb670b150cd141fb0be4018e435e7bd82e9a64a234ce5b81ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90e679df660067d3aa2ce5345142a3de42ce784149c3988d01d70d59e9f2546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877108094d78a4d990caf25d655e6708b61001686a3d3ce80c4ded8c638608b`  
		Last Modified: Tue, 03 Jun 2025 14:44:08 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded7418a3db2b946dcfafa98b3002dc52b4440a336c3968aa0c06479ecaa7cec`  
		Last Modified: Fri, 30 May 2025 00:15:18 GMT  
		Size: 199.1 KB (199052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a29f632f9a5094ce88d919278ab4438be0b05d5db67866d19104cfb06edac19`  
		Last Modified: Fri, 30 May 2025 00:15:19 GMT  
		Size: 15.0 MB (14965297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eaafbaf632fe76960398010c82edd7108561c1064d9855b12af052db499fc4`  
		Last Modified: Fri, 30 May 2025 00:15:18 GMT  
		Size: 100.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92c0ceb1ebf15bbbfe497c1081e1ce5c9c60b3865aeead5457b414b259bec76`  
		Last Modified: Fri, 30 May 2025 00:15:19 GMT  
		Size: 2.1 KB (2112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:3b12301269ccfb7fb95adc4e046a7f9a695b6ca100b23b268aa4a4b7e47cfca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 KB (498245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4c8fa9f71a22181179871c0b816960713141995689a20ff5474c7b9c4f2c90`

```dockerfile
```

-	Layers:
	-	`sha256:e5ab667cda623480e6f8d6ab97ac26a456c650c620d4353ed2d178c157cf2dc5`  
		Last Modified: Fri, 30 May 2025 00:15:19 GMT  
		Size: 466.3 KB (466274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb228d24751432abedeedba4e45d2c976c3020077f5369eb87f4595088f4cae`  
		Last Modified: Fri, 30 May 2025 00:15:18 GMT  
		Size: 32.0 KB (31971 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; riscv64

```console
$ docker pull redis@sha256:21391620bd96e7b96249548b10abc6a1b11ac5156b5612de3adbfc8f4a60efb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17053061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9237b2f2405e86305095482d64b3d656a000bd61ecde7e5c073f6505ec63f556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:67cbac19c804b83369d3c441094bb8424767ad35c87102f2d3bd7ba00c287223`  
		Last Modified: Fri, 30 May 2025 00:28:06 GMT  
		Size: 13.5 MB (13503372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb3d2eaf3e012f68ef6e15ec8ce87e5f8f4ef163b457a66b5d225eb2df4156a`  
		Last Modified: Fri, 30 May 2025 00:28:04 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e83b5a96b08162745a153091e1526e54b1c2fcdd5f1c4229353ae514fd91c1`  
		Last Modified: Fri, 30 May 2025 00:28:04 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:8886ca69d7a145f48d5d98814cb3c65c5eb6ed4ae0aa94d28837158a6567ff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.2 KB (498238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f949de57e52afc74180b8269c987dfd0f75f202431eeca07a9ca086c4bcf5cac`

```dockerfile
```

-	Layers:
	-	`sha256:4545fd0d341ebb21a189987ae0f286e34aac274582a935af923cd9413363fd13`  
		Last Modified: Fri, 30 May 2025 00:28:05 GMT  
		Size: 466.3 KB (466270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:286205dc55f7b1127ac2d66abfd198f33942ce87369f958f2c34862c23b64223`  
		Last Modified: Fri, 30 May 2025 00:28:04 GMT  
		Size: 32.0 KB (31968 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:8-alpine` - linux; s390x

```console
$ docker pull redis@sha256:6be83b534f329766f2496ada872fa7639605d2fd0620ffd099829501b8f49a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18378582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ac2d591de9cad4196964a2ef21fc2d1fb79666cc574aa55f2fa8ab63949d4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	addgroup -S -g 1000 redis; 	adduser -S -G redis -u 999 redis # buildkit
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 	apk add --no-cache 		tzdata 		setpriv 	; # buildkit
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/8.0.2.tar.gz
# Thu, 29 May 2025 16:02:07 GMT
ENV REDIS_DOWNLOAD_SHA=caf3c0069f06fc84c5153bd2a348b204c578de80490c73857bee01d9b5d7401f
# Thu, 29 May 2025 16:02:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		dpkg-dev dpkg 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 		g++; 		arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		'arm64') export BUILD_WITH_MODULES=yes; export INSTALL_RUST_TOOLCHAIN=yes; export DISABLE_WERRORS=yes ;; 		*) echo >&2 "Modules are NOT supported! unsupported architecture: '$arch'"; export BUILD_WITH_MODULES=no ;; 	esac; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 	apk add --no-cache --virtual .module-build-deps 		autoconf 		automake 		bash 		bsd-compat-headers 		build-base 		cargo 		clang 		clang18-libclang 		cmake 		curl 		g++ 		git 		libffi-dev 		libgcc 		libtool 		openssh 		openssl  		py-virtualenv 		py3-cryptography 		py3-pip 		py3-virtualenv 		python3 		python3-dev 		rsync 		tar 		unzip 		which 		xsimd 		xz; 	fi; 		pip install -q --upgrade setuptools &&  pip install -q --upgrade pip && PIP_BREAK_SYSTEM_PACKAGES=1 pip install -q addict toml jinja2 ramp-packer ;	wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		make -C /usr/src/redis/modules/redisjson get_source; 		sed -i 's/^RUST_FLAGS=$/RUST_FLAGS += -C target-feature=-crt-static/' /usr/src/redis/modules/redisjson/src/Makefile ; 		grep -E 'RUST_FLAGS' /usr/src/redis/modules/redisjson/src/Makefile; 	fi; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		make -C /usr/src/redis distclean; 	rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	if [ "$BUILD_WITH_MODULES" = "yes" ]; then 		apk del --no-network .module-build-deps; 	fi; 	apk del --no-network .build-deps; 	rm -rf ~/.cache ~/.gitconfig; 		redis-cli --version; 	redis-server --version; # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28b387569101501f6fecd80073d3f0c4b782162dbedf40cd97cf67ba329a17`  
		Last Modified: Tue, 03 Jun 2025 14:44:13 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cd34ab59dab0e071b50add404b64e1df8880181b82db537fd61ae94279ff32`  
		Last Modified: Fri, 30 May 2025 00:14:36 GMT  
		Size: 197.8 KB (197757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8af2d305ea528c811faee502bf91113272cbbcd866cdfe7c5f2f8fa551ecec`  
		Last Modified: Fri, 30 May 2025 00:14:37 GMT  
		Size: 14.7 MB (14710060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afde61e7f35d650536d224c2dcaab5630df6b3c220dd37d4f1c0778c8d61056a`  
		Last Modified: Fri, 30 May 2025 00:14:36 GMT  
		Size: 99.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1466e17aa6e629706cc8b2d83a59a09b186465297bcbeea139b5856a5f267b72`  
		Last Modified: Fri, 30 May 2025 00:14:37 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:8-alpine` - unknown; unknown

```console
$ docker pull redis@sha256:c6df76dbfc8e421bbabb07a6fdc99a41832123b8113fa1fd183744dfc9595be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.1 KB (498110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b939621964131ea38bb1a0b6130d4a987568da41d9486e732de6505434d19f73`

```dockerfile
```

-	Layers:
	-	`sha256:1bd3d9cc3eac1a8d85ca177e732518f9597b7f1e00528538c22cef32d25cccca`  
		Last Modified: Fri, 30 May 2025 00:14:36 GMT  
		Size: 466.2 KB (466216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b4fdaf40c0fb8b466abec04e3cb547c6f279259e906ab7715802fe04b9b8eb2`  
		Last Modified: Fri, 30 May 2025 00:14:36 GMT  
		Size: 31.9 KB (31894 bytes)  
		MIME: application/vnd.in-toto+json
