## `haproxy:latest`

```console
$ docker pull haproxy@sha256:b532d345799840273ac30491b9b5e1c6cb6c1ca236bdf82e474adcd887ab2bcd
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
$ docker pull haproxy@sha256:80047884498fdb2126dc4a649dc2f74d0d6b603fcd64035bac922e54890b78ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38494390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7636b8f98cdce6786243d3822a70c6e9529a6763dacab79d50de7cca3011a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04a79f4825e709dd8c7e44c1d623d2e0efa927282c8e3ecbe8172c47b23ce67`  
		Last Modified: Wed, 10 Apr 2024 11:25:07 GMT  
		Size: 3.1 MB (3066713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10205d2ac0d4f99b5a77a294d61103fd53eab726b1bd40fe7f997c611b33d7`  
		Last Modified: Wed, 10 Apr 2024 11:25:06 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d89e4d7a2059361f434a9ea85b6b7915850e96fdbf82592b06d91f669388f2`  
		Last Modified: Wed, 10 Apr 2024 14:05:44 GMT  
		Size: 8.5 MB (8535472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286806c429c60bec084e704c9f53aea7c9874012221982fdcfa55ee7b7698c0b`  
		Last Modified: Wed, 10 Apr 2024 14:05:43 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:626fbad45aa29581a285beb3fdcf37a04555cf166000dbf871ff6a75df80739e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b9ad2ecfe08bfa275fec44221de1ed13815dccb6403b1cb3718a0183e87f2d`

```dockerfile
```

-	Layers:
	-	`sha256:d657b2c45a2a18e994720e27b522a3a0e41d225ebc3c7e1c12e6cd06b3d60679`  
		Last Modified: Wed, 10 Apr 2024 14:05:44 GMT  
		Size: 2.3 MB (2344233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf65b72b6d21c8d0175c64fbae1a1b5b5ca5f34f40e1d6141c65863bf3461a`  
		Last Modified: Wed, 10 Apr 2024 14:05:43 GMT  
		Size: 21.6 KB (21635 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:2dcb4fa4de25a9f4aa1a7e0ac8b3dba5a6fef1f716595a8f623399c5c27a6d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36000632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd390f6a25fd06a0f835c4efcd9d56f6ea58ba70af37b459e9af96b5b47b66c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
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
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b5a34ee36ae15dd43056cf701a1403641978033b2210956010490147b63735`  
		Last Modified: Wed, 10 Apr 2024 16:04:06 GMT  
		Size: 2.9 MB (2903692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e951340a005e25cd308920f23a63479f4398f338efe5d7a14ed9ea3d9479754a`  
		Last Modified: Wed, 10 Apr 2024 16:04:06 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf31c640d5de6d8966ed4def556a89560e17c03099336721d4a9dd82fba06e9d`  
		Last Modified: Wed, 10 Apr 2024 21:06:04 GMT  
		Size: 8.4 MB (8372373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4da786a6e92e75b37931430945e3fa3e7d841f968979fe62f89bc35ef5ad0b5`  
		Last Modified: Wed, 10 Apr 2024 21:06:03 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b94230e7b8118aa59bc00ea8266963c3a0f930c6cb549ebf0c1788dbac41aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77404632fd77db82037b53c2e112d1f0e99dc37a6c8285840dc60616f41c9f8d`

```dockerfile
```

-	Layers:
	-	`sha256:fd0dff41bb6ae52a6f0c159f95986e30af3057e177825ed482029030ac76c648`  
		Last Modified: Wed, 10 Apr 2024 21:06:04 GMT  
		Size: 2.3 MB (2343211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23deff2acd1962e9f78828a96362175e1ffb1d2f1d6676d1e315d194c6ccca94`  
		Last Modified: Wed, 10 Apr 2024 21:06:03 GMT  
		Size: 21.6 KB (21634 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:21a675a5b7cbede9ed33833aea1366f955e4e82db1377e9b839cb7d1236641db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41041978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47187b5e5447ce898933a64262422ce510d24fc98dab5c5fe3f95a349e7d038`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c3c90a4b8d9022a6a98743bd036c60b3e210e31913161d56a5e28bb4a07943`  
		Last Modified: Wed, 10 Apr 2024 16:10:06 GMT  
		Size: 3.3 MB (3314242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b6d6d845b05de6f905ca83123dc48fe9479f23383be6b857508556e37f46de`  
		Last Modified: Wed, 10 Apr 2024 16:10:06 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241dfb5892505b533cf524516679dc8d7ba808c9899578ea2e60416456c7bf67`  
		Last Modified: Wed, 10 Apr 2024 16:11:21 GMT  
		Size: 8.6 MB (8563937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43e5010bab4eab7e5c2b8c236b17f565f9587125d6871e2e503d8b8206013c3`  
		Last Modified: Wed, 10 Apr 2024 16:11:21 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a81bfb6ca1ef4399add76d898510e3c5d15fd07db0d2198d7b6e1b949dd40f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377ca000cf560842608929043b62eaf86f4d5a7045cd40c263f44611111a3e26`

```dockerfile
```

-	Layers:
	-	`sha256:ab39ad13c9165e817bae641df30e5f1bd24420148e387f28f7cd4b2243e7082e`  
		Last Modified: Wed, 10 Apr 2024 16:11:21 GMT  
		Size: 2.3 MB (2341186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933a053d9308a53d055d06cb85932e978fdb62e226c976ece0f1436d5056f466`  
		Last Modified: Wed, 10 Apr 2024 16:11:21 GMT  
		Size: 21.5 KB (21537 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:82cca3577e1d3a6d1f4297eb549ee971ce42a980e6e1a550ed8bb824dd0bbc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41983411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ec26696ef08c81bd4f5b94b4effefbfaaa239477b568e5364c814498121b9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb9395f77f13cd738e9cce27b166ad1cd6efa719d33b01eca84560e960d9f81`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
		Size: 3.5 MB (3496197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be7b3d87f77c85ea10812fb15fadaebf5794af28ae96d702912660683fbf07`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ee5b136f78d1e1cc311d75d8d1387eb03453463b98c7a1b85891d70a555751`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
		Size: 8.3 MB (8339059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734db26f8b3f17c7fe304118bf39faa847534bd9a495c59657589e3ef33d1326`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:57bd2d96d10c19ed051363e2e34d899b0c88e058ae76aebbd9b3f13ba471eeee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b9769d2f6706a8dae4a719ab1444cd31616b8a29a7a8f720976ab77cc67afd`

```dockerfile
```

-	Layers:
	-	`sha256:ef36041264e252328277c204737d9d5c450c9c8d2dde3cce4f50da4b0da3aa61`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
		Size: 2.3 MB (2338096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d801fe67403231a4ca530a47f832f87ebdee3fd6b7a8d2d4ec4cbb59d1fbf87`  
		Last Modified: Wed, 10 Apr 2024 01:53:18 GMT  
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
$ docker pull haproxy@sha256:4ce0d31e7125b1f198e7aa274cc1f7138bacd8f46b5738c15cdd7688388c6a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45879667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8415db11b663ddd2276f47154fce7d0da176b418b0f4580758ed3b7493c946b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f416ca29cf336188b6f62135862afbdd35d06f535c920b2f210fc409cde9db28`  
		Last Modified: Wed, 10 Apr 2024 16:15:00 GMT  
		Size: 3.7 MB (3694091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721fc2c69be4a2240f419bf488d3f879a2151e1b56888bb3509313a3abbc72a`  
		Last Modified: Wed, 10 Apr 2024 16:14:59 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2770b01437e2d9457ced423a85352770a35e1d087e619df0ddeae514d0884`  
		Last Modified: Wed, 10 Apr 2024 18:39:49 GMT  
		Size: 9.1 MB (9059094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbd160be23d10516f2e7dd4dfecf3478dbf4e2b55a439a0c30fa1c0b699f8f0`  
		Last Modified: Wed, 10 Apr 2024 18:39:49 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:cd4a3a22f202f619a11c252a36426a7a2747472e7ce5dce47f56a4e231704458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db807b98c69bad1a32819942ea2c4696aa9e5bd2fe2c3cf580c87d4aa70add9`

```dockerfile
```

-	Layers:
	-	`sha256:d28d0ac70191ef5791a1d2bf7014e244042f52d09b78eb959f55f60deae11d86`  
		Last Modified: Wed, 10 Apr 2024 18:39:49 GMT  
		Size: 2.3 MB (2345282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a072f060e843aa5fd40322b2b7f3174b904b834dace2df36fdc42cd85a6d236`  
		Last Modified: Wed, 10 Apr 2024 18:39:48 GMT  
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
