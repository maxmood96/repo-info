## `haproxy:lts`

```console
$ docker pull haproxy@sha256:1ece2a6ec5d7af4dd4c7c112f5609ba2ac12b5efb4538fbd4c0d55013a7f5a78
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:cfedbdeb479c0f2cadd8e7ae8643aa66cdb9de94334a48e9c1f7d706b3518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40847096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d022ccde5a9fffdc4c191b93feece943538f0bc1246d25827f3e68220eb3c2ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5163600a4f97942444a353a9a48ebd7526d1297dd210d37bcb14d0cbba37d871`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 3.5 MB (3491080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf52ea83b24169c90c49117e2c38c3417d35303016d83ef1925cec4e7936d28`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e21b336545788a2ccea8363619f687b370b7a8d1a7031f12efe859a2183c84`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 8.2 MB (8230188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444caeba79c80f89d8c32815e826760a2139de8cfdad1584a9f1c5d5d1bea1d4`  
		Last Modified: Mon, 08 Apr 2024 21:58:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:e6adb7d6adbf2d6bab7ec433a252a0e1d1ad4881d456b81a3de7ae58ef004aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a8ac56047e7812ae2f45d8dc3ebd9aa8c8962f3319f16e4a7ce681d4232f29`

```dockerfile
```

-	Layers:
	-	`sha256:8736dc0907537388adc8b5bbdfebf1bbfe0a53b227753b6ec8d09edcd28cc495`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 2.3 MB (2342255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9932f772fe3973474fc91c25d0eff5eb1fa81ab6d4e70133e93d1b064e4eee`  
		Last Modified: Mon, 08 Apr 2024 21:58:32 GMT  
		Size: 21.7 KB (21691 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:999a2d969f1209b881650d76dea452a2e6eff891bf3d6a55789ceab71af8afd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38079515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc453822491679ff2f93dd0e44b9676bdd6ea692fae777c81ddfd6c8b7f8a1bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e13f24f23750a4195ba7dfc3d065c9c9b4f1e78e9eed3c6a103b191354e564`  
		Last Modified: Tue, 12 Mar 2024 14:46:14 GMT  
		Size: 3.1 MB (3066590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41351765f2be436094521c9eb864dc5a5e8125b0d0d51df0dcf2e094a2652d9`  
		Last Modified: Tue, 12 Mar 2024 14:46:13 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de8df76aece19d8f6fb6f2347c44377e61cee255e32d601c7f6d7fdc3707af6`  
		Last Modified: Tue, 09 Apr 2024 04:49:36 GMT  
		Size: 8.1 MB (8127266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ea21d2ea6e47a4368aa1ce87049e8e162e44093f25bd3c7604fb29a3f9f4fa`  
		Last Modified: Tue, 09 Apr 2024 04:49:35 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:a7ee52571c109462f6dd8ff2c36184468e29687a6df7d48e02a19f5f48d27ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe5923b07f099217a4be04dbaad59ecd1cbefaefd4471ce944bfe53d3072459`

```dockerfile
```

-	Layers:
	-	`sha256:6c021523d64e0fc29d2078da00fbec729d533f59e2ecac69c0ba3fc42d859662`  
		Last Modified: Tue, 09 Apr 2024 04:49:36 GMT  
		Size: 2.3 MB (2345519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17748c3db3cd394699a1c6456ea30371042718fd076e0097a092d47189e63769`  
		Last Modified: Tue, 09 Apr 2024 04:49:35 GMT  
		Size: 21.6 KB (21637 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:cd79def6802f9e2f16d963f767eb64567b3763d7dd2cc705339b597e590f56b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35600938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3137d8827fc664f30b2655f84805bc8550e6ef24c806fd31cfd3f13c5c8eb53e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642a847d6cca0f4ed1e9e0b05331cbd314a3408e3f125c0fb249670d879832b`  
		Last Modified: Tue, 26 Mar 2024 22:50:17 GMT  
		Size: 2.9 MB (2903786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e7c6fdb285fdfdeb27dc319a8894b4df60d42999f0afffd70092064daae7f`  
		Last Modified: Tue, 26 Mar 2024 22:50:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b3d9fc881d80c0f5e48f10747140240a00c1a8eeb77ca16ce3b62ced511f9c`  
		Last Modified: Tue, 09 Apr 2024 06:37:21 GMT  
		Size: 8.0 MB (7978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5acad2b3c64c77105d2fbb0f658e137e6a7f415aea749ff8796bc68d6d24cc0`  
		Last Modified: Tue, 09 Apr 2024 06:37:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:63a600a41dd2340b3ce731423a1cf676be241afb58f723af9acd599093d04c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fcec50c398ec65018ead6d04a96483689205808329137d12a20a0ae9f5737d`

```dockerfile
```

-	Layers:
	-	`sha256:5a14393f4ddfabf0ecb0d0ae0279895f62bd4827957e5d55b8a9812d7d3e738c`  
		Last Modified: Tue, 09 Apr 2024 06:37:20 GMT  
		Size: 2.3 MB (2344497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4a2fc7947cf04997e5a84ac2502e11afe842525a7625d03a2dea544f5f60ad`  
		Last Modified: Tue, 09 Apr 2024 06:37:20 GMT  
		Size: 21.6 KB (21635 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f6fcf0b2feb2ecde9b9cd04a22ff9962c438fc845444edd0041dee6db8d0ea46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40630538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cef940d8231b590ab3992887c193cbdb69754f97fcbed7e52702acb770a8d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53f800c3e777c80feb2c784d56b125380934eb8e8df3b183be4395f2ab5b69d`  
		Last Modified: Tue, 26 Mar 2024 23:19:42 GMT  
		Size: 3.3 MB (3314234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc27d12957ae2770c48ae915f0ed4b11e0801ee1e6b3ae7b661a29aeb65ede0`  
		Last Modified: Tue, 26 Mar 2024 23:19:41 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf397154a92869528a117e1a58aa94b6f69db82cb937bf1de140734b76c9731`  
		Last Modified: Tue, 09 Apr 2024 06:19:38 GMT  
		Size: 8.2 MB (8158225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f67fa114e5f7ade969c4f13406c5b2450c01c02488488a2ebee74f5027579`  
		Last Modified: Tue, 09 Apr 2024 06:19:37 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:a4c1d9aa73171e26732fcfbb6747f9a2f49a053728562341d8b4e817e7f21fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d376dfb6bc0a1b597d99bb962bd992dd14c72e090553989d07af5e42fcbd1b`

```dockerfile
```

-	Layers:
	-	`sha256:b77a789565d2c51b7b3e61b8c401d57d26408fa15741cb8ca1cb4fd06cfb48bf`  
		Last Modified: Tue, 09 Apr 2024 06:19:38 GMT  
		Size: 2.3 MB (2342472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e40fb4e9f52081eb4fa70a33b52470165e0fa235f594d8540acbe7b43ea6cd1`  
		Last Modified: Tue, 09 Apr 2024 06:19:37 GMT  
		Size: 21.5 KB (21539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:813c386b3b3dda709714bc2133f752b9032194b9d33d91e312d106a71d509752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41641863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3686db5dc6d244ed2410830e1366a53a0cf29b05265459866c1c774302e79f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cf5dce524f99068d1d2d56239884169b7607ddd5670e6ee4ebfa4eb1abd7db`  
		Last Modified: Mon, 08 Apr 2024 21:58:46 GMT  
		Size: 3.5 MB (3496207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2d6bcfe82e8916873c69777d224cd3e8b0a408df1cf221d4b7b56680045969`  
		Last Modified: Mon, 08 Apr 2024 21:58:46 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc0cce78ff2d225acab3a6dc14a2b60b97f0ea6d0d9fca4a8221a220492be0f`  
		Last Modified: Mon, 08 Apr 2024 21:58:46 GMT  
		Size: 8.0 MB (8002139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e4f03c401ca5f74ec63a8ec3dc18c3070205c122a0b6b96d19639afe84bd7`  
		Last Modified: Mon, 08 Apr 2024 21:58:46 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:96f8f905e73ff2f469e840e78a2d2780b4b665b19f340d341f58fbff70c0b497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1ea5e9315dd66daa498d0a1f0d3653740a1370af4bb1dd2e257cb1a63fbcf8`

```dockerfile
```

-	Layers:
	-	`sha256:d8576da0e8dbc26be54ac6d8a303d5948eadca37a66d8f78319a270b38dc615d`  
		Last Modified: Mon, 08 Apr 2024 21:58:46 GMT  
		Size: 2.3 MB (2339382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b264818941a57c9769a2105c8c561cdaac0b4df9b54fb527fa06f43898156c`  
		Last Modified: Mon, 08 Apr 2024 21:58:45 GMT  
		Size: 21.6 KB (21649 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:be789704cc6073ae3b0da9ef5f64376ebaabc3e5e848ccb8227849b3f5dcd046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40305500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce767e5448bf60360a3ce5354a810d5491922d8eb4b1bac87bec983474ebf14c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01c0f6dae87df14cfb4709821228b0f2d2b4862c96f139ef00ced07e720eb8e`  
		Last Modified: Tue, 09 Apr 2024 14:24:30 GMT  
		Size: 2.9 MB (2890370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf7705eb5a24c6ae3d0f91bf9c99cd99de93879bcf8856bd797f8ed908185bd`  
		Last Modified: Tue, 09 Apr 2024 14:24:29 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7e17918f75f04527348eb78a25a2dd9496b3ce1dca84e304b003d17cbfddc8`  
		Last Modified: Tue, 09 Apr 2024 14:39:26 GMT  
		Size: 8.3 MB (8294273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27aa6441234b97e8eccbaf10e7c48b144f6592d960d800c5441d0eb257c6553`  
		Last Modified: Tue, 09 Apr 2024 14:39:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:599e39905dde9d5189c06ec866043b1e56074d78b7cc23bdfad14026058bd17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eae6f17668f08dc2d91f6aa07061ed25b8c5dd131fe63881abf0763f6a7ce7`

```dockerfile
```

-	Layers:
	-	`sha256:bf4a9327d922aaf318cacbc8fcc84bcc68fef9a45621ea3613e6c9d63d77bad8`  
		Last Modified: Tue, 09 Apr 2024 14:39:25 GMT  
		Size: 21.4 KB (21391 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:9af22e08847fdbe3b15a6b62ba253a50e5a1e32597f6ddf26359aa53a887d243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45471362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76132da6b56c8edffc15d7d95f2307de2cadde852000298ac319e2d46e4ac687`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0384e2278148b94aad8cb3963a5f4e2c3b6fca7d7c2712ab8212aa9447b8d0c8`  
		Last Modified: Tue, 26 Mar 2024 23:11:27 GMT  
		Size: 3.7 MB (3694025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74c9ab659b133ac1a1e8a3fad3025aa5cbf279cee6c5b7f5a4e0caa4c28961`  
		Last Modified: Tue, 26 Mar 2024 23:11:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a118f96d444dd11167d0645bc5f2b4ba2da32685a72a387279c9018647bae8ac`  
		Last Modified: Tue, 09 Apr 2024 04:30:14 GMT  
		Size: 8.7 MB (8656666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f002249e2db0b4585f6f8d445dba87589ef6345f1b84512fc7ef67c5ca8a5d7`  
		Last Modified: Tue, 09 Apr 2024 04:30:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:b8b7997594d019f7f4bce880181b934f5b6643ad1310524c044d6ab3e9bc0c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408b6663d9c89633c57e99ca9a486079f7e2fa97c6dfc9de4dccf6f066138f6d`

```dockerfile
```

-	Layers:
	-	`sha256:b79510618d88cf61101e1180971b88edb4967b1416d5d8e1915b7a0104a27250`  
		Last Modified: Tue, 09 Apr 2024 04:30:14 GMT  
		Size: 2.3 MB (2346568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7fc3dd48ca9bc9e91a89fa332f65b06789d0e67195a6b55ab3e31fc2c10ef1`  
		Last Modified: Tue, 09 Apr 2024 04:30:13 GMT  
		Size: 21.6 KB (21579 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:57a46015199c01699dba5012d75db55b0714233d548a9e2b6dee69b4b55a8427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38730633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32e66f2b70619fc5d02996a54c5179cc1dbf5858feb5f38351f6124c73a825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.8.9
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.9.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=7a821478f36f847607f51a51e80f4f890c37af4811d60438e7f63783f67592ff
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8087d6385fc29ebe006f13e0c4ef869b684f736f73004fcfdd3f4f9a61b8f8b`  
		Last Modified: Tue, 26 Mar 2024 22:56:56 GMT  
		Size: 3.2 MB (3157178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03ab9af5b68543194ff5084ee5041576fd6187abcf6e244bb02199465148e95`  
		Last Modified: Tue, 26 Mar 2024 22:56:56 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db44b28cb82298ffb87c9ffe8a7acf953854641dfa59f74e2f37179016285f4`  
		Last Modified: Tue, 09 Apr 2024 12:54:59 GMT  
		Size: 8.1 MB (8083125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10d08fdc0c6fb1116f462c57e829f02fad9a0900045b958dc9c42f1f4685035`  
		Last Modified: Tue, 09 Apr 2024 12:54:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:ed4082b6e1d463dbf89bbf2ecab764275b8e45a2d7f4a2c8279513539eeb8f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fee2fcadef99db9b5eb0693ebcc5b442d46667143349a2abc4c67b8d72f016`

```dockerfile
```

-	Layers:
	-	`sha256:5a93adf8a958769d212e2c34ef7ac89b12609a19cc2b64ca2c4fe732a309673e`  
		Last Modified: Tue, 09 Apr 2024 12:54:59 GMT  
		Size: 2.3 MB (2342084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d58b00d4186114c6e5d53e9edd2b48e2488bd463b2ce8a76378549c3d619ef`  
		Last Modified: Tue, 09 Apr 2024 12:54:59 GMT  
		Size: 21.5 KB (21489 bytes)  
		MIME: application/vnd.in-toto+json
