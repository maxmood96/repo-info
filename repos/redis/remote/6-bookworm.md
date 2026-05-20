## `redis:6-bookworm`

```console
$ docker pull redis@sha256:a3c4a4c39535d402567474dbc40afdcb126db6b248be6e26f29eec43c5974f9f
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

### `redis:6-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:1c326910753b4314a2de653113657a181507b2a6950dceee16320f7b84aade87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38733795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46fba92f74d17746a0d2e44676978d20d7e76b95d79d05a6d432f31df5ca1df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:17:26 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 19 May 2026 23:17:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:07 GMT
ENV REDIS_VERSION=6.2.22
# Tue, 19 May 2026 23:18:07 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 19 May 2026 23:18:07 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 19 May 2026 23:18:07 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 19 May 2026 23:18:07 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 19 May 2026 23:18:07 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:18:07 GMT
WORKDIR /data
# Tue, 19 May 2026 23:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:18:07 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 19 May 2026 23:18:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403a49da2c85c6efc0573e5b0f7b7183d329945ef95545ff4b9fa1e56eba971e`  
		Last Modified: Tue, 19 May 2026 23:18:13 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4bbb4f6df1a6373f7d7f5b0d92cb0605b90a21090d5525bc69ec777f2d486`  
		Last Modified: Tue, 19 May 2026 23:18:13 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f8fa97e14c0c67779e0ec8a811b13f64d9ab6493568b34eb694d88af6641ba`  
		Last Modified: Tue, 19 May 2026 23:18:14 GMT  
		Size: 10.5 MB (10497550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be3d651ee7ceac2d26f7e6ec2e1de34c24ba1fe2df227b0d2a3e7feb442dcb5`  
		Last Modified: Tue, 19 May 2026 23:18:13 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde12fb1907c2aa5e5e04a465c2aa3b1ab2868ff69693b72a2636655baa5f8bb`  
		Last Modified: Tue, 19 May 2026 23:18:15 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:434cc9e0ee25cc815261aa725f85d9d9e2884a430a44296065d30465e7f763e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd9e84ccc865976656b42f0c47efe0e663c1c6c6efc874b82389aab4a194c64`

```dockerfile
```

-	Layers:
	-	`sha256:3592d9a1e4adefb03d6d29c5548c8fc285291468a6ae5d960854a5b4ad01af27`  
		Last Modified: Tue, 19 May 2026 23:18:14 GMT  
		Size: 2.4 MB (2373064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0cfa1b0a092c0c03d259118e82735da9a14cb2a45feb63b6aaa707659b051e7`  
		Last Modified: Tue, 19 May 2026 23:18:13 GMT  
		Size: 25.1 KB (25148 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:3b3536ad49084de0a731415bc102a2181ef0580be67af529795167df43acc96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35846493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54947155af2e6d56e88c0ab8580121d62371913d5622628451532e6fd7c9da8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:53:55 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 19 May 2026 23:53:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:54:44 GMT
ENV REDIS_VERSION=6.2.22
# Tue, 19 May 2026 23:54:44 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 19 May 2026 23:54:44 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 19 May 2026 23:54:44 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 19 May 2026 23:54:44 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 19 May 2026 23:54:44 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:54:44 GMT
WORKDIR /data
# Tue, 19 May 2026 23:54:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:54:44 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 19 May 2026 23:54:44 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafe46441b518c4a781e20a9ca9d0a79dc9e50fb3abd2501b4105a084fb30c33`  
		Last Modified: Tue, 19 May 2026 23:54:51 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b5068fa83398c81c0c1543e5d55268320d2e1b369c18c6700cb75a99a6cb2a`  
		Last Modified: Tue, 19 May 2026 23:54:50 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b61ec370cf50cabdc2e65f78ddd4cddc7b9b680be9ad3853b3f8a10109e4fd5`  
		Last Modified: Tue, 19 May 2026 23:54:51 GMT  
		Size: 10.1 MB (10075496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17b683953301a605816265d088581b018d0c414d784eceefc205e01e4aa682`  
		Last Modified: Tue, 19 May 2026 23:54:51 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d560e4163da2df246fd7f3fd0656e869b39273380b82910aa09a9a49f5fa238`  
		Last Modified: Tue, 19 May 2026 23:54:52 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:be53fe48ed078b722f45d84aa144cee59fc57672549b9e32d69c94b623601914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8906a667f5b96e423017b89c4967a153f25691f928b5ed3b01093ae3fde66e81`

```dockerfile
```

-	Layers:
	-	`sha256:d11833823f40b3e6b65b7851a34c0535828c099427db34bc6acf2f2ca9237843`  
		Last Modified: Tue, 19 May 2026 23:54:51 GMT  
		Size: 2.4 MB (2376884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2117e9969586148faffb7ee8a6ba1404290d5ff95220131171fcf938ae8df057`  
		Last Modified: Tue, 19 May 2026 23:54:51 GMT  
		Size: 25.3 KB (25284 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:34636238c66fbec7ded448e69a2cec39ffc417240b8e283585d307c9e780be79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ed77417f603c427f598c6584d1c4897fdaae1a0dac864859d62e2a462ac75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:57:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 19 May 2026 23:57:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:59:21 GMT
ENV REDIS_VERSION=6.2.22
# Tue, 19 May 2026 23:59:21 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 19 May 2026 23:59:21 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 19 May 2026 23:59:21 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 19 May 2026 23:59:21 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 19 May 2026 23:59:21 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:59:21 GMT
WORKDIR /data
# Tue, 19 May 2026 23:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:59:21 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 19 May 2026 23:59:21 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b71675a3b720086e7d9ce1217932f468f7b64903ed129c1b11ab07d246a92c`  
		Last Modified: Tue, 19 May 2026 23:58:33 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7079dcb590b866205e9e9f636c162c4fb79ea45704e6da484456a33cedeb53ae`  
		Last Modified: Tue, 19 May 2026 23:58:33 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed9af24b76d0cb5c7521b4f1338b64adee8c5829e37b3eba5aba0d6bd983c21`  
		Last Modified: Tue, 19 May 2026 23:59:28 GMT  
		Size: 9.8 MB (9794111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd9b92dc6ce57c8ee74a3e9369bb28802e94d6067cc7ce9eca82bbcdd79c84d`  
		Last Modified: Tue, 19 May 2026 23:59:28 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad7bce72fdeb2b6dee0a4b40f5d5e2f10fb015fa415dad0253859a64ea0751c`  
		Last Modified: Tue, 19 May 2026 23:59:28 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:2cfebb7de3fa1f452c4bb7af796b108b0bf4ae0c7656137e3c8ee66264957e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11f861fb75ef3edceda3e7ddac33e4ee328d7052942fc6432e81ed943a32103`

```dockerfile
```

-	Layers:
	-	`sha256:a500ed50900792931770234d1443a65c3c00f4c150d97011b364327eb8229635`  
		Last Modified: Tue, 19 May 2026 23:59:28 GMT  
		Size: 2.4 MB (2375301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5bcf9164b8092f5716f0e2557e3e8932e8d84011f7287e21c5c9ab0768ea81`  
		Last Modified: Tue, 19 May 2026 23:59:28 GMT  
		Size: 25.3 KB (25280 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:567dc972173880e2cfd9c849038ef88e1186225bd4fc7229f1654e539b2aaed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38558231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bc07cef72452af640ae11814b8cce67c3361d4bc2962762848663dc79bf4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:20:51 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 19 May 2026 23:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:22:53 GMT
ENV REDIS_VERSION=6.2.22
# Tue, 19 May 2026 23:22:53 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 19 May 2026 23:22:53 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 19 May 2026 23:22:53 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 19 May 2026 23:22:53 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 19 May 2026 23:22:53 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:22:53 GMT
WORKDIR /data
# Tue, 19 May 2026 23:22:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:22:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:22:53 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 19 May 2026 23:22:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6c2dfa3e0ed52409eab261d7fa6cd488f49435fe4d451aee42b9073f96b0ee`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e3e6f10391291962cabfbd2ccd21f7d168d99d27a1f6d1ce14ed3f233ed535`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1cd10021d0f36d40410dab2b0679999118cc694ffb1af02dbf715a6d0566dc`  
		Last Modified: Tue, 19 May 2026 23:23:01 GMT  
		Size: 10.4 MB (10440481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663674854ab0be3d480936903dc5dc4b54d8b60e63d2158b0790eeb0e93996b2`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3cda08acc358e2aace351ae9d6f3b1f114b477ee3bdb22c2049cf39c460a66`  
		Last Modified: Tue, 19 May 2026 23:23:01 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:3ca82e40f8bcadac21f75848f0f025b71e96a7def6091b605c4a567e04f4c3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc50850b2b450cdd45a90b051fe2ddfa38e1cb950b28d7935e5d41434833a610`

```dockerfile
```

-	Layers:
	-	`sha256:8e1ed542b20f33603af934860be0f82aaa713a0db80477041727b07f16c166fa`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 2.4 MB (2373345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8dd64b3a56550f750a12700db8b2e9b7419b5056ae69098c0938b5a06ee3650`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 25.3 KB (25321 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; 386

```console
$ docker pull redis@sha256:1a1e595700afd21d7b1150dd504d73fc77d41c29623d326c96992002978934cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39449951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72886f0beac473f5647810220eea0fa1c3dba8445ff049e71795e2b58f18620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:01 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Tue, 19 May 2026 23:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:43 GMT
ENV REDIS_VERSION=6.2.22
# Tue, 19 May 2026 23:24:43 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Tue, 19 May 2026 23:24:43 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Tue, 19 May 2026 23:24:43 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Tue, 19 May 2026 23:24:43 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Tue, 19 May 2026 23:24:43 GMT
VOLUME [/data]
# Tue, 19 May 2026 23:24:43 GMT
WORKDIR /data
# Tue, 19 May 2026 23:24:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:24:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:43 GMT
EXPOSE map[6379/tcp:{}]
# Tue, 19 May 2026 23:24:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d3908f09acba9c51e5ce2a415528dfca3c8e737fb282e84a55f5f644713c14`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61c900b10876fce4855974441bfdbde546844090221e24b9aca2a0af2ffb219`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a0413e81e79d55c6da81dec92a374e1b8b4cdc218e2128bf519734777a8185`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 10.2 MB (10228651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee20c85b784ac2ca2f0737a7e950c7793ea2e9b87abdf0d452d37f299b6d01`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c751b41cb6e08def4f7f83775a4bf84c0bd84d110e22d07f7c5adb443f1c77`  
		Last Modified: Tue, 19 May 2026 23:24:51 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:d1a4ee43614fe214b099a7f2b8130c3c0266df70aa0132812207fd41745ae692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8fa917f5aa86bd436f18efc4f3d9a2a4208742c6f9e138e32e4dc4252b79d1`

```dockerfile
```

-	Layers:
	-	`sha256:e9607e6bb1ef33cf7eadd7cedfed0226837a9882688daf666919bf7fb39a3a0c`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 2.4 MB (2370237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:896fa1efc05bdff6342c3efc0928f2d3e04f5b7d20cbd20425075c37c6180ba2`  
		Last Modified: Tue, 19 May 2026 23:24:50 GMT  
		Size: 25.1 KB (25101 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:40c47e3a1de7bbf1372ecce5abb9df471a237f06be08ce37b59f88ada5163a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38945278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831b2b8d6239ce93536eee0811b9c0c00739d0706eb0be8abd0c6086f2f09ffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 09:38:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 20 May 2026 09:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 10:02:53 GMT
ENV REDIS_VERSION=6.2.22
# Wed, 20 May 2026 10:02:53 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Wed, 20 May 2026 10:02:53 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Wed, 20 May 2026 10:02:53 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 20 May 2026 10:02:54 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 20 May 2026 10:02:54 GMT
VOLUME [/data]
# Wed, 20 May 2026 10:02:56 GMT
WORKDIR /data
# Wed, 20 May 2026 10:02:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 10:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 10:02:57 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 20 May 2026 10:02:57 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:83efaacc11aede9fdd3dcef1c025f5df70c81553b815dfb44caceaf1fa9eba75`  
		Last Modified: Tue, 19 May 2026 22:35:42 GMT  
		Size: 28.5 MB (28522504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeac8f69221145565da5fc9641d6c2f0e036fb29d08bd807e9dc2b7daaa884e`  
		Last Modified: Wed, 20 May 2026 09:45:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f08f5589c88619e7f0aa1b1cede62de5e3a284a7a2aa40f83dcb7884651b0`  
		Last Modified: Wed, 20 May 2026 09:45:32 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e19eee79b0f7c0d2d7a75999aa7001e113ff70000f5a44604f46f96bca1fdf`  
		Last Modified: Wed, 20 May 2026 10:03:21 GMT  
		Size: 10.4 MB (10420069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e352464285e22ef1be81b8a72542ad39795048d4260a2cc54e2a568f9d015`  
		Last Modified: Wed, 20 May 2026 10:03:20 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6affb006d147cb2fa02d45c2d902b1b6aefcf35820ed53095409359adcc8290f`  
		Last Modified: Wed, 20 May 2026 10:03:20 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:37b2fa8e82d6ca02aa8ed45646a12f0eda49feab977353d615090e606045abc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6c95a073aa98e492890d639a3d22341dd1b881a9ea9dff0fba882663c2e252`

```dockerfile
```

-	Layers:
	-	`sha256:12abd405908d9432b4f038793d36a62ec972fd01b7e7b478d7fa3398bdb70747`  
		Last Modified: Wed, 20 May 2026 10:03:20 GMT  
		Size: 25.0 KB (25027 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:43f3eaf9d7a400b864c156d72f380561d85e2455f06cdde18c768c169c5855c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43422770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cf97c822a6b21d3c16cbac6fa48b708ae9a63f87f1ec506885f6fd02851a7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:07:43 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 20 May 2026 01:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:12:30 GMT
ENV REDIS_VERSION=6.2.22
# Wed, 20 May 2026 01:12:30 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Wed, 20 May 2026 01:12:30 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Wed, 20 May 2026 01:12:30 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 20 May 2026 01:12:30 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 20 May 2026 01:12:30 GMT
VOLUME [/data]
# Wed, 20 May 2026 01:12:31 GMT
WORKDIR /data
# Wed, 20 May 2026 01:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 01:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 01:12:31 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 20 May 2026 01:12:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f967545f4e532c3f5033e8e97a249af83d0cc1a7907fd79b248e87e07f04618`  
		Last Modified: Wed, 20 May 2026 01:09:32 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbae66e4f697ce464e7029e9775b5897f3de2fecd750d51565e3a796a73658cd`  
		Last Modified: Wed, 20 May 2026 01:09:32 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3d44f48ccba4c2a2ac736a804875b933bbc736c91d173f491de1980519217`  
		Last Modified: Wed, 20 May 2026 01:12:48 GMT  
		Size: 11.3 MB (11344323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f5097ac478d10e0f98c2043fddb3449682a9d45093de1d01ea96dc269fa799`  
		Last Modified: Wed, 20 May 2026 01:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f9751f51fcb900cc95a6c287eba10f16aff132d1dd18c2a9b4bc4d6320602`  
		Last Modified: Wed, 20 May 2026 01:12:47 GMT  
		Size: 602.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:23dd0f343092f794bfe3d5bec6d916f80134242c217916a35a5e5f73f7bc997c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a72a0dcf5598202e4ddaac0acb83e15b37df57b9ffd4b3d31d94a43f26bdc83`

```dockerfile
```

-	Layers:
	-	`sha256:0dcfd809b231ae23ad467475a6a8858968e343b82a8630beb0d504670bfcfd04`  
		Last Modified: Wed, 20 May 2026 01:12:47 GMT  
		Size: 2.4 MB (2377458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba8323c3fbcf1d78f0f6ea2d0c1fcd6e0a1051f6fc72cef363a59809cc3c8e3`  
		Last Modified: Wed, 20 May 2026 01:12:47 GMT  
		Size: 25.2 KB (25211 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:4db01bc2561a327ae194ab4deb378f4b27da7eb914f635bf5bd5d92fed6e048a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37351775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae9277d1f3a57440940f369d2cb9fc5386ffbb12cb84dc53c2af6452e9e0419`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:14:11 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Wed, 20 May 2026 00:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:16:35 GMT
ENV REDIS_VERSION=6.2.22
# Wed, 20 May 2026 00:16:35 GMT
ARG REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz
# Wed, 20 May 2026 00:16:35 GMT
ARG REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
# Wed, 20 May 2026 00:16:35 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 		dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 		rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Wed, 20 May 2026 00:16:35 GMT
# ARGS: REDIS_DOWNLOAD_URL=https://github.com/redis/redis/archive/refs/tags/6.2.22.tar.gz REDIS_DOWNLOAD_SHA=224a32db84ce3be2bf432ce7c78ac858df7851bff1e089e71e15dc442be9e95b
RUN mkdir /data && chown redis:redis /data # buildkit
# Wed, 20 May 2026 00:16:35 GMT
VOLUME [/data]
# Wed, 20 May 2026 00:16:35 GMT
WORKDIR /data
# Wed, 20 May 2026 00:16:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:16:35 GMT
EXPOSE map[6379/tcp:{}]
# Wed, 20 May 2026 00:16:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7db26a0a93802b65ea10e94eb0ce9d3449c20693341ba7c3cae6d1b35c0b63`  
		Last Modified: Wed, 20 May 2026 00:15:32 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03877123837fec5ebf475fd2f4beb30e053f29a28431803bee5bbaf04c89c3e7`  
		Last Modified: Wed, 20 May 2026 00:15:32 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f5e14d98af6b7545e6e57bc636f1b3c07788943dad9376a390658204eee998`  
		Last Modified: Wed, 20 May 2026 00:16:47 GMT  
		Size: 10.5 MB (10460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0af44e461b89e02c61c522a500f8caf3c9688f5e69c710354039dbd8b0e437`  
		Last Modified: Wed, 20 May 2026 00:16:47 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4a2ebd11881a8f366d25306a34a9a48c998adfb5076739b46bbb90f612658`  
		Last Modified: Wed, 20 May 2026 00:16:47 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:240ba6f02f8be94857679af4f6e090cfadf41534b141a8e1c4642d674d61a4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fdde7fdffd51ef954176c0eca683e17ab3ad519a6f6c0e6b23888ec4cfba30`

```dockerfile
```

-	Layers:
	-	`sha256:a360dfd1c8c8388b91e9c3d12d2162b648da1930402b3f5d9a8b6da9934f8a66`  
		Last Modified: Wed, 20 May 2026 00:16:47 GMT  
		Size: 2.4 MB (2369896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c447f03aba1207c4e84c293fde7baf95acfe27285338b407839b92ac209f0aaf`  
		Last Modified: Wed, 20 May 2026 00:16:47 GMT  
		Size: 25.1 KB (25148 bytes)  
		MIME: application/vnd.in-toto+json
