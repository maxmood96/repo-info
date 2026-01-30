## `haproxy:lts`

```console
$ docker pull haproxy@sha256:4631662b3e9487286a45a122d45bc208347ff7515125466d9351aaf0c54a0ef7
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:1ee4ab6bef97860bbd21e4eea0735b13ef5ed8b8bf3d8cd8fcfe309ef39c8932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44e6901889a6e2b80b5d6478ea33ff7a02865a0b42d01d22ce390b71bda70d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:38:30 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:38:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:12 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:12 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:12 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:12 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:12 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d212cd74640a6bfdd5f0249be657c04a064206f917d20796d0bc6aa101a8d58`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 4.5 MB (4538484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd419659aed773e450b279c899f2aecd5902c817904b6fd0ad09b26e37ec898`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4a36f5607bdcf58fc5bf9e76303cf1235bf64dbbd3c1710c5233ea5398fb2`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 13.1 MB (13129639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b9ee110481f7efccb4bc123157383d085a2729fab9326075e284ba6b0e2fcf`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:2bc6ca064a4c33ba2d032f5bb1ea169562f7eaaf48bbccb100c689c38dba8682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccd989f670ced65a28877e5cb38ef2ce9db7c3e33e6ae50cf9a9721eeb21687`

```dockerfile
```

-	Layers:
	-	`sha256:fbd7d9753c3ebf79aaa047d83d4659df304c507c155cc34efb0a7f41db1875cc`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767ed1201a8cfd439bd1f3f8761ddf76eee3df9275eb291f3f56e4b0ea33e7ec`  
		Last Modified: Thu, 29 Jan 2026 19:39:20 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2122535e5ee86f4fd90a7dfe126e54b8f87e434d78e34d29cb185eccfdc3e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45122107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6df097bd2161cb990bef08a785114d1436f386af5ec8657444f46e9b3ca554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:38:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:38:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:35 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:35 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:35 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2af9fadb492d37d9d9f192eae9126ae2201e6ca324d7fba00ec4e52380c8c54`  
		Last Modified: Thu, 29 Jan 2026 19:39:43 GMT  
		Size: 3.9 MB (3908579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5829317b209b5dc77a253e5f5d4ee484d341fb0638cba037bdb0ec288e7cdf`  
		Last Modified: Thu, 29 Jan 2026 19:39:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a16e30dd187e97d3a36cae02fa61de73458f60bee68e57fbc745ee1baf76fda`  
		Last Modified: Thu, 29 Jan 2026 19:39:44 GMT  
		Size: 13.3 MB (13269165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c700ea71cac4cf2f4d2a517f17a5c605694d78b3c947aefeedbcf1cb4d8e7e8f`  
		Last Modified: Thu, 29 Jan 2026 19:39:43 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:d5414f34c318b80eb5b46536c702f5ae54fd8ae694da68a9b54867c8c23f675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa5f5a789bc3430ab1a4684f1d0ae8f7e26dbab1ee7ddc8e8da825d13622701`

```dockerfile
```

-	Layers:
	-	`sha256:e2cb0f88ee66c390239fce3a1b8fe03538bea5212a6ea2ef0eb73b7e3b95dbff`  
		Last Modified: Thu, 29 Jan 2026 19:39:43 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9dd903b19d68478fc74784cfbb733eeae7f2cd7db6d90bfd13956cd501cde8f`  
		Last Modified: Thu, 29 Jan 2026 19:39:43 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e96d65373c8e133c7bdacc77f13ca7844aa5f54053495c3d8b2adb2a955cc522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42922824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4373f6852f10f13f0022e641094b65eac9a978f8ef052bc704417ff330ad0d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:39:06 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:39:07 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:55 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:55 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:55 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:55 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:55 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e0f3a2f6bdda1aca392cd276f14f90ea61ecf47eea7b48ee7b40c87fc307eb`  
		Last Modified: Thu, 29 Jan 2026 19:40:03 GMT  
		Size: 3.7 MB (3690705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b934ae2176db544891c88cf9dbf1c6b2a4248ef7011f3026fdca080d1071a5c1`  
		Last Modified: Thu, 29 Jan 2026 19:40:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174db14dfe030898ff32a6bcf8e1e989d571e59aa0ff4f23736f564bdeaef9f`  
		Last Modified: Thu, 29 Jan 2026 19:40:03 GMT  
		Size: 13.0 MB (13021898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f87ebcb0d49da549e3159a75833b147733b62d47db36f38bd682e4c0cccb90`  
		Last Modified: Thu, 29 Jan 2026 19:40:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:2aeefd9efcc1813edc993032d7857dd95985ce813835e3cf7ffe9564a554b8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d425cbe914c0a7d3538033b211acb758c2c11b892f9082704d6040a757905571`

```dockerfile
```

-	Layers:
	-	`sha256:16bae0515b7d7f15eb98e55b8425feff26a91fe51be8f4524127adf409bc371e`  
		Last Modified: Thu, 29 Jan 2026 19:40:03 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e93079c40e59babea0d4be4cf3d40fc885a4bc81bf19eb90b62df6d6b87a40`  
		Last Modified: Thu, 29 Jan 2026 19:40:02 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:dd2d14dbf60adba65669d41c24478b9d34a7c9d5ae7313d2513b494928eb3594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48058098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca07ee59ad0501bd1171eef63e2b4048b26a29a2aaaec76119ed553da0c08d4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:38:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:38:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:38:58 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:38:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:38:58 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:38:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:38:58 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:38:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:38:58 GMT
USER haproxy
# Thu, 29 Jan 2026 19:38:58 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:38:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c489135b58642b632be22eb9063c7b0873aa959adbd2f2101aadb3f5cf57a9d5`  
		Last Modified: Thu, 29 Jan 2026 19:39:07 GMT  
		Size: 4.9 MB (4887001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773a842df67822c8686ff10083347748e5cf4b08ff8d83bd9ca9491dbba9206d`  
		Last Modified: Thu, 29 Jan 2026 19:39:06 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc28c4f1fd9d5841dc945867bafb3f16401966ac917d15d283acf4dee705c8c`  
		Last Modified: Thu, 29 Jan 2026 19:39:07 GMT  
		Size: 13.0 MB (13035411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a251b2f82c927c8e40421d3d15d64b1b03022576a53832fb692494d2034a24`  
		Last Modified: Thu, 29 Jan 2026 19:39:06 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:f68c39ab848a64716ec566e3dc6c786eb5bf29c97284829e8bb1f3265fc77e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32791dfaf4d6d16cc600be702c4dac07b0e8f46f271b5eb9f51d9fbab9dc8e81`

```dockerfile
```

-	Layers:
	-	`sha256:7ddd6ae8694a3db6176f6df56f0489a61c40f1478e691b5ff41572fbde14c886`  
		Last Modified: Thu, 29 Jan 2026 19:39:07 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf8b27d20f387cef0568a95a632f9de0df6019aea2f4f32a54affa5e2239381`  
		Last Modified: Thu, 29 Jan 2026 19:39:06 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:98a1f8e796f66eb816ed78e0e09bcc00501bb6c34b54592f7802260790908ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48601216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ba03373646cc568349406a36ebd15548306566fbd5c70a1ff38d438210a441`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:38:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:38:53 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:39:51 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:39:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:39:51 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:39:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:39:51 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:39:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:39:51 GMT
USER haproxy
# Thu, 29 Jan 2026 19:39:51 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:39:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d956c7050015bb019b69b9812cbdf45e97655950ea90b9b56564618be0d4a136`  
		Last Modified: Thu, 29 Jan 2026 19:39:58 GMT  
		Size: 4.5 MB (4491550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0263b491eae475f9588f401622d52c8ebdbd58f61eeed698f4578239a7a6d5`  
		Last Modified: Thu, 29 Jan 2026 19:39:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa4b93f02bd27072228af3eb1cbeecfaccedb2e9591cad65190533c71622974`  
		Last Modified: Thu, 29 Jan 2026 19:39:59 GMT  
		Size: 12.8 MB (12819552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8df0746f438011ceeb87e36b2777bab61511bc785c63dd4b8a1a58b4b31a1dd`  
		Last Modified: Thu, 29 Jan 2026 19:39:58 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:ee575968862f055e71132023cb30467ba5a3559f846685235ef3b0afa00e064a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d58375e3000e97a721c7b98cb9eae05e0321e2f6b0ca42ebd8ba72efefd20d`

```dockerfile
```

-	Layers:
	-	`sha256:7df0a19443bdab90615c33431e7f31ea27076f50f58e152eeecd0782cf0797c9`  
		Last Modified: Thu, 29 Jan 2026 19:39:58 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b70e28553ea69001d51e1a79a34b4eafb8873e90410eb6a6e3fd970039fcf3`  
		Last Modified: Thu, 29 Jan 2026 19:39:58 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:916c2053bbadf6f81e40ad43581dbbc7a3c2f68fc0e213162177fb28478ff411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52736903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec466c32e0c73941101cbfda4ce33580bd5ec6320de0be154f294323fe008017`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 23:13:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 22 Jan 2026 23:13:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:50:21 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:50:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:50:21 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:50:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:50:21 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:50:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:50:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:50:22 GMT
USER haproxy
# Thu, 29 Jan 2026 19:50:22 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:50:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa0b86aaffa72589a0ed3180a4e85a3287db4d843d88dcfe29e31e38af801b`  
		Last Modified: Thu, 22 Jan 2026 23:15:19 GMT  
		Size: 1.6 MB (1638943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8665a1a0095494300e3c741d5b78a6e4368d503acde3c342dc17f514741baf9`  
		Last Modified: Thu, 22 Jan 2026 23:15:18 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975a9ef8a9c16ec9d0d67aad1be53fa5238de4baba2041318ae762ec8258331d`  
		Last Modified: Thu, 29 Jan 2026 19:50:39 GMT  
		Size: 17.5 MB (17500717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e024618f043adf642307fb199f8aaf8ee05120871c173a40e8c043ee88c0d1d`  
		Last Modified: Thu, 29 Jan 2026 19:50:38 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:6a86eca2ddfb59acd1b672255e178792f369f649a2f459a96de5b00196ea090d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6560af49e0f7ab6afd6a21bc7f9c1dd09921a12e2e4d3c737078e2102025ee1c`

```dockerfile
```

-	Layers:
	-	`sha256:5f46e11577ccafa353aa5a29a6d3ca762e4ccef7dba26a99ffb1080788b67d95`  
		Last Modified: Thu, 29 Jan 2026 19:50:39 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7674a5ed9261e6d180ac69478e5ae7506c8bb80a7718e05baf8b0e5532158c`  
		Last Modified: Thu, 29 Jan 2026 19:50:38 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:b46bef925def12f4f03a995ca0b488d15116903f6f392d62a38ed9553502ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42506294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196ef661f0651174e7a0ebf2d334c3a2b138203483bfd359527154dece8b178d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 04:15:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 04:15:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 14 Jan 2026 05:01:59 GMT
ENV HAPROXY_VERSION=3.2.10
# Wed, 14 Jan 2026 05:01:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Wed, 14 Jan 2026 05:01:59 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Wed, 14 Jan 2026 05:01:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 14 Jan 2026 05:01:59 GMT
STOPSIGNAL SIGUSR1
# Wed, 14 Jan 2026 05:01:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 05:01:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 05:01:59 GMT
USER haproxy
# Wed, 14 Jan 2026 05:02:00 GMT
WORKDIR /var/lib/haproxy
# Wed, 14 Jan 2026 05:02:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef327ed063ab2d97771576bb92df4e7d6fdb435ee05c4e2e49e1af9e22ea41`  
		Last Modified: Wed, 14 Jan 2026 04:31:22 GMT  
		Size: 1.5 MB (1535110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b313eba330c10af5933ffa967f5e092c975c49ddddd00eadc61dce980288a4f7`  
		Last Modified: Wed, 14 Jan 2026 04:31:22 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b2f7b52cefb25983d179100008089d50f3c3bfb10663c78c41d07f0cc4d0`  
		Last Modified: Wed, 14 Jan 2026 05:03:04 GMT  
		Size: 12.7 MB (12697850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988c313247b4cfa6b64bdae9fefd4e0cc217f08f48feb5fd079ebe6289134f0c`  
		Last Modified: Wed, 14 Jan 2026 05:03:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:ce890a8ddbfc3f680d248ee4134747dc8b29daedf6b5349bc00711aca0220d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fca0541392a624230907deba8bb801b2107c758cbd342ac5ca2b8eb020da4aa`

```dockerfile
```

-	Layers:
	-	`sha256:324c013785c78f9127a317f30562a489aa30d91350679da9f2a83f5d52af24d2`  
		Last Modified: Wed, 14 Jan 2026 05:03:02 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a17cc788c9df581fc1822660846ee5278e844dd5ecfd4927b3d261c19ceb4a`  
		Last Modified: Wed, 14 Jan 2026 05:03:02 GMT  
		Size: 22.4 KB (22409 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:3ee5e6ea306e03a56cefa09beada667b80155abd03d80ec3ad0b5fd786862262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47459877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d959a457f63a38ff4407385680e30289052c1ae26ca750b06e52cc1cca52d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 29 Jan 2026 19:37:02 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 29 Jan 2026 19:37:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 Jan 2026 19:38:18 GMT
ENV HAPROXY_VERSION=3.2.11
# Thu, 29 Jan 2026 19:38:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.11.tar.gz
# Thu, 29 Jan 2026 19:38:18 GMT
ENV HAPROXY_SHA256=1ded04101274ae686d11f55fb3874638e79bae4211e3e8caff95ef8b1b96a54b
# Thu, 29 Jan 2026 19:38:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 29 Jan 2026 19:38:18 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 Jan 2026 19:38:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 19:38:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Jan 2026 19:38:18 GMT
USER haproxy
# Thu, 29 Jan 2026 19:38:18 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 Jan 2026 19:38:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83d17e7231e4e1e1800309500cf044cb65aa4c722edec61e350d27a898e5457`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 4.2 MB (4202060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec18d2a1a54b53e5fadcaf09b3c3ceb735283f431938af7c3855e203db24f9b8`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3597df154a515def438fe1b5303a8bb0abd4d49710e804c36d53296b314789e6`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 13.4 MB (13422763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133256517b2348fcad31699c6ed4c0d839c861cc6ce06d3a2fad3ac27c232d0a`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9624e3877b02ac4b873c4f009162146cf56ab3829cc70f77bf69cb0957f00b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f365c46afe1c4e5196d3e0e50c669a5d43504c51ca7e2d56e7fb1788c30738d5`

```dockerfile
```

-	Layers:
	-	`sha256:04f6f24cc1229e96f7d45b727a25ae283e8d9da081364cca8ab669b2180a516c`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b599c33574b85334b36ad088d9d05d6e39d6651eb6c6cd39ae8345c148847a4d`  
		Last Modified: Thu, 29 Jan 2026 19:38:30 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
