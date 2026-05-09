## `redis:7-bookworm`

```console
$ docker pull redis@sha256:1ca537d80c33a9fbe1c18732cd7414f67918921b4aa64faa7a5a180e749a40db
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

### `redis:7-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:f99f6510ed39a92f36c94d3bbef168ac291dc7c8887ec9a2735f60996db9a4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43585633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70125e3902bec6b175663659b9e5770956501a04a7f2a3c0918d1744615fbc6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:33 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:35:25 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 19:35:25 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 19:35:25 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 19:35:25 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:35:25 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:35:25 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:35:25 GMT
WORKDIR /data
# Fri, 08 May 2026 19:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:25 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:35:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452a5de4f44dda923fc813ecacddcde7eec7289457bf541911f3c7c24bd3172`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a25297b00f67882951f8eecd11e8dd4d0ab882bbfe71f04865637168f95c0c`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b08f650ca7cc7aa7214a27c3ed30e0eb05578e77965a0527835e4baaa4bc528`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 15.3 MB (15346643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e2ff3290479a290d6504ba6559ca5084a45b27d5323bcf409d7fe70d6a5948`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa83398dd5663956c9ca5b24577559113ba3a3953395e42e3b3df9a98206528`  
		Last Modified: Fri, 08 May 2026 19:35:35 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:ed8ac7712aef7bf8ebe6c9d46c3c47738e19a4997ddf5c2d11b95dc7c3b9ec82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87319f17d81b495f292b7175d613f5b95f6d75620eea17834379187e1e7f391`

```dockerfile
```

-	Layers:
	-	`sha256:7bcf7124e3c9956e9bc9aae691ab79632c26146bcdeaa73110a380979b0b8c05`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 2.4 MB (2373040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2945c5e3f19686d0b07fc677ea9f927d2cd3a3963f3cff0a9fac8461e4490fc7`  
		Last Modified: Fri, 08 May 2026 19:35:34 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:70de59d874ee22a98cb509db4098913fc31b0ce36d9a7effc2c9556cd3683395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40830060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9deaab9b78038d79ec02be3725af49168d24bd2931237254e21aa36c79915d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:55:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 20:55:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:56:23 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 20:56:23 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 20:56:23 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 20:56:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 20:56:23 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 20:56:23 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:56:23 GMT
