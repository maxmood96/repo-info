## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:c16af36fb30d753b4ebc92a4364057b6f3ac0edca145ccb99cda1c4f67de3778
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
$ docker pull haproxy@sha256:87b3abdb1aec52be4835fbc1ac26a946e1a8b0351626243296820c1a46fd82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbf881dbdcd887946e57005446aa2617c9c023a8754a9301ccd8a792a547114`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee403fd4eaf7a88ef2aebec1dbd1aa2ce4428976f7c3d33350086f342440f8e`  
		Last Modified: Fri, 24 Oct 2025 19:13:16 GMT  
		Size: 1.3 MB (1279652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feecdb703e145ae937151c6752f9dd0bcc3808813c32362bbd19bd47252b5bfd`  
		Last Modified: Fri, 24 Oct 2025 19:13:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dcb10e0f56db08411085a5b82e44a8e43fc08065fb68a4d001db2a5b62e163`  
		Last Modified: Fri, 24 Oct 2025 19:13:17 GMT  
		Size: 11.0 MB (11025620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74f7c3e96ec72f457b8b177c0c2f58f30dbd4f34f0d15b57f189c0eac3a9fef`  
		Last Modified: Fri, 24 Oct 2025 19:13:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:06860fd889995fffe919a67e420106ad89c93c4ddc9e83ac5720802568cf5fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d122e2da871cdcfbb6d21e8e60ed39ee2eed5402b66d53dee6604fd56e312f`

```dockerfile
```

-	Layers:
	-	`sha256:dd60da4cdcaf5635fcdf66248b672aeecd169905c521b6c1c4d23ba35c6cefd4`  
		Last Modified: Fri, 24 Oct 2025 21:56:21 GMT  
		Size: 2.1 MB (2099870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833df7c9374d6cc5554fe041376e2e2cdced225dd24e9d0395bde73c66397b00`  
		Last Modified: Fri, 24 Oct 2025 21:56:22 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:3f7ddc23d250cadbe4e8c453cdfb305b13f8eb7f8d65e91ea0c5ad3f5f8ea001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40317631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc5f61f32569be45400088d7fd15978040f1f1893e4c38f6f1335ad8ad7ea95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:20:51 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 00:20:51 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 00:21:39 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 00:21:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 00:21:39 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 00:21:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 00:21:39 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 00:21:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:21:39 GMT
USER haproxy
# Tue, 04 Nov 2025 00:21:39 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 00:21:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116fd34b141121da31e05f5368bdbadbfc61f327cdc4857940de99f5370aa791`  
		Last Modified: Tue, 04 Nov 2025 00:21:52 GMT  
		Size: 1.3 MB (1263093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d8df6a050b527c1ba34c60128f4a8169a67ed21f18fff812bc9d3713527839`  
		Last Modified: Tue, 04 Nov 2025 00:21:52 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dcff792daef09415d781969f54b720c01b212181bcb7b54607ee77b43e41b8`  
		Last Modified: Tue, 04 Nov 2025 00:21:54 GMT  
		Size: 11.1 MB (11106461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ae002bcd6a81f82c98d3a304cb051808ea80627ddd0938089630910b8e43c`  
		Last Modified: Tue, 04 Nov 2025 00:21:52 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:686c27019ae19b7df40d1e5dc40aa0215e733f946414aecce17b5ef4d6bf32e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72724a230c4351d503f5378d901ac16aabf762fbe3a0d60ffcf63645da01880`

```dockerfile
```

-	Layers:
	-	`sha256:4330920998b3831cf499969a60c1a021cd25535794fa499d8790a8d0dd5fe48f`  
		Last Modified: Tue, 04 Nov 2025 07:57:20 GMT  
		Size: 2.1 MB (2102865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f59328619df00b13763435d900c286fd7de5cfea827bd9ef00e4250fdfa746`  
		Last Modified: Tue, 04 Nov 2025 07:57:20 GMT  
		Size: 22.1 KB (22130 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:07c7825ea57036f4d21cc3698e764c63ca29b0a25d6e1705f13fcc684265072d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38345531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e348d14ae14bc9ac361b68f0d938cac0089fbcfcf5a795fdaa6bbb8a5431e587`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd68b149cff526c1b9fec36bb073c082740292159175e5176c3ff83f081ea6b9`  
		Last Modified: Fri, 24 Oct 2025 19:38:47 GMT  
		Size: 1.2 MB (1236584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409e03cc8c7f21372ea40a8ee691657a563e543fa9437bc51fcebcb68604fe20`  
		Last Modified: Fri, 24 Oct 2025 19:38:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab82c487cefa3e9bbfbbafc9fbb6dfe8212d284da6d1b3bc306d511f397f3947`  
		Last Modified: Fri, 24 Oct 2025 19:38:48 GMT  
		Size: 10.9 MB (10894415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8412882dcc4cd9e5b4e38d478ec237cda21c22637bd4a8317d55303e5d5ab`  
		Last Modified: Fri, 24 Oct 2025 19:38:47 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:91b87667eae641e22d428ddaffa8181866be10a545814c6d05391bb6e547ccfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8b8b03b05d994ebb36f1e23ae4c165c60f517a9f1371cabf87d4a8f003053`

```dockerfile
```

-	Layers:
	-	`sha256:fad0ec757ed883e50b50cac64fc4468658f10cc7676b2266284572f0829a2728`  
		Last Modified: Fri, 24 Oct 2025 21:56:31 GMT  
		Size: 2.1 MB (2101306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8659a22187ff15567ac1243b8bd72b3b693684d5145e1373da7b024a53f8dc`  
		Last Modified: Fri, 24 Oct 2025 21:56:31 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:27d3e098e8f586d16c528a182314447f4ebbde08860c5f5fd2d2fb4f46fafb5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42359008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7404338e0546e9d9e4937ae26e76173e64a00fb0001dc2f8ffecaffc2ade4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171c11450ea9678aa3cf4b71e38ff4ef8b0ed9db7c89e9b70159f5d7bc257b7f`  
		Last Modified: Fri, 24 Oct 2025 19:03:33 GMT  
		Size: 1.3 MB (1261433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1648d8804435cbc31bed62c699104d1eb9e7fa91655cadb17958fdd7350087c7`  
		Last Modified: Fri, 24 Oct 2025 19:03:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a9ce5bdd2166c7cc05d2a018cac757ddd3829733df0ea3795a65edec53b6fa`  
		Last Modified: Fri, 24 Oct 2025 19:03:34 GMT  
		Size: 11.0 MB (10953803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbea596b6fa5777b60693804f50914295abfe1437c869a15071cc3fafe2eb87`  
		Last Modified: Fri, 24 Oct 2025 19:03:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:77168545f49e5d7629aa7d84b8bbca3ff33899e635ee01fd8935c69ae8fa5dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e2d524552dda75ece191898be849551378139a270269518573308c782dd40`

```dockerfile
```

-	Layers:
	-	`sha256:9bc1fe805250dd9748a598c52343bd0a7846f7da436e99e3c2d7bac3efe9b51d`  
		Last Modified: Fri, 24 Oct 2025 21:56:35 GMT  
		Size: 2.1 MB (2100178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f940fb571d9812ff4c8b347abbe710854a5d580914f3112d487c7259bc1bd17e`  
		Last Modified: Fri, 24 Oct 2025 21:56:36 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:3537707c4076868ea709fb220ce469036e62b016482701b681adf6eddf05eefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43317483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76536f5f22a248decd82eb3c3e18e7d97e8491e778469308918c036d9d171328`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae424218e5afeaef84e58c1ac00d0b4b75d3aa0955313930f1476d140ec264cc`  
		Last Modified: Fri, 24 Oct 2025 19:15:20 GMT  
		Size: 1.3 MB (1287383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6683185b73af5cd4224785909c58b6495f2a81f10b1b2ef058c63a16b4074547`  
		Last Modified: Fri, 24 Oct 2025 19:15:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9218c2b353219019fdf0c9ed032255f85d8c28b76a587eb2493648e855bf70e6`  
		Last Modified: Fri, 24 Oct 2025 19:15:31 GMT  
		Size: 10.7 MB (10733832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca9b071d724b2b53775e8116fdb9da5629210d274d90b594296d1476a696c49`  
		Last Modified: Fri, 24 Oct 2025 19:13:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:cdce71ad23773a13404c4746f8dc6d050e3c091ea175804f7b210f0cf3fe4ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3909e93f7165302557eaa3e2f88723553f20ca216d1c7ae6f9cc7ee557924aa1`

```dockerfile
```

-	Layers:
	-	`sha256:497caeace75ae7447d7df4468ecd17d58f8dd5bdfa02dbaaf6bde9a96380b122`  
		Last Modified: Fri, 24 Oct 2025 21:56:39 GMT  
		Size: 2.1 MB (2097043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e4f1a4650f71a8d244677340fb3417ef1f9bf658907cee013952c87d1a1671e`  
		Last Modified: Fri, 24 Oct 2025 21:56:40 GMT  
		Size: 22.0 KB (21978 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:bfc21053dd3040cb665732b4038812f46c21484c17d2619a2d8898c1d9f0a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46598650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4b3b8cb6e45c675c1885dea897fdd33fecac7501014a96d079e6afe28a146b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa480cd28c6d83024f0956dd0a6069d31ced439970222c630288cc6a8b49304`  
		Last Modified: Tue, 21 Oct 2025 01:24:17 GMT  
		Size: 1.3 MB (1309951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ae4de58a89a04bf56cab7ffd8d3594d5efe269445274257939ca966029ac4`  
		Last Modified: Tue, 21 Oct 2025 01:24:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a985ae09948231d5807c4f5a18a63f23787b2664627c7450e32c48dd1138b17d`  
		Last Modified: Fri, 24 Oct 2025 19:18:46 GMT  
		Size: 11.7 MB (11688542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88581203fd3596f0bf926e1d1c398fa72623d3aec7dbae8f5be2f9a2aa72e818`  
		Last Modified: Fri, 24 Oct 2025 19:18:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:589e725a9c7392e5f053e48b82ea0ad57e4fbe826a6d93f887e2735459244ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4a9e4d613fbe8122266f9f7bca2a8cee06b36d616c48de2f78dee272bb8b23`

```dockerfile
```

-	Layers:
	-	`sha256:8909e8559d85d8663399c0b9ecf51bbef6bf4af3a839bc66c46662cb33c0c5fc`  
		Last Modified: Fri, 24 Oct 2025 21:56:43 GMT  
		Size: 2.1 MB (2103419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e4a5d40a6b24bf1d111ad879a5a0529c04424a9647a0fd44385c9d61b12313`  
		Last Modified: Fri, 24 Oct 2025 21:56:44 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:0023ab581a735f440fa36586526a9203d42a113e115f7b3c0257c95a1ccd5420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40197853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4162c90ca456d460caf662e69d817d15a2c9e5b5f66270ffe92c280471de38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:09 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:29:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 01:56:07 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 01:56:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 01:56:07 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 01:56:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 01:56:07 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 01:56:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:56:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:56:07 GMT
USER haproxy
# Tue, 04 Nov 2025 01:56:08 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 01:56:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836074591cf2eaac43844893e7ee7c070600bede40c85dbaa76a64e9883bc30`  
		Last Modified: Tue, 04 Nov 2025 01:43:34 GMT  
		Size: 1.2 MB (1248235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f280dd96306d81fdaeec082edc939280b3e785a6db4331d7050e4679b4b6d41`  
		Last Modified: Tue, 04 Nov 2025 01:43:33 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402344a6282a53a3804f5250fa5c06d7524f06edb10f43bf80f470f5a9bd7099`  
		Last Modified: Tue, 04 Nov 2025 01:57:26 GMT  
		Size: 10.7 MB (10672195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d05db15a819feae17e1dd28aa1fdf7cfb54738dcfa133f3732f893380047e`  
		Last Modified: Tue, 04 Nov 2025 01:57:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:86a1b3a5fdb316d8be54856435f121c19a309eb5e5bacf06fa587b1d72a723e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912dab341ddf52ea17dfddb92328f5710ef010cc962050265ff0ec5dc33ca108`

```dockerfile
```

-	Layers:
	-	`sha256:2866004cce9eecb02da11e8a0c4b0fdd87ff2da4713f92a3e5b09bc999e16ff8`  
		Last Modified: Tue, 04 Nov 2025 07:57:37 GMT  
		Size: 2.1 MB (2093814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78576ca2cebc2c9c02233ed87dd882b21d9b7f5157f072fbab51faafb5dd0218`  
		Last Modified: Tue, 04 Nov 2025 07:57:37 GMT  
		Size: 22.1 KB (22065 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:416f76e0939f5d6e8695e30410647ca23c083084a997fe7daaf83fe3730e6804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42469627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24f264f2fa7b691dfa468b7cdbbedd87dbd989924272e4fdf0d76643c6e99a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.2.7
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Thu, 23 Oct 2025 17:13:31 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Thu, 23 Oct 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 23 Oct 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Oct 2025 17:13:31 GMT
USER haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 23 Oct 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdbafedea5d5252d209f3230c0a782066a9adab715d650edf6456f1314148cf`  
		Last Modified: Tue, 21 Oct 2025 01:24:27 GMT  
		Size: 1.3 MB (1294444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2627b87008b67bae410024700ba44b608d1c45e0cff1e5f524ad9a054507fe`  
		Last Modified: Tue, 21 Oct 2025 01:24:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357858f26d6b04e8add3fffc6cd65f2e86d35a628335b5cd33366b18b305b38e`  
		Last Modified: Fri, 24 Oct 2025 18:25:18 GMT  
		Size: 11.3 MB (11336290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431027f0c5276c931ad051264ce19d2cb2169e30e801a5751547cec4715e5bcc`  
		Last Modified: Fri, 24 Oct 2025 18:25:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e29fa990b07ab8d90adc63251a658e9ead2c48ea841f5d83094718de6b464872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8786f4a757b0334dd4023b243e91ff2bee38cc6e4b5266ec72dae76ced37b1e`

```dockerfile
```

-	Layers:
	-	`sha256:dab8ce86fd18ef39b5353631e8ea74510548c129b27c0cd22bebb6aa437bf58b`  
		Last Modified: Fri, 24 Oct 2025 21:56:52 GMT  
		Size: 2.1 MB (2101315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effe5695cda8a5ce417457bf579a2dc365e0c1c6a09762ff9e09f111c2617f60`  
		Last Modified: Fri, 24 Oct 2025 21:56:52 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
