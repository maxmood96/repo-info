## `haproxy:bullseye`

```console
$ docker pull haproxy@sha256:41fc92598bfb514d6f797e5ed74f15924ed4703037c1465ab05757813e91a455
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

### `haproxy:bullseye` - linux; amd64

```console
$ docker pull haproxy@sha256:589ce62c065455e5b2515053e231213e660afdc1e6dc8bf64d56ba2c45b288c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9156375cc8d516c9d505c1b62882a4aebda96d0a0df3a7a22a380fc09f9404c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:05:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 02 Aug 2022 04:06:40 GMT
ENV HAPROXY_VERSION=2.6.2
# Tue, 02 Aug 2022 04:06:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Tue, 02 Aug 2022 04:06:40 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Tue, 02 Aug 2022 04:07:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 02 Aug 2022 04:07:13 GMT
STOPSIGNAL SIGUSR1
# Tue, 02 Aug 2022 04:07:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:07:13 GMT
USER haproxy
# Tue, 02 Aug 2022 04:07:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cfcc587b51e8abe185be61cf2d5240a02be462c6a4b5ab7e9c5049caf8ad14`  
		Last Modified: Tue, 02 Aug 2022 04:11:45 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d777e6f63af06f96d7a639daf8dfc12a1a231c0cf7766ee31cf4f97207507`  
		Last Modified: Tue, 02 Aug 2022 04:12:04 GMT  
		Size: 8.0 MB (7972753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ba30e63c6ea2475c3f5d8d43cfb866eb704cfc298c7773b24e2b32b4ef1c4c`  
		Last Modified: Tue, 02 Aug 2022 04:12:02 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:ead7eb508fa118fdf3a270fa2f34f6add1c0234e2dbaf5e6264c78b661475b42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36778775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b158ecb3534c3b945f718f41609bab4f1bb56b3e2fc68d26c8886c9d0953f0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:37:14 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 02 Aug 2022 01:38:52 GMT
ENV HAPROXY_VERSION=2.6.2
# Tue, 02 Aug 2022 01:38:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Tue, 02 Aug 2022 01:38:53 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Tue, 02 Aug 2022 01:40:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 02 Aug 2022 01:40:19 GMT
STOPSIGNAL SIGUSR1
# Tue, 02 Aug 2022 01:40:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 02 Aug 2022 01:40:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:40:19 GMT
USER haproxy
# Tue, 02 Aug 2022 01:40:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f67b2a193c438461f5e8418669ac2522b5ddac11fa75bf91ccaef940fe2cc`  
		Last Modified: Tue, 02 Aug 2022 01:49:22 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e121da5cf36319d20fa928b1fc22e92a4da732ca485bf7a7382aca8c6375e`  
		Last Modified: Tue, 02 Aug 2022 01:49:43 GMT  
		Size: 7.9 MB (7871374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff8cae24b4276c0e6859b5d4d250bcc7c50c0caa40dde8eb4d4377c18bd7317`  
		Last Modified: Tue, 02 Aug 2022 01:49:41 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:44d3688c68a26040df2434bf7d500956b7df4fb143618e7502a9bf698f91be7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34290233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cea18a92cffb2fb6167b96d2eb2bac9e10ff2366ec1b224e8a1561bc1c9fbd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Fri, 29 Jul 2022 19:27:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Fri, 29 Jul 2022 19:29:54 GMT
ENV HAPROXY_VERSION=2.6.2
# Fri, 29 Jul 2022 19:29:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Fri, 29 Jul 2022 19:29:54 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Fri, 29 Jul 2022 19:30:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Fri, 29 Jul 2022 19:30:53 GMT
STOPSIGNAL SIGUSR1
# Fri, 29 Jul 2022 19:30:54 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 29 Jul 2022 19:30:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Jul 2022 19:30:54 GMT
USER haproxy
# Fri, 29 Jul 2022 19:30:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2abe2126b60566bd38b21e72c7a891a9c1253df6d3d685cb77bf56bb3c98219`  
		Last Modified: Fri, 29 Jul 2022 19:50:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc08de299be7ca09f28f10bc7c737dac93a81b341d5c6fba73ee72878cdc5149`  
		Last Modified: Fri, 29 Jul 2022 19:50:51 GMT  
		Size: 7.7 MB (7727785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989f7755b97ab37b958440bcd83896e9f6e408c81decd25ea75088942c2f58b1`  
		Last Modified: Fri, 29 Jul 2022 19:50:49 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:a0a725c5821655eb91d95c55f6af1dd09b3c09518532801805905df8c00896bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38041961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d23690ecceee42925d7ab1c4448feba4abe8a64305921b1396819ff4d000c2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:15:53 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 02 Aug 2022 03:16:41 GMT