WORKDIR /data
# Fri, 08 May 2026 20:56:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:56:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:56:23 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 20:56:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845982a798997332a8af153924363fa91addc53a78b62f76a96b9d8c4d02a225`  
		Last Modified: Fri, 08 May 2026 20:56:30 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca67d2317156193c4369196426f9be78cb112e1c2febab7c9fb36afa9db7e462`  
		Last Modified: Fri, 08 May 2026 20:56:30 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83fd931453b881e7cb4e3baafdafc12d74e12524c8258f0c5dc445ede48e54d`  
		Last Modified: Fri, 08 May 2026 20:56:31 GMT  
		Size: 15.1 MB (15061681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18451a882d968d19532bada861f75ef30531951dc871238c65d40d90cca80747`  
		Last Modified: Fri, 08 May 2026 20:56:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070405d23ab4145dd99a3a3aab6861f21362087cfff53946f845dfbd5e39900b`  
		Last Modified: Fri, 08 May 2026 20:56:31 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:024f4ef15be759cbbc7d725eb2b62848da6fc55dcb8b54c4700b5b983b448654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2397ddcef14ae66868b6af8d7ee017207fca63c022dde0bdba047d8565327679`

```dockerfile
```

-	Layers:
	-	`sha256:219058b814e0a81207af030a544ae72ac001b23220455091071d19c96eea73db`  
		Last Modified: Fri, 08 May 2026 20:56:31 GMT  
		Size: 2.4 MB (2376860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d97f54f6535bd5b9c616dcffd25729a8ba0c2027b7ce869b8483f1b6617f082`  
		Last Modified: Fri, 08 May 2026 20:56:30 GMT  
		Size: 25.3 KB (25272 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:3e100b14dcd323ec9609400805ebe22af0554b81c083ac55d0429d63fc5bfd7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38663899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe63d88df6427d80a4b29e3872cc129c787d0e112ddc318faeaec82f1c50a5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:27 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:42:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:21 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 19:43:21 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 19:43:21 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 19:43:21 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:43:21 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:43:21 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:43:21 GMT
WORKDIR /data
# Fri, 08 May 2026 19:43:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:21 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:43:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75112e10cfbbf2484c0c6d445693302873c8b12c995f9760d89d0778a80b95c2`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f48d7af3824a1073a2eafb0adb7230c500da8b70a02644fd6d85abebb236071`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3560223bc4993473a5629663667cb7c05e1cdbc0ac2f3771cb36d0ec9fd92c2`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 14.7 MB (14719782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05af809719002a170b9dbf595adae7eedb23765ad6608f5cb039c4fdbbce5b6a`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447dde60f7fc9c76015cf8f549c8ccb76f5245342de6556faca776956efe3ae6`  
		Last Modified: Fri, 08 May 2026 19:43:30 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e60d41f13db426c5aec2a95cceb87ed1d6d74f113a6d22331a96ea77db6e1a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5819dd7ec93c1afcd453e03a3606b5eaa7fcc99f1e9e808bdaac396f032cc3e7`

```dockerfile
```

-	Layers:
	-	`sha256:c31e0a378b6f49b30b2b6fb88d0791892500b11b2a9f6b0ecdf3bb8d1ebafffd`  
		Last Modified: Fri, 08 May 2026 19:43:29 GMT  
		Size: 2.4 MB (2375277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc5275f2766a5763de0466858ea0f4a6d8b6bcdc65194e10b66329b18eeec02`  
		Last Modified: Fri, 08 May 2026 19:43:28 GMT  
		Size: 25.3 KB (25271 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:9b2f5875ff6273bdc08e296427f3c727256578754800be9fc7d3a4f4e93a9f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43470487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172d77a365ee97a4abcb74edeb7379e39849e83c925f648bf1f672db24ab1887`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:35:52 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:37 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 19:36:37 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 19:36:37 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 19:36:37 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:36:37 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:36:37 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:37 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:36:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:36:37 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:36:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde829678b425ad7ddd32c13ce2934097ed0db4a09146eeec8de62e149842511`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f874705b7660b2891a2810d91e92b2d79c1b5f70eea87491355d6259ea77a4`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37389807cbe92bb08d88bf7af317d1f0e7b40db2274f7ac7e82214e02116b381`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 15.4 MB (15351620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64c2dc529dd2c270f81050a5143d576167a5e22e65b870e2eaedb564f9c86aa`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e3fcb10749e92a83fc2b825ab4cd8a0b78c11b6b9c3d842b3ec5fed2fcc9b0`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:df2c268d0497b818da837a9f92994f84ac51523f99894452e0a8c0671743bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176d260f0d8eb21c5085357058d3cd1dc0f6e23031d3681d9aacd9316cadb9fc`

```dockerfile
```

-	Layers:
	-	`sha256:fafb14b84dc4e0468113357e2b7114b14844526719f16a47837dd8d5e3b30af8`  
		Last Modified: Fri, 08 May 2026 19:36:46 GMT  
		Size: 2.4 MB (2373321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e3f032d948444c2857ffbf43b639674d0b1fa07a6de6561b28e1e1949fe3af`  
		Last Modified: Fri, 08 May 2026 19:36:45 GMT  
		Size: 25.3 KB (25310 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; 386

```console
$ docker pull redis@sha256:59b2d6cd9c5a572a595b9eb2d5c5d6531bb31734410fa05119b55c01ddaac44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b6da95dafb7f42c72d0df91a7e74a413c93e4a1dfc582845b9dc86d8f4d93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:47 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 19:42:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:35 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 19:43:35 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 19:43:35 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 19:43:35 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 19:43:35 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 19:43:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:43:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:43:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:35 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 19:43:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a0db0c1baad3c47919dc22515e4e320960c4eaefc89f3f17650a28251653cd`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d7e9c350f4bbae85fbd0eb8ed0b366db84262d7e6fbd69bb229be898dac35`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22d223886f05be2a514810a6f4d00d2829530e79af4f81cb337c9557ecbc10`  
		Last Modified: Fri, 08 May 2026 19:43:42 GMT  
		Size: 14.9 MB (14868044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690502156e53678fc7a2bd6efd71c061e747ee43409c758a7c6a26ebcf3b46a6`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4611b4cb94971613116621b0f4c084a94f8ce3102531f7e8896c6ffdeb899f`  
		Last Modified: Fri, 08 May 2026 19:43:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0b865f5dfa10aa7f273b331db7b1992d863a3d0a5f0b420af134d41db835f449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2236bfee3623a0ae9c8b319de4f0b21fe881b1eb017831f98d6d6e0c1bdd7a`

```dockerfile
```

-	Layers:
	-	`sha256:6744723060b02836ab7029ca73c79dace37dfb4a37f1b2e1debf24e8cc01a2d3`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 2.4 MB (2370213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcc14fc0d6f34c17d44dca4e784a1e197dfb44add557403596e26b323c67f5a`  
		Last Modified: Fri, 08 May 2026 19:43:41 GMT  
		Size: 25.1 KB (25089 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:6e481ff283a2b173dad0e6460e0cd72e0278a992f6bfad885c6cb1859cbbbf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43965938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920680fef810ad927f06f2f893b8f3014353a8c7223e1e89fd9243016b158641`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:51:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:51:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 20:17:45 GMT
ENV REDIS_VERSION=7.4.9
# Thu, 07 May 2026 20:17:45 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Thu, 07 May 2026 20:17:45 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Thu, 07 May 2026 20:17:45 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Thu, 07 May 2026 20:17:47 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Thu, 07 May 2026 20:17:47 GMT
VOLUME [/data]
# Thu, 07 May 2026 20:17:48 GMT
WORKDIR /data
# Thu, 07 May 2026 20:17:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 May 2026 20:17:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 May 2026 20:17:50 GMT
EXPOSE map[6379/tcp:{}]
# Thu, 07 May 2026 20:17:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1bdc534ce4a1e0d7ff161c131dd4f30a3e0afa362f1cd64aaaf83f0d7b346bfc`  
		Last Modified: Wed, 22 Apr 2026 01:26:21 GMT  
		Size: 28.5 MB (28526265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d6e893853e8676c41b86da89ad29389bfc75e9621d6baa8f32254034d5ff58`  
		Last Modified: Tue, 05 May 2026 17:57:53 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3963f3a6ea15d06251f87fdf9b97bafa53354c18dac669fa4269ee6729ae6`  
		Last Modified: Tue, 05 May 2026 17:57:53 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daacfea6d904d82473979fb24a13d361d08357cc75c8d53dda2eb84f3934eb9`  
		Last Modified: Thu, 07 May 2026 20:18:18 GMT  
		Size: 15.4 MB (15436967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3575b5ac12ce98770aeb6b50cdfa3bc5a29b7ea87e80bd79fc328f17cd6b4`  
		Last Modified: Thu, 07 May 2026 20:18:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aca55ef0896e0b13b3fba80efa1730aa0eb461742ab0e425d3cc860e314dbb`  
		Last Modified: Thu, 07 May 2026 20:18:17 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:85a158eee92c37ac7ceff9bab9d1b79ea574f5e6c5630dd51531d782e5840630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b4ae60178b6a507b74b4b95651607d453db854e888e28f92f64e92f7f0c02e`

```dockerfile
```

-	Layers:
	-	`sha256:96d5660ec47f647c34a40d2d6ac6ecc8f701e315438dd9f560ceab3da6147a92`  
		Last Modified: Thu, 07 May 2026 20:18:17 GMT  
		Size: 25.0 KB (25014 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:9b8a62af102468fc01e6c42b6b30cd00f6f26879d36ec64a046fbc7c97a90ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48599491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd12faccf9674225e0794dc813d79114f1b3b432c32b8c9b3bac20234ce5427`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:22:00 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 22:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:24:21 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 22:24:21 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 22:24:21 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 22:24:21 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 22:24:22 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 22:24:22 GMT
VOLUME [/data]
# Fri, 08 May 2026 22:24:22 GMT
WORKDIR /data
# Fri, 08 May 2026 22:24:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:24:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:24:22 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 22:24:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412440315a8cff98a9b4ab67b220e8c7a1ac5123dab938c84ae168317ca2dad4`  
		Last Modified: Fri, 08 May 2026 22:23:41 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b2ed4a7c63fb6631de14c4628b9c762c6f82bd147e12819a2da24f6874542`  
		Last Modified: Fri, 08 May 2026 22:23:41 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbc2789ad6fe7a68faaf3a60db46c6f060803b1108432e6951a12ef3d4d8589`  
		Last Modified: Fri, 08 May 2026 22:24:36 GMT  
		Size: 16.5 MB (16518330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c0f86bc97635d101ee2787a5d3e3649add9d8f299c1bf762b52f4502343472`  
		Last Modified: Fri, 08 May 2026 22:24:36 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0031d236a51f9922faf45b2ae258e94b78352c0ca7165500753fcfd32997a42`  
		Last Modified: Fri, 08 May 2026 22:24:36 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:7356671ea3a400dce4f20af82893e9897a390463025f4e38d4d8b3d287b92048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3f0b42d282212feabf6fa8bbb3f53e0b13c0a076dcd4665911da17433a93ee`

```dockerfile
```

-	Layers:
	-	`sha256:4f5fe7a6365c70a89d256badb792a0b99b21c24c5b768b69ece4f0264f2f95b7`  
		Last Modified: Fri, 08 May 2026 22:24:36 GMT  
		Size: 2.4 MB (2377434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7b7ab41245ea4c2b22ef8413e2bf8160c9dd082861dacd93a4e62d06fe81bd`  
		Last Modified: Fri, 08 May 2026 22:24:35 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:8d475b5dda86d62463ad67e4bf0c3606e6dc5b315608d5560be1d4ee894222b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42275081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e43009844b47b72853bfd645fd1570687670f1224802108fb3dd1c7e214ae9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:48:13 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 08 May 2026 20:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:50:34 GMT
ENV REDIS_VERSION=7.4.9
# Fri, 08 May 2026 20:50:34 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Fri, 08 May 2026 20:50:34 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Fri, 08 May 2026 20:50:34 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 08 May 2026 20:50:34 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 08 May 2026 20:50:34 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:50:34 GMT
WORKDIR /data
# Fri, 08 May 2026 20:50:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:50:35 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 08 May 2026 20:50:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9e46036007c6998fa75cb09a7d9c03090dc7b1105d5b5c2a2011760405987`  
		Last Modified: Fri, 08 May 2026 20:49:40 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3033a80175d7929c4032b5dd42bc3b42a5bcc27ed10c316b2b3d760b387c8c95`  
		Last Modified: Fri, 08 May 2026 20:49:40 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886c9d6f89033f0a111bf96e5d4b39c579154270a3d2db744a86ed1e4ff91896`  
		Last Modified: Fri, 08 May 2026 20:50:49 GMT  
		Size: 15.4 MB (15380772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6cc1767af6507b4287d8b0149d1176176194c8d66d62984526f3cc14e8c73b`  
		Last Modified: Fri, 08 May 2026 20:50:49 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb799d290834e999a2cefa2dab415beb7f0089317481a7be87073625c06a8`  
		Last Modified: Fri, 08 May 2026 20:50:49 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:7ca8d13fe7217fe1c2db518bbf5e5717a76994719d0af7cf1d3ae7b22666a465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f96e22fc291ca1c3e06fe6c15ef562c88780da5856b2dcc0a9b8f271638734`

```dockerfile
```

-	Layers:
	-	`sha256:d9161da6580be4c64566d11dbacb144c6ec5fce16758d1839f0b7c722bf37252`  
		Last Modified: Fri, 08 May 2026 20:50:49 GMT  
		Size: 2.4 MB (2369872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948cc9354f3bbd86a8059cc9aa8011d4a1a5a49e8509b4e85c064e3864a2c173`  
		Last Modified: Fri, 08 May 2026 20:50:49 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
