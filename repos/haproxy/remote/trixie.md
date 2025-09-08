## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:b85702f373277d0adcadcd61ad3b73887c111fe22a39e332842f36c8e901f209
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
$ docker pull haproxy@sha256:d721ff8ac51b4dea8d40a69c774c9ed1ea9eafcbc05a697ebd427d4b3d16daa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42042650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50638eac51982d74b3ac12db7d5e278a6f68fd9a9154d9797bae753d3c97ff06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ada74b0c9094f8ba8a2331db1c5e395a061b571b459f85de43891c435efa0`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 1.3 MB (1277831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5587fd693769b649478ec014986f19c7a36b64cdfbea311c29a74b489812f5`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f530dc3474a1299b6871422a074334600e1e070911bf946a466cb5b0ead460e`  
		Last Modified: Mon, 08 Sep 2025 21:56:03 GMT  
		Size: 11.0 MB (10989688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8868c5ca7fa3b609c9a68a0f0b0043dd59dcb943a9182c732fb0d9bab9bbc5`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:78799c9fc93790acd999c064b67a137fec947e2a3fd506001ea2df271490a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d13c2aa0ef540402567e8f5dba0387b8aafc731d8d6c42d28c876c4d761da65`

```dockerfile
```

-	Layers:
	-	`sha256:12ae376414ca815b7a6b1e4eceb08c40cf909e905c9a2c5b80902745ec141aad`  
		Last Modified: Mon, 08 Sep 2025 21:58:53 GMT  
		Size: 2.1 MB (2099816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d7c61ad15f897cc27b6f62516f296aa7c73230b7e65d352ce3b446b38b3ed8`  
		Last Modified: Mon, 08 Sep 2025 21:58:54 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:b8b7f2f363f79480706e47007dc03884fc6703be3d8eb5eabd34f3f90da91dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40279577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407b034ccda1fdfd1fe82a7125a3e9536e385bb4ea0bdbea48ca5bd88c0c3361`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a69d3728889fc78f0bfae23c58748160c7a53fe762c7da4eb5a2ba3d343b86`  
		Last Modified: Mon, 08 Sep 2025 22:00:15 GMT  
		Size: 1.3 MB (1261266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3f9a9bea0b5d040918d7047db413552ef7eb1616e6c9cf37744f0823a44315`  
		Last Modified: Mon, 08 Sep 2025 22:00:14 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3aeacc7320453b7845bd968b422c0b308283428a54234f63a0181d2c43159`  
		Last Modified: Mon, 08 Sep 2025 22:00:16 GMT  
		Size: 11.1 MB (11074914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4b1fcde59b79492521276648454691fac98dfce42e33ac716d72adcd149e06`  
		Last Modified: Mon, 08 Sep 2025 22:00:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b7c2980b98b9e21ececd3a7ec3be6093a62e2d48145769a724d770a5f400d199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c437a4e6aed15c04c35476c9eed8530ba45bc9216c7b0e44a26841806de9e6ee`

```dockerfile
```

-	Layers:
	-	`sha256:f14e0f3e06e4e5a3b980c4947ce9e5d05d363827462c3242391efbee7f0e171b`  
		Last Modified: Mon, 08 Sep 2025 21:58:58 GMT  
		Size: 2.1 MB (2102811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f01f07c89cc69548815929fe6f24e00e5c00c343b66348ace548001b78ddfc`  
		Last Modified: Mon, 08 Sep 2025 21:59:00 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:8a2b11f50d646aebe950126f360f088fc0d79fb78b7c32dec2c36cfbcbafb228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38302814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ac92aa43af18ced97342b64b8837438d627111405bbac2104760034302c073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227f053b05790f2ef1838744592959b3d72863d503dd11647e37926c2af4a66`  
		Last Modified: Mon, 08 Sep 2025 21:56:13 GMT  
		Size: 1.2 MB (1234652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3035ac985917261852d8ac20b9d674e690c2c404748e0d7dab5a1627743f679`  
		Last Modified: Mon, 08 Sep 2025 21:56:12 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457eec745bad0dac9595a27459f12bf6b46986eab4b7dc9a31120822e9b7c15b`  
		Last Modified: Mon, 08 Sep 2025 21:56:12 GMT  
		Size: 10.9 MB (10858680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130eef3b991bf6111fbbb3bea75a386e3469c8cf242ccddd249ff3e03a22e34a`  
		Last Modified: Mon, 08 Sep 2025 21:56:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:8e819ffd8f5ff5da978ffcd3386b90a77627dc777114130efc68748bb73d2758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c82cf3f0691449bd01bb5608a69e24540d388aeadeeb0e75130b435c6b2bfe`

```dockerfile
```

-	Layers:
	-	`sha256:6773d13f3a6598a36ee88516b92e9c4dc46c49a053b39dd12af390f5a6af14c3`  
		Last Modified: Mon, 08 Sep 2025 21:59:04 GMT  
		Size: 2.1 MB (2101252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30508f6eebff4d3634165949feff5cd04f11a268451b1ebcf76075b54d5cce4c`  
		Last Modified: Mon, 08 Sep 2025 21:59:04 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:07e2c1554d823f5b781149af25a4de28979a225d3abaa03531c1bdc41f5e23b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42319600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f88635d24a20e3b6a8cf1c0700f683b6637e829a534b081a6e193b71546e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7689fa76405f3ee5b0aa049c879c13dc0027ba6e46f3dadcf16662b630c634`  
		Last Modified: Mon, 08 Sep 2025 21:57:11 GMT  
		Size: 1.3 MB (1259729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ad934f44e717f0cba4835dada7e9e7c4adc4df6cced1196cc92211197d29d4`  
		Last Modified: Mon, 08 Sep 2025 21:57:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e745ef27b0ab9de1b11c2c7d966f1bf50e0daeeac53f596b7039f8c0b1f078c3`  
		Last Modified: Mon, 08 Sep 2025 21:57:12 GMT  
		Size: 10.9 MB (10921605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1cc7ce25c77a7ecc47d0b114d80eab6eb103e577682e112552b171325be649`  
		Last Modified: Mon, 08 Sep 2025 21:57:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f36c96b69f3cf57c64682488b908f2c4edaee523e2d57ff1b3f58b9172845faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ef017af7bf0da1d22a07ea3f283d152c8ac22c549ed9cf66ccc1fca938cf46`

```dockerfile
```

-	Layers:
	-	`sha256:a5971a4e5683e2ef3ca8a8d97682baa6d5ace9a6c7acf2e46b64492cbdaa1d38`  
		Last Modified: Mon, 08 Sep 2025 21:59:08 GMT  
		Size: 2.1 MB (2100124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e5cb5d7635750b9e817a8b6371bb370c643bf13a806adae3d885c191126bb7`  
		Last Modified: Mon, 08 Sep 2025 21:59:09 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:9d25c3ab0f776d26b1f2205acc8c1c4e5b0de4d16960f559f356d5c07a6ff4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43277200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae482ee3828da75feb5ba7e5d8107349aad56333bf8ab3e2f6022f60d9979072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b98c06a51dd82a82763ab8e6a3bfb982f5810868ee4211fd5544b108bb5a16`  
		Last Modified: Mon, 08 Sep 2025 21:18:54 GMT  
		Size: 1.3 MB (1285589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd3d0da28508a1c1d85fdc2b31418ed0b74a1b92ab70f1771ea398eb3a28e77`  
		Last Modified: Mon, 08 Sep 2025 21:19:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35327d05f11787711f639f09e458c81d2a85d91cbf69649074f050635b4b1840`  
		Last Modified: Mon, 08 Sep 2025 21:19:11 GMT  
		Size: 10.7 MB (10700190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11989d4a33507d95ac8586a985ee3ee23e0bdc88efffa8b3033bee25ac3924a2`  
		Last Modified: Mon, 08 Sep 2025 21:19:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ec2cbd8a1287194e51dfd295ec4b6582fb7178e8ba9912c4480d218cf2756c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3942edfa02925f4aa979062c8be1422d705253f745bc41882f538b5792b1e083`

```dockerfile
```

-	Layers:
	-	`sha256:21a456960979485c51fef0446f51bff9ada05d597a15b9dbef523664a70d3aa7`  
		Last Modified: Mon, 08 Sep 2025 21:59:13 GMT  
		Size: 2.1 MB (2096989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25fd6174818b5f38c67dac54bcbc403878a5e55c3bfa61ea4b4866dd4cefdd5`  
		Last Modified: Mon, 08 Sep 2025 21:59:14 GMT  
		Size: 22.0 KB (21980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:48d811504fdbd452b6cf077a98e18bac98d605e451827d86239afe95cbb574d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46538023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34013efea10efc484904b383ac3f815050a1a175d77d5ea23278e231ba4b2dd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c15d09803707ad88fd8ae7bd3e3473c0c9583fe7f9ca440584f3e8ba92e5aa`  
		Last Modified: Mon, 08 Sep 2025 21:42:43 GMT  
		Size: 1.3 MB (1308048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47a2affb5724eab70b721763b7be782703b51ddad19885199e3032bb5d885f2`  
		Last Modified: Mon, 08 Sep 2025 21:42:51 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b194dbed64b414f6ab50a9d7d38136a4f5aeda5a2106e1c28e093379d102fe2a`  
		Last Modified: Mon, 08 Sep 2025 21:42:59 GMT  
		Size: 11.6 MB (11633981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e072fe63d451f47401a170aa4bf763ef462447d4d7ce643ef394cf36c44aa`  
		Last Modified: Mon, 08 Sep 2025 21:43:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f037bd92d6883284d9e4dfc267a8f036823cc3cc8e6f698c74d4a5a26070f768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf99b7fbd1f2ae0c4127e0426b8ef69ad29b52e1f8296af46cadb054652d15d9`

```dockerfile
```

-	Layers:
	-	`sha256:9524a68683e6edd3b04ec565c3a384c63397ac6c0e7ca71736969422912bea5a`  
		Last Modified: Mon, 08 Sep 2025 21:59:19 GMT  
		Size: 2.1 MB (2103365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c82430653ad41493ac392fae463f168dbef19b4f16f46fdcdb5c333034f03f`  
		Last Modified: Mon, 08 Sep 2025 21:59:20 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:e425b5f924bcb6dd610ba8dccb91e186fecc798ea5685e90879614cca72afae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40169169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cda4862bc2d8c9285db4762d6659b4731e1bf416c842f662dca8dca3216f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311997e7d313b262fb90a639c3470f7f75355644de3ad48a51c6291339fa813e`  
		Last Modified: Wed, 13 Aug 2025 08:02:36 GMT  
		Size: 1.2 MB (1245287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca61b8b42954da27ebbbea9ddcf76e632bad4a77f5a1e536d221667706c007a`  
		Last Modified: Wed, 13 Aug 2025 08:02:36 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b720e51bf1acd8ba5f78b8aea506a27065ec178e502d61e340854360db4df58e`  
		Last Modified: Fri, 15 Aug 2025 08:56:30 GMT  
		Size: 10.7 MB (10650616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba85ed3d7c3ada13d40e5d6de38d7bb7d0a947a385ec654a3ab96721142d89eb`  
		Last Modified: Fri, 15 Aug 2025 08:56:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:3768839364b07d157e6ae6363b36d08453a5015ddb100f73b2e5bec19cfd948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b369a81e0b90bbb7c97e2e7d45c86564f0f4fb722a0149cace9224099d453`

```dockerfile
```

-	Layers:
	-	`sha256:fd1d824f2bb51e49e23f1f286481ab523406159e3e24dfbe0e846735119eedec`  
		Last Modified: Fri, 15 Aug 2025 09:56:23 GMT  
		Size: 2.1 MB (2092912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee3e3f762006b9c22a8f6db47f937e4cdf671a4c5e7fc5be655896d92ee54cb`  
		Last Modified: Fri, 15 Aug 2025 09:56:24 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:b17cc63d2883f8f2c96b099fc92cbc0a221d8c6611967128ef4e216d022a2483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42411970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace9f853cd255d1a6326a2e7cf77dfaf988927592768557458fbb0a78a8f187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307fb7f4966f1d48604abeea53dc31cf0d4083c5a8be502d9d579c4c4dfc6fc2`  
		Last Modified: Mon, 08 Sep 2025 21:53:52 GMT  
		Size: 1.3 MB (1292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcad8b9064876b58201eee23caa04b9792e730cdcb67f0a24e91158749476d78`  
		Last Modified: Mon, 08 Sep 2025 21:53:48 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab084030f2dde04f1597930aa34a9b7afa17199d183fc701d0f8b1fd8d999fa`  
		Last Modified: Mon, 08 Sep 2025 21:53:48 GMT  
		Size: 11.3 MB (11284465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c899d1b232ae1ca024ba6f5ba1f6ed512c2224b9c701990b27233274bff98`  
		Last Modified: Mon, 08 Sep 2025 21:53:49 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:65d23a508775b05881907759bb1197c26c2ae33eeb07ddbd096c18502945e53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c32cdb67cad212f4f6cf63222c3167938bcb585cad5a42e471808496619f8`

```dockerfile
```

-	Layers:
	-	`sha256:bac46d5d01316c8f603e6ddf8e7f8e5ba467ccf1ccae5f1438ddb41c711fe732`  
		Last Modified: Mon, 08 Sep 2025 21:59:28 GMT  
		Size: 2.1 MB (2101261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24544af6c6c0711870d6c0049e416f46a65f40d0451754610fb2b34fc536204`  
		Last Modified: Mon, 08 Sep 2025 21:59:29 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