ENV HAPROXY_VERSION=2.6.2
# Tue, 02 Aug 2022 03:16:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Tue, 02 Aug 2022 03:16:43 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Tue, 02 Aug 2022 03:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 02 Aug 2022 03:17:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 02 Aug 2022 03:17:13 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 02 Aug 2022 03:17:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 03:17:14 GMT
USER haproxy
# Tue, 02 Aug 2022 03:17:15 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c78f434ad963a51aa8df3906f3d85402d0f8bad43144f183d459008327ae130`  
		Last Modified: Tue, 02 Aug 2022 03:23:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e5cd70710c935545641615d6e55528eef89f51d5119ebae39abcef12d3f375`  
		Last Modified: Tue, 02 Aug 2022 03:23:40 GMT  
		Size: 8.0 MB (7985915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aebbbe9f85f5343c25b52c557e958809dde59d8867789db29494b956545e41f`  
		Last Modified: Tue, 02 Aug 2022 03:23:38 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; 386

```console
$ docker pull haproxy@sha256:6b25d8efee1147a0db62c4fb332f82614582fff0e5a0c8f200023f4159e2e5d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40130223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaaa8c9956ecf0a480b404c821a41be2029e632d9384746bde284c1f2395c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:52:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 02 Aug 2022 02:53:00 GMT
ENV HAPROXY_VERSION=2.6.2
# Tue, 02 Aug 2022 02:53:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Tue, 02 Aug 2022 02:53:02 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Tue, 02 Aug 2022 02:53:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 02 Aug 2022 02:53:36 GMT
STOPSIGNAL SIGUSR1
# Tue, 02 Aug 2022 02:53:38 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 02 Aug 2022 02:53:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 02:53:39 GMT
USER haproxy
# Tue, 02 Aug 2022 02:53:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a380c96cfea544a4d7f868e08c9412e23fbdf473e4fffd4a23855e3452d663e`  
		Last Modified: Tue, 02 Aug 2022 03:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d54a18fcd53eb985cf0c288ee911155a2725d25158ca327cab4c67214a36d4a`  
		Last Modified: Tue, 02 Aug 2022 03:00:42 GMT  
		Size: 7.8 MB (7754431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c7471d3805816bf142483aa62ac71fbb25edff8386c3d5605137c15c20b98b`  
		Last Modified: Tue, 02 Aug 2022 03:00:41 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; mips64le

```console
$ docker pull haproxy@sha256:d3664d0eae325fd391be1f869b427c72a4381f651ef208539cdcfb647acb503a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37720626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1cc3449ef25e2c1b3b10adac8e19a26b0e9a9275ab15a09d9bed74d79a01da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:36:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 02 Aug 2022 02:40:30 GMT
ENV HAPROXY_VERSION=2.6.2
# Tue, 02 Aug 2022 02:40:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Tue, 02 Aug 2022 02:40:34 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Tue, 02 Aug 2022 02:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 02 Aug 2022 02:43:47 GMT
STOPSIGNAL SIGUSR1
# Tue, 02 Aug 2022 02:43:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 02 Aug 2022 02:43:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 02:43:53 GMT
USER haproxy
# Tue, 02 Aug 2022 02:43:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d45cc2bb9d4dd6d083acc14be458c29169097e7c9d08a4e59ba21aac1cf4026`  
		Last Modified: Tue, 02 Aug 2022 03:02:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c9e59d6c7fb50d1b4d696750e5416c909260dbf07778cccfc90ad674d687ae`  
		Last Modified: Tue, 02 Aug 2022 03:02:48 GMT  
		Size: 8.1 MB (8089913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b862f9c2865a15b7cd91c17d058f61e6678a0f7e2823063e281955f76400074`  
		Last Modified: Tue, 02 Aug 2022 03:02:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; ppc64le

