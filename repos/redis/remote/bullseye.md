## `redis:bullseye`

```console
$ docker pull redis@sha256:065ed8e1adfd56ffbb9bea845538cddda573b35c5cc24501388c90208b540595
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

### `redis:bullseye` - linux; amd64

```console
$ docker pull redis@sha256:54043f92c16727f142fa93c377b279f91879abf974c244ce72099b35fefbd7b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42456481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd647f2d808bd524e67f3c6ce259d9fb1ba159ddaf91b8cefb3e740c9499b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 06:08:58 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Thu, 09 Feb 2023 06:08:58 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 06:09:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 01:56:25 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 01:56:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 01:56:25 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 01:57:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 01:57:13 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 01:57:13 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 01:57:13 GMT
WORKDIR /data
# Wed, 01 Mar 2023 01:57:13 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 01:57:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 01:57:14 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 01:57:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac509f65c3e925781d771dc15fd63c2bd795abdc461f29bd9a3acd0a19f65d3f`  
		Last Modified: Thu, 09 Feb 2023 06:12:23 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51afc2cce3dfa745f19f601b33820e4a960311cd81b0a6a816b1de8e5ae6d7d7`  
		Last Modified: Thu, 09 Feb 2023 06:12:23 GMT  
		Size: 1.5 MB (1462938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e0fee18c680be6f957adeec5abbce93d95cfa923f86101d0fcb17f6692fbab`  
		Last Modified: Wed, 01 Mar 2023 02:01:46 GMT  
		Size: 9.6 MB (9579292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4c8dcae6afbf5fc1ccc4954e85509da27002cd86e54c8b793e0eb3eec06ecd`  
		Last Modified: Wed, 01 Mar 2023 02:01:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d285bc8f049a0ec5a43b90b8d141b78a87783417177b89e7d8351f022b1ecfcf`  
		Last Modified: Wed, 01 Mar 2023 02:01:44 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; arm variant v5

```console
$ docker pull redis@sha256:4a80155ba27b0e798d6bbee7d31d02595c2f6902c7a6e51d0c87453914ba519f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39742693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76670f50539990dac4ee5a4a48049383436cc902d6f830c514109f7c8ebcdc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 01 Mar 2023 01:48:54 GMT
ADD file:b4fb1081f6eb8a0560d56d5781bbcedaac1453615d56e0943245dca784785ea2 in / 
# Wed, 01 Mar 2023 01:48:54 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 06:41:52 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 01 Mar 2023 06:41:52 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 06:42:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 06:42:09 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 06:42:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 06:42:10 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 06:43:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 06:43:07 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 06:43:07 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 06:43:07 GMT
WORKDIR /data
# Wed, 01 Mar 2023 06:43:07 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 06:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 06:43:07 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 06:43:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3c3af56dbec5913ef8aec0f1ca7112eb5914b4ad346ccd48f836dd7ec0621ba5`  
		Last Modified: Wed, 01 Mar 2023 01:52:57 GMT  
		Size: 28.9 MB (28915776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79c1782b6c609d8355540f965d766de8594752c235d72d7ab276fafa8c86b01`  
		Last Modified: Wed, 01 Mar 2023 06:45:57 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f7182cd715403fee5325c2da95bab39e2937182dbe5daecfcf39d0d28b8749`  
		Last Modified: Wed, 01 Mar 2023 06:45:58 GMT  
		Size: 1.4 MB (1439937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3533e32a62fc7aade8390808753e6429807e84bf2f19978fb8acf58eb54836a`  
		Last Modified: Wed, 01 Mar 2023 06:45:59 GMT  
		Size: 9.4 MB (9384547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c1b5b7346e285653b835a321de60d97328e8af14c8a29982c91407663ce198`  
		Last Modified: Wed, 01 Mar 2023 06:45:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179ab6d6b5afa4e8a002b3f546ba9be39a8121ab9726e5a4b285d444569fa8e`  
		Last Modified: Wed, 01 Mar 2023 06:45:57 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; arm variant v7

```console
$ docker pull redis@sha256:f53021ec9d8145e690d301ddac6c16b88e35d477f45b5d801ecd8d3158de46f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37227956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d2a5dc5925f63abe927bb2a1e707a49de2677abab25632c32617cb743db567`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:07:42 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 01 Mar 2023 01:07:42 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 01:07:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 01:07:55 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 01:07:55 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 01:07:56 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 01:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 01:08:39 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 01:08:39 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 01:08:39 GMT
WORKDIR /data
# Wed, 01 Mar 2023 01:08:39 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 01:08:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 01:08:40 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 01:08:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237d7d750cf2442f340c438ee52a68bb5577160089370ab7cdab98dc581c72bc`  
		Last Modified: Wed, 01 Mar 2023 01:13:46 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3251f1ecd3c3ad6cf1a35105204e8c0942507e7f461faa4aa77ccdafbe15d5b`  
		Last Modified: Wed, 01 Mar 2023 01:13:46 GMT  
		Size: 1.4 MB (1431020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295e6eff4a1b8a2978cfdc55d83adf62087404a1f3b86c05fa7b6e1ac839c5d5`  
		Last Modified: Wed, 01 Mar 2023 01:13:48 GMT  
		Size: 9.2 MB (9216830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7be9db453d2b29b3b0bb5a5d3d4443da15f3a7df8f3aafceb667b71098a552`  
		Last Modified: Wed, 01 Mar 2023 01:13:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0186f934150a226965bc0af128b7792ebdcd77d5d823367096a5cb6ce68a5f`  
		Last Modified: Wed, 01 Mar 2023 01:13:45 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:0ef8e71166deef5fd1b5dcde6348bace84dfb9466c9dd5e64a4e1f8a73bc5e57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41058851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0504109b2e19a4314cfd3f5be3c319b46c33de3c05d32e32214a378beb8f14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 08:14:00 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Thu, 09 Feb 2023 08:14:00 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 08:14:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 01:58:18 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 01:58:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 01:58:19 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 01:58:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 01:58:58 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 01:58:58 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 01:58:58 GMT
WORKDIR /data
# Wed, 01 Mar 2023 01:58:58 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 01:58:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 01:58:58 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 01:58:59 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ad00da4bdab78010a424d0031db69b2ef92ade14a7310720938aa418f2c5c`  
		Last Modified: Thu, 09 Feb 2023 08:16:56 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf81d284940808950d9ca22ed2da84316220418c67f026ce6f786a6ceae94ae`  
		Last Modified: Thu, 09 Feb 2023 08:16:57 GMT  
		Size: 1.4 MB (1394544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1847a169588cb826b2f556cf000cc73f7e859364382ac2fde3a8a31341e02cb7`  
		Last Modified: Wed, 01 Mar 2023 02:02:56 GMT  
		Size: 9.6 MB (9599353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874a3939a50fc5bfb7cf4f5b446a0154044295c763d2f051e0304d5de538f05d`  
		Last Modified: Wed, 01 Mar 2023 02:02:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41f2deb9499a81cd04f53050378fee3cd80dd1fd959c995f4efefcbcd4112c4`  
		Last Modified: Wed, 01 Mar 2023 02:02:54 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; 386

```console
$ docker pull redis@sha256:59b44fa4212944543262ccc0227232d24ba8f661aca5b8611379f444fcd8b14e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42988307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dfe6ce2dfb6062e632dbf6bcf6723214a10a77dbbc98c618d89220a907229d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 09 Feb 2023 05:12:53 GMT
ADD file:7740abd3129d33122ce51153c0b6c3323b9cbe9ea0e81672e16b2d7b210d24e3 in / 
# Thu, 09 Feb 2023 05:12:53 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:02:14 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 01 Mar 2023 01:02:14 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 01:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 01:02:28 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 01:02:28 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 01:02:29 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 01:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 01:03:42 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 01:03:42 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 01:03:42 GMT
WORKDIR /data
# Wed, 01 Mar 2023 01:03:42 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 01:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 01:03:42 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 01:03:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:20744f4988404b1dee2cd438157b288d16a89da472583c0f04332ed389b258f8`  
		Last Modified: Thu, 09 Feb 2023 05:18:42 GMT  
		Size: 32.4 MB (32396875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6319b74c2ccc4ee923add04bc3c88f6e95d8d9c664367692e19bbd5d66103915`  
		Last Modified: Wed, 01 Mar 2023 01:11:14 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af698fa07b6d81e307eac2ae202606af193148fa33b1047e98865629ee7c45c`  
		Last Modified: Wed, 01 Mar 2023 01:11:14 GMT  
		Size: 1.4 MB (1438537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca998809b4fa7b580210599b9d4671db2837800bb3b9e87b998be057b53c1cfa`  
		Last Modified: Wed, 01 Mar 2023 01:11:16 GMT  
		Size: 9.2 MB (9150459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07de7500d951de2cd108cea4c21f582f00fe90098198e8b446b79043e612517f`  
		Last Modified: Wed, 01 Mar 2023 01:11:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b2d5c69e3ef6e044eb0e2f6778ca3f51519c3972bf5b34f03768ac82adbd25`  
		Last Modified: Wed, 01 Mar 2023 01:11:14 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; mips64le

```console
$ docker pull redis@sha256:4d2565624ca65526608d7bc8259b33e49f81ead3be2161486043564e7e3e21fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40771591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d502e34b3ddc60e1a829b453c88ff5c018723a2db8f70052cb2140b55036ff8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 01 Mar 2023 02:10:54 GMT
ADD file:0bcd66a6a099cdb6e018ddc0f00270be93dccd3be6167ce36e9efc99c31549d9 in / 
# Wed, 01 Mar 2023 02:10:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 12:47:01 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 01 Mar 2023 12:47:03 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 12:48:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 12:48:06 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 12:48:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 12:48:11 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 12:52:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 12:52:32 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 12:52:35 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 12:52:37 GMT
WORKDIR /data
# Wed, 01 Mar 2023 12:52:39 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 12:52:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 12:52:44 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 12:52:47 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:89f6b45a7afd174bf0d443156831cacd9e6a26c834ad62610b6db53c731d257f`  
		Last Modified: Wed, 01 Mar 2023 02:18:50 GMT  
		Size: 29.6 MB (29634488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140bb94d43448f56789a9b1c954c0ed0bddaf39739d8ee0a40aa47a2801e2658`  
		Last Modified: Wed, 01 Mar 2023 13:02:05 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba561d82fcad2228d630659c5600b3a96acfd564f7cc0dcef89fe3e4a4d46ef`  
		Last Modified: Wed, 01 Mar 2023 13:02:06 GMT  
		Size: 1.4 MB (1350459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199019ada87fb07bb23437b1a1f1921d7da43d3c3c549c699c1ceb9ce8a46bac`  
		Last Modified: Wed, 01 Mar 2023 13:02:12 GMT  
		Size: 9.8 MB (9784357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764490f9771ccd6a7cf8963f0cc5d4c3f611c5107db952427b062e4794ed602c`  
		Last Modified: Wed, 01 Mar 2023 13:02:05 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31245c2e8b9f008150e5b176e4c9247d645cd81befb5dc2ce0a56a76b068e586`  
		Last Modified: Wed, 01 Mar 2023 13:02:05 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; ppc64le

```console
$ docker pull redis@sha256:0692cd8f9c044c48754cc989584fbdc77ca7d9464ed99b631e1e8ff19530568b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46766208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2b071d97d82fafc93c2c0e080bf07688e9932dd01938d03c21f5ffc0ca399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:58:47 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Thu, 09 Feb 2023 09:58:47 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Feb 2023 09:59:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 01:03:41 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 01:03:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 01:03:41 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 01:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 01:05:17 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 01:05:18 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 01:05:18 GMT
WORKDIR /data
# Wed, 01 Mar 2023 01:05:18 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 01:05:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 01:05:19 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 01:05:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e823a80ccc7f3394fc74d43b40fe3f5dcdce6c9954689d80240f7b2a509fa0ba`  
		Last Modified: Thu, 09 Feb 2023 10:05:59 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e013f9f8a7c86c34325ce22af155f092fd5d456420ccf7ac3e8f5d1426666b2`  
		Last Modified: Thu, 09 Feb 2023 10:05:59 GMT  
		Size: 1.4 MB (1385256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b41590803bc2c71390025db7651b99ccdb501046748e74ef69114374c6daee`  
		Last Modified: Wed, 01 Mar 2023 01:13:09 GMT  
		Size: 10.1 MB (10089255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a0a60b8d350e383801c33d00cadcf58209c29bdb9c5bedb744b2a6ab09a76`  
		Last Modified: Wed, 01 Mar 2023 01:13:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c723046ca8319e698c66503db833097db02a64888c761b5eb70dc8c8280e71fa`  
		Last Modified: Wed, 01 Mar 2023 01:13:06 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:bullseye` - linux; s390x

```console
$ docker pull redis@sha256:fe8c59e6882f74f3250e0a284e27b368a1a9c06539e9713a4f6c8c49fc2b6392
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40944671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df23fc1984ff81f472a4cd4c50a342d7c3dcea6827c53eda60e93f36f86205fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 01 Mar 2023 02:50:30 GMT
ADD file:01aa3de7444f0716938e0d85522be065193be4ffb6788b3190a0f4fefdbb8d65 in / 
# Wed, 01 Mar 2023 02:50:31 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 09:54:18 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Wed, 01 Mar 2023 09:54:18 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Mar 2023 09:54:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Mar 2023 09:54:27 GMT
ENV REDIS_VERSION=7.0.9
# Wed, 01 Mar 2023 09:54:27 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.0.9.tar.gz
# Wed, 01 Mar 2023 09:54:27 GMT
ENV REDIS_DOWNLOAD_SHA=f77135c2a47c9151d4028bfea3b34470ab4d324d1484f79a84c6f32a3cfb9f65
# Wed, 01 Mar 2023 09:55:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Wed, 01 Mar 2023 09:55:09 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 01 Mar 2023 09:55:09 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 09:55:09 GMT
WORKDIR /data
# Wed, 01 Mar 2023 09:55:10 GMT
COPY file:e873a0e3c13001b5e1c63f9dbe60cc65722af522671787f68b8e8cbcae7d02ac in /usr/local/bin/ 
# Wed, 01 Mar 2023 09:55:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 09:55:10 GMT
EXPOSE 6379
# Wed, 01 Mar 2023 09:55:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7b8d78f42e32e7fa234bcf890ae6603acab2881bca68a9d8c429981c7f42b1d6`  
		Last Modified: Wed, 01 Mar 2023 02:54:48 GMT  
		Size: 29.6 MB (29646854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacaecb7810b426cd935c67439b36f49896044d3bbf9dde03f6c59e8a73b49ad`  
		Last Modified: Wed, 01 Mar 2023 09:58:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfce39ed1f9268eead6e28ffa1569119967e13aec59f682f6c5bfb10a4b6d3c`  
		Last Modified: Wed, 01 Mar 2023 09:58:23 GMT  
		Size: 1.4 MB (1428281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587d3f0947669602481e4e9d354372040a7ed912e0f839a87e017f83afcf8500`  
		Last Modified: Wed, 01 Mar 2023 09:58:24 GMT  
		Size: 9.9 MB (9867094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48397bf4e5142deaf4b467709eba30ec40bf16417215428716bb300f03b88552`  
		Last Modified: Wed, 01 Mar 2023 09:58:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3676c9e3c87f6d9ad06e22d22c356bc430ebad61373922eabd3ade47a004049`  
		Last Modified: Wed, 01 Mar 2023 09:58:22 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
