## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:fb4c30415a7c1968de413564eae9bc2a64c63eb0a69e17200b85b4dd05e46331
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
$ docker pull haproxy@sha256:03209805748569ea78b643b59d059466831132299ff37ae6181480e9530a06dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42085034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58bfe65ce76794a0cdcbd9b3a29fc99f6bedba97e60d9db6512af92115d384a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:11 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:05:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 04:05:48 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 04:05:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 04:05:48 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 04:05:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 04:05:48 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 04:05:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:48 GMT
USER haproxy
# Tue, 04 Nov 2025 04:05:48 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 04:05:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7664710de582e786054c1b90538791cf97ee10f48af0edd4b799910a9336936`  
		Last Modified: Tue, 04 Nov 2025 04:06:01 GMT  
		Size: 1.3 MB (1279631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d5d2c6edd7674911eb1992baff1cb9f8e42bd3e293bcb3894d97a7dfb792d`  
		Last Modified: Tue, 04 Nov 2025 04:05:56 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e36fe1659008c6c6967e299ca69bf638d21b7c708403d63fbeadef3d00d193`  
		Last Modified: Tue, 04 Nov 2025 04:06:01 GMT  
		Size: 11.0 MB (11025660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac672ece3e1a746836078848db6960cf45f1cca3825ea21c7a3b55be1f7d0d`  
		Last Modified: Tue, 04 Nov 2025 04:06:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:41e90c1e27517f25cdf18c676902d9d27f1778eee04d0e07032133833e642cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1774876560738e3b3dcf79157f73c7442fc6e597e6c89e3269dec1ec9667192`

```dockerfile
```

-	Layers:
	-	`sha256:cfe4656f72d4425e24855672982166bc13982a84a65b90e2968fa9d907c2a00f`  
		Last Modified: Tue, 04 Nov 2025 10:58:27 GMT  
		Size: 2.1 MB (2099870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceaed23b0dc518e5f23c01e892d49328e48bad69f9c8f76dfb72de8db7755e0`  
		Last Modified: Tue, 04 Nov 2025 10:58:28 GMT  
		Size: 22.0 KB (21991 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

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

### `haproxy:lts-trixie` - unknown; unknown

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

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:1654f3e6e8421736ebed309e6c232a959bd99ca479494004a0c68c2794b8a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38345719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5fb2e1315c9f10cdd7be55f8204c0a0dcb5f74f4a54ae8e82b127b45abc33e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:05:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:06:00 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 02:06:42 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 02:06:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 02:06:42 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 02:06:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 02:06:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 02:06:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:06:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:06:42 GMT
USER haproxy
# Tue, 04 Nov 2025 02:06:43 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 02:06:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec9b6f989bd27a38a861ef1db26df136b928a744c72988ab0564fbb60306fb`  
		Last Modified: Tue, 04 Nov 2025 02:06:56 GMT  
		Size: 1.2 MB (1236609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c3125a7c97c601a5fde9f7a5512fed16e74cb39c43e8123f5996aa0bde293`  
		Last Modified: Tue, 04 Nov 2025 02:06:56 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f0bb27c73bff7a9d77a965a6a56020f81fdc4bed24c811296f4f0c20d7643`  
		Last Modified: Tue, 04 Nov 2025 02:06:57 GMT  
		Size: 10.9 MB (10894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b948f6c0ccac000b240684e685c1e0186817d8d8497095fc352ed972e63a23`  
		Last Modified: Tue, 04 Nov 2025 02:06:55 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a186cb7ba6f4eafc59546d40220c20c236f00fb92a9e1cee7f7d27c9ace6233d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8c53bcda6b21b3034def7033981a5b66e45574178334ec2128d36f7e1af501`

```dockerfile
```

-	Layers:
	-	`sha256:d7f5796aef1ec01f6a9c4a92ce689c4e3cef539b9f1890cd8c13eb4a78a256bd`  
		Last Modified: Tue, 04 Nov 2025 10:58:34 GMT  
		Size: 2.1 MB (2101306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24daf1e0cce9f0fe60a06fdf43a1ce35829f06192a2577184da2aa5eebff2519`  
		Last Modified: Tue, 04 Nov 2025 10:58:35 GMT  
		Size: 22.1 KB (22131 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:c6a8ad10f0eaa085ef5955915f4d3640a62f3c2489af69aaea53da45d7e8c1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42359121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2fbd38bcfa291a37aa9394ec35d45564ba9273c74c13ec17f3153d5ba0035a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:18:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 01:19:08 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 01:19:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 01:19:08 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 01:19:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 01:19:08 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 01:19:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:08 GMT
USER haproxy
# Tue, 04 Nov 2025 01:19:08 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 01:19:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89bbdbe432f301ae8bdb961331121ab9e0d79bb1ce236e2eeaf04b14e99105a`  
		Last Modified: Tue, 04 Nov 2025 01:19:26 GMT  
		Size: 1.3 MB (1261425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a0c8d27a88d9ef2f4accfab7ac0cda3ef36e443fa2d38367ea732fdaa603d3`  
		Last Modified: Tue, 04 Nov 2025 01:19:26 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f485eec1143a7e49ac04d100b57285a3c7c877491af3f2339fd0ec3654de0ce9`  
		Last Modified: Tue, 04 Nov 2025 01:19:27 GMT  
		Size: 11.0 MB (10953758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdf7eef78d7e625868a642b948afa50fdd0f838c822f9c188ded6b0b3582b0`  
		Last Modified: Tue, 04 Nov 2025 01:19:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5d3c9b91a1e18dcb817ef094086e19112b210f8a8bb83c14b8dd12251c84341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f47851c45b11b05bbfbb52267720f88dbbd63143db5d6afc62772f5fb25f35`

```dockerfile
```

-	Layers:
	-	`sha256:9d3bbd86c132027fc03fbaa932c860b95d3a24299b2b0101541dc9fca4218d5c`  
		Last Modified: Tue, 04 Nov 2025 10:58:38 GMT  
		Size: 2.1 MB (2100178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653252a71daabbc4ab7ee6ae9b77d8cd7a08b096b9aa30b064e4266e0a74f611`  
		Last Modified: Tue, 04 Nov 2025 10:58:39 GMT  
		Size: 22.2 KB (22175 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:a426a7849ab492a61c38aff244b577028da2c0a491a376398ac758b9f3dfa960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43317657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbb088da156e12a9817b06215ace233c9ad1f1ed063d8ca40324e2d441a5db6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:33 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:18:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 01:19:16 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 01:19:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 01:19:16 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 01:19:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 01:19:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 01:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:16 GMT
USER haproxy
# Tue, 04 Nov 2025 01:19:16 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 01:19:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444f257e1dbddac2c7272f06053df105f9e95ecbbdabee1f376805f2b513be92`  
		Last Modified: Tue, 04 Nov 2025 01:19:30 GMT  
		Size: 1.3 MB (1287398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d352bcb4d32c2ed80830d905b6eab0202490734fd17f7c39c18fa06e1b05a92`  
		Last Modified: Tue, 04 Nov 2025 01:19:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474ba19da1b35dbedfd4be73770572e25e8813c52464dd42aadd20b781dfd3b2`  
		Last Modified: Tue, 04 Nov 2025 01:19:32 GMT  
		Size: 10.7 MB (10733837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7639ce00eedc801c6e4344004425faeb03cc3c4df3718eb3fffa665b376d8c5b`  
		Last Modified: Tue, 04 Nov 2025 01:19:30 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:775e8150ebccace8912fc4b7815ba629bcee046e45d175e8be39d58c28001f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9137f27db47929bbb84cd494fb4f23b4290b54aa68ea9e596f632e71db793177`

```dockerfile
```

-	Layers:
	-	`sha256:66fff2765023dd445bdaa2661fdd99de9d4b4eb084f0edb891857dee38fca31a`  
		Last Modified: Tue, 04 Nov 2025 10:58:42 GMT  
		Size: 2.1 MB (2097043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc3431838ed4179f43c64081a6b3757e579822f8c7eed993c9893db3e0323ac`  
		Last Modified: Tue, 04 Nov 2025 10:58:43 GMT  
		Size: 21.9 KB (21937 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7be07ae9c4d291cc88450ad10ff403b4facc327df7c58bc84664947a05efef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46583653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a272ff873fe7f15e4122e22e8745e1f8af1e07ce9f1fc3c3b57f828dfbb2c788`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:22:45 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:22:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 01:25:45 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 01:25:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 01:25:45 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 01:25:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 01:25:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 01:25:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:25:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:25:46 GMT
USER haproxy
# Tue, 04 Nov 2025 01:25:47 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 01:25:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae96894c1c4858618d661edcbfeb64b47ab170ebfd9ecbfd02da926d7191372`  
		Last Modified: Tue, 04 Nov 2025 01:24:19 GMT  
		Size: 1.3 MB (1310382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c3e26f470aea20bc0a644c9beef1df14455416eae54469c3c763f5b59dc5b4`  
		Last Modified: Tue, 04 Nov 2025 01:24:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1667c659214167c8aa60a81ddd11a211584fb74bc66df211b51a49f66560f078`  
		Last Modified: Tue, 04 Nov 2025 01:26:15 GMT  
		Size: 11.7 MB (11672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f27fb6ee5bfdc5ac7c12398accb33dcb7cc6b69e17375c2cd89e110424110b`  
		Last Modified: Tue, 04 Nov 2025 01:26:13 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:41bc400923414d0f4bce7f1b3dd7a15211e0ef36785c803ac7134bdfca0c5b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b8faff37eadddf697134cb6911e1d5cd40ae3adb867a4457fee9bb9d4afe8c`

```dockerfile
```

-	Layers:
	-	`sha256:bae5dd1e2f0b434429bff3acc5f9b95e2b2c145fc45b3e6e245fb64bdaea0441`  
		Last Modified: Tue, 04 Nov 2025 10:58:46 GMT  
		Size: 2.1 MB (2103419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b4c38d43db4357aae8d9d8275dbf45ca21aa773fd802fac88f41b5d39dc6db`  
		Last Modified: Tue, 04 Nov 2025 10:58:47 GMT  
		Size: 22.1 KB (22064 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

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

### `haproxy:lts-trixie` - unknown; unknown

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

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:7ec41c88dac84b2ab048dd7f85e757519920f4de7121b5809a2ef992d68ad9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42454601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5506db22f8c5f48fcdc486f3beb10114990e8827e3b0f55484a13ed9c8c6de9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:45:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 06:45:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 04 Nov 2025 06:47:20 GMT
ENV HAPROXY_VERSION=3.2.7
# Tue, 04 Nov 2025 06:47:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Tue, 04 Nov 2025 06:47:20 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Tue, 04 Nov 2025 06:47:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 04 Nov 2025 06:47:20 GMT
STOPSIGNAL SIGUSR1
# Tue, 04 Nov 2025 06:47:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 06:47:20 GMT
USER haproxy
# Tue, 04 Nov 2025 06:47:20 GMT
WORKDIR /var/lib/haproxy
# Tue, 04 Nov 2025 06:47:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8c55aa7ae905e16c2ec5dfcfe076140b73f8baf0dd09604707dc5c28c5bf6a`  
		Last Modified: Tue, 04 Nov 2025 06:46:17 GMT  
		Size: 1.3 MB (1294657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649ec4af6bfa8dc7ad3242a026a7eebbac02813bc24d25527cbdeb4ca960160e`  
		Last Modified: Tue, 04 Nov 2025 06:46:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c2facc35221d25777cb84571e0397898a7475ff740ba84f7a24b4f4f31d2f1`  
		Last Modified: Tue, 04 Nov 2025 06:47:38 GMT  
		Size: 11.3 MB (11320915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1d97d0b64626c21bcb285af0a1871022040d484885c57d256fb391054a3de`  
		Last Modified: Tue, 04 Nov 2025 06:47:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0b956e6030c8fff9aa9f27a23ea64d13441e85e870577374968f912cb9d71524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5616152fc780241f61c22130699b6eb6e6b5da88da557de491e7a8cbedc3c584`

```dockerfile
```

-	Layers:
	-	`sha256:364f9f43a16c7fd11e80fa55280f74b2c86def17c9fec448e36683fa9652840c`  
		Last Modified: Tue, 04 Nov 2025 10:58:53 GMT  
		Size: 2.1 MB (2101315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afecfadc0b2c05a76bc105233fa319de7e61724adf33caaa236569e17c8efa20`  
		Last Modified: Tue, 04 Nov 2025 10:58:54 GMT  
		Size: 22.0 KB (21993 bytes)  
		MIME: application/vnd.in-toto+json