```console
$ docker pull haproxy@sha256:06e3ce8c7eb8937bbaede5853795c117b997d03ba7979e2c7e83a7733f71982a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43645514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3408ade565f4c2c3fb3059d8032394633b9f161787f3185fba6958fe107d88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Thu, 28 Jul 2022 22:16:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Thu, 28 Jul 2022 22:18:35 GMT
ENV HAPROXY_VERSION=2.6.2
# Thu, 28 Jul 2022 22:18:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Thu, 28 Jul 2022 22:18:36 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Thu, 28 Jul 2022 22:19:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Thu, 28 Jul 2022 22:19:21 GMT
STOPSIGNAL SIGUSR1
# Thu, 28 Jul 2022 22:19:21 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 28 Jul 2022 22:19:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Jul 2022 22:19:22 GMT
USER haproxy
# Thu, 28 Jul 2022 22:19:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390dd9d95ff39603c72fca171eb0e756481c50bb7b2aa4e81b5edfa6f210ecb`  
		Last Modified: Thu, 28 Jul 2022 22:32:11 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77016985427b8d3b851d113556608b43042b0bbb8fcc0e09cc6351229c84fb06`  
		Last Modified: Thu, 28 Jul 2022 22:32:55 GMT  
		Size: 8.4 MB (8371126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc4ee686ad6dddce2f7d3187af54c1691b9e228761c956b573d9808d90c93c`  
		Last Modified: Thu, 28 Jul 2022 22:32:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:bullseye` - linux; s390x

```console
$ docker pull haproxy@sha256:607b7e3db947232601fa0576fca4f85cbab0c0358015abbb048962920929efd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37622637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad22f1b72163870fb9cbccb29cf4343e103a005d3f7255ce764a886f153d242`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Jul 2022 00:43:45 GMT
ADD file:70135711d42f7b2b32586e31afb57a0590019326efa82abf1402dc7a8f02a3f2 in / 
# Tue, 12 Jul 2022 00:43:49 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:10:20 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Fri, 22 Jul 2022 18:42:03 GMT
ENV HAPROXY_VERSION=2.6.2
# Fri, 22 Jul 2022 18:42:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.6/src/haproxy-2.6.2.tar.gz
# Fri, 22 Jul 2022 18:42:05 GMT
ENV HAPROXY_SHA256=f9b7dc06e02eb13b5d94dc66e0864a714aee2af9dfab10fa353ff9f1f52c8202
# Fri, 22 Jul 2022 18:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Fri, 22 Jul 2022 18:43:14 GMT
STOPSIGNAL SIGUSR1
# Fri, 22 Jul 2022 18:43:15 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 22 Jul 2022 18:43:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Jul 2022 18:43:16 GMT
USER haproxy
# Fri, 22 Jul 2022 18:43:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:447abc12b0c6da6e339b4fa17a2a7dd672d6f0631d30ee44c28b8b06e78884bd`  
		Last Modified: Tue, 12 Jul 2022 00:53:41 GMT  
		Size: 29.6 MB (29640209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80854fd4dd6dcc0dc1a9df241e17f4a6984c0a21dd7e60d6822b31f397931bb9`  
		Last Modified: Tue, 12 Jul 2022 02:23:49 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb3e02025ef13cebe18f7477545b8776059aaf6b2345f37674a5c32c09f5430`  
		Last Modified: Fri, 22 Jul 2022 18:48:47 GMT  
		Size: 8.0 MB (7980542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2b6014dc80be7b190172c6ca6265e696e1a2c2c1b72263bcba2cb37c7a3b88`  
		Last Modified: Fri, 22 Jul 2022 18:48:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
