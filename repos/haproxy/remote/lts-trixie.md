## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:fcfb4c1a1cda3bf7135050b260208f6f23b409d1d96ee42366584764595396e5
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

### `haproxy:lts-trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:f65519e702d23db92ac46f2a4984445c625d5b7ec029549ad6a81f43b7c85567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44490946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0336ab7a54059a3801a347fff20cf93584a4f2732ca8a7f11b35f8be9bce96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:53:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:53:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:53:47 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 18:53:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 18:53:47 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 18:53:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:53:47 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:53:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:53:47 GMT
USER haproxy
# Tue, 24 Feb 2026 18:53:47 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:53:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9290414500ec65a4a34f4150c04a41f9c9557a7fc0ac0c3cd9b436fa20b6c718`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 1.6 MB (1580887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c2bd964478dfe25135af7797c05e9bc0abd36e059339718788d10ea5fa7310`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656cd48975440fa7eebcdd632be828634e853db795e9c510fde3c800b05c4030`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 13.1 MB (13129785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171a8a6df072aae7758498bd586dfd325c11e3840933bbc9fb00ae7c4774d2c7`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc33d982e6dc2fd3a9e0ea6d60808ab01335a2eeee538e9afa4d3e129a3883fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf886035263323aa713df5ebc6a12b8c8843b7e60a0e56ad938c02bbf3ed3022`

```dockerfile
```

-	Layers:
	-	`sha256:de75a0ad0f2555638519e57e60e7b8a96f5a6ae989caebc8123a0a25f342e002`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9ae290f7079e6b6cf1be24de322dbde9b56a9eab39c09a1be8ef7666be9775`  
		Last Modified: Tue, 24 Feb 2026 18:53:54 GMT  
		Size: 22.3 KB (22349 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:af08692089ee83cfb3ac0fa154a96076214711196a4fcc9a8ad3a23d363a627b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42757962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868389370f28b1c706402cb75e86b767b724250fd245b1d5705fd8d737b5f508`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:57:04 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:57:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:58:00 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 18:58:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 18:58:00 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 18:58:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:58:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:58:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:00 GMT
