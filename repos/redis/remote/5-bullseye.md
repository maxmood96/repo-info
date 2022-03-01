## `redis:5-bullseye`

```console
$ docker pull redis@sha256:44058acf18cb451c205fd484e04a6b3c205f1d4dff72a4779b848f1e15fcb89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5-bullseye` - linux; amd64

```console
$ docker pull redis@sha256:d6e29e9910fdd3c288ba39a207c02351e7b5e5bd2df4890bea2838915085460e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40081868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d7b5ad28a2d2a8679cf24adc22cb11886cf61d477f6b8ee8f33fa001aa71e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 22:41:18 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 26 Jan 2022 22:41:18 GMT
ENV GOSU_VERSION=1.12
# Wed, 26 Jan 2022 22:41:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Jan 2022 22:44:24 GMT
ENV REDIS_VERSION=5.0.14
# Wed, 26 Jan 2022 22:44:24 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Wed, 26 Jan 2022 22:44:25 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Wed, 26 Jan 2022 22:45:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 26 Jan 2022 22:45:42 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 26 Jan 2022 22:45:42 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 22:45:42 GMT
WORKDIR /data
# Wed, 26 Jan 2022 22:45:43 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Wed, 26 Jan 2022 22:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jan 2022 22:45:44 GMT
EXPOSE 6379
# Wed, 26 Jan 2022 22:45:44 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6530a7ea347970d67d6fae6cc7a20afa47d97ecb81c1ec8984c0e44893fd979e`  
		Last Modified: Wed, 26 Jan 2022 22:48:24 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f5202c6d9ba08aa9dd6f769132c036149ae4a3ee25765454180ecc0758a664`  
		Last Modified: Wed, 26 Jan 2022 22:48:24 GMT  
		Size: 1.4 MB (1442359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794a1ae80e03d0b5809b1d07fe0ed1f53eed6d481894608a08c8a17e359d9ff9`  
		Last Modified: Wed, 26 Jan 2022 22:49:17 GMT  
		Size: 7.3 MB (7270978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfd5af341d5f5996ae0899b52a40254d095a777f9d23a87957b85358643c80c`  
		Last Modified: Wed, 26 Jan 2022 22:49:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b19def99ff0d45e201bd9291c56938822935235cdf0439afb9855c760c5f7b`  
		Last Modified: Wed, 26 Jan 2022 22:49:16 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; arm variant v5

```console
$ docker pull redis@sha256:22d9f67ce27d8624c7cb7136842d877498c9ad9f7bd482e853377082f893a333
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37459888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81e31827c9ac0e7be780491cf0fd3db4aeff2949b00e5df7f267eb97c246fbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:53 GMT
ADD file:eb61ee802e5118b26e1fec2c7fc58e34de0de54a5fd47dc6318c11a039ef528f in / 
# Tue, 01 Mar 2022 02:02:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:44:04 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 01 Mar 2022 02:44:04 GMT
ENV GOSU_VERSION=1.12
# Tue, 01 Mar 2022 02:44:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 02:50:35 GMT
ENV REDIS_VERSION=5.0.14
# Tue, 01 Mar 2022 02:50:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Tue, 01 Mar 2022 02:50:36 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Tue, 01 Mar 2022 02:52:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 01 Mar 2022 02:52:09 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 01 Mar 2022 02:52:09 GMT
VOLUME [/data]
# Tue, 01 Mar 2022 02:52:10 GMT
WORKDIR /data
# Tue, 01 Mar 2022 02:52:10 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:52:11 GMT
EXPOSE 6379
# Tue, 01 Mar 2022 02:52:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4aa6e26b4dfdac27e5b5e15b7ebf4366149755a79dd653a5b68d9d93dd94c695`  
		Last Modified: Tue, 01 Mar 2022 02:18:33 GMT  
		Size: 28.9 MB (28909528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48103ce429daf296cfa3f3524e6af15243fc22c79efa72a6172ff5d74e406850`  
		Last Modified: Tue, 01 Mar 2022 02:54:01 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e3be2e159572ae85c704159ad1d6efe109518bff774047c5a913603d73b5d3`  
		Last Modified: Tue, 01 Mar 2022 02:54:02 GMT  
		Size: 1.4 MB (1402394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fae59bf6b64aa0a80c00995cc9bb041b6c13accd3969665006d58690b421b9`  
		Last Modified: Tue, 01 Mar 2022 02:55:35 GMT  
		Size: 7.1 MB (7145699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ade8211905b6534ae4dc03875e5a6e2fb3b888badd40a3088894c428aec5d8`  
		Last Modified: Tue, 01 Mar 2022 02:55:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd13f2de94c2fb78c53bf7ba83d2ff333bd7c0a15c8ffc480b9898f88086da92`  
		Last Modified: Tue, 01 Mar 2022 02:55:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; arm variant v7

```console
$ docker pull redis@sha256:bb359891a44f99b11682170c532fd06d44ea048a3d3e49b8e3da7be34ae826d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34970479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9989e204bd95802884b691619cc8964c76a517137ccbecc74e4b00f0a08ab79a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:08 GMT
ADD file:7f27f5b43b7cb04e509fe145266d9bdeacfcacb024cafac32e57ef1c831d5ea7 in / 
# Wed, 26 Jan 2022 01:42:09 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 01:53:27 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Thu, 27 Jan 2022 01:53:27 GMT
ENV GOSU_VERSION=1.12
# Thu, 27 Jan 2022 01:53:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 01:58:24 GMT
ENV REDIS_VERSION=5.0.14
# Thu, 27 Jan 2022 01:58:24 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Thu, 27 Jan 2022 01:58:24 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Thu, 27 Jan 2022 01:59:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Thu, 27 Jan 2022 01:59:56 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 27 Jan 2022 01:59:56 GMT
VOLUME [/data]
# Thu, 27 Jan 2022 01:59:57 GMT
WORKDIR /data
# Thu, 27 Jan 2022 01:59:57 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Thu, 27 Jan 2022 01:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jan 2022 01:59:58 GMT
EXPOSE 6379
# Thu, 27 Jan 2022 01:59:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:aaef1f1162ec03e01b5b955d41da400544ec2374093ae3dbc330ab2bb36df3e1`  
		Last Modified: Wed, 26 Jan 2022 01:57:59 GMT  
		Size: 26.6 MB (26564933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323e8c1e38940b1338bd17fd2f853496007f92647e382467a59695d824dc1a56`  
		Last Modified: Thu, 27 Jan 2022 02:02:55 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964c4f61fdf303dc26a378faf399867802000ba7e85eeaf9122bf0b722ebe5b0`  
		Last Modified: Thu, 27 Jan 2022 02:02:56 GMT  
		Size: 1.4 MB (1393997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb84d91be2953ac588b0d9662f947f098d01226ab9325bc7e0afaeaed6362bd4`  
		Last Modified: Thu, 27 Jan 2022 02:04:29 GMT  
		Size: 7.0 MB (7009284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccaf4ea4df3975a57fa63b47b517006717ca5a3b912057bf94801e2c77e329c8`  
		Last Modified: Thu, 27 Jan 2022 02:04:24 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677aef0df70a8c52f23ec8c4adf88f0525e98abfcf751167e470ba1846c89d6e`  
		Last Modified: Thu, 27 Jan 2022 02:04:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:5a22b6bfadead2f6c3bf5161a2f2e95f54ae03c1d330359da3f14a3de13adc4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38748053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f0e2a53573042c1a7061acda8ddd1cb4133f4c1cee95aafdab47298f736599`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 07:36:41 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 26 Jan 2022 07:36:42 GMT
ENV GOSU_VERSION=1.12
# Wed, 26 Jan 2022 07:36:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Jan 2022 07:38:58 GMT
ENV REDIS_VERSION=5.0.14
# Wed, 26 Jan 2022 07:38:59 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Wed, 26 Jan 2022 07:39:00 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Wed, 26 Jan 2022 07:39:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 26 Jan 2022 07:39:36 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 26 Jan 2022 07:39:37 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 07:39:38 GMT
WORKDIR /data
# Wed, 26 Jan 2022 07:39:40 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Wed, 26 Jan 2022 07:39:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jan 2022 07:39:41 GMT
EXPOSE 6379
# Wed, 26 Jan 2022 07:39:42 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0e295b9b0c971245d7a3ca60e937b01db4f328cf29be67f8b83f3708401cbf`  
		Last Modified: Wed, 26 Jan 2022 07:41:01 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f1df9dfc4c6ddd2cdb8e64d60f717d31cadcebe7dfb9541c95783d00f4f3eb`  
		Last Modified: Wed, 26 Jan 2022 07:41:02 GMT  
		Size: 1.4 MB (1377921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85028f78f386932e5a2e376d791027984bc1447e0dda691c37305336758b437`  
		Last Modified: Wed, 26 Jan 2022 07:42:02 GMT  
		Size: 7.3 MB (7311233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cf921bf4e01a45c4e7268f631c47f78b815cea6cf822c57361945e9c703e6b`  
		Last Modified: Wed, 26 Jan 2022 07:42:01 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0b0fcf5d42d3a68c8e2b3c8f48607ff1687c7513cf3d49a044bd53e7e4c69b`  
		Last Modified: Wed, 26 Jan 2022 07:42:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; 386

```console
$ docker pull redis@sha256:3c6a588a565858fb5cb521c86b8bcd4b2b0dd7a7d9bcf62de61097782e7ed320
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40783632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59949b27d55409ca745435a88367a3ce7dac5c0b0873b6e71eb8aa101505060`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:32 GMT
ADD file:e92ab504d4c0d3bd63da83254e6ca400b607c32e0f5037039648559b91770870 in / 
# Tue, 01 Mar 2022 02:07:33 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:57:45 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 01 Mar 2022 02:57:46 GMT
ENV GOSU_VERSION=1.12
# Tue, 01 Mar 2022 02:57:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 03:04:23 GMT
ENV REDIS_VERSION=5.0.14
# Tue, 01 Mar 2022 03:04:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Tue, 01 Mar 2022 03:04:23 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Tue, 01 Mar 2022 03:05:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 01 Mar 2022 03:05:30 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 01 Mar 2022 03:05:30 GMT
VOLUME [/data]
# Tue, 01 Mar 2022 03:05:31 GMT
WORKDIR /data
# Tue, 01 Mar 2022 03:05:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 01 Mar 2022 03:05:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 03:05:31 GMT
EXPOSE 6379
# Tue, 01 Mar 2022 03:05:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:04a87e821be7e4b29d48011b7aa4ff884ca57fd36995cb3b99fd2fc24ac562d8`  
		Last Modified: Tue, 01 Mar 2022 02:15:51 GMT  
		Size: 32.4 MB (32377389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cc60de8ed9670a36e309aa25e7cdb479b95b5b6a82e5f7e7b41c070dbfc40f`  
		Last Modified: Tue, 01 Mar 2022 03:07:31 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c42cfdae4ee655d30ff97b0e731272eee257cb373867199b882f5448ba0e9f`  
		Last Modified: Tue, 01 Mar 2022 03:07:32 GMT  
		Size: 1.4 MB (1413437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82f7b3c377bed1091c28bae7622941ffe704ed8e404cc1f6676862bec920894`  
		Last Modified: Tue, 01 Mar 2022 03:09:21 GMT  
		Size: 7.0 MB (6990538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e4d6c998733b0c40d8b4ffda24d5b86cb68f722d892c436e527e8a77c2c567`  
		Last Modified: Tue, 01 Mar 2022 03:09:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c3a628383f00ea6f1b466b2e53b1413a22d700a0f73648a9a16d0650deba33`  
		Last Modified: Tue, 01 Mar 2022 03:09:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; mips64le

```console
$ docker pull redis@sha256:a088f74c16e81aec457ed40980e41b3f238cbb11a2f058b5dd062b655ce723ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38605275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b058601a43935dff00271c017b8862b2935fdbc0de75739c31bfd75ca656ffcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:49 GMT
ADD file:1901e1e1292cbfcd557262ec5d08551cecd0070b24928414d220472664fe3fdf in / 
# Tue, 01 Mar 2022 02:02:49 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:41:09 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 01 Mar 2022 02:41:09 GMT
ENV GOSU_VERSION=1.12
# Tue, 01 Mar 2022 02:41:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 02:52:10 GMT
ENV REDIS_VERSION=5.0.14
# Tue, 01 Mar 2022 02:52:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Tue, 01 Mar 2022 02:52:10 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Tue, 01 Mar 2022 02:55:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 01 Mar 2022 02:55:04 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 01 Mar 2022 02:55:05 GMT
VOLUME [/data]
# Tue, 01 Mar 2022 02:55:05 GMT
WORKDIR /data
# Tue, 01 Mar 2022 02:55:05 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:55:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:55:06 GMT
EXPOSE 6379
# Tue, 01 Mar 2022 02:55:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3baeb8c34a522fc616f97412d47dc1f665e93552c57aa8237ee1d673f9757cba`  
		Last Modified: Tue, 01 Mar 2022 02:12:25 GMT  
		Size: 29.6 MB (29632966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e222b179bbb0acbf2f7ffc214bd6b2f2d76459286de94dc6f0e3e96d589aaac`  
		Last Modified: Tue, 01 Mar 2022 02:55:41 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed990efcf77af511092f3ec397827b82b371607083d405be1c4be9b0717c33`  
		Last Modified: Tue, 01 Mar 2022 02:55:42 GMT  
		Size: 1.3 MB (1330927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60cd83854738cb31dfd7dc0fc77f11f1731064408e8e4285c65d96b30bd6c55`  
		Last Modified: Tue, 01 Mar 2022 02:57:01 GMT  
		Size: 7.6 MB (7639144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189081f48e46b2183df2f3d25aad99a21998277254b392ac573b7622df9fa66d`  
		Last Modified: Tue, 01 Mar 2022 02:56:56 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35a87a61a3bc79cfc06d9ab49524c82660da13bb2ed1d86fffdd24afc13510c`  
		Last Modified: Tue, 01 Mar 2022 02:56:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; ppc64le

```console
$ docker pull redis@sha256:a40d5758da4db23e41cae74c6ce5033f6a847ed41eb94ebc7284d761968a49a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44437723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71252688e95fdccd4268a77ad5bb8098761c9a3974644262fd96511cd04bfe70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 26 Jan 2022 01:46:51 GMT
ADD file:c03f34c221e57fa5cb625c166d1db9f72d6ba2fa17a3c41a5d04d6875d098949 in / 
# Wed, 26 Jan 2022 01:46:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 21:34:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 26 Jan 2022 21:34:28 GMT
ENV GOSU_VERSION=1.12
# Wed, 26 Jan 2022 21:35:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Jan 2022 21:42:23 GMT
ENV REDIS_VERSION=5.0.14
# Wed, 26 Jan 2022 21:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Wed, 26 Jan 2022 21:42:28 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Wed, 26 Jan 2022 21:45:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 26 Jan 2022 21:45:07 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 26 Jan 2022 21:45:10 GMT
VOLUME [/data]
# Wed, 26 Jan 2022 21:45:13 GMT
WORKDIR /data
# Wed, 26 Jan 2022 21:45:14 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Wed, 26 Jan 2022 21:45:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jan 2022 21:45:19 GMT
EXPOSE 6379
# Wed, 26 Jan 2022 21:45:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3149ee4a73508a4c39107d64a3fdc1b021626a22a0ac95e62fa0cea49ab77fba`  
		Last Modified: Wed, 26 Jan 2022 01:57:01 GMT  
		Size: 35.3 MB (35273030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa0f54bff7d41fc2e380fb414edafeaa3f1a92698f7d654ff7b37071b559f1`  
		Last Modified: Wed, 26 Jan 2022 21:46:43 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1352495caa97dcf9904ebf682ccac1c8401bba694dae97d80b65004b18a516b0`  
		Last Modified: Wed, 26 Jan 2022 21:46:44 GMT  
		Size: 1.4 MB (1361371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e5b4f9760c55ee4fb99254c9edd37bd70ca76d4977c18b1409901b61710e72`  
		Last Modified: Wed, 26 Jan 2022 21:47:49 GMT  
		Size: 7.8 MB (7801044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfee1b96120a55c883801025fa6391e480897d8d179333bc1950b7c1c64363`  
		Last Modified: Wed, 26 Jan 2022 21:47:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eff7abcd90561832e573f2e3838035f0ccf56e1ebf0dca6cfd4db3da9dac2a`  
		Last Modified: Wed, 26 Jan 2022 21:47:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-bullseye` - linux; s390x

```console
$ docker pull redis@sha256:66aaf6ef9b2572d49fac4475bdd7e78ffbe475facac8b08afa760a22a4afab44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38685694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddc2a765b7dd6d5810368dfbc025e852532c68423a02b3dc0bd8773ef46deee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:56 GMT
ADD file:d869ad3392a4e752c2f73d08a4cc13594c94bfc050bd037db0ca9827a0207072 in / 
# Tue, 01 Mar 2022 02:01:58 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:27:01 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Tue, 01 Mar 2022 02:27:01 GMT
ENV GOSU_VERSION=1.12
# Tue, 01 Mar 2022 02:27:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 02:30:39 GMT
ENV REDIS_VERSION=5.0.14
# Tue, 01 Mar 2022 02:30:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.14.tar.gz
# Tue, 01 Mar 2022 02:30:39 GMT
ENV REDIS_DOWNLOAD_SHA=3ea5024766d983249e80d4aa9457c897a9f079957d0fb1f35682df233f997f32
# Tue, 01 Mar 2022 02:31:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Tue, 01 Mar 2022 02:31:13 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 01 Mar 2022 02:31:13 GMT
VOLUME [/data]
# Tue, 01 Mar 2022 02:31:13 GMT
WORKDIR /data
# Tue, 01 Mar 2022 02:31:13 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:31:13 GMT
EXPOSE 6379
# Tue, 01 Mar 2022 02:31:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f81abce72636770dac4258df46a31beeb6ad81dfddd5b7c9c3fa6942ea074922`  
		Last Modified: Tue, 01 Mar 2022 02:07:33 GMT  
		Size: 29.6 MB (29647132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3943f5266f6b9d89d1d57546c5d4672bcd1b3f73095ea00bba99a4ecf1623a5d`  
		Last Modified: Tue, 01 Mar 2022 02:32:48 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93bebfc36b194a07470e8b630ec72f6e6882f8a1854371fd4008ce657ebdd37`  
		Last Modified: Tue, 01 Mar 2022 02:32:48 GMT  
		Size: 1.4 MB (1429226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcaf0ea2af8b2f125d2cde5660ac54a6a291edae1ed18e816a3767295ecaffa1`  
		Last Modified: Tue, 01 Mar 2022 02:33:49 GMT  
		Size: 7.6 MB (7607065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a0bd0e5b663e5d6cdc0d51c8e384dcb6f619b8112e0a70deb21cbb3224b139`  
		Last Modified: Tue, 01 Mar 2022 02:33:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60aa6aa7bfb92b4ad462c456009ce1eec07a8dc12a2f4171b4dda8ee369378`  
		Last Modified: Tue, 01 Mar 2022 02:33:47 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
