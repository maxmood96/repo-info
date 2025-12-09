## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:b15d4d6722360dc363501c29f089b37327489c1a9439479da126066d2a47935f
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
$ docker pull haproxy@sha256:a04c5e705f4ae32b45db7af24f070ab880c72d62b24ff0f3a54872501d19f14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43356906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee7c8d4c5cf878e280197e5b5895429adf3fb5f5bfd455356f03f4e69175e01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:32:56 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:32:56 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:35:14 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:35:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:35:14 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:35:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:35:14 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:35:14 GMT
USER haproxy
# Mon, 08 Dec 2025 22:35:14 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:35:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0646a4095503e6ad88c88b659746ba5cc0ff80ef8a345f203f7c77b4b48e7158`  
		Last Modified: Mon, 08 Dec 2025 22:33:39 GMT  
		Size: 1.6 MB (1580886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e087377657fdd035c1ee3525a141085cf13dab744acfd8f3d613293a918bda`  
		Last Modified: Mon, 08 Dec 2025 22:33:38 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3111f9065436d186e1e069fd99968eef2a4cf1354649b4cd9d21586d6a086b19`  
		Last Modified: Mon, 08 Dec 2025 22:35:27 GMT  
		Size: 12.0 MB (11997889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa26b09be1834c41cff4ed7755c3c554e9c29aedc61e39680fae1f435f4d62a6`  
		Last Modified: Mon, 08 Dec 2025 22:35:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e5dd88a25012b8956d0216840e174ac1aa2f778c5e7ced4d59475c6121c3f658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d5f75001e5408cf58150c248ed9a24a726bfe4fcbbc14ca370697dce121fab`

```dockerfile
```

-	Layers:
	-	`sha256:5f8935e0283c5409edc9162c4925fca94463cf3a4773f5eef5e4cd522fd100e0`  
		Last Modified: Tue, 09 Dec 2025 01:59:31 GMT  
		Size: 2.1 MB (2113700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41143f65a768c0bdca9da8c764e330f57170fd41be1bc8e8c6c210b14345c214`  
		Last Modified: Tue, 09 Dec 2025 01:59:32 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:c8778724f8663942fd50b7695b76547865af7878caef6442285b80794282c9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41588499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e17cd74235f0b9facf6fc04ea1abe31f69d93c27ffc7859627591ac2169ea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:32:15 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:32:15 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:33:07 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:33:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:33:07 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:33:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:33:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:33:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:07 GMT
USER haproxy
# Mon, 08 Dec 2025 22:33:07 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:33:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac49ab778abdc9575d189bd3d5a36338ac5d805bcd8bb1294df13e39e379325`  
		Last Modified: Mon, 08 Dec 2025 22:33:20 GMT  
		Size: 1.5 MB (1534765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfd722f815fa7b92633e01d7b74517f864eeedf9062e9a599192c0e0ec1f552`  
		Last Modified: Mon, 08 Dec 2025 22:33:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da3e4df73a0208109e8bdb38a00e0da8acd0c02ac1f6ad8362c10a555e4078`  
		Last Modified: Mon, 08 Dec 2025 22:33:22 GMT  
		Size: 12.1 MB (12107906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3376fe6691202e2b692cbf1838cf9677de0b0a5ad7d9aeb590fee2b1bf7c8700`  
		Last Modified: Mon, 08 Dec 2025 22:33:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:631dbd7eba50f0ee2300920c65334942e506464ee5f82f1354c95d243a8d86e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227e171f3a0d2a30af0f7ae7805e202aadd8af5d9c91e7c8f644640d1963d58e`

```dockerfile
```

-	Layers:
	-	`sha256:a7ae2de82dda8ab558f114aae775de3bd4835c01dff9b79ffc93e15fbc3b5f01`  
		Last Modified: Tue, 09 Dec 2025 01:59:35 GMT  
		Size: 2.1 MB (2116680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c09e8c09f74daddac7f2b59b988ef465846057dc5cf863a1a005fc646777f20`  
		Last Modified: Tue, 09 Dec 2025 01:59:41 GMT  
		Size: 21.7 KB (21725 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0f2952021a3c902e9a892d65b2af60177f15cdddfca21a5d4f33c84ab0e1de4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39643445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8956dd98a60fd690251f8598827267c81e7a90ecf3f99844489e7d05867e7520`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:22 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:22 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:34:08 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:34:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:34:08 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:34:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:34:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:34:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:34:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:34:08 GMT
USER haproxy
# Mon, 08 Dec 2025 22:34:08 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:34:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9225fa4e48625e4e4603c4bd7c7d483983611b9b2f106846f49476765470e2d9`  
		Last Modified: Mon, 08 Dec 2025 22:34:22 GMT  
		Size: 1.5 MB (1488776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30035df07984aad0da5025347328dfb77e93713c0dfcd5d80f9367638c6f3eb4`  
		Last Modified: Mon, 08 Dec 2025 22:34:21 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d34b59a88befc575879a167d15a8b837f08e6b13fea1a6992a507b92481ca`  
		Last Modified: Mon, 08 Dec 2025 22:34:23 GMT  
		Size: 11.9 MB (11943021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00e22452dc7efb0bb4a5ba6b14cfe367447b2bc22128b796fdd278b43e3ec08`  
		Last Modified: Mon, 08 Dec 2025 22:34:21 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c35e91f12f89b871ebc70850977a84b6677289daaf41971f0e3a314e80fb16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcc73906f23edef011c1a496d417178e191b709062e90f317c626b7d78fd328`

```dockerfile
```

-	Layers:
	-	`sha256:a2cd0c89f18ade146869f2ad5d4b4de0bf451d4016e0a49eeee9c7856b1abbb3`  
		Last Modified: Tue, 09 Dec 2025 01:59:45 GMT  
		Size: 2.1 MB (2115123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644fa269217a45b5708cd51d315ee656fbbd0f03ea198a81f6f05dd94f1cbde`  
		Last Modified: Tue, 09 Dec 2025 01:59:45 GMT  
		Size: 21.7 KB (21725 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ccbd0c8615a6945fb6ddb725354d51aa4b33c7dc564de4973f579dc09b6a8491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43605643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6315904ad06bd6ee8127ffad894396e51d2f172e8c8057fcd0393e92fce69622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:33:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:33:56 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:33:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:33:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:56 GMT
USER haproxy
# Mon, 08 Dec 2025 22:33:56 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:33:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a1031c83e29b2bbbf6e1fd8c5bdd90acb169e9ff0c3453410683be9d0d06a0`  
		Last Modified: Mon, 08 Dec 2025 22:34:09 GMT  
		Size: 1.6 MB (1563633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abb51f56186f0beb7bca66140e9a1444362f79b2fc5a194b85aad200c59d3c5`  
		Last Modified: Mon, 08 Dec 2025 22:34:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9d200d7fa453647ca416e88b2aca1a3ebf691345362f4d96880cbd322f89f9`  
		Last Modified: Mon, 08 Dec 2025 22:34:09 GMT  
		Size: 11.9 MB (11901747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc4efd81bb5b8db1cc0dc6cbe0722d028ca7ca6c5460b0a08d2a27d3f893a7a`  
		Last Modified: Mon, 08 Dec 2025 22:34:08 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2592cdab88beb1c20d6177d7eb47782ddad7fdcc243f369bc48d4fc2c8fc225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf56edee60938bb86593b14ce7a7e107e46344cdae5613775798d0d72f14e17`

```dockerfile
```

-	Layers:
	-	`sha256:9c1905fa53ae80f3961fe5b80b8a561c703ee63acf881532660566418df997ca`  
		Last Modified: Tue, 09 Dec 2025 01:59:51 GMT  
		Size: 2.1 MB (2113985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f337d69d63a58140519f29f1f5a93518a16e5e90975590302846afbe77c4ed76`  
		Last Modified: Tue, 09 Dec 2025 01:59:56 GMT  
		Size: 21.8 KB (21760 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:7b287839d86bb86abbecdbf2666f0078902f8d5b36d49ae235e22caef600d635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44692984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ff6fbc572c452df66337559f0bc63847f1b0e8e8fc91b242caad84d3d3626d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:34:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:34:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:34:12 GMT
USER haproxy
# Mon, 08 Dec 2025 22:34:12 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:34:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ca1bce75611eae8203b818b1f807e8e4a0cc7ae1a09452f0c8bbca47e4460`  
		Last Modified: Mon, 08 Dec 2025 22:34:25 GMT  
		Size: 1.6 MB (1603041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece95ac162e05102daf344b1657b19148ddb93ac9e100695cfc9664666c90dde`  
		Last Modified: Mon, 08 Dec 2025 22:34:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f41429904ee9066ed239d7bcb7fe3190fb491ce778460575592116ae2b69198`  
		Last Modified: Mon, 08 Dec 2025 23:33:39 GMT  
		Size: 11.8 MB (11795234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6847aa3af18ab5d5587bb6f2b659f6717baa5c380c26a8ddb359c38676abc65b`  
		Last Modified: Mon, 08 Dec 2025 22:34:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1fbb0d13bfdca94a334d3e6c53e6ea98747a8bfa98e972a51301215cd731e3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e67cd5a4a4db85c0c0db88aee52cfc0be1c89b2016a54ca4949012aba765678`

```dockerfile
```

-	Layers:
	-	`sha256:04bef0923118ae15bc5c720aba63ac1f49b21f1f8f588af3b1381ef62016ce11`  
		Last Modified: Tue, 09 Dec 2025 02:00:00 GMT  
		Size: 2.1 MB (2110881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07113c1c8c5e38f693f39d041749be96b3a20627ffbea0807a4de6841f31975`  
		Last Modified: Tue, 09 Dec 2025 02:00:01 GMT  
		Size: 21.6 KB (21557 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:f838698280bdad67a824ffbe6757f01689fc6c715a40eda202ba50bbb8fdcc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aa8746b963a3cc97f30879d65fffb7da3dc14aefbc7bdf91ebd1182dda1a7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 09 Dec 2025 00:18:29 GMT
ENV HAPROXY_VERSION=3.3.0
# Tue, 09 Dec 2025 00:18:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Tue, 09 Dec 2025 00:18:29 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Tue, 09 Dec 2025 00:18:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 09 Dec 2025 00:18:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Dec 2025 00:18:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:18:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:18:30 GMT
USER haproxy
# Tue, 09 Dec 2025 00:18:30 GMT
WORKDIR /var/lib/haproxy
# Tue, 09 Dec 2025 00:18:30 GMT
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
	-	`sha256:91ae06f950fa05c81cd883b35423cc4555fd01862a3ff99543be065aefbc6678`  
		Last Modified: Tue, 09 Dec 2025 00:19:03 GMT  
		Size: 12.7 MB (12684921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2074ce31615fcfaf3de0f0bd4070393cab6ad1cb34b43b77da542af1a445d2`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f44b85d59c2fb3b65658744191dfb4e572355c73d07680b77d3ea32290267e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf62b3eb857c2440d5380a2586ce2504a85b357364a5100b3ab57492a3196f3`

```dockerfile
```

-	Layers:
	-	`sha256:1105201650f2d3354cbcffeb5b39e6deabd44d23706debc47b004c09df083eff`  
		Last Modified: Tue, 09 Dec 2025 04:57:46 GMT  
		Size: 2.1 MB (2117246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ef9f8c9ec7e350077c787750939d0845ae95b448dda7974e186c6b493e9650`  
		Last Modified: Tue, 09 Dec 2025 04:57:47 GMT  
		Size: 21.7 KB (21663 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:e49749be116f7dc6f3105e6f8430b0c0eee3b599c6c11f35ccb7a53932de3ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41333677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f86b1f6e9f2b9726ee094a005ccbd69c95df8013560cb95349f92cc4a5815b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:15:22 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:15:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 09 Dec 2025 03:43:07 GMT
ENV HAPROXY_VERSION=3.3.0
# Tue, 09 Dec 2025 03:43:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Tue, 09 Dec 2025 03:43:07 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Tue, 09 Dec 2025 03:43:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 09 Dec 2025 03:43:07 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Dec 2025 03:43:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 03:43:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 03:43:07 GMT
USER haproxy
# Tue, 09 Dec 2025 03:43:07 GMT
WORKDIR /var/lib/haproxy
# Tue, 09 Dec 2025 03:43:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764214954a48097c0e9e75920ec71940c64da22d529cf119465be01a382f7bf`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.5 MB (1535074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8e3b90d2e358dca114fe7f69a507e4f358fbe2966b2f6df9510975fe1daec3`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ab07952406c1a69ca9bd3c86dd673d9de7465aebdbfb6518c506f19e2dd253`  
		Last Modified: Tue, 09 Dec 2025 03:44:19 GMT  
		Size: 11.5 MB (11523810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f40fc819a48bf6f23a681f2b7b96203ce8ff53b3a00a9e02ef71a6ce0951e75`  
		Last Modified: Tue, 09 Dec 2025 03:44:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:cb99e58acfc36d3bb8d09bc81713d7b31f48f6e52ef479c4eab77431c51cad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba18cc05c863c5f6a0486559f273d1a24caccd091ec7a78a37c25baf55101c81`

```dockerfile
```

-	Layers:
	-	`sha256:5d2fe3406260fc0ac801af89e53c9c0dd6b41b7092c73c3b6a19b386296dd5ea`  
		Last Modified: Tue, 09 Dec 2025 04:57:51 GMT  
		Size: 2.1 MB (2107637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e409015f1a7879da27022b93cafe3e291344b936174e79cde4e378a8c357b183`  
		Last Modified: Tue, 09 Dec 2025 04:57:52 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:bbccc276ee29368293480bf59d54f6f16650386d251d8ed6fb62a88035108a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8dad6ca4afbad60d7cfe0c42516dde6a0e68a2f32384af7dbad1d24a6eb4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:29:46 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:29:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:30:52 GMT
ENV HAPROXY_VERSION=3.3.0
# Mon, 08 Dec 2025 22:30:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.0.tar.gz
# Mon, 08 Dec 2025 22:30:52 GMT
ENV HAPROXY_SHA256=bf2da6b69f82d7b855be977ab9e1d4704eef5629b657ac72afb5958a869c902e
# Mon, 08 Dec 2025 22:30:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:30:52 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:30:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:30:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:30:52 GMT
USER haproxy
# Mon, 08 Dec 2025 22:30:52 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:30:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c68105d562e6e1e2201401f6f7ba3d0d73c730d4cd3cd1fff86f0138002f7`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 1.6 MB (1599483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0052d8eeab3ea5047d4a29c92e67ddb241a0670e49d355f08539023ddd65b`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403895b67900d390ec152fd5db361466d8d1467b3425f67ad26e440d77df0c92`  
		Last Modified: Mon, 08 Dec 2025 22:31:09 GMT  
		Size: 12.4 MB (12362407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd377e5dcab22f4e253749446c2c68a45a4e6b85bfac824615b4a4a61879c68a`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ef2cbdde2de19f62c981ddaae5d7db4b493b80a565ca7713c3e0403880bc53cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad37509cffb12b94a598cbb14e8651ed83f5caf8806825b755d307b8253e46ba`

```dockerfile
```

-	Layers:
	-	`sha256:37e57e8fb9a68de02643b43e6f3ac937dfbbeb4c193a18a1695caebed7acf36d`  
		Last Modified: Tue, 09 Dec 2025 02:00:17 GMT  
		Size: 2.1 MB (2115144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a162a50cb350348a218b455b54bf4fa8b08a7df1753306ed625a53ae27055a`  
		Last Modified: Tue, 09 Dec 2025 02:00:17 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json