USER haproxy
# Tue, 24 Feb 2026 18:58:00 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:58:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866b8b217ab5ae8f60c1f67924ffc1b5570db4cdf679f488ca9c7aa889cdc787`  
		Last Modified: Tue, 24 Feb 2026 18:58:08 GMT  
		Size: 1.5 MB (1534875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4535ec4eaaf15d8f9b4aa08522a3bfc572ed713f98570825c173df17b9fc4f4`  
		Last Modified: Tue, 24 Feb 2026 18:57:54 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5006eb6bf171e307a6970c29ed075f06f98a383d11a5e266b25b28ea8f27bf71`  
		Last Modified: Tue, 24 Feb 2026 18:58:08 GMT  
		Size: 13.3 MB (13273840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a498b5c4f65e906e1a379508b28d65074ca486208e4965487cbbf5e23d5d2f`  
		Last Modified: Tue, 24 Feb 2026 18:58:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e3701347584d5508dc614e9a37add4079afa74353d6794522d6f8ce213859e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afff830ce9ccb9268fa0bc050057156b78295cb8cf420b5b10596eb344235617`

```dockerfile
```

-	Layers:
	-	`sha256:c6f399922525a7578eea43fd04d0c9dcdce1bf1e45ad189421d9dc3b361d9a3f`  
		Last Modified: Tue, 24 Feb 2026 18:58:08 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813dfe70a075bb6c996948a7ad538e9e9956454b551420bae0991caa6a63c177`  
		Last Modified: Tue, 24 Feb 2026 18:58:08 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:50dc74f149b30fbcc21c78fd99ca191d50a95897f01d87c700911595ce0e434d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40729491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2329075b11bc0e54821932c66922099eda12e15ddf7eafe093f6cd8bf48ab839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:37 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:58:37 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:59:25 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 18:59:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 18:59:25 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 18:59:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:59:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:59:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:59:25 GMT
USER haproxy
# Tue, 24 Feb 2026 18:59:25 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:59:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2e9272c33e9ed9d294ea3b88ee9e1144393532244831b625d158e0db89c019`  
		Last Modified: Tue, 24 Feb 2026 18:59:32 GMT  
		Size: 1.5 MB (1488880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed59f887443d50e7a352032fb1209623e9ed0e676d433e5cce19d38f2949675`  
		Last Modified: Tue, 24 Feb 2026 18:59:32 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a7ae850e94b62563fc52122f31b68347b1a411470dd884b3634e03e074b85a`  
		Last Modified: Tue, 24 Feb 2026 18:59:33 GMT  
		Size: 13.0 MB (13025225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845e7d0e049444a7539b56e303241aa9864912e55a5aeb3bb287ecd70a10892`  
		Last Modified: Tue, 24 Feb 2026 18:59:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ae62f7db8d8c5eb52f43cf824b99af25447870ce9d762e6fe3d1e60c723d3206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33954af7a3d0f9182b062d66eecc9bbda11c6cdefb7f54633638406b9219f97d`

```dockerfile
```

-	Layers:
	-	`sha256:322cfe5e2674532ce0309539a4a89496b38912c1637c41a05d6af33b7b31c9bc`  
		Last Modified: Tue, 24 Feb 2026 18:59:32 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e77f9af3523c46afddda6edcbd60ffe3bd85c56d7635ad3c15098250027d8a3`  
		Last Modified: Tue, 24 Feb 2026 18:59:33 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:163e47c0a84dd96515b350c7c7965f5a7385f54f0ec2ccc3a0a5b0801a12f3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44742286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c91480a6f7bc64da9494f9d81546a7efec74c6f7eadf0ca55a3eebe612ef205`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:01:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 19:02:00 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 19:02:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 19:02:00 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 19:02:00 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 19:02:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:00 GMT
USER haproxy
# Tue, 24 Feb 2026 19:02:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 19:02:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4d7ebb5fa2d0341c44c9f869df0767e8d47925b33f5bbf33bd4680613771a`  
		Last Modified: Tue, 24 Feb 2026 19:02:09 GMT  
		Size: 1.6 MB (1563184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b840b06ac7b5ca8769999134f7cf76549fab3bcf734334cf1788c58affc26c35`  
		Last Modified: Tue, 24 Feb 2026 19:02:08 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c09b3ce896cbbdbe1856a7784f2aa0f26f516b22ca257d4b0653d4e8bd55a5e`  
		Last Modified: Tue, 24 Feb 2026 19:02:09 GMT  
		Size: 13.0 MB (13037361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35daaf8379235c4c912d6695882b0e49739d8aa837cd31554eacacad2e1d00bf`  
		Last Modified: Tue, 24 Feb 2026 19:02:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:814a47eaa0d788274a4699842f197ab53b8c3501e37ae54c9f8d152384ae97f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2021b84c416988d297b5ca3c12fd11e0eebf579f4729d68f52bf1829b94046b8`

```dockerfile
```

-	Layers:
	-	`sha256:6bf2fcaee4225ffaba566d7513114ce04e854f84e1015306e13c0ca67ffc3124`  
		Last Modified: Tue, 24 Feb 2026 19:02:09 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155077f56cf4147cb8d07a252ba3585abe6d3dde44c2300c95adfb9785532b99`  
		Last Modified: Tue, 24 Feb 2026 19:02:09 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:352b4c11770d75db58297c6fba3af84c824dba1971ec8419c2a43b5eaa0e3c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45724831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668028c454d0176367230433825082feab8ef9053d3caafe90f915f76ae45d21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:57:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:57:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:58:19 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 18:58:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 18:58:19 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 18:58:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:58:19 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:58:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:19 GMT
USER haproxy
# Tue, 24 Feb 2026 18:58:19 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:58:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36072ace481856e7ad672f2acc500ad69293445888a3ca3c15908aa948b889a`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 1.6 MB (1603185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fc80c6844677c6f5b4686010850602759c2ada6c35ddb6f4c6f4f6a058926e`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec7c84ab546530a26dd36aa163e24e3a13b2b2d2a39628aef20c1d6016d4dd6`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 12.8 MB (12826089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541c17f383fe280f6238d7ef51a494ff26bc72eaa35e6c07febb1c17d29fd8f`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:478bb3c4af9ff7411d536a65e82077565322034bf2828d95a7052a2a637a1a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff517128d39a6e5b0a5532dfe774593ef1e4db67f9f91888d0dcda7c20c69703`

```dockerfile
```

-	Layers:
	-	`sha256:58e88853242057024f3bb8250d548047935a0e5ab40d941edfe75f4bca1d9585`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d567538149b06b54607982009be1c6fc20dc61b361a77c511c40e8afb414f11`  
		Last Modified: Tue, 24 Feb 2026 18:58:27 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:5306db2d464f6af6f9a03f24c6db00944c6d5077a062f953639b25a0a7afd922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49052101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615e4eafb5758c99f711618e2da6c2f2a2be90fbbfdd811e8c0d8ed3978a33db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:56:45 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 19:02:05 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 19:02:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 19:02:05 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 19:02:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 19:02:05 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 19:02:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:02:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:06 GMT
USER haproxy
# Tue, 24 Feb 2026 19:02:06 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 19:02:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb569d4cdf73275b0f9928916fc94fc9f6bed23e006ee4fe505204c8ba710fd`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 1.6 MB (1638813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aad80bc3253c69fac51646fff38bb785f1a5773e13a6c0151f2a8b102491d7`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e823c21f30c2d7359350f5326ce0b4521459c28d27963111312588884c51dcc5`  
		Last Modified: Tue, 24 Feb 2026 19:02:21 GMT  
		Size: 13.8 MB (13811433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63732e6403cc267e35a8066db8293035c3d8e2dafc7d70c51e01176d67150526`  
		Last Modified: Tue, 24 Feb 2026 19:02:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0f1dd3f21db7634bda18f09575d1120e15a1b64c62ad4dbd5a45d7cc12e97859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1731c27e5c48935d4660ef253ae9368a05048d4eab57deab67a629b9785114fd`

```dockerfile
```

-	Layers:
	-	`sha256:10b9532eb3fb14253db120aa3644be325782d8d4b81d2c94d4bae3c3a116f4a7`  
		Last Modified: Tue, 24 Feb 2026 19:02:21 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d58af9825322b2829a519a409c3c53e4cccfa3be63a7906aae413d9b20b7c43`  
		Last Modified: Tue, 24 Feb 2026 19:02:21 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:e870b4daef72463826d43c8da73b66af4ed53fd3b9071e78fde0ce9fc9cd9b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42533656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f5429104f4a7db92ca1bf1551515b6df9ce532b492031052178705511db6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_VERSION=3.2.13
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Wed, 25 Feb 2026 01:38:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
STOPSIGNAL SIGUSR1
# Wed, 25 Feb 2026 01:38:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 01:38:11 GMT
USER haproxy
# Wed, 25 Feb 2026 01:38:11 GMT
WORKDIR /var/lib/haproxy
# Wed, 25 Feb 2026 01:38:11 GMT
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
	-	`sha256:a61ab47a6c70b7a65e636a636d15300bc8d806b38dd094e41f4dbcc9430146bb`  
		Last Modified: Wed, 25 Feb 2026 01:39:17 GMT  
		Size: 12.7 MB (12720500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd827a7e8595336e82551bdbfb85d2d23cc86779421261d3696d99ce6b14b5`  
		Last Modified: Wed, 25 Feb 2026 01:39:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:4c40f3954b546a9dfff9c62f9d5fa93d6a001509e572a909f0fa2feb0c5665bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7809a2b2aa6c3c55f805657b4902f3b131bdefa07f7016926d33454f93dcd6c2`

```dockerfile
```

-	Layers:
	-	`sha256:cfdd89364c3f6a310d4bb3ea52b0d35e00f269cdd141e2979cc8b94f03534ee3`  
		Last Modified: Wed, 25 Feb 2026 01:39:16 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dadd11b970339f4f3dbed7540a8f59b22426818567d76a16c6fa4d9c8ba1ac`  
		Last Modified: Wed, 25 Feb 2026 01:39:15 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:798084776fad3a5a1b549907537e7f948997ace3957043eff21d2d4dd9f7e845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44868836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b639080d7700b3e881d055d2f08efef82cdd717504e76e1ee9355670dcf9c21e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:54:45 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:54:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:56:59 GMT
ENV HAPROXY_VERSION=3.2.13
# Tue, 24 Feb 2026 18:56:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Tue, 24 Feb 2026 18:56:59 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Tue, 24 Feb 2026 18:56:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:56:59 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:56:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:56:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:56:59 GMT
USER haproxy
# Tue, 24 Feb 2026 18:57:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:57:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb19caba33436b7867ed8f90f624f5e4dd9e5a76bd7486fa51d6746f8429c249`  
		Last Modified: Tue, 24 Feb 2026 18:57:18 GMT  
		Size: 1.6 MB (1599704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebc1179fe99fa598a1de8a2042c5ec08851905b0cdd166b10ab3779ac5ede59`  
		Last Modified: Tue, 24 Feb 2026 18:57:18 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e4c08cd52c5fd2636f673ed6e3d6ba74b844f716b5fdcddf9354954f46451`  
		Last Modified: Tue, 24 Feb 2026 18:57:20 GMT  
		Size: 13.4 MB (13429308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee20deb05da0427f9be1ea9383b59f1c4d0fb753e0678e48114bd743e9225c`  
		Last Modified: Tue, 24 Feb 2026 18:57:19 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:49fa575a83703fa51de8e9eca78fe8263fb39b7ebeabffb23d7b6605d10ac332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d7331ccdcfbe13953bf4328e4e7f205e8d4e96f5e63259bca44a4b264cb17c`

```dockerfile
```

-	Layers:
	-	`sha256:3d24e5c2d30d8d6b244d22bf0d6542a53ff5d9a66ecb7c1e5e7e1f4913097370`  
		Last Modified: Tue, 24 Feb 2026 18:57:19 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2136efac184d073dd45bf65ab9482bb167d29ab54cb8329c673ae0bf7a234283`  
		Last Modified: Tue, 24 Feb 2026 18:57:19 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
