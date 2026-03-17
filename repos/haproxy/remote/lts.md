## `haproxy:lts`

```console
$ docker pull haproxy@sha256:90c986928807ee80c0a3d2ee5c8648beddbdd3575df525bad26cd4fceb4b117f
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
$ docker pull haproxy@sha256:3caccc1c0bcd473a9dc080bcc224583ca36a2269e31e8f459ee3cb62098f9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44490838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108bed99dc868f7bea6d29e115c9e952ff7dc06ace52a7f25fb58fc7a0508320`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:51 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:15:51 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:16:34 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:16:34 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:16:34 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:16:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:16:34 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:16:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:34 GMT
USER haproxy
# Mon, 16 Mar 2026 22:16:34 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:16:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8240fabd4157a1d684fe87fd510cbbe36ff429ab1fb59c82393d1fe9baa7bab3`  
		Last Modified: Mon, 16 Mar 2026 22:16:41 GMT  
		Size: 1.6 MB (1581142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53486f90731a06192b5a2f94f2dd23af4c1b139146e72461555d94f63f76f5a`  
		Last Modified: Mon, 16 Mar 2026 22:16:41 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed9a66e81b46e7a1bd019b8525eb421cdec6b08bf25a50a795d46aa5fc3c01`  
		Last Modified: Mon, 16 Mar 2026 22:16:42 GMT  
		Size: 13.1 MB (13132558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad74da9316b50d83b8f277bfecde7b91af01ce8892da03b7b6ca0c3c06af0d59`  
		Last Modified: Mon, 16 Mar 2026 22:16:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:85778a9d1c28cf7b66859c62fccaaf41c0a949e9a3acb0c92ed2545bf250f9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a99029baeab07f58f8193bf63f8ae35da9811f26cd520a9a47e54b215c092c`

```dockerfile
```

-	Layers:
	-	`sha256:e8e48daab223cdfb5c71b8ab4018a7990494af970036974e8210c68b526d68d7`  
		Last Modified: Mon, 16 Mar 2026 22:16:41 GMT  
		Size: 2.1 MB (2113806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6dcc695a27f1fde26516e015b6cc9ec5d8e144b4e4ae4c520f9e27ad8d843d`  
		Last Modified: Mon, 16 Mar 2026 22:16:41 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:7220805ea36befc1e466178b428a979e5ef1f1d5c36ccb567f90eb653aaf19c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42759069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed334e4a88259c316873aa47d9db91008ff511bb01e440bcc012008137b6b179`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:37 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:16:37 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:17:30 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:17:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:17:30 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:17:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:17:30 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:17:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:17:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:17:30 GMT
USER haproxy
# Mon, 16 Mar 2026 22:17:30 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:17:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f772bdb2340efaf9c2422a66b2e56fb013fd583fdd00fb01dcf5bbc104c1f614`  
		Last Modified: Mon, 16 Mar 2026 22:17:38 GMT  
		Size: 1.5 MB (1535714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf225f5d69f1dbf93913c279b0bf340a4f85ddfe2d6d0f1b4e02ac39a2d4e53`  
		Last Modified: Mon, 16 Mar 2026 22:17:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79046ce10f47a3ffd46f4de065056a99718183e29fc756b09f05cf765deacdf`  
		Last Modified: Mon, 16 Mar 2026 22:17:38 GMT  
		Size: 13.3 MB (13278067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942b6e5b2625c415dc2a2a442acfa43ea76d5b26e4aeece5e96ec78e7900988`  
		Last Modified: Mon, 16 Mar 2026 22:17:38 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9c2c4fa1bb968dc4f1841da096fdc484cc9bd1d4043f48397aec5c6783dcdd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7215370078ac7b71f9c4c47a414bc44125a08ada533c4ea0daa33cc7e6d083a4`

```dockerfile
```

-	Layers:
	-	`sha256:d9fa25a41f974da6e8cffe70daf86de289f5c07f39dbc4ce12e7226b0b41a41e`  
		Last Modified: Mon, 16 Mar 2026 22:17:38 GMT  
		Size: 2.1 MB (2116786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e39d4a0e5759c2980c0b2292338beec1acd4bf631aae35cb667f557f9da4d0`  
		Last Modified: Mon, 16 Mar 2026 22:17:38 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:64aa5ff8e7f3668e436a3ae44c0033d4527f59c44aeab8102cdb5646f5e2ccbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40735490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736f87a778ed4084bd926e4aeeac419dce7e8d85a2ca1f42f78b27ef5685323d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:18:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:18:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:18:55 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:18:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:18:55 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:18:55 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:18:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:18:55 GMT
USER haproxy
# Mon, 16 Mar 2026 22:18:55 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:18:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316c21bd73ad103a3e2a5dfb82119fab5ae8e43020609c430a8b31d093d32a37`  
		Last Modified: Mon, 16 Mar 2026 22:19:02 GMT  
		Size: 1.5 MB (1489558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa389763a08c96bb69bb36449fb1508aff5b77df2e3ae51b0726bf302b3820`  
		Last Modified: Mon, 16 Mar 2026 22:19:02 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e4c491c9346c6fbc45c5ade0e913ef76bf557beddaeecfe26c209026d5949c`  
		Last Modified: Mon, 16 Mar 2026 22:19:03 GMT  
		Size: 13.0 MB (13034789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9742c70a849bdb27c0cf28d282cd8880a5401f32654c5a7230d2adeae11fbf0`  
		Last Modified: Mon, 16 Mar 2026 22:19:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:459ec8d7201bcb8ec3f28fa84daf84db75f4fdbf2f477d2a25e67e6dcd1cb347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2109efcc9e436f7abbbf66f798768ec48451c35640aa1c14a62969fa6779976`

```dockerfile
```

-	Layers:
	-	`sha256:d56f619a72fa33885e137c2970961c156c7b1034c59e0722712f18b0053638f5`  
		Last Modified: Mon, 16 Mar 2026 22:19:02 GMT  
		Size: 2.1 MB (2115229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d315a9aa745daf2a0193cb907b7345a6db1cadc0e6de535b10fb4ae7ddad16ba`  
		Last Modified: Mon, 16 Mar 2026 22:19:02 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:391e84360ff3fceb1562a37e062b570ed0c5909e94a1a8ac6c4e72768d303fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44744858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2245dbbc5f3eab07e4fa26fa096cd8ad8896d7c15c7a0e60a239d839597ae30a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:15:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:16:41 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:16:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:16:41 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:16:41 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:16:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:41 GMT
USER haproxy
# Mon, 16 Mar 2026 22:16:41 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:16:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf189bfeb5bb0fe8b4552bb6f055c0ce8d33e59a6a947499abc8626131b4683a`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 1.6 MB (1563671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174925477ca12217d0cb5f7294d91ee24b46aaa10213e6ba696da83b95590ae`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9651b5b5d271c2a80ba9d7d77c9a977acb2524156d84b460cffd36bdad05f08b`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 13.0 MB (13041134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674181ffd2dfb0b36b916d7f060bca98b57358c072cb5ff224850244212af68`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:6830b3820c3c8115a5e588100c9b0b2d05823cad31a2bf2de0660c9e00f1c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810f85937f6db40178b1e94d9776b47b09ad1fff7ec6d7241b543f05b303d6fa`

```dockerfile
```

-	Layers:
	-	`sha256:729dbe86cd2f0cce801f5758d53f92351e283888ea80074b872779f8a392fdee`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 2.1 MB (2114091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2110b5e7e4e340236f8f4d7dd1c9a0291fb4211bfc5cb4a4f532c4d1a19d6c`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:234fc20b6421dd182f921e1ccc26497b30bb7671c7674f28a9df7d161b9524ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45722141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26d4bf49fdc871625e793dd743de31c37ae91816c3f695782ad213ffab03bd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:15:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:16:52 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:16:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:16:52 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:16:52 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:16:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:52 GMT
USER haproxy
# Mon, 16 Mar 2026 22:16:52 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:16:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83466fd2b41e9db6f264876ce148cc85cdc74450204170a1ec377f54f8b04d43`  
		Last Modified: Mon, 16 Mar 2026 22:17:00 GMT  
		Size: 1.6 MB (1603314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174925477ca12217d0cb5f7294d91ee24b46aaa10213e6ba696da83b95590ae`  
		Last Modified: Mon, 16 Mar 2026 22:16:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d62be6afee16579952ccaded9e428ee98cd32db866124afd203fc7bb828ef`  
		Last Modified: Mon, 16 Mar 2026 22:17:00 GMT  
		Size: 12.8 MB (12826058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66898381914a9d7414b4b9b58b790cc89283b6473ef8ba06b3a9f617b33f61c`  
		Last Modified: Mon, 16 Mar 2026 22:17:00 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:0051abd64320be69e4dbaac8bb52c12cda62b9df015fd3522f0a39a3ed8fcdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20619ba5ccb439c66eab14f4b17ec2254d0789ed82e4d42d2e093019b9d074a7`

```dockerfile
```

-	Layers:
	-	`sha256:cb97a1e0b329d8a03b8b60e333514be3f824c72be1ffcb439d7afc73b5361c3b`  
		Last Modified: Mon, 16 Mar 2026 22:17:00 GMT  
		Size: 2.1 MB (2110987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5201a403ec7708102531bc6d43161103f7805c21a6b7f9ee65e05601e5779299`  
		Last Modified: Mon, 16 Mar 2026 22:17:00 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:f21f589dad2a6c7c0ffb4fd94f8c23d45de5aa137436254ab50758d9faec7501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49072348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd421501cda9daecded15f29579e39a35dca1f56429bc5f6ae97a6dc76498acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Thu, 05 Mar 2026 17:51:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 17:51:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 20:16:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 20:16:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:16:40 GMT
USER haproxy
# Mon, 09 Mar 2026 20:16:40 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 20:16:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a512800400158a521cd6324ecbeca708089d7bda87efc9521342ea8da8b39`  
		Last Modified: Thu, 05 Mar 2026 17:53:28 GMT  
		Size: 1.6 MB (1638778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80dfee41595e422fd3eb516690027fa831c5e35f049040fda219efd0f3225a`  
		Last Modified: Thu, 05 Mar 2026 17:53:27 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17745c8c660d55926fb1b4fe5107256ed6cb734959ed8fb41ccd80881f662d5e`  
		Last Modified: Mon, 09 Mar 2026 20:16:54 GMT  
		Size: 13.8 MB (13831710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa071e7e39f72070553df304309ae80d25da980b9d4c2ca337f2704fb878e56`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:0dc04c618c353cc142db7456c1fd0083c46d05a2e98cfa827ae895f27418d814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e03f2cd52fd27ed1212be8b0abde86d6c37eca7fcfd1e80080a0301c91ee867`

```dockerfile
```

-	Layers:
	-	`sha256:c8c88dd796e540d9f34c1d552befb4fbde876c90e94dc9826853901985689ef1`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96da89a6901f17bdb9c81c5f5c6b89accbcb2400006c30885c603b723caf6f36`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:ff017e46507135bc7b5fcbc31ca3c1fa5e5336b7baa46c9a86f311d20bc11d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42548454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9eddfb0d52993a07d5c5d0a56212d7b1cd6de1c3fac7dae9d69fe93b5242ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 10 Mar 2026 03:05:52 GMT
ENV HAPROXY_VERSION=3.2.14
# Tue, 10 Mar 2026 03:05:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Tue, 10 Mar 2026 03:05:52 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Tue, 10 Mar 2026 03:05:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 10 Mar 2026 03:05:52 GMT
STOPSIGNAL SIGUSR1
# Tue, 10 Mar 2026 03:05:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Mar 2026 03:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Mar 2026 03:05:52 GMT
USER haproxy
# Tue, 10 Mar 2026 03:05:52 GMT
WORKDIR /var/lib/haproxy
# Tue, 10 Mar 2026 03:05:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96667720c6f66d54c4069d1f4a90a9b99842eca810ad17a3c151ac557902e5f5`  
		Last Modified: Tue, 24 Feb 2026 21:12:01 GMT  
		Size: 1.5 MB (1535095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1449ff18173ad675507b1278e800bb7a82b1db725d4424087ede9e6b7dd711`  
		Last Modified: Tue, 24 Feb 2026 21:12:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7f2a13b4b339a23416884a847cc619ebef1b648244e84a21608d0bbdb2c120`  
		Last Modified: Tue, 10 Mar 2026 03:06:58 GMT  
		Size: 12.7 MB (12735301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df73e327897442dedd42208d1b6d045a3e0ddf3acf18da7e2586c69cde05a8`  
		Last Modified: Tue, 10 Mar 2026 03:06:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:7c0a7fd01ddcd0c8284fff365351b71e1c7ce97ac1d9312e84d2136f2c358006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4855f14b1e7bbcaee367dadbf4d6569112b09617fa696634087451a31c4e79a`

```dockerfile
```

-	Layers:
	-	`sha256:1671d93b8eca687f5a5bb73ec8d3c45ddd0ba58947cb6e948d8e7b8f5be6b110`  
		Last Modified: Tue, 10 Mar 2026 03:06:57 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23d474e040a71af7d59fe005e20131904332e80cbd12f6217462701f0d64e92`  
		Last Modified: Tue, 10 Mar 2026 03:06:56 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:76dbd6c51eb71317d7da6cf5f4f8e7f0954083fe5c7fd61750cab9892ed33e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44869436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77791fdb380a0a154f72830cd3752bc71c7eeabdcbe278ff19e1cb0959fe52c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:36 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:16:37 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 16 Mar 2026 22:17:43 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 16 Mar 2026 22:17:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 16 Mar 2026 22:17:43 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 16 Mar 2026 22:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 16 Mar 2026 22:17:43 GMT
STOPSIGNAL SIGUSR1
# Mon, 16 Mar 2026 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:17:43 GMT
USER haproxy
# Mon, 16 Mar 2026 22:17:43 GMT
WORKDIR /var/lib/haproxy
# Mon, 16 Mar 2026 22:17:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc085f7e86be3e38367fe6017b634639132a8e40c93dbf0459a8b6d65a1d478`  
		Last Modified: Mon, 16 Mar 2026 22:17:57 GMT  
		Size: 1.6 MB (1599849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf225f5d69f1dbf93913c279b0bf340a4f85ddfe2d6d0f1b4e02ac39a2d4e53`  
		Last Modified: Mon, 16 Mar 2026 22:17:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383175b998971f6a9d3dd36b5718802059550946f526498ccf423ca8dc00f624`  
		Last Modified: Mon, 16 Mar 2026 22:17:57 GMT  
		Size: 13.4 MB (13432685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8255f307d19eb1a65b40b6f18875f827e6a21e379c4aeb83df061f292b9de0`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:e0f9da10cc6c9f3a2e3401d4d10b09bf82774ee8b63982bce7d11a1de38da315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7a8dede640c6387783ea7bcea07220ae1eb2723c4043914f7a9b83353aec69`

```dockerfile
```

-	Layers:
	-	`sha256:b44bf5d1e1623581e16496f046344a651009c6a24d93872da082c6479d9639cb`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 2.1 MB (2115250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d250574e3ba2c4d773b5eede7b6df8dbb27e3ff33271e42b6b9a0198bf0fe5`  
		Last Modified: Mon, 16 Mar 2026 22:17:56 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
