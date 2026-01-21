## `haproxy:lts`

```console
$ docker pull haproxy@sha256:4a72e32dfd568951c0febdfa32a12c2d9de10491c34f2cf280f46d9db2635a42
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
$ docker pull haproxy@sha256:e8afd882b1399bc976b62b187113287e952fba7b1e3c8d021d207443d0bab5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44465854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c609a0b1fbf0749de15d093f3ebbb88d0e43f8de98ae3bf42c522b80f986d46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:15:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:16:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:16:24 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:16:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:24 GMT
USER haproxy
# Tue, 13 Jan 2026 01:16:24 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:16:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d424cf6b4957e3f632805be74e8e8b0a8fb0cbd5bf05262077449cd61ec9ad54`  
		Last Modified: Tue, 13 Jan 2026 01:16:38 GMT  
		Size: 1.6 MB (1580916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b64a49cca41bf3140c2a9d7fb80efd93683829766e87cb156c4c35a0f3be4e`  
		Last Modified: Tue, 13 Jan 2026 01:16:38 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc5519ee21c9e16f5a3341d287d34fa9dade629d0c273bf4ce06e156a1c5bb`  
		Last Modified: Tue, 13 Jan 2026 01:16:32 GMT  
		Size: 13.1 MB (13109618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dcaa8e42a7a38628498f122bb3461c2f86acdc3bea396ed6c691efeb9147a`  
		Last Modified: Tue, 13 Jan 2026 01:16:32 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:ef104e2e1e12d3074f70374194493d1022c09ccab061c1235e69f707e4a35429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8be9602519873ba8643ada119bce12fcc3bc2939b1cf472aa84f55d2dc98061`

```dockerfile
```

-	Layers:
	-	`sha256:22cc16a2d102ffcc0b59efd6a4f04e71254b87422669d9f68c42441dc49b878c`  
		Last Modified: Tue, 13 Jan 2026 04:59:13 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d55e9fefe621d8a9a38c4853fa6073aafd8b9f601e9dfac24968bb1fe63e68d3`  
		Last Modified: Tue, 13 Jan 2026 04:59:14 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:1963ab6544f45ccadf7e294f48325ee0521aadd9c10cd045a17a1af763053f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42730991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa31e680c92e893f0dcce54e4bdcf1d7fbd2fd8ff94c90a8ba5ca68aadf909a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:17:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:18:38 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:18:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:18:38 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:18:38 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:18:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:18:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:18:38 GMT
USER haproxy
# Tue, 13 Jan 2026 01:18:38 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:18:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c637625a63aa70823d2102ff1e74e7ba782b012a09c3a316d6e60a50477b43a`  
		Last Modified: Tue, 13 Jan 2026 01:18:46 GMT  
		Size: 1.5 MB (1534827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f7bebda5e3837773c4b4af2ad24fdf7765f5ce506316c25b67cb5ba5b9d626`  
		Last Modified: Tue, 13 Jan 2026 01:18:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4570c8946ae7d4223be1cc17b4da25bf5b077071462dff3d3615c3f1fe8169be`  
		Last Modified: Tue, 13 Jan 2026 01:18:54 GMT  
		Size: 13.3 MB (13251801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bf086af5f23c707a0a5635eb3630f0de4e0def1faa99cc1452ec41847cce5`  
		Last Modified: Tue, 13 Jan 2026 03:15:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:3fcc21b45e55bcd0c9f078c6db31107764f70679c7ff0a165c15ecfe638fbc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842222827172efc1f67eeac8da3808c2cd24ac2e98bbae3c96155a42a12d87f6`

```dockerfile
```

-	Layers:
	-	`sha256:66b4742180612e5fad3ff199757bdbe5f99b2827e2f06b7b6d7d0edcb264337e`  
		Last Modified: Tue, 13 Jan 2026 04:59:18 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae16b993067b37a3a773465b5cfe611610b86526d1ee95d431b81a2e477e4b5d`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4910007b5cd3298308f742842762c198b33bd414bf88170a4b8b46aa8430e58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40704904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81fef570aba0a2dee81f0544b2be6573b0b92eee53a2cb779fad9c23a068e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:19:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:20:40 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:20:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:20:40 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:20:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:20:40 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:20:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:20:40 GMT
USER haproxy
# Tue, 13 Jan 2026 01:20:40 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:20:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c232dc0984ba8b7763956735e68e744ea47267dfd08f3b4717d4e0ac807a159`  
		Last Modified: Tue, 13 Jan 2026 01:20:55 GMT  
		Size: 1.5 MB (1488866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace8c6921fd7756719a1ca70caf557de65b982e9c50213d0e5eb9472d76daf0`  
		Last Modified: Tue, 13 Jan 2026 01:20:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb193109df80e35d170e247235b2ffde02728acedbfd00d18af8ef874ddfaeff`  
		Last Modified: Tue, 13 Jan 2026 01:20:57 GMT  
		Size: 13.0 MB (13005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0defdf567f4992975f0ebe360c3d06fa7eeaa3156acbd3db779cfc3711cee5d`  
		Last Modified: Tue, 13 Jan 2026 01:20:54 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:e43550a9e3c4f9ed564544f59578a557f62abb00cbadf5a95758d3c76cfa2b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2040d04bd95c39c8c98494f926923e1815551131a1710ed0eb3296b7b066f2a`

```dockerfile
```

-	Layers:
	-	`sha256:f0217f080f59c8c23fb6036605bfffa8fc8825c2f84747ea8c3ec5223e8bec24`  
		Last Modified: Tue, 13 Jan 2026 01:20:48 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f70f6181d0386267e8288d45b284ba0363697508c921e301cf0e4ebbecff3b`  
		Last Modified: Tue, 13 Jan 2026 01:20:48 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:70ed6dbbf9dd9841831f949eacf5f3728d3f60349b090cec31121cf22290cfc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88340f273907efdd61fa70d4ef6898cc5d546fdd80be2f9722a51c06e1097cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:00 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:16:00 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:16:43 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:16:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:16:43 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:16:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:16:43 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:43 GMT
USER haproxy
# Tue, 13 Jan 2026 01:16:43 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:16:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b16d218da7f2beea9af31479ea81c147754927313e45ea1f1f042a0f30e066`  
		Last Modified: Tue, 13 Jan 2026 01:16:57 GMT  
		Size: 1.6 MB (1563681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf0f79f762cc6b423342a4bc59d5d52fda3f535d359662b9539228c9de5fecd`  
		Last Modified: Tue, 13 Jan 2026 01:16:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215a349cb6c9f49125f203fe9c67a8e6d5b2d948e189a512dc09d4161db5b77`  
		Last Modified: Tue, 13 Jan 2026 01:16:58 GMT  
		Size: 13.0 MB (13016000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59941673d196de455ef4a999b52ed993b96bd676150232414ee146aa8cc9fb86`  
		Last Modified: Tue, 13 Jan 2026 01:16:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:1114d6c537dd6efd1d2daedd44ac1ec94c3f89b62b85f8c36f0af1db94ef9ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0309f55e516c0a03d1d07282742a3a1d9a7c9660f7800b5c6dcd8702505164b8`

```dockerfile
```

-	Layers:
	-	`sha256:b208d058966cf65678e2e87371bd5d3d36059d8d636a99a84941f10409a8311b`  
		Last Modified: Tue, 13 Jan 2026 04:59:38 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdbf7bf493d152b04be999a369c92a0e4fe604bd533b638e663db88b3d7a1ff3`  
		Last Modified: Tue, 13 Jan 2026 01:16:51 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:4738ce2db0707069dd4af4e0965f61e3e6ad2e375362bf3c318db95eea40c50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45697038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e36740e1b25632acb0a4765081831adafed32934f51c3961e3a9ecbfc8926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:07 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:17:07 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:17:55 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:17:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:17:55 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:17:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:17:55 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:55 GMT
USER haproxy
# Tue, 13 Jan 2026 01:17:55 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:17:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fe074953a41c2efa3b82d4a5694cfda28ff5868fb6fa0cd9496df5349344e3`  
		Last Modified: Tue, 13 Jan 2026 01:18:03 GMT  
		Size: 1.6 MB (1603061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b567e1b8a1291b87a103a7240017dc755dcfc4d44fbf499df758ec376b15a5a`  
		Last Modified: Tue, 13 Jan 2026 01:18:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be4c6bf53eea102c1c5decbcdfc839a7501072236130f867cdb95be60349a2b`  
		Last Modified: Tue, 13 Jan 2026 01:18:11 GMT  
		Size: 12.8 MB (12803863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c4175f20435178b6af212eef2cf56573a6c9362e69ce03680ab87158fbcd80`  
		Last Modified: Tue, 13 Jan 2026 01:18:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:61f83f268cc0d153aceb965c5f8377ab1ff4dc28210c8b62ef2dae5d11b295ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1924801ad88a9aa1ba945ce155c08d8c2d5d4047b09ed49fb12ee7e24c936dd0`

```dockerfile
```

-	Layers:
	-	`sha256:10be1f99303e46fb3dc7d93bfb0dc695edea57c7d325f26d58008dd42857facd`  
		Last Modified: Tue, 13 Jan 2026 01:18:03 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb782dbae3b42a366b6559f0ab895ebcfdf5d3079045fd79c05cde79a226d0c`  
		Last Modified: Tue, 13 Jan 2026 01:18:03 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6f69e4dd628dcf2e3b9602f9b2d6b8ca305f30993a58444e27a12cc5f088874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165b6d2a1219de4c38be33dff28498e2275efd46e264e17320aeb3ce980cbfc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:23 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:17:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 01:21:49 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 01:21:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 01:21:49 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 01:21:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 01:21:49 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 01:21:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:21:49 GMT
USER haproxy
# Tue, 13 Jan 2026 01:21:50 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 01:21:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd29135c936e51adf8caf7d3f0e6cf6cdb82f6390a398fb89d6fb985e597531`  
		Last Modified: Tue, 13 Jan 2026 01:19:50 GMT  
		Size: 1.6 MB (1638928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087ca31af377d1c3a213203c77c6df043d31e261426f38f3ff3a4dc133843e29`  
		Last Modified: Tue, 13 Jan 2026 01:19:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5b305eb7d432f8293a718a610223923e7dc13f22a6993240af64c406393d0b`  
		Last Modified: Tue, 13 Jan 2026 01:22:12 GMT  
		Size: 13.8 MB (13788921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3d69c4708141358275542f1bbf12dd4d5eae477f8c90aebe3333372fe3a16a`  
		Last Modified: Tue, 13 Jan 2026 01:22:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:835430476a2bac4a4871ddc5d833221a551f3963bb41692c3777afe0ae7291f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702736c519f6a879a2c3929a2d3dc7af6ced9da128cb98fa60b0d71b8e0ff059`

```dockerfile
```

-	Layers:
	-	`sha256:34fb3abfaddc1aba07e832e68a5c9a287391b656dba5970ac69001ab5007f6fb`  
		Last Modified: Tue, 13 Jan 2026 01:22:12 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef179cae582af05a255858d81709b8de86d95412827e40526e06dd99f584da8`  
		Last Modified: Tue, 13 Jan 2026 01:22:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef327ed063ab2d97771576bb92df4e7d6fdb435ee05c4e2e49e1af9e22ea41`  
		Last Modified: Wed, 14 Jan 2026 04:31:31 GMT  
		Size: 1.5 MB (1535110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b313eba330c10af5933ffa967f5e092c975c49ddddd00eadc61dce980288a4f7`  
		Last Modified: Wed, 14 Jan 2026 04:31:31 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b2f7b52cefb25983d179100008089d50f3c3bfb10663c78c41d07f0cc4d0`  
		Last Modified: Wed, 14 Jan 2026 05:03:15 GMT  
		Size: 12.7 MB (12697850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988c313247b4cfa6b64bdae9fefd4e0cc217f08f48feb5fd079ebe6289134f0c`  
		Last Modified: Wed, 14 Jan 2026 05:03:13 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Wed, 14 Jan 2026 07:57:28 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a17cc788c9df581fc1822660846ee5278e844dd5ecfd4927b3d261c19ceb4a`  
		Last Modified: Wed, 14 Jan 2026 05:03:02 GMT  
		Size: 22.4 KB (22409 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:2572f9d111100b43b797f642e6785d6210a5a1d5881dbeeb1e3935e6676a3bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44842272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f049a33ac15df923312a9da20c3cfd268111eeba9564c251dd1b5af181c388b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:10:49 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 14:10:49 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 13 Jan 2026 14:12:01 GMT
ENV HAPROXY_VERSION=3.2.10
# Tue, 13 Jan 2026 14:12:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Tue, 13 Jan 2026 14:12:01 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Tue, 13 Jan 2026 14:12:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 13 Jan 2026 14:12:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 13 Jan 2026 14:12:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:12:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:12:01 GMT
USER haproxy
# Tue, 13 Jan 2026 14:12:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 13 Jan 2026 14:12:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ba4b4334b9cf82500a762309288dc25341d41691b194a35b8add6afb792006`  
		Last Modified: Tue, 13 Jan 2026 14:12:13 GMT  
		Size: 1.6 MB (1599534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053768023ffdd4117115f3398dcabcee19be17446bdbfe0116edcfdaf7c0e15a`  
		Last Modified: Tue, 13 Jan 2026 14:12:36 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2531cb667c927c1469939b1e63abe2c09e265153403f7c96f0c83c07c8aa1408`  
		Last Modified: Tue, 13 Jan 2026 14:12:13 GMT  
		Size: 13.4 MB (13407691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b493ffb08a2c105cf12e98e2a4eae9099bb1a8c703764ecd15cea1113f41058`  
		Last Modified: Tue, 13 Jan 2026 14:12:36 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:249b7497cb402e032a70caeb23e7a9e1b734b1b117ce3cadef9f09927afb9907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b59cd52f358fc0fb9e34eee29610713186f3c72666991ad95e534690c7c6e1`

```dockerfile
```

-	Layers:
	-	`sha256:a3f86a1f9312feefdcd20fcc64d270ea397f373fba4c92c3346fd242cdb583ab`  
		Last Modified: Tue, 13 Jan 2026 16:57:32 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41722713cda53cd5b3078544a682e956ee79762d8fc78532c70a20a24e5c4a2f`  
		Last Modified: Tue, 13 Jan 2026 14:12:14 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
