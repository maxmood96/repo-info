## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:c60719100ae3b3dc9727cd496329a1dd33cadc77c9a480a9e27792f22ea34c3f
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
$ docker pull haproxy@sha256:c9763bf7b49451dd3a5d640cd39f9bbcc851ee61afe2262737c1dca593bf3553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a18312e7ddfff4dff7b4f5243ddcbb2a417a2d201cca2186216fe84873ab9a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 18:38:04 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 18:38:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:38:41 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:38:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:38:41 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:38:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:38:41 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:38:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:38:41 GMT
USER haproxy
# Fri, 19 Dec 2025 18:38:41 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:38:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954982adb92399b0363606b5b199c5cfd36cdad226fe24e0bd34716a828ffdd7`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 1.6 MB (1580918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0dd852487908d2c3963d9ba676c190f5b62ad202b7a8667ce6d5ba0a3e78a0`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaf3e15a24d733d9d91329f5c440f38b7a2e837387af952e9e8ca26adab21c`  
		Last Modified: Fri, 19 Dec 2025 18:38:53 GMT  
		Size: 12.0 MB (12008260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7210107dcca3d426dd7bb68ebde819561f757b9e5ebb4da440112ce7c1d7ff74`  
		Last Modified: Fri, 19 Dec 2025 18:38:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:41de5a06f5b897212495210f188876f49dbafa850f4e9dbade2bb815fdb227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9511846181461b6c3c28e0252201c4a55f7554e94a30974491bfd043c05ab5`

```dockerfile
```

-	Layers:
	-	`sha256:eaf8561e9ca6c24002296659320ea80c759f9bf7b537e4ca0cf93fc7e027cb81`  
		Last Modified: Fri, 19 Dec 2025 19:58:13 GMT  
		Size: 2.1 MB (2113700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6395dbbe2b5cb82a7be4aadb6f0de38424c541fcaa0e98b55c84774cbb3004b7`  
		Last Modified: Fri, 19 Dec 2025 19:58:14 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8cc57b7a7748f016ce6f18fa491f1048d038f9780410820a2b9564c13361481d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41596462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39155bb58a34a2dce5a63b5ab9475c12d16f08b302df83a87e982be13deaebff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 18:36:20 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 18:36:20 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:37:13 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:37:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:37:13 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:37:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:37:13 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:37:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:37:13 GMT
USER haproxy
# Fri, 19 Dec 2025 18:37:13 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:37:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f66b5867a0c77f89740cf895e8c4e528d7dc580de675b6a98fcc3b873d0e27a`  
		Last Modified: Fri, 19 Dec 2025 18:37:28 GMT  
		Size: 1.5 MB (1534812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0262db6a2abd740598e210fec9a81f4de22cc370b7cb44bc5190ca25e48a296e`  
		Last Modified: Fri, 19 Dec 2025 18:37:26 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b97abbf99dabbfa91b89db89d64635456d7a05996f3ee6a96adf691ca0978b0`  
		Last Modified: Fri, 19 Dec 2025 18:37:27 GMT  
		Size: 12.1 MB (12115819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6aa2b57449559870d5073c332560840c9171df975a93b5fb5603a3dc0f95d0`  
		Last Modified: Fri, 19 Dec 2025 18:37:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:994dfd2e1cbec7c4da71a432805f17a9133554eb0f2c46195f29d85ef4ae8fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18cdf74391c0dfa86a9061bd84f02d32584ef4d085f805faa03fe1bf5999e6e`

```dockerfile
```

-	Layers:
	-	`sha256:31c7ffd1c8481b0fed912ac8c73281a77a70696b13868a834926830a7031c08f`  
		Last Modified: Fri, 19 Dec 2025 19:58:19 GMT  
		Size: 2.1 MB (2116680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f5d7007d6f7d9a7bf33822eb7e9aae96fa0fabb7d18f4b1137b3de1f76d7e7`  
		Last Modified: Fri, 19 Dec 2025 19:58:19 GMT  
		Size: 21.7 KB (21725 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:feeca9a0e6dae3c52aa0e1cc91d18216cc1eea0537e13ffe77f5ea09474e1b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39654196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878306ff2b4d9ab7c9e9c865ce8735356d630e9e1cb512c5bdd807fff51e9c83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 18:37:15 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 18:37:15 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:38:01 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:38:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:38:01 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:38:01 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:38:01 GMT
USER haproxy
# Fri, 19 Dec 2025 18:38:01 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:38:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a840d730d0eb86b288e54a7e2c66bd8230e31f67d21830c1ad2a29cdce310f`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 1.5 MB (1488781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b295604fd6016e7f286bc148f543a931e625f42ce31c0d835e0fd9df3a469`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aea4c20d4e1a5b79b680d16516eee8c36179f54cbeb940b1a5320ef226ffb2`  
		Last Modified: Fri, 19 Dec 2025 18:38:19 GMT  
		Size: 12.0 MB (11953761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a0428cb2cffd2e173c0d0470fbc75c597d05c0b7b8e4c1f1e3cca0991fa06e`  
		Last Modified: Fri, 19 Dec 2025 18:38:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:329e6d5dc68d4021a2deb9a91f6413bdea4eaa14e90a781c4a31078de7b753f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b354e8011573fdf0f8cf29047458e72d948184682cf4431f3e43fe1561d5d`

```dockerfile
```

-	Layers:
	-	`sha256:aba2929190196fa211443c85146cafd06bf1c42dfc9ae8dfa31ad98029ff9369`  
		Last Modified: Fri, 19 Dec 2025 19:58:24 GMT  
		Size: 2.1 MB (2115123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc2f57f9419ed8830d289a961fd7832ad48a508c31f20ac99eca21b9c37035f`  
		Last Modified: Fri, 19 Dec 2025 19:58:25 GMT  
		Size: 21.7 KB (21725 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4f2a24d7305560b5685863e3e7ca7213289f298c4958d9ef409accae92e206e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43617355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8416850ba435e16387c7b199b4d3f85a958604feb3daa3261819271147d27c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 18:51:40 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 18:51:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:52:22 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:52:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:52:22 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:52:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:52:22 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:52:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:52:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:52:22 GMT
USER haproxy
# Fri, 19 Dec 2025 18:52:22 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:52:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a4c54fd1e4cf5fb6726e2d3a3fdb08fbb5bd4060cc4a57f002b27e09702aff`  
		Last Modified: Fri, 19 Dec 2025 18:52:47 GMT  
		Size: 1.6 MB (1563673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6141f89c504b713d187431f27d90ae34ac03f9380df07314a747a94bd08e14`  
		Last Modified: Fri, 19 Dec 2025 18:52:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39e5090d4d0367ef5bc1ed71b5909f354e04474ac032677e4cb1894077ab8b2`  
		Last Modified: Fri, 19 Dec 2025 18:52:48 GMT  
		Size: 11.9 MB (11913414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc06331f1b46686729dfdbc6f0f9efcc7512178a1806eb6802dcba6889fec359`  
		Last Modified: Fri, 19 Dec 2025 18:52:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:61e023212327babe01b8bf8723a461009808211ab2caaf9124f68b518afb23f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892893fa61e0be2a41ee52b5adaebf0c4027315213abcb46d148280554fa8016`

```dockerfile
```

-	Layers:
	-	`sha256:6bb080302fc267bc0190c23e9bf39920953c3dc8a378181365f6b132e781039b`  
		Last Modified: Fri, 19 Dec 2025 19:58:29 GMT  
		Size: 2.1 MB (2113985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c03ed2b60f62b38048214f2595d10d7b8c02ca51ecfbb94e99ac7f811212fa1`  
		Last Modified: Fri, 19 Dec 2025 19:58:31 GMT  
		Size: 21.8 KB (21761 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:f38ac04ece8d9bdb61b67d08e6cab4c2e2710326507458d709503c2f8f6dddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44702041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b432e261015509a36a72e83ac2c68b263c28f3d47800172b0458bc37129fdae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 18:36:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 18:36:42 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:37:30 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:37:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:37:30 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:37:30 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:37:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:37:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:37:30 GMT
USER haproxy
# Fri, 19 Dec 2025 18:37:30 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:37:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ededd2a5c1ffffc13afe19cc63c372bc3dbbb88404fcd844cd3e38685d103842`  
		Last Modified: Fri, 19 Dec 2025 18:37:46 GMT  
		Size: 1.6 MB (1603078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a832767ae8824d7e57a8cd775f6128d72cf7bcae432b37a348fe4d881ebae4f`  
		Last Modified: Fri, 19 Dec 2025 18:37:46 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1529cc752bf7bc9377117e8ccc107220cd26721a5c24dff507a1df2711e31`  
		Last Modified: Fri, 19 Dec 2025 18:37:51 GMT  
		Size: 11.8 MB (11804252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a969ee993f20b0be88e2de22b03d65144bcff5846f6c1ecb0dfcd04e1a6bd`  
		Last Modified: Fri, 19 Dec 2025 18:37:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5c67476b5391be207ff02862afc519ac50f0fbc09cfb5b2654cb64bcf0d81184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7437190bb06128f306833a25957aa8f07537cdd78260acab76613dff129a04`

```dockerfile
```

-	Layers:
	-	`sha256:e9c8b9e386264cfac08736766a749bc5e36b55ba2132facd27adfc6239e5f8c6`  
		Last Modified: Fri, 19 Dec 2025 19:58:35 GMT  
		Size: 2.1 MB (2110881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6505ce7d881a30156d8cecfe58129e0a863612820872f5d7b7e5cad224f36ee4`  
		Last Modified: Fri, 19 Dec 2025 19:58:36 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
$ docker pull haproxy@sha256:feb9b7a154c9d7541431d6e36f7633668a901d12e0e530f687b6aefa3170b131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43822438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d2d6e7d75ef89c9be510f5d836c3313b0be8bc5aeb98674396a1892ab2fc79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:29:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:29:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_VERSION=3.3.1
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.1.tar.gz
# Fri, 19 Dec 2025 18:36:36 GMT
ENV HAPROXY_SHA256=b77acdae8a7600db9576fc749292742c109167648005513035dea767e45a00df
# Fri, 19 Dec 2025 18:36:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:36:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:36 GMT
USER haproxy
# Fri, 19 Dec 2025 18:36:36 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:36:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8857bcfd6e09fe182ea0a989223ba1eb04916420f173722698d912903efd50`  
		Last Modified: Mon, 08 Dec 2025 22:30:31 GMT  
		Size: 1.6 MB (1599481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e42844e2073c2a89e62bcf78c0de0281a07555ea442a2586a4db3eb2fe0999f`  
		Last Modified: Mon, 08 Dec 2025 22:30:31 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7834d5a41af9bfcb0c61533c7210093e233cb0de3bab2a2f1491857f28c49f6f`  
		Last Modified: Fri, 19 Dec 2025 18:36:53 GMT  
		Size: 12.4 MB (12386917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d5a16307df8b8d450ea21675b597f7ec4a18b82d9099e6e205eea7365d013d`  
		Last Modified: Fri, 19 Dec 2025 18:36:51 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f663f01f1ca74bf29c4789585e157cab0bf681bcc026888ed3a38e795a7bdb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d495f1ee6fd453345d3b8b8476dce6d81f8d392765f9025e148a9069ee2878`

```dockerfile
```

-	Layers:
	-	`sha256:cf823462fad04bfdd435612f62e8dc24cf71fe422c87f41e705cadebe29c2230`  
		Last Modified: Fri, 19 Dec 2025 19:58:48 GMT  
		Size: 2.1 MB (2115144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d06626fd56f7fced71ee46bbaec83b148eea0534b38567ac4e9aef54d8d13b`  
		Last Modified: Fri, 19 Dec 2025 19:58:49 GMT  
		Size: 21.6 KB (21603 bytes)  
		MIME: application/vnd.in-toto+json
