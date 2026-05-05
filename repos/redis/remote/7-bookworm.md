## `redis:7-bookworm`

```console
$ docker pull redis@sha256:5a77f0f4698389019f828f6387049ce1d5adbea204e56422aa7720dab7034287
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
$ docker pull redis@sha256:e8577bcfff1446c06b476ba3888e90591795b9e0f928354c36833529dc4bc2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43585605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5e0c2e51b76e50ecf027799a2d3e2d957543874f76cfdec73947c1b3fa19a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:56:00 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:56:52 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:56:52 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:56:52 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:56:52 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:56:52 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:56:52 GMT
WORKDIR /data
# Tue, 05 May 2026 17:56:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:56:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:56:52 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:56:52 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3b1a1491cadda933a3e3b843b0565aea87655268485fbc6b3949eb371ce0c`  
		Last Modified: Tue, 05 May 2026 17:57:00 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816adeb7e0898f8d319be4874318337149ea744a35c97e0b67ec2c428e90f03`  
		Last Modified: Tue, 05 May 2026 17:57:00 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2049e5b28ae6c2c3d388ac220468336746bf20c87a47bac9cbd91dac3d0a2`  
		Last Modified: Tue, 05 May 2026 17:57:01 GMT  
		Size: 15.3 MB (15346628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bf0e5c5c48e15205762ff23e3bc93ef022a17c8c5b8edf4535288827c2c5af`  
		Last Modified: Tue, 05 May 2026 17:57:01 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283cccd97f046ffa880b592e981d547440d97204b7683317368c86704cafd8c5`  
		Last Modified: Tue, 05 May 2026 17:57:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:af66552872b1f5677b640c1a4d4ed59fc8c7b1cecb2b73d8d2e6ac4b4c540e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee89914e5743ec02201e010c3447b05d0e43bf90905ccc4901584de3d284a93`

```dockerfile
```

-	Layers:
	-	`sha256:3899e85550c7113e6274c67f542ad84e0fbd99c86972d532cdc89e54d6aa53db`  
		Last Modified: Tue, 05 May 2026 17:57:01 GMT  
		Size: 2.4 MB (2373040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f976ebefd30463c0abfeefda516388bee56218b6967ad567bc27095d72a910`  
		Last Modified: Tue, 05 May 2026 17:57:00 GMT  
		Size: 25.1 KB (25061 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:c731da3dcf4ea5325ee19f31c8eb119ed7ee5a1ccc12fff46e88ead88913c6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40830060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb29ba22b98542d0e9a029c7d47c2008e36e045f69030fd7a07b9117b084887`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:54:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:55:54 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:55:54 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:55:54 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:55:54 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:55:54 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:55:54 GMT
WORKDIR /data
# Tue, 05 May 2026 17:55:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:55:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:55:54 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:55:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:10e5e7c244713d6618375e8360e3d0989303f5cbb40b7ea158ce628f92e32f96`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 25.8 MB (25765657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3319abaf1d08ebd2e3adc94574355cbd94795ecbc44c204fc641b079a4cadf`  
		Last Modified: Tue, 05 May 2026 17:56:02 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cda4baa696f615dbddd23d7da42d02cbd58bf68a22b0337e379743a85dbdd`  
		Last Modified: Tue, 05 May 2026 17:56:02 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ad11cb7359809edb4b14af8eec1ef5f755b6d45d07800f618c76d216bff6e`  
		Last Modified: Tue, 05 May 2026 17:56:03 GMT  
		Size: 15.1 MB (15061676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63efa949737bcd9f93606fe81dd4845a083c5c51a41e2ecb07c10493a01011dd`  
		Last Modified: Tue, 05 May 2026 17:56:02 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cbfe4b45ddcb48c126d8222ec7dc9a3e48c4a63c8024ad5c36ae91e85e9c43`  
		Last Modified: Tue, 05 May 2026 17:56:03 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:cacf10aee568b8d140d5d47937073c5daa8cf2c011dd0cef8df2f295709b6c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855ba799f220f5800182051d7d6f8f29d429cea18cf9574d2424fed8db102b84`

```dockerfile
```

-	Layers:
	-	`sha256:7cbd0d229b8896dfd3408b3fdf6d15db76f1913bef9c32d53eec2f52c22c6e1b`  
		Last Modified: Tue, 05 May 2026 17:56:03 GMT  
		Size: 2.4 MB (2376860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d80de17f50cd814faacf376fad0f97c012ecda696f4e758213496ca8941eb6`  
		Last Modified: Tue, 05 May 2026 17:56:02 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:da0b9cb0c88b38e6e5f6a91bade3f51ab8c01e84aaf73a4dd6f3a4d741144d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38663946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3feab78058a696110fc900617c948ba0740c82f128901673629a118b35baed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:55:33 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:56:27 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:56:27 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:56:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:56:27 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:56:27 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:56:27 GMT
WORKDIR /data
# Tue, 05 May 2026 17:56:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:56:27 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:56:27 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843a6e1c652db75110762a0857729c1ecf66c470a391545a3125456ddf39e4e3`  
		Last Modified: Tue, 05 May 2026 17:56:35 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c502dd30e11b4643099a2053bcba9c1b3f36d2658a2a8ed1723452d47df3da`  
		Last Modified: Tue, 05 May 2026 17:56:34 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99958b9be29934c52688f09586ceaf4f4aaf1da868910a14995ade347985436`  
		Last Modified: Tue, 05 May 2026 17:56:35 GMT  
		Size: 14.7 MB (14719793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e54daa1a6e3132ca66d05b3ef0230fc4250e0f4fe848e6843de6a9e91ffc96`  
		Last Modified: Tue, 05 May 2026 17:56:35 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736f5dc3ebe63d50f9b2d49515b6c44a8efb63a9818973a03ae9ec1557748213`  
		Last Modified: Tue, 05 May 2026 17:56:36 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:1a467705ef66559eba70fc50f561281df474e5fba72e583b5075f1cc5290837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c359b0191997b1cde8cdecd3f3095039d743fe8e31f422bece1c0fd8a1add1f`

```dockerfile
```

-	Layers:
	-	`sha256:23c3fcef8243a96e241046a46fb9abe90389480b2fae7f08f07cd2379bda7e98`  
		Last Modified: Tue, 05 May 2026 17:56:35 GMT  
		Size: 2.4 MB (2375277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb889ba942b7904e003e71c870ee16d42e52e2d7288db86422e8f43ad72ba88d`  
		Last Modified: Tue, 05 May 2026 17:56:35 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:c18e2755524c9e8d4b7cdea1a44ddc67600f5a3dd910e10a9dfdb75262c88f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43470460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc549f33c372567bc225cdb1f4e6d15eebf3fa44660dbc0e02c78300eda37b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:54:16 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:54:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:55:03 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:55:03 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:55:03 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:55:03 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:55:03 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:55:03 GMT
WORKDIR /data
# Tue, 05 May 2026 17:55:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:55:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:55:03 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:55:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff17e4f17de06c2aeb6cdce9f25d6c10472c4b9e40f7ce03c4e196e65a7588c`  
		Last Modified: Tue, 05 May 2026 17:55:11 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7de83a418304ca60a8ed0708d366ba28e1c107ec1c19b997e2910691f12b92`  
		Last Modified: Tue, 05 May 2026 17:55:11 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a170233efad6438f6ab676874c1b9aebb8220a25dd270d2bb01cad7deb295`  
		Last Modified: Tue, 05 May 2026 17:55:12 GMT  
		Size: 15.4 MB (15351618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5eb4f7a90f4383994c41760bdb67746d470be13a153fc4ac6223d36575a9f0`  
		Last Modified: Tue, 05 May 2026 17:55:11 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3871c07a440fa309e02232698391d5c62321eb0b0043588eecca362ecc9137dd`  
		Last Modified: Tue, 05 May 2026 17:55:12 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:0f7e426d1f9bc21b553ab841c5c1e04ffa5f68c8b1274215348dc34cbb36301e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28889dc169c27a02dbfef67f73a313eced4745f8b2d00807ea2dd7c81531c512`

```dockerfile
```

-	Layers:
	-	`sha256:c84d177c9d268414c93dd64d374546a8c80fff59f18b46c7f32be635ab63a480`  
		Last Modified: Tue, 05 May 2026 17:55:11 GMT  
		Size: 2.4 MB (2373321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e879ca2fedb8fe74e1ad6970fd13fb05dac37c1000ce96d9e59e9c640c890e7`  
		Last Modified: Tue, 05 May 2026 17:55:11 GMT  
		Size: 25.2 KB (25234 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; 386

```console
$ docker pull redis@sha256:db1595559b09b16ee46364d66b4e4c86be0497a0f41d26b04b097397bb271e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9cfe41cedb456721a60fb6a4c01ea700e07121720fdada6c2633adb4db83b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:54:27 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:54:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:55:17 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:55:17 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:55:17 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:55:17 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:55:17 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:55:17 GMT
WORKDIR /data
# Tue, 05 May 2026 17:55:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:55:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:55:17 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:55:17 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d078cb96837d98f7b39c6488bce00f4a8aa96c5c5c57f696be59d72876b5ddd3`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16fc54f0fbb6fe88d79ba060db0e76bb5bb8d7490469b02404618537d29f72e`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16e1bb0e207aef505dbf6c8a13c935116ced2fe0ff9c0bfc2361b793b15e79`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 14.9 MB (14868058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4642ba03b69ba3edf0dba25da0546be463278809cc98fb2f1daa6bd6bbc527`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a20d82eb42510034fda20e57aa82d5e936a447343d760900ec2cd8d81bed75`  
		Last Modified: Tue, 05 May 2026 17:55:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:8ec005dfbff4c865c4c410eca31d2e2d432c4220d058a83c13a3f3940e8e9b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101e3ab688ceab553117a26f75f36ce58653b510ed017dacbd9c8599547ff1ff`

```dockerfile
```

-	Layers:
	-	`sha256:48588d41135be3d7ecf6f3c0bd27871989523ca292c89c553884ce435b1a1ec1`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 2.4 MB (2370213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c25950f4d7c047c2c581eda9f4db89b7066867f85594998209903fa5dfb51b`  
		Last Modified: Tue, 05 May 2026 17:55:25 GMT  
		Size: 25.0 KB (25012 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:1b6729f4b648a6233cda880a1e5bf65624b5836fbf085a28e198962511a1ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43965937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b4c31d363c4ca384b2b9918e6536e9076443105edd2d54deb62898e72c2b58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:51:07 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:51:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 18:03:43 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 18:03:43 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 18:03:43 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 18:03:45 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:03:45 GMT
VOLUME [/data]
# Tue, 05 May 2026 18:03:47 GMT
WORKDIR /data
# Tue, 05 May 2026 18:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:03:48 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:03:48 GMT
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
	-	`sha256:94104823ffd0de8aa3977746abb0a0136fd9dec97ae41d36b20032bc776cd4a5`  
		Last Modified: Tue, 05 May 2026 18:04:19 GMT  
		Size: 15.4 MB (15436944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ac1d7b72dc88730b3ed5c08bc840dad153355ffbbd9a080f0a5be7e7876af`  
		Last Modified: Tue, 05 May 2026 18:04:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a50fa0b998fc2e7e5caa6785f900a113798ccde6ddb2f17a468afb6b253f97`  
		Last Modified: Tue, 05 May 2026 18:04:17 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c7e6f312b23b0da04569c11da4c043e7096f2bbc2c807f552088dc724279404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 KB (24939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc71da177adae7551159d0b74a85f902b850cb87fc39ac3f340935790af900`

```dockerfile
```

-	Layers:
	-	`sha256:b9f9d070e162477db0d8bc2b844147e6da95fc608f8db288e3e4b1aec927e03c`  
		Last Modified: Tue, 05 May 2026 18:04:17 GMT  
		Size: 24.9 KB (24939 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:2070e09399ec4b4946fccaa8edebb90c5d8b1b73666e65dad4dfc4687cb4585b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48599575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606bfaa67bbb25847f725c4bd42f57fe70e7e8106ca58177c45ad71308f8b7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 17:54:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 17:54:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 17:58:18 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 17:58:18 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 17:58:18 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 17:58:18 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 17:58:18 GMT
VOLUME [/data]
# Tue, 05 May 2026 17:58:19 GMT
WORKDIR /data
# Tue, 05 May 2026 17:58:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 17:58:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 17:58:20 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 17:58:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc86d02147152571c418f4a27479b30b86954b5da6a9c23f1ae72c76ac200f46`  
		Last Modified: Tue, 05 May 2026 17:57:13 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db69ed1031a80076a976930f1827fda0b30a7921e68a58221623c0587349a861`  
		Last Modified: Tue, 05 May 2026 17:57:12 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b875fdbacfc7e4fce356d8e0a5c5b9d9543785150d287d20e1fa0137e832b420`  
		Last Modified: Tue, 05 May 2026 17:58:42 GMT  
		Size: 16.5 MB (16518445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac16e64ef5fe343bdf3efe828bcd23690e4f77fa8ec5d64a1bb1d334f270cb`  
		Last Modified: Tue, 05 May 2026 17:58:42 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505a4a65d579f6fb5e39c134fe36c4a8b8aa69ba8a734a54eb91a253e536bac7`  
		Last Modified: Tue, 05 May 2026 17:58:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:14305af1dcbc21163c8393e4a1ae673e91ee29c105e18d7de31e6ad56200f040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fda321cd2ff1a8210e1a4f0d82b9ed82c1092d6f48d9ddca961873814d8eb`

```dockerfile
```

-	Layers:
	-	`sha256:fdc6541a431f6502d2a58ca55b51bbc8bf36fe73f602916574ae0aa63f11dfb0`  
		Last Modified: Tue, 05 May 2026 17:58:42 GMT  
		Size: 2.4 MB (2377434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569754f101245992c3338b89302e661de8109438da71f66b2d49e7772511504d`  
		Last Modified: Tue, 05 May 2026 17:58:41 GMT  
		Size: 25.1 KB (25123 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:e6b540cb45557dddad20a0b70ec706031135422d49fcb8024c1be70b08bc8db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42276153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67700f1d1163162933f7422354d3af01479b86fbd8c2512be685833cb40c8d15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 18:11:29 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 05 May 2026 18:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 18:21:24 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz
# Tue, 05 May 2026 18:21:24 GMT
ARG REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
# Tue, 05 May 2026 18:21:24 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 05 May 2026 18:21:29 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/7.4.9.tar.gz REDIS_DOWNLOAD_SHA=94a3f84963f710e402bf7dbe61ed9ee3b43862d1aba995faca7a23621b51f652
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 05 May 2026 18:21:29 GMT
VOLUME [/data]
# Tue, 05 May 2026 18:21:36 GMT
WORKDIR /data
# Tue, 05 May 2026 18:21:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 18:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 18:21:40 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 05 May 2026 18:21:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d0b7b18ce704fffeec1d81d0a430f278cd7e57e29fea6605b74cdf54d41da8`  
		Last Modified: Tue, 05 May 2026 18:22:49 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c368103dc5263a140047d1f05bfc54fbc0be37425f04b940ad3f00f029a89130`  
		Last Modified: Tue, 05 May 2026 18:22:48 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d218bb692514c6a0185d7c6ecf49c39da0bca772da023da00d03957e5049985`  
		Last Modified: Tue, 05 May 2026 18:22:53 GMT  
		Size: 15.4 MB (15381850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d859144e9770b95a18235f4f8049eb115f947880062e90a5ea1c53b1bcd68`  
		Last Modified: Tue, 05 May 2026 18:22:50 GMT  
		Size: 95.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9083b7ac13dbe3e9e15e2d6061e6b30c55a09cd3c85a53efcbcf92a2cb0f6594`  
		Last Modified: Tue, 05 May 2026 18:22:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:3e56ec26b789f4e444266db3e2e1b2325cee373838f81146ebd9dec548655546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83800121f130de7b8b5a465f72143fbb35b3e480199d1c73de49ba19e3bcd58`

```dockerfile
```

-	Layers:
	-	`sha256:a4debb16379c77f5bfc1b72eeebdf5632e7300132a6b15371c36e93b054fa39e`  
		Last Modified: Tue, 05 May 2026 18:22:50 GMT  
		Size: 2.4 MB (2369872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed36c33d18e5818d60a7f5e94b04f0defd94a2dd765c0b67bae2ef5c9ba6de5`  
		Last Modified: Tue, 05 May 2026 18:22:47 GMT  
		Size: 25.1 KB (25061 bytes)  
		MIME: application/vnd.in-toto+json
