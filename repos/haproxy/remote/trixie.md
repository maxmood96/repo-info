## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:771a5bef8d654d4cb38f435a35fe0d36fa780efbcc4407f567440be3a6b75696
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
$ docker pull haproxy@sha256:c85a446271ab0a83190e5959f184f810077fa859a750dcb3a7157852092e898b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ec315b61fa7d4ce9b201e32ed887ec750f39ad5c5bec25c981278b585181a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:16:09 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:16:51 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:16:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:16:51 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:16:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:16:51 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:16:51 GMT
USER haproxy
# Mon, 29 Dec 2025 23:16:51 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:16:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c8da3e2ce5d90a5d4d1bb6861c6afa22af5efa03f96a3a4d705d9d9a97f811`  
		Last Modified: Mon, 29 Dec 2025 23:17:04 GMT  
		Size: 1.6 MB (1580896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45010fd3ab2b407281828b9a70791b6e5493761845077fa056e0a44e3fb01ebe`  
		Last Modified: Mon, 29 Dec 2025 23:16:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1847c8cf341786fb5e553a47f5526f59ade41721dbf047df2c2155b112cb19`  
		Last Modified: Mon, 29 Dec 2025 23:17:05 GMT  
		Size: 12.0 MB (12008229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f3e31691a293d43fb1c390d57f43d99f31907cb4c7264330831d20721e4e6`  
		Last Modified: Mon, 29 Dec 2025 23:17:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:735488d292f1a831804913264260ad69b4c3209a00cf8b45a6dd595a542c0dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752f2dc600c65292cd251d33b74a15a317ba58f6765b7cc4ea23ae661d147e48`

```dockerfile
```

-	Layers:
	-	`sha256:812c61d541a970a118b2e3d4c486486c5778f43e61745f694b5a615ad16b5a6d`  
		Last Modified: Tue, 30 Dec 2025 01:59:22 GMT  
		Size: 2.1 MB (2113700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4c7390d59e50eee5f0246789d57b2a3647c33d95e1faa8dd79f93c5b4c9836`  
		Last Modified: Tue, 30 Dec 2025 01:59:23 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:3b893b7a7d2ee47baff5a082e754770b7b410f053a0f1d9e234aae7f8ff70abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41596392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d25046d64747be977b792477174ac8a5f127e447341a7863ee9022b8278f5fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:16:06 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:16:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:16:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:16:59 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:16:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:16:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:16:59 GMT
USER haproxy
# Mon, 29 Dec 2025 23:16:59 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:16:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c33ba1103e43d9370a85fb48dcaf0de17a0520e62a899d8e4ae6b601d7b7b76`  
		Last Modified: Mon, 29 Dec 2025 23:17:13 GMT  
		Size: 1.5 MB (1534804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4373a798718f53cb555cc9d1acddd2687064c5f39a6b830e495d63e4c1e7bf`  
		Last Modified: Mon, 29 Dec 2025 23:17:13 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f369eaac7768fb093125dfed84621be6db307f0de5a00bc8bcd10871960be`  
		Last Modified: Mon, 29 Dec 2025 23:17:14 GMT  
		Size: 12.1 MB (12115803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fd9e03978524776d06f416329cd5b29e23628aa9109be0021a3f5c7ff7568e`  
		Last Modified: Mon, 29 Dec 2025 23:17:13 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:50cbb8eb95d02fe1a04e98adef34ab3926cca7df1af4ef5aa56ef7fb35960093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17c53f1a5adf9dfa85daaf4e01d8e129e265973ef903f5a9dd7da0b8c739d6e`

```dockerfile
```

-	Layers:
	-	`sha256:5c38d5d07971a56be14da384c35d4e4662244818cd66ef2ea466dd4a84aebfd4`  
		Last Modified: Tue, 30 Dec 2025 01:59:27 GMT  
		Size: 2.1 MB (2116680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e4b74ff5c8fcf2079480be5c244eb976d64205ba1fab22db4e249090e71075`  
		Last Modified: Tue, 30 Dec 2025 01:59:28 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4fd9ba350627f145a65cfd91424867f31132b4231e76f9a1f8e24fbe2d4d27df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f49b702ac94c73c8acefe940fe45d99bac8dd98e08fefbcbfc6a5d6a5cae6ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:50 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:15:50 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:16:35 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:16:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:16:35 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:16:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:16:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:16:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:16:35 GMT
USER haproxy
# Mon, 29 Dec 2025 23:16:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:16:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed235345ea2029c932ab60e94721ec073c6aa9dd048c816d83a90e0ee06b2ea`  
		Last Modified: Mon, 29 Dec 2025 23:16:48 GMT  
		Size: 1.5 MB (1488787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66077c6d92683943358200ca60d2a59bf9fe64a1150aca5c390b5f3cde3bc04`  
		Last Modified: Mon, 29 Dec 2025 23:16:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ce3ec70a837ca2085be81e72f6201202bc8bfc250446e87fb3293367421b4b`  
		Last Modified: Mon, 29 Dec 2025 23:16:50 GMT  
		Size: 12.0 MB (11953754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09a6ea326da699606adbf1f26d9bdc7adb9b9516cf87fddf188f7cbda24d05`  
		Last Modified: Mon, 29 Dec 2025 23:16:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2864d273110b23730e75ccb9ba02d9eaa8ffeff3dc5eba325bebf7fec7002f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd60ad462e0d5bc1685fd8088dc1264d46aa17d26b19ee17f1d76c10e4f24f9`

```dockerfile
```

-	Layers:
	-	`sha256:e03e4333edef6e00889c12213e982d1a1ef810f7bff6f0a7cd46a275e554cbd8`  
		Last Modified: Tue, 30 Dec 2025 04:58:16 GMT  
		Size: 2.1 MB (2115123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd25e653ebff773c69b4c0d741d1a59d3436663a178a60125b6d7510924e74c5`  
		Last Modified: Tue, 30 Dec 2025 04:58:17 GMT  
		Size: 21.7 KB (21725 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:01f5ab15b52ee1f03c787867112a40382035f569ea7411ef14af55b66565fc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43617334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1a00c51f100bbbd4e2c991cff54115e8a78a0d4eeacd1c47bf4c1e8b71dc14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:14:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:15:48 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:15:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:15:48 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:15:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:15:48 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:15:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:48 GMT
USER haproxy
# Mon, 29 Dec 2025 23:15:48 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:15:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f123d21eaaecfe3eb089934aa98dadf5c2ca644e14b4b56d053316bfb59ae1df`  
		Last Modified: Mon, 29 Dec 2025 23:14:58 GMT  
		Size: 1.6 MB (1563655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad3dc042b670383899b856aa5bd36d0a9e04265b3d2dfb9306a0da63cf5e12`  
		Last Modified: Mon, 29 Dec 2025 23:14:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70352cf3f4f0efea04aa9a0fd82fbc9adac822aa1f9f24f9eb933513d74d8d6`  
		Last Modified: Mon, 29 Dec 2025 23:16:02 GMT  
		Size: 11.9 MB (11913408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585a3e692dc8ee31ce79ee242f770bf13c3adf7d3a8074e9c7d62c61608e0896`  
		Last Modified: Mon, 29 Dec 2025 23:16:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e212c4aa5f238f04e44f6168c674b63b92c17e615ba7d8d5cb98cef9ea81a83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4db990127e106efe3c4addf4d745e3fddc052c35fe62faabb6467782bca2ff3`

```dockerfile
```

-	Layers:
	-	`sha256:4166e2d516fb30feeb63fd1955d0367b3867c48c25ddff2ea9a1ab63c644b93d`  
		Last Modified: Tue, 30 Dec 2025 01:59:35 GMT  
		Size: 2.1 MB (2113985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8409e52b6567f4b81eb1a88f32cedb41aba798b47a5a7f75df594771773818f9`  
		Last Modified: Tue, 30 Dec 2025 01:59:36 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:2d2a98b41f6992d799c825ee4bb2607fdd4b8f893172d5cac758e4ffaab0ff97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44702132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043b0e228c5b7b36f1b624713b14ff97dd9b5faf40d69e471cf3dd31ba77e128`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:51 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:15:51 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:16:42 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:16:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:16:42 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:16:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:16:42 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:16:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:16:42 GMT
USER haproxy
# Mon, 29 Dec 2025 23:16:42 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:16:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f168c8c4ecc0c67b4bfcab5cac7a9aacc286dbf81ba45ceb565a19eedb377f6a`  
		Last Modified: Mon, 29 Dec 2025 23:16:57 GMT  
		Size: 1.6 MB (1603093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d518279178e5b2876f7ee446e7a3d1bbb765d05a31505f3ab25fe271e6e008d`  
		Last Modified: Mon, 29 Dec 2025 23:16:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aecbed722c16911519011b74be0b1fa0bbdc5de024e84a147f965534250a066`  
		Last Modified: Mon, 29 Dec 2025 23:16:58 GMT  
		Size: 11.8 MB (11804299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8fb87ec627236a0c36e8c0953acfd42fd77bf3be7972b29e02776cab59fd24`  
		Last Modified: Mon, 29 Dec 2025 23:16:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:62426ee637051c76315915db480514251b451465a834226c55807a443dc97549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e49f089477d62a9fd4736f4affe3d1413199c7006eca490f4d690be83dde92d`

```dockerfile
```

-	Layers:
	-	`sha256:3ee7551459afc3942ee1f219f1cbe34abd9ccf561c3256d29824129291f8b3a9`  
		Last Modified: Tue, 30 Dec 2025 04:58:23 GMT  
		Size: 2.1 MB (2110881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c180647dae7d7642729de797548aafe7a94b8ef33832a1bba27d8331f4c08d4`  
		Last Modified: Tue, 30 Dec 2025 04:58:23 GMT  
		Size: 21.6 KB (21557 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:692648b6fe84a63ba3a8ae4f893cb8c1d611e847411fdc89bb2caaec66abd3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47949695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76af76d4a8af1489150a7077b55cf768c2c4b82d22c9c7fa65bd4f7df1428b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:36:37 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:36:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:36:37 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:36:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:36:37 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:36:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:36:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:38 GMT
USER haproxy
# Fri, 19 Dec 2025 18:36:38 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:36:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185480bdc18ea021a0fc7f5119aae641bd26bbb0177eb9faf2ff183fe47f022`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.6 MB (1638932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c1fe78578524cbf853cfaafa2576e0205722868fb7fcd5b0011a9d050049d`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491866a51c1e8c6c69cec4b98c8794592c4d974c8079aecb71c8954cff4ee5a5`  
		Last Modified: Fri, 19 Dec 2025 18:37:05 GMT  
		Size: 12.7 MB (12712230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58162b57e5454d0308af5bb5bb58667000f0c7b01fffaa3af0a67d59018b3b99`  
		Last Modified: Fri, 19 Dec 2025 18:37:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5059f1b5a953d412c5eb42a6d60471887b3b98af2ab9cfaf9f59745e80b475d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad10ce8cac800c4089b9cc547cf48636c075a385ea58fcd3f530a909440505fb`

```dockerfile
```

-	Layers:
	-	`sha256:485c485972ecf52cd47ecf7c5cad4793d097bac75317fa853e894329ba1eaa9d`  
		Last Modified: Fri, 19 Dec 2025 19:58:40 GMT  
		Size: 2.1 MB (2117246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f161668d88fb67f7fa13cec09715e692ca49eacba92f71dfc1e9acb811bd246`  
		Last Modified: Fri, 19 Dec 2025 19:58:41 GMT  
		Size: 21.7 KB (21663 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:ffb51de2b7f6e2879f4a380872df14d290d8c9adac9b2a9aba843ef9e4b1bc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41339054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9f6beddf3ed7cc697bca701983058df690935bbaa80da79a520673f5af2b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:30:07 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:30:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 30 Dec 2025 01:58:23 GMT
ENV HAPROXY_VERSION=3.3.1
# Tue, 30 Dec 2025 01:58:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Tue, 30 Dec 2025 01:58:23 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Tue, 30 Dec 2025 01:58:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 30 Dec 2025 01:58:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 30 Dec 2025 01:58:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 01:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 01:58:23 GMT
USER haproxy
# Tue, 30 Dec 2025 01:58:23 GMT
WORKDIR /var/lib/haproxy
# Tue, 30 Dec 2025 01:58:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306661d9ddb361973108b269c5a7a80f6657e752a63c49de5f7c724708b5cb7`  
		Last Modified: Tue, 30 Dec 2025 01:44:32 GMT  
		Size: 1.5 MB (1535079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931f081a7c2f17b5783986400a9a24b12cba9370be682d4eb23cc8e328befc2`  
		Last Modified: Tue, 30 Dec 2025 01:44:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b53cc45cce51a81f9478d3e493683d2bd4a061991ae7ba3b0fa78ec5d47ed6`  
		Last Modified: Tue, 30 Dec 2025 01:59:33 GMT  
		Size: 11.5 MB (11529206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a237e041fd36adaa96ed1239e5dc3bad38369534deb3bfe8e820e08ebc26fd`  
		Last Modified: Tue, 30 Dec 2025 01:59:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b55518174b8bcf7e09b4473bea9ad2bb27bb96d63c526a324d424300e4c2d11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd8273e89bf49f189a02dae133e6c1ab2f932a76bc687da122f2cfab53d8731`

```dockerfile
```

-	Layers:
	-	`sha256:ff487d8ca6b44a97ac9c47f7dbd46bac8212b056d3afa2b183623f889af9f0e3`  
		Last Modified: Tue, 30 Dec 2025 04:58:29 GMT  
		Size: 2.1 MB (2107637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f1c409fdcb59f3c9a1c2df69e348e9f5ccf116c27aaae1196dfaed6324f517`  
		Last Modified: Tue, 30 Dec 2025 04:58:29 GMT  
		Size: 21.7 KB (21663 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:685561eff4c9eaf6d58a806fe6f70429fde463c35efc85188adb1644f86405bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43807066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da75f7b1846111f0bf76ce564b48ef38dfc86afa6d0e629fdf031b763252798b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:12 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:14:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:15:07 GMT
ENV HAPROXY_VERSION=3.3.1
# Mon, 29 Dec 2025 23:15:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Mon, 29 Dec 2025 23:15:07 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Mon, 29 Dec 2025 23:15:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:15:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:15:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:07 GMT
USER haproxy
# Mon, 29 Dec 2025 23:15:07 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:15:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214750d64bd6cca1938456e19743ad32bb86245c69dc747aef87bb3a136ec6`  
		Last Modified: Mon, 29 Dec 2025 23:15:27 GMT  
		Size: 1.6 MB (1599454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec92cd795004ea17e7e92bec2b7106f2f95c83921949c6a00dc5752c548fe22`  
		Last Modified: Mon, 29 Dec 2025 23:15:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657fa0ba0d5083267af924046bbed190ff999e32acf683a5aec7d62fde9890c7`  
		Last Modified: Mon, 29 Dec 2025 23:15:29 GMT  
		Size: 12.4 MB (12371556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bcbe1692800e9cfc99bc419402d30269254b6b58e75918b239bb7a00523fb8`  
		Last Modified: Mon, 29 Dec 2025 23:15:26 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:bfc8de150fd221867d6bb46fbc64e10dc8f8022f9cb4e4904f7b90ef53e4eefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8c14d0ebbf80447c639f2d1b8bf11ffec91e60a6b70c111a59fb7823f7b9a9`

```dockerfile
```

-	Layers:
	-	`sha256:9205c85a2b4d0676b9f50cae3d1b608869dca6ba77b01f34f479f900644aef9b`  
		Last Modified: Tue, 30 Dec 2025 01:59:47 GMT  
		Size: 2.1 MB (2115144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b70789ef175170c4c781aa748085e022a6cf4399f20c5745a6d0f65f0ed5c3`  
		Last Modified: Tue, 30 Dec 2025 01:59:48 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json
