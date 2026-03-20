## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:43f0142a9c484826af05e4827c72ad1445194b231303360cd36462e35b5c010c
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:b67602e3804ec9de37cd94ccbe77dba44c9d8a7a0e1340a9b0f37e11ecad981b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45870201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9f3993140ad5ff3d87e6563cf43c91609aa28d29cfd5fd9d4cdd54e455abf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:10:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:10:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:11:37 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:11:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:11:37 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:11:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:11:37 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:11:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:11:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:11:37 GMT
USER haproxy
# Fri, 20 Mar 2026 00:11:37 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:11:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd155009e8986bc66d79bc7d100258b593d962f1b40acf54935250c84947076e`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 1.6 MB (1581183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fcac05f829df468569e53e2e1b95297ccfa387e172c06c63b6e259b8be591b`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d9b7622b81d42bd3583a77efcea2ebe63fe82d8b729a546a8540a8962203a`  
		Last Modified: Fri, 20 Mar 2026 00:11:45 GMT  
		Size: 14.5 MB (14511879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415aa948a84b2980b8c7eabec0619be3e7dafed59cf2210456a97edab4cd732d`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e58b8d4ebe54b98373f2e2023f85c37f89cb563eef030a94e824316a8e27db77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bee6175532f032843eb5b7967ec2142198356261a63e9e60be938a72d79ab0b`

```dockerfile
```

-	Layers:
	-	`sha256:f42cfa83fa018ee7923577eac548d82de9464b6b56ea8dbf294636403d793311`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 2.1 MB (2113798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b225aee4b1f698104fb1b80663be17577c28afddc42795ccfb39a266542582ab`  
		Last Modified: Fri, 20 Mar 2026 00:11:44 GMT  
		Size: 22.3 KB (22337 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:b018e331fe044d37cd97ba03b51972fa6ef516ba8c96a81ae4f7a47404a3ed41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44186677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cc0b8eafc1298896da2a58d2072e4632f5498b8f18dcd7b48a1b10dfdb6306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:07:40 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:07:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:08:38 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:08:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:08:38 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:08:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:08:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:08:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:08:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:08:38 GMT
USER haproxy
# Fri, 20 Mar 2026 00:08:38 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:08:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a616eda4200bc0fb0ba255e03f18e0fd663af68f8d9a67669f5b23c076cb15`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 1.5 MB (1535689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e633c86d8aaca4dd23b4bfec92278a998426a9807bee77e8ec5f60d8bb019d`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aedb5612d930dc18a918983993be9a3b09ab427aa9659d0692134079381274`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 14.7 MB (14705701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbac514ac6eb5429aeeafb42a4c9c82c416069a3b3871204694fde0636fa77f7`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f11288076e040912820c19fe6d48d5727ceb8b158e7ff6447158aaee445cae65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dc4675b24c7be9b29cd4a6c559ff09a632448b2c013f9cd4cf6d4e637589e5`

```dockerfile
```

-	Layers:
	-	`sha256:05ec413e1eefda89fc01be9a2e44a44bf12c609ffd496ee76998bfdc93c37d95`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 2.1 MB (2116778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7507097634213d3a8c5d17d43c4110008b5ee8eb5a8b4005c341bddcc8e80e`  
		Last Modified: Fri, 20 Mar 2026 00:08:47 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:470b7726395c01c46938a9c5550778fcd2e94901f6c6d86818c8a5ca9e7b59ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42207244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f0ab21fe334074e3e4cbecccc97988f6a2bce53de8aa6aed33f7b945740517`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:07:16 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:07:16 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:08:07 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:08:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:08:07 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:08:07 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:08:07 GMT
USER haproxy
# Fri, 20 Mar 2026 00:08:07 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:08:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eb9a6b4a273da9c0a90f53cea5b3590fa5d540c0e531d712dec1f063998f2d`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 1.5 MB (1489551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9e2febc3ab3c5cafd32bdf29331e5283c2df8e5920fd8aa7e3889f098262dd`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7a624b4c751fd0f4bf787f0f48eb09ef495ac80923b27f4581355c2e9a0a1f`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 14.5 MB (14506551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef84026de5aac1c56e135c70e11143268c0872cef54d523ed5c6c10f2c5a020`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ae950b2098af363882e963f9be7cf8f02ef8a436562f94a00694c3f34b4a6712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806873e5571e2029b313e767358ed81159651940cbe3c2919618ce051e2a028f`

```dockerfile
```

-	Layers:
	-	`sha256:2aa14304546be82ef2c31b6b95a2300d68238962d40f64e63fb7128a0a2b924b`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 2.1 MB (2115221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e26858d63d9045ebefac5af0cfcb88f6e89ef43222f9492692b2b54bacbc38d7`  
		Last Modified: Fri, 20 Mar 2026 00:08:15 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:c2fa36488c3c8763579ebcff5d415db7ea33a7a11b86b440a531e7a0e11d8782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46092454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa37b282696e2dba14dce4abaf2874e28f41711c420859e6e58d6f004d4863c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:09:32 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:09:32 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:10:16 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:10:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:10:16 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:10:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:10:16 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:10:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:10:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:10:17 GMT
USER haproxy
# Fri, 20 Mar 2026 00:10:17 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:10:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a62db3984d9cd5ca4cd8b6c74ba3f6b9f1921469227a92fc36e1dcf48f76f0`  
		Last Modified: Fri, 20 Mar 2026 00:10:24 GMT  
		Size: 1.6 MB (1563668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf63b924d176a4f1932e72fbef5466d0e47f5e696953fd472b745859f991772`  
		Last Modified: Fri, 20 Mar 2026 00:10:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9369dbfd5bdc98b1375fba18c0fcb462fff164380f2f3353e23089daee065a44`  
		Last Modified: Fri, 20 Mar 2026 00:10:25 GMT  
		Size: 14.4 MB (14388731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6869d2abc9c5d018964ad42e67f4a3cf0b1c52bb9ae5a372c3890d22e754c43`  
		Last Modified: Fri, 20 Mar 2026 00:10:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:75f61415ac31e9d024227614734e5b1f882bd1962809a8d7167d54df1d9ea9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ca2dd91e4b70d76846e222eb7ee0d6f90a0ebc3c9f814c68a8bb2a17626132`

```dockerfile
```

-	Layers:
	-	`sha256:ce2927eac6c495b20f47149a8bd06e938f549d8cb95c191d7151d7513f09d253`  
		Last Modified: Fri, 20 Mar 2026 00:10:24 GMT  
		Size: 2.1 MB (2114083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f052e58189a7bf293e80237629eb823114744244dde59cf3f4b08bd9952f7a5`  
		Last Modified: Fri, 20 Mar 2026 00:10:24 GMT  
		Size: 22.5 KB (22495 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:465f21a7f2cde144fe7f8bd868a22f1d11fe2a82d26a6a718fb96973a93aa158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47186851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c7b39ab20f2a0ad8d58b0bfb4abefeb43b107e6d7fbc24e67ad070852e065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:07:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:07:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:08:26 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:08:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:08:26 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:08:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:08:26 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:08:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:08:26 GMT
USER haproxy
# Fri, 20 Mar 2026 00:08:26 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:08:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beda4d4a024c57e14c99aa9eaefa638ae2f714240ac7b00db3ff25a5ca930398`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 1.6 MB (1603317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae1e7aea6c1daa38ea9927ba2be76a7633343a8d41ee6ada0ec8310ae2a6adb`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5082a9b6a492beae9dffd66e39217351e53802aff3fed6bac7c3818c9b9651`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 14.3 MB (14290764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023f9131ea498b56642ecba557fbac2343a66bf1aff32059c797c614ffd06405`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:665da82de1b688772405d6153c3685bc8f7158ca3e0b6f591069278c5c61e05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e334b5eff64b62514d69b3065415c6d0546bf4437498d97af19412bbc4dc8`

```dockerfile
```

-	Layers:
	-	`sha256:1e9bd9c9bad6fee107e10bba6ba64cf04f4f7283865281c980050b439d5e1524`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 2.1 MB (2110979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3722eddaeea0690a67caa41792901f420e1659d680d0aa28f7bb7121eb78b62b`  
		Last Modified: Fri, 20 Mar 2026 00:08:34 GMT  
		Size: 22.3 KB (22292 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:bb1fdf53c4040b29bd7a74f2e5669544351404a44ae7b330a9b0e1c4ce83251c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50467299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbecc3395d776e142a0c7c945b961033cbd8fd3bf5a2cb7219497b2eb5e7b5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:19:03 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:19:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:20:45 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:20:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:20:45 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:20:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:20:45 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:20:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:20:46 GMT
USER haproxy
# Fri, 20 Mar 2026 00:20:47 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:20:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8be08ecf343f5cb5e6450fb126810370c7628b0f32c70add96ef0f793648df5`  
		Last Modified: Fri, 20 Mar 2026 00:21:06 GMT  
		Size: 1.6 MB (1639099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886932b704a6a75f33107b58d5a39dccee9939b6b01317f81cfb209221387518`  
		Last Modified: Fri, 20 Mar 2026 00:21:06 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7897eeec4ce25726c8c644c7e7a24842f27f4e04a3e6a6ea272765152bbe832`  
		Last Modified: Fri, 20 Mar 2026 00:21:06 GMT  
		Size: 15.2 MB (15233724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5300f0a95108ae9e8a3eaa44a4877bd75d8a0b34a0a29ad3898fd4762c4fa8`  
		Last Modified: Fri, 20 Mar 2026 00:21:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:3767578c1520b832e395e0101a975c196cb559e414a865c83d74451204f5f2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5159d25cb77cc6ff119f145a5fde4ab5f72d1b3c203250f6c968afea582756a`

```dockerfile
```

-	Layers:
	-	`sha256:24a2741e65189df5eaba35a9bcc905766b0169b1c82b5cb45820514bf9bcac15`  
		Last Modified: Fri, 20 Mar 2026 00:21:06 GMT  
		Size: 2.1 MB (2117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd7bf4de7406b95ad2ad434ce6b981d7c3e6ac8ba670b1152839bea437cd5a8`  
		Last Modified: Fri, 20 Mar 2026 00:21:05 GMT  
		Size: 22.4 KB (22397 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:99a93e6a2a07953d7875280623fe6a2d4beff6025d5d37cad728b3e71403c28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43625590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78482d06eb77920832c78e52fc6db78065790255928c2fb0361fb8ec014aed9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:55:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:55:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 23:27:16 GMT
ENV HAPROXY_VERSION=3.3.5
# Mon, 16 Mar 2026 23:27:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.5.tar.gz
# Mon, 16 Mar 2026 23:27:16 GMT
ENV HAPROXY_SHA256=9de6e765b426f07c1080aadd2fba5b682a1cc175fe8eb45d5eb948292a866e02
# Mon, 16 Mar 2026 23:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 23:27:16 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 23:27:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:27:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:27:16 GMT
USER haproxy
# Mon, 16 Mar 2026 23:27:16 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 23:27:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f1ab55edf0343340d10d9e190f592772a6aa472dbec939a28458d486f4818e`  
		Last Modified: Mon, 16 Mar 2026 23:11:51 GMT  
		Size: 1.5 MB (1535446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615603a22644b30ca863396c7eeeef1590c57f033d6fbdcc6fcf03ae4a1e2851`  
		Last Modified: Mon, 16 Mar 2026 23:11:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbc1ce30f857714e8a1bcba53c665aa865ca3c795e4edeac573730681bd3375`  
		Last Modified: Mon, 16 Mar 2026 23:28:24 GMT  
		Size: 13.8 MB (13812868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18b290c04f4e4d22cbdd984960802a37c666d3cd7272410e7e370a1207bd7b3`  
		Last Modified: Mon, 16 Mar 2026 23:28:22 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:77b5a9bd54a8894a88476d7b4b4b533ebb17c9755a035523536125258a27f9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0057ea835ab7298779d46f9bc94949935f8b9872ab0723835f05b6a1d1217d`

```dockerfile
```

-	Layers:
	-	`sha256:7136cc98e734c29be067383c57ad6aaa59f99f7c3b0d4ee5a70625e7aa7b4f31`  
		Last Modified: Mon, 16 Mar 2026 23:28:22 GMT  
		Size: 2.1 MB (2107735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd16a7b99dca916a31d856922e41823bd97fdbe40303a4125cc0203be8e8fdb`  
		Last Modified: Mon, 16 Mar 2026 23:28:22 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:adc80b1123ede6a82bfe8cdcd2d5f026552a340fe57d71028b724559cba9982c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46330270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13ca67fc968a850902dab7e7282c9af840305d6f627126042b19f058d06ba4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 00:07:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 20 Mar 2026 00:07:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 20 Mar 2026 00:09:00 GMT
ENV HAPROXY_VERSION=3.3.6
# Fri, 20 Mar 2026 00:09:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Fri, 20 Mar 2026 00:09:00 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Fri, 20 Mar 2026 00:09:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 20 Mar 2026 00:09:00 GMT
STOPSIGNAL SIGUSR1
# Fri, 20 Mar 2026 00:09:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:09:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:09:00 GMT
USER haproxy
# Fri, 20 Mar 2026 00:09:00 GMT
WORKDIR /var/lib/haproxy
# Fri, 20 Mar 2026 00:09:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d19291eaa883f14f8459e108a28ebcc622f1f53d73e1a2716b7b812cf4e4a09`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 1.6 MB (1599892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8070a81db975a72748d228f8aeb55a537404cd4c5a7d3a0f0fd5bdf2585a2e6a`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6283ca2777578217e2c5a8cdf5c80b96b79779872362be4c34d5b298da4bd0`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 14.9 MB (14893474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3814b77464bca30dc616dcce1c91574fc8bd13d7e19e412458de825f80bb7c`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b446a23c25c99fcf734276c4b0d60a1b5f5805bba981ab207db48512b9cdaa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ae7855ce140a491756057afeaa76e9dc5ff4d5b607048755040b545a0bb158`

```dockerfile
```

-	Layers:
	-	`sha256:b2f6906a7d29ba1f0a05e87d9072e40c9e2b9e9d1df9d36a89af9b5bc0764d5f`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 2.1 MB (2115242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af7bdc2519441124f8dd1c3b5478f4a0fff02cdb28d79dfd631802bd664cff7`  
		Last Modified: Fri, 20 Mar 2026 00:09:12 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json
