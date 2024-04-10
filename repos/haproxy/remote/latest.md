## `haproxy:latest`

```console
$ docker pull haproxy@sha256:fdfc61f6b6fd80689e02bd6e5bf05468e3669223f7eab29bcfd2923c34b721dd
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

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:dbfb164db90efa4f9a63a6ca7d7d5944359843557c891daa86d44fbfd9d66a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41196766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7d41c0adac3e2cb83458ff18c04cdbad8ee111f4e5695162d3734934570292`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac993fb7f46641a65aed0f2c478009325936d66ebde8a82bc8cbad25ec4c785`  
		Last Modified: Wed, 10 Apr 2024 02:54:40 GMT  
		Size: 3.5 MB (3491140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c555fa37a6ba829fbcca13302abcafccaba87895dcac81ee8b89ed6f33618243`  
		Last Modified: Wed, 10 Apr 2024 02:54:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1ce9a5734ef6177e6957f1a8e3992f4f6d5147f986cdce253ef7c4552948d3`  
		Last Modified: Wed, 10 Apr 2024 02:54:40 GMT  
		Size: 8.6 MB (8572631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4104d9a681bcdb6c1d0fc93feb9ef916fbf0273f571dd87918a42b16c93e3`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:281ecdb82d448263c704bb72cd55860dd9ff30a253f4cc1d9497f48d8b89ec44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ce419c5089b8e2b00a53df0bd52ab6b2e7d800675a6b4fd6490631c48f039d`

```dockerfile
```

-	Layers:
	-	`sha256:62d5111926eb0334d31c4bdeabdd6608f94c1e51d7d1e03dee9f7ddd11a74c4b`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 2.3 MB (2340969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ce50f1e6f8858401b86a819c81f1d37d763e6db9af00457d0c66d054af9ea4`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 21.7 KB (21690 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e466abca53f94cdb37fdf32ce3a6b0c8c4ba632cfda4516c6958a62aadb100db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38487755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896f1d17e459c35e6147c4afe477f5a602bd1e9ab6306940990060f5d180af49`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:1aed75e3934c48f33db1c721bc35850de57d23ca20611777409e26bd38144917`  
		Last Modified: Tue, 09 Apr 2024 04:38:00 GMT  
		Size: 8.5 MB (8535505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc54b95f571ec85ec6998b9b2c9f97b60bf5e1342742349a9c84f4c6254f57e`  
		Last Modified: Tue, 09 Apr 2024 04:38:00 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:cf62bf10e988757427eabc10eec29f516ba3fc5a9ee806a9fdcec381cb53ed51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201446b8b727451edd1c80dea9a574d57605b2e3325e288e75a2ecd6710fd95f`

```dockerfile
```

-	Layers:
	-	`sha256:94561d225117bb515555e4a6f98c0718f8ec5712ac838ecfca6c095c94e656e4`  
		Last Modified: Tue, 09 Apr 2024 04:38:00 GMT  
		Size: 2.3 MB (2345517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63eee3afa653b63b4e8178cfb86ef272b7943195632fb59af3bb36ba03b4615`  
		Last Modified: Tue, 09 Apr 2024 04:37:59 GMT  
		Size: 21.6 KB (21635 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:4d300f3f7b3d3bdd065c8ca2ed9b4fb1b8aa96cd720efa99a59fef702e0f516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35994552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980e8bc5b1802af1e3a8c4af2a4ae204e84470dd7727e13aaa651156b526ef9c`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:ff3f9243a022dedea0646e3ca0cd3cb58d9e9b84e8357340baa3bb1b7731f8fa`  
		Last Modified: Tue, 09 Apr 2024 06:34:21 GMT  
		Size: 8.4 MB (8372398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ad92424030c21c1fb937aff2accd93731ae2ec9e02b99d8888d6160bc2437d`  
		Last Modified: Tue, 09 Apr 2024 06:34:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6b9f925d885cdcdcdfbe20a71afde66ebb6247dd5589f47533031f4ca4d859c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cce75000f48b9a29965c427f7b6387360a16faec0eaa48d28eb7c926c02e88`

```dockerfile
```

-	Layers:
	-	`sha256:1cba293b4caba180660c4f62bc6d30fa1eb83ed14e4b1f3b652df3b5c1299a50`  
		Last Modified: Tue, 09 Apr 2024 06:34:21 GMT  
		Size: 2.3 MB (2344495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb75aba473d8669c5d64a88716909e082e38eb4e27cf88a0a862cae968884868`  
		Last Modified: Tue, 09 Apr 2024 06:34:21 GMT  
		Size: 21.6 KB (21634 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e7946f6ce3e78954ac3f186b9b37dad5744083a3f158a5c007624919a9036366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41036272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf0f279a82014e522096a1fc953b069e1769c9e35fe922df1df7fb3ac8f5ad`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:dfa1a0c416e2065441342a75a43b1899dfb7ebc88b1849e61d9ecc2b9ec08cd0`  
		Last Modified: Tue, 09 Apr 2024 06:07:24 GMT  
		Size: 8.6 MB (8563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c602f2a2d6cdcc4fed90f99af2e5223e0ed5c70b455a2906e492b06e2e9179`  
		Last Modified: Tue, 09 Apr 2024 06:07:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:535c91c520ccc071a1baa7f1173bcb8c00bb46a610a42b6752a13fb5baff9553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931d481f1dca0ab489131de7619551d86d6419303dcd653609b2622164f81d90`

```dockerfile
```

-	Layers:
	-	`sha256:065a4031705c68a35aea861b8387e241a0875ce8d4b600b945771199cd7eaaf2`  
		Last Modified: Tue, 09 Apr 2024 06:07:23 GMT  
		Size: 2.3 MB (2342470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3583dd14d173cf8408183af035223d5df760e7a9af3fb87c513e05e04ad330f5`  
		Last Modified: Tue, 09 Apr 2024 06:07:23 GMT  
		Size: 21.5 KB (21537 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:930cdf55233800fc91760ba2d1f55827957c563f241fe43bbd3ce0782d59224f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41978897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0c4c2f67edbe9a38c7db9ef42bc54dce2014b92f43b65492ea874e27ff80c6`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:fdd6a5f10d6990baf20d4d696167da09653c727d7d116c1b84c77a774f864501`  
		Last Modified: Mon, 08 Apr 2024 21:58:19 GMT  
		Size: 3.5 MB (3496258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39489c100ec47b7a327f910d72fd95bde1ddf31849da72ccc4c6edd89afda196`  
		Last Modified: Mon, 08 Apr 2024 21:58:15 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3467e99f7ed9be659d003f5578d352da6a33d6b83ca5b8f18b1cc947ac6132`  
		Last Modified: Mon, 08 Apr 2024 21:58:19 GMT  
		Size: 8.3 MB (8339123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a77f17546d2a17782c46551ea3d5dc181d2edb01440f996b21f4300a16cfaa4`  
		Last Modified: Mon, 08 Apr 2024 21:58:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:4d05668c8108a91fbe5e70d7a1bfb619b5a31bb3efc9e3566779d8f3ff252d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331ddbfd0e26cbf770c40ae2e40aa55763902925f30a2788719e97e450f129b4`

```dockerfile
```

-	Layers:
	-	`sha256:72f93a5a597f4443156db16b4ebbece28e7543ad0ab8d87437e390721ccc2bef`  
		Last Modified: Mon, 08 Apr 2024 21:58:19 GMT  
		Size: 2.3 MB (2339380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5860460c22dc8c5d047e6a6ebd173dbf38f944402614e907d3d627315da153`  
		Last Modified: Mon, 08 Apr 2024 21:58:19 GMT  
		Size: 21.6 KB (21647 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:02c41e458ecc2713af95cb6b225742cf4db2f2f16707182354379023fc54892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40708686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280c7b5639d02e327894e6155a21909a829119e2f4f26141a37c7084f05f5a5f`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:40ceaa779bc0d8b55b47e659e57d9d110e8be525df2840f2f5ed9638e7591db2`  
		Last Modified: Tue, 09 Apr 2024 14:34:43 GMT  
		Size: 8.7 MB (8697459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81caf273848c66bb51e6e4c64f0760045327f23294a85226734d32e06d94ecf9`  
		Last Modified: Tue, 09 Apr 2024 14:34:42 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:9f7f64af57abe3732d54ea635ec5aee43c8d44e5096cef7cc1b4a2fb28962cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f1c31d55351630ad8be496ca1e6b584b608424adcd67cb1b6479d4eb56eb7`

```dockerfile
```

-	Layers:
	-	`sha256:0616bb9745d081da500f0af73b69b2907f039be37da152bba761211fcbe2b9ea`  
		Last Modified: Tue, 09 Apr 2024 14:34:42 GMT  
		Size: 21.4 KB (21389 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:5911fe195584bd561ba66bd3fe82bcc772848cf0725a24ebce43e773557ca8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45873997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348e6cb8f305c4451e15787ec280e52e5d8105462c7fdb71b79c36d4c8a22b99`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:6cba6671ca16179438cef15357f6099a5c518d83d1f3fc99e7a9ac531e22e9f6`  
		Last Modified: Tue, 09 Apr 2024 04:27:27 GMT  
		Size: 9.1 MB (9059303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce6718970f14f9906feccc11ff3dabfe276a4ee26a92ffafad2ef3d437c87e`  
		Last Modified: Tue, 09 Apr 2024 04:27:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:97e64f8f6dd033ac840abc121c063f30cc0fff9214d5b7678f1055508327d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a46eeb138421c1706e79529b48989ba7fd2f316b0e5a04471fcab465193cec`

```dockerfile
```

-	Layers:
	-	`sha256:358a46ee09817d7ea74feb87592381bfbb556000dfb758c8d78da094c7727eba`  
		Last Modified: Tue, 09 Apr 2024 04:27:26 GMT  
		Size: 2.3 MB (2346566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf4a2c1d0e67e0566a8a807b001f7d3ff230c61aa7fb72de4f3688408b79f34`  
		Last Modified: Tue, 09 Apr 2024 04:27:26 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:6b0e57cf1357d0ce0a8ec410be4d39c174800628ca0cfc56ba9ad8848ece796a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39114592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ec7250834a60fb02dc2772565d844cd5e56d418810d45ff87c89c5565ba27a`
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
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:a35a9782e9b7e6d68358e5c3609709282cd6cd23cc3cd62c67fc1ce44013d9bb`  
		Last Modified: Tue, 09 Apr 2024 12:23:05 GMT  
		Size: 8.5 MB (8467085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb5714ffb0ff2b72f68417f9516f9164872b1d7dc8c5facdb56b4bf5284989`  
		Last Modified: Tue, 09 Apr 2024 12:23:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:433a5419771ceda98383188e50e9a5c7d52a7a514af5e36285b7768d93453b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7509ffb1b4dbd6c4697ff4a07b8d4aff3669b9cedb70847484eacd9ec25889d6`

```dockerfile
```

-	Layers:
	-	`sha256:4375a1e4fa4a36145ff754ca6a34f47d699d6d131ed46d975b303cd9f71808bc`  
		Last Modified: Tue, 09 Apr 2024 12:23:05 GMT  
		Size: 2.3 MB (2342082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4834f55d4d1b48874dfe1d0339a6e3959de46da9767e31c5304e152389b5e3eb`  
		Last Modified: Tue, 09 Apr 2024 12:23:04 GMT  
		Size: 21.5 KB (21487 bytes)  
		MIME: application/vnd.in-toto+json
