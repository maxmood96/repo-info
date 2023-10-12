## `redis:latest`

```console
$ docker pull redis@sha256:cacfe1d34dad1b12708dedff1d20b3bb448b87df50ee770010e56eff0782c0cb
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
$ docker pull redis@sha256:28aa338c21f38494f6ce55dd3dba3b96f00f7da4a84f273c801a685dbfd66d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0542ad1e7734b17905e99f80defc1f0a7748dd6d6f1648949eb45583d087de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75410c1f8b4830146d79153b677a7ad05acc0d806394ade9bc99b74b8d2f5c`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667874757cc14509db1ff8dc204c80802123cbaa8b40c4a85bc5ba5f63b3161c`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 1.4 MB (1439899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150b93d249d2e2452a04f3e6cdc5d360407f6e4865fdd7f8ee65da99f945fb8`  
		Last Modified: Wed, 11 Oct 2023 19:01:34 GMT  
		Size: 20.8 MB (20835618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c83735e284f05034aed569d607687e904f323bb051a9efc39e8be0bb9533b`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa899a007ab2c3778a4aca2b9cae642930b50bea94b54eaf110df004f78cd2e`  
		Last Modified: Wed, 11 Oct 2023 19:01:32 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:bb2437e4c53d0d898bfd399601e1e23dca2ee2afcf3acfddc6822c5a45927ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2895047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece259f95fda286c2b43e385eb555e586575d3b19dfe9e62c6ebbafae04ff42`

```dockerfile
```

-	Layers:
	-	`sha256:d9a56db828b285f996af40acead2c4b7dc198c4648a1bf2da29f54d9aa010b5d`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 2.9 MB (2865613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b9cf720b9e64d5196e13e20777f8ee01650a7d06e77660f9cdc17d77653c39`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 29.4 KB (29434 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:4005f2e960b1f79d7be4deeff9cbb4e6cc7986f93bfa0f9bbe43a90e82266b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47516497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90e0a044042b22a5fbb31cf426497f34f1bbfb2c2f8776c1919ef0fd61f9787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:8c43adb3245fc6f2b10aa5a86c850db5dcf3515eaf7e46630922fe21f806bd2a in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:904e6393ef1ee28b37171369eb4f7cb04714631c711799819fccb83886bd212b`  
		Last Modified: Wed, 11 Oct 2023 17:40:47 GMT  
		Size: 26.9 MB (26922150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce2054d07ed58033f19085bd13f4611a7c16da409796785d4cc36439d07b952`  
		Last Modified: Thu, 12 Oct 2023 14:16:55 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601aa7f481958ba6c2619971775bf28dbdd0fe90efc8bdeaedf245ea299b0c5c`  
		Last Modified: Thu, 12 Oct 2023 14:16:56 GMT  
		Size: 1.4 MB (1417760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b388e4d276dd8fb91868a0da753e05e79d599efedc3166f450affcad40929091`  
		Last Modified: Thu, 12 Oct 2023 14:16:57 GMT  
		Size: 19.2 MB (19174783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160fe505d13d10a40c38daaed9f5d2dc6310b7931bad81dbc578c92bfb8cfd5f`  
		Last Modified: Thu, 12 Oct 2023 14:16:55 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f10a6f100eb47326aef081d2bb7d87a81e7bf1d7fb8382c0eb38c9770e918a`  
		Last Modified: Thu, 12 Oct 2023 14:16:56 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:739ea18f6464810a585c9e61c81f05caab3b6c0f5c169aa43413979d762ae59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 KB (29193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92be0a41060972abaaffa873d169fc7d74f54698b2facc9bca92c4535478473`

```dockerfile
```

-	Layers:
	-	`sha256:06695bd57af0b92ac65bb2385768831b9e1d28ac6883f54ac76842283e35580b`  
		Last Modified: Thu, 12 Oct 2023 14:16:55 GMT  
		Size: 29.2 KB (29193 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:50bb2a92eb7c0e98a7aff350802394059ae145f93f9f3f14ee8f04d9e2299b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44756747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bfda8bc2f4657e9420b596b10401d39cef5bd772656ac622b7361533fec3e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670e91b1de7bdea8ad830648230fc9cce53bfd34e1e562991ee97c58a782198e`  
		Last Modified: Thu, 12 Oct 2023 21:42:29 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f848b34a64d32c9c571e7d7478d9adc5c1d15af6d3f5df2e4da6f4dcd91a4b3`  
		Last Modified: Thu, 12 Oct 2023 21:42:29 GMT  
		Size: 1.4 MB (1408347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9787dcd432c5901826bd88c1d71e1a4c7fc0bb5057117412ff2a4b5bc1ba198`  
		Last Modified: Thu, 12 Oct 2023 21:42:31 GMT  
		Size: 18.6 MB (18597669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf933e50814817d1ae0c322004e4131f4274af56c1e91d56663ef8a70c94df7`  
		Last Modified: Thu, 12 Oct 2023 21:42:29 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3222ca733d08c5affe342f598841ddd115d7d5b319ab4f2eb14ea1106e544147`  
		Last Modified: Thu, 12 Oct 2023 21:42:30 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:d16d5cd1a3dba51337b6c7890e498ba7104e174d7da2709f4866b9bed17d232a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f836426582cb039b0322a4510306fdcad158ba9d22780a35a933de87116e69f5`

```dockerfile
```

-	Layers:
	-	`sha256:a0f64935ad32c9d42627add89053dcaaaa35bbfc0880cb743cdff031c5848c98`  
		Last Modified: Thu, 12 Oct 2023 21:42:30 GMT  
		Size: 2.9 MB (2852552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71ebb2d7893c78545beaa6ceb9e447409e548f7ac00136b5d3695ab84fe92cd`  
		Last Modified: Thu, 12 Oct 2023 21:42:29 GMT  
		Size: 29.4 KB (29407 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d5d5ebe54a83171fa73ecb5a5dee94d9e2b9eb7b5d509ea5714e64087906368f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50410504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886b7ab5a9b5fbafb43ec484973b824c969f686dfcb4dcf44654fb5eec3d697c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc70419cf2a347b5ebf78157ad472716792a147dd21971182ace25710f41cd7f`  
		Last Modified: Thu, 12 Oct 2023 20:08:24 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7288668abaf49af93254bc6f207b71ea884315c295a0ba0db8f46636526a199f`  
		Last Modified: Thu, 12 Oct 2023 20:08:24 GMT  
		Size: 1.4 MB (1372439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffbe1d1e9d6b33eee938348fb19d10190d0202e1b6f38446b8a38116924d269`  
		Last Modified: Thu, 12 Oct 2023 20:08:25 GMT  
		Size: 19.9 MB (19856978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beecd2985ee6ed3fe7139df66fb877fad9f86360d361ff04f8a3e5f9132c2366`  
		Last Modified: Thu, 12 Oct 2023 20:08:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4310bc5368cac9f13acaa745ad051ee102c13f460f698d97aa5a455c3fb709`  
		Last Modified: Thu, 12 Oct 2023 20:08:25 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:a55cb3dfad8a723abfacf1c878a36b1e9442003561a80e12d0951abaa27add42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f380c3f1c33151137bd78aa254ffe0277d2d4b797a0e8ddb507883344766449`

```dockerfile
```

-	Layers:
	-	`sha256:3366a8025d6696934bf6bc9299308a60e35bfc6e1567fb716e63279c293de8ae`  
		Last Modified: Thu, 12 Oct 2023 20:08:24 GMT  
		Size: 2.8 MB (2847126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6942fd69a01e95f9eb574cda9178bd27f3ae1f1382624c40629f2e44ebfc96a4`  
		Last Modified: Thu, 12 Oct 2023 20:08:24 GMT  
		Size: 29.3 KB (29285 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:31bd1568369d7a1a70efa89fd583a228c824c591e7c78e09d906413839456d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51489138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a7eac6c602d851b9d35fb663670a4f9f57233af2ccff2b53357c13b0318990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:31318c1b1f05d559cce42f5b12eef97d916932217e0b987fb07c0fc11bf0a14a in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b27d0f1369837277a82877763487cdd2535037988fc27e16f11cf74e103ae4cd`  
		Last Modified: Wed, 11 Oct 2023 17:45:31 GMT  
		Size: 30.2 MB (30164118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75410c1f8b4830146d79153b677a7ad05acc0d806394ade9bc99b74b8d2f5c`  
		Last Modified: Wed, 11 Oct 2023 19:01:31 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264d0ea5ef2f547bfe93bc46418f5481e586cbf7031765d8d0238875bb6fd24`  
		Last Modified: Wed, 11 Oct 2023 19:02:25 GMT  
		Size: 1.4 MB (1416424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a21ba994132969d0729929cf7c12c8f9cc5e58cbc15aea1b8b9918e05ed9248`  
		Last Modified: Wed, 11 Oct 2023 19:02:27 GMT  
		Size: 19.9 MB (19906794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b4743ffdf147295259b5332ab31351bc5b2ed4bd0a366f7cd9fb32487ebd0`  
		Last Modified: Wed, 11 Oct 2023 19:02:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c508d356c66ab091e1b0f8aeac6fd13392ce328d33e1675dce4d142416549c`  
		Last Modified: Wed, 11 Oct 2023 19:02:25 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:1212d27db058c59f64fa8204ca2449e82e19d424bd51c871e3add6ceafecea83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 KB (29164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92aebea2af06d3873e19ade34dfee9fc08c14239fe946bec02f0a51ff64b5c`

```dockerfile
```

-	Layers:
	-	`sha256:e7269dfa2c9c2ff8ec1fde1321f1e4055fafe2198a951743f3e9699aaf333067`  
		Last Modified: Wed, 11 Oct 2023 19:02:24 GMT  
		Size: 29.2 KB (29164 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:5972d9afdcf76c6c20d97811f5a7f69cf1940e34d5f281c48155fa3095e4ed40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56500185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d48628c5a89e6ace8455dfc447e4693d811eeb8b2da811d037d337a95717b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:850547a08e38ebc5a3659df86e70039a8d9828ae26ae485b077c98a959248dcb in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0f581c6294fe7421dfee024e2c7dddd73ef3fbd7ff23b05bc3c1bf9f50885e85`  
		Last Modified: Wed, 20 Sep 2023 03:20:59 GMT  
		Size: 29.1 MB (29121674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d44a2ed54cccb98e0c8d8bfd3e9348ee3a0bf1428969f7a2c62fe9a0972d5d`  
		Last Modified: Tue, 03 Oct 2023 23:05:50 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa00742665f7e553b3bc45e87c03bd98bc4da28e1f5bfda6e8789427814cee`  
		Last Modified: Tue, 03 Oct 2023 23:05:50 GMT  
		Size: 1.3 MB (1324116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba13329995a4529e131930d11af821e0c03d1329576c068f613ebb3fee309468`  
		Last Modified: Tue, 03 Oct 2023 23:05:53 GMT  
		Size: 26.1 MB (26052597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed5d403365cf084baf61edef65d6736c7c696aeee49bf9b51c02864eb539b74`  
		Last Modified: Tue, 03 Oct 2023 23:05:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772d7570c390780b55ed8dbc2593254efd11bf1c8911ee8e352722fea09c33ab`  
		Last Modified: Tue, 03 Oct 2023 23:05:51 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:071c90d898c9abc5d3a2cec22d88f289a4d306d00633d7f028c4c434b8e81ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 KB (29154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adce51c1deb33c8d58cc86c84fe80637254738f908824fa803dc67cde3e44693`

```dockerfile
```

-	Layers:
	-	`sha256:fd5d5a8662e63cfc9c1a67e74512bc1a4e79b2dc4bfcbcc53f3d5c6d8f67ba8a`  
		Last Modified: Tue, 03 Oct 2023 23:05:50 GMT  
		Size: 29.2 KB (29154 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:843ed83e9b61ce98d0d5c7997e413f84aa21337aad9a2f1d0d6a500648f84ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63006835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee3a12f4fdfb64b4c326d8cb5471a63cb9b929a34052445f407bf6afa8a203f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:9a37b479e68a0d18babbef8dd04d09a0e6844a0080876d14144a34bfd9d0897a in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:696a66e961f2033dcf69b003ad7faf28ed2248da58efa1c08a9d496739a8eeeb`  
		Last Modified: Wed, 20 Sep 2023 08:49:51 GMT  
		Size: 33.1 MB (33119461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a5e143415842a5f669709af637faa5a01610f07493b4465e9dd6acf35e33fb`  
		Last Modified: Tue, 03 Oct 2023 23:02:37 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a8c07cdef0780ba543dc1c5271114516e2654b4927b012c80217e3654d4d1c`  
		Last Modified: Tue, 03 Oct 2023 23:02:38 GMT  
		Size: 1.4 MB (1358927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d135571fcd0043cfb676f8366d34a0e087f635634bd92e887ef11c3ee77888`  
		Last Modified: Tue, 03 Oct 2023 23:02:40 GMT  
		Size: 28.5 MB (28526642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3677e8b31440a9fce03dc8a94637f5a3818f5e80a308df78abfdd32b47e1439`  
		Last Modified: Tue, 03 Oct 2023 23:02:38 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e78a99561925da9f9c49fdc4c799ccb137c5d248326e41c991d5086c6d845e`  
		Last Modified: Tue, 03 Oct 2023 23:02:39 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:478b5d69ed06c55d81b95e8c883c268466b995697d723d236543da81c7085bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2898467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40221f3907041cdb8ed9691da6ada2993068f206f0c7ea5fbc788bd27454f2e3`

```dockerfile
```

-	Layers:
	-	`sha256:cadf019405d4d49523a2ecb00ed53e7ad2fe384f4b1ece330e99e811f047aac1`  
		Last Modified: Tue, 03 Oct 2023 23:02:38 GMT  
		Size: 2.9 MB (2869132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a792d7d262ee2709fafb5cec29b9bb23ead43889de5bfc133f28cf3e0d879fd`  
		Last Modified: Tue, 03 Oct 2023 23:02:37 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:4f99b355cbcc64766db9e7a99a2f2dcc98d5a5a37ac12ea263c87af41a4a0d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53547945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e8b4be815efd8397d633e210a10d49cdc1c23bfefdbdf041781b589023297e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Wed, 06 Sep 2023 21:03:16 GMT
ADD file:6ed982ad3e8566d63315a27a81b33069910952aef4b2d3e0b607bd2caeac7ca4 in / 
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["bash"]
# Wed, 06 Sep 2023 21:03:16 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV GOSU_VERSION=1.16
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_VERSION=7.2.1
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.2.1.tar.gz
# Wed, 06 Sep 2023 21:03:16 GMT
ENV REDIS_DOWNLOAD_SHA=5c76d990a1b1c5f949bcd1eed90d0c8a4f70369bdbdcb40288c561ddf88967a4
# Wed, 06 Sep 2023 21:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
VOLUME [/data]
# Wed, 06 Sep 2023 21:03:16 GMT
WORKDIR /data
# Wed, 06 Sep 2023 21:03:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Sep 2023 21:03:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 21:03:16 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 06 Sep 2023 21:03:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:26dcff366e33abcf08b812052a4c12496aa406aa267655e984aa7a84ca254cd8`  
		Last Modified: Wed, 20 Sep 2023 02:59:47 GMT  
		Size: 27.5 MB (27489966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98793b8f09c9ffcfade45e13946ac7a76a944ca573ead98a5554d3f8926dd6b9`  
		Last Modified: Tue, 03 Oct 2023 23:36:31 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7422a5babea5a71de43f5cce871efed4ceccf350cd2b85f8934ca20b47a7e0`  
		Last Modified: Tue, 03 Oct 2023 23:36:31 GMT  
		Size: 1.4 MB (1401400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40656bdaeb66134712a28da5d14a8e38796929fe2a67914ed8f9281b16f2aead`  
		Last Modified: Wed, 04 Oct 2023 00:01:34 GMT  
		Size: 24.7 MB (24654777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab2b899997da6c3b91f828692a9db89a58b487623547f414a4944f53ce640f`  
		Last Modified: Wed, 04 Oct 2023 00:01:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4b44d973a2d66a95318271fd479259f5e6bcc45ae8b3131ed743d7aae89190`  
		Last Modified: Wed, 04 Oct 2023 00:01:32 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:f18cf80411269f4c68497bca128cfc5aa9b93e335e64d7922447c5a63af1ec75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3424f99ec99d0dddc93d29dd0fe9edadb2a51edaf1e12fd97a09f98cd8417ac2`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1edb9912cffa07c6babbdfabd11726350577edc45b87ccd0f12e0183b1b01`  
		Last Modified: Wed, 04 Oct 2023 00:01:32 GMT  
		Size: 2.9 MB (2851623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cafb95bcc438fe54a401a79ecbf7f1f9e1add16c67653448222a4c67ffb7437`  
		Last Modified: Wed, 04 Oct 2023 00:01:32 GMT  
		Size: 29.3 KB (29267 bytes)  
		MIME: application/vnd.in-toto+json
