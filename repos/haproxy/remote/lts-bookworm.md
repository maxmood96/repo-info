## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:ab8bab29deada22b5320267b80564bb807276a4ac063ccc818b25abcc108dcb0
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

### `haproxy:lts-bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:918b5151047c560875c51649e133ad2d6522c8724af78e4ad55b745952f31413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46734728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94e2554aeae6bfed7e2aa39031a67f3c956e324a9b0a2322f6f507b97ecdd8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 27 Feb 2024 00:14:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04600a17db0590534db58192fb9c32fee50653d08afb7ff3a546d1e927c1366`  
		Last Modified: Tue, 12 Mar 2024 01:55:46 GMT  
		Size: 3.5 MB (3491059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a4f169c2baea5bd74314bd073462da7f49623b829b69a7b99943ac5afc3b1`  
		Last Modified: Tue, 12 Mar 2024 01:55:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5323f37f4464bea103b03ea6af14fc8637397ea7b2614ee736ba343e1c983454`  
		Last Modified: Tue, 12 Mar 2024 01:55:46 GMT  
		Size: 14.1 MB (14117849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a37d44badfc8dbb65414958799f8ba9f3b79977b3199e4921c1e9e188f96731`  
		Last Modified: Tue, 12 Mar 2024 01:55:45 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6a1c6d56a10ad20518cc6b9d152ba5649340d741aca74b780f7645ebb275f1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d72b57eaec2e15ad801c284c7d288df10ad6f8c0eaa620b03b5f5e9522bc8a`

```dockerfile
```

-	Layers:
	-	`sha256:544e92b1036162e6c993680e8c9264a207ebde0df67d06ff6d419c4d4c51b87e`  
		Last Modified: Tue, 12 Mar 2024 01:55:45 GMT  
		Size: 3.6 MB (3594744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e838031cb43d921dedaf5bc6b4a31e41b039c51cc04abba8a2150118d704e9`  
		Last Modified: Tue, 12 Mar 2024 01:55:45 GMT  
		Size: 21.7 KB (21670 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:945a32ebe7758a166c2edb5b95875fa381896f1e128e9f1de6335d760a7a42ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42643507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d074cd1bd2957276680f36959e5a5bf0d7bbb29880803562fdd3648724874576`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 27 Feb 2024 00:14:01 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
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
	-	`sha256:fc407c7a36016587563a937740ec86b2cf3e0f819bd6aab81e81e5540d6b5602`  
		Last Modified: Tue, 12 Mar 2024 14:48:16 GMT  
		Size: 12.7 MB (12691259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2924fb66b27255d766df9ed36455b75023ffccbd8e19fab9bc4054678b39b1`  
		Last Modified: Tue, 12 Mar 2024 14:48:15 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ccf9f968fe423cf207c9321d48b9154f3c994e345c3bfd5b2dd5f272f80f221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764403de7332cee1dd9d691f0843a8dc13ddc866bf6fa75dd91de270c63891b7`

```dockerfile
```

-	Layers:
	-	`sha256:2e7b232189ab0458d6e88e69d8e2945852d56ce30af21f2584b58f1b9cda8e27`  
		Last Modified: Tue, 12 Mar 2024 14:48:16 GMT  
		Size: 3.6 MB (3565000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f7fd6cb80f3159ff53e449776e87fe40c93e3c748f7965457d3d7c49029ece`  
		Last Modified: Tue, 12 Mar 2024 14:48:15 GMT  
		Size: 21.6 KB (21615 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d12b4486e413d60c87961aaf1e6add4dd330ffaa6a178c72925b617bc4a2928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39916269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab4a6c4b45a428ac8285210241356c88e074ab230c96e7c4a218abe4400566e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6a3c0c328ab9cd2be5d1f32ef176edabda43d2d24956c6bb6e1988e84f65a`  
		Last Modified: Thu, 15 Feb 2024 01:09:55 GMT  
		Size: 2.9 MB (2903713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f75f8a3d1e7fd4b9fd30b9e4da17379e819f42f9c180e3f892bd4c9c7899b7`  
		Last Modified: Thu, 15 Feb 2024 01:09:54 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869ddf072c378b84d902b44616d520c6229da17c5c7af0f05373e0ad9772c1a2`  
		Last Modified: Tue, 27 Feb 2024 20:52:50 GMT  
		Size: 12.3 MB (12294272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15eef87ecb4e2982e6b82e04d91efbce4ddbaf72c22dd584cf743d908cfe551`  
		Last Modified: Tue, 27 Feb 2024 20:52:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ddc4c6c5bf34e5bbd0c97ebf65c1c3adc430bb3aaf70e0efe832e4cd12a15770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe653f372004a09d6ef7d079cbc7b2122c853c55e2c0f8e97f9938f50c0ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:02d071df2edb63295f46d4949b6b8c261e66bd404018462bcf5cb3f2e2fd173f`  
		Last Modified: Tue, 27 Feb 2024 20:52:49 GMT  
		Size: 3.6 MB (3564744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c05123d26a409ebf5bec6c89ef6a58ee572d88da3061a88bb98062a6985d062`  
		Last Modified: Tue, 27 Feb 2024 20:52:49 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:480a14da3b0b8c13832ba9f512ca6ef7c8e8543a68d38b52965bfb9be20aefea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45535247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff75f9332d138631cf6d4d969672c715e278dd0b2bb49cfb761ef1b4b941a99a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 27 Feb 2024 00:14:01 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ca146aeb522b42978dab483e4757eb7695eb6e80e433bc2aa616a8a022c040`  
		Last Modified: Tue, 12 Mar 2024 21:45:13 GMT  
		Size: 3.3 MB (3314211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084953382f6e216e77936b195f1948216fdb3374c9c4fbe313077ed149c4d83`  
		Last Modified: Tue, 12 Mar 2024 21:45:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc1fc3c39b9ec3f38e0ffd8ca0151b3a9c27609ce0b054319d5a20850371d6`  
		Last Modified: Tue, 12 Mar 2024 21:48:15 GMT  
		Size: 13.1 MB (13062962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268906b5288aad1d1c58d3387361b82e1e491d9204bf30d0999ef375dfbc141b`  
		Last Modified: Tue, 12 Mar 2024 21:48:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b9e281b09195b3eba70aff237bf4f05e0d72c28672dd14de2b30235bbf863bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b23b54ab1c9af41ef970d40bca2f0924e168105e581c67c030a1ef7a861f2e7`

```dockerfile
```

-	Layers:
	-	`sha256:0fa5cb8ccbd72cb5e04ddaec9dd766566ea010ca637f264883ba31c146e01a53`  
		Last Modified: Tue, 12 Mar 2024 21:48:15 GMT  
		Size: 3.6 MB (3565895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2def9ad427390d0f4f9b49c7b0dee3f0011a67a97ade073e18d8e838837eed`  
		Last Modified: Tue, 12 Mar 2024 21:48:15 GMT  
		Size: 21.5 KB (21517 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:7b6f3d597eb371b996341334eb16c4ef65dc43b78b4f6a7790c57598eb5a558e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46987355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4483e4b7460be7cdb223336144caab4ddd53b67d0ca644a55abd0951afc48a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 27 Feb 2024 00:14:01 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3449ebee0436381e9843caba4622f2f997d29b23ab179d085b245979394238ee`  
		Last Modified: Tue, 12 Mar 2024 01:55:56 GMT  
		Size: 3.5 MB (3496180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cf7f90af7a7c24517a9f62e4022f158f245aaa45aa4ffdd41341df8fdbc4c3`  
		Last Modified: Tue, 12 Mar 2024 01:55:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71b16e6af1de9db7d4de0336ce9cc7b13f7ff901bc663fd721cd3f2c0e52ae9`  
		Last Modified: Tue, 12 Mar 2024 01:55:56 GMT  
		Size: 13.3 MB (13347661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b244b09c07a04cb44865cf3787ced0779ee13c6669089b62830794005911b0c2`  
		Last Modified: Tue, 12 Mar 2024 01:55:56 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:efc9d063e006b790eb2f20ede2a7e5f72bf3fae2594806c8513de3f6de9232b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13dd9fe67cb3e1cc165882ee4e428f9bb2379b8bc53f357c1f091e52682fc98f`

```dockerfile
```

-	Layers:
	-	`sha256:edee65d3327ba42ed39c9be283eebe1ff7e132c03cda6f0faca052497a8356d8`  
		Last Modified: Tue, 12 Mar 2024 01:55:56 GMT  
		Size: 3.6 MB (3588652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d486fe4a6310c49e498b3a319904422e0dca4d70ec2f43134d99998b34c25ab`  
		Last Modified: Tue, 12 Mar 2024 01:55:55 GMT  
		Size: 21.6 KB (21627 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:af6dd93ce55170c01656e6cfa615e7c430487ce5fd36c2c35bb47232d4982895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45537831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866b021ae46890e81eca7414beb6f96cf6d84d942bfba830dc2bd318e0d34c39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99344e399ebf8dc8d6b8afb534765405cd5e418ecd0efdafb7ba302fc24dd0eb`  
		Last Modified: Mon, 26 Feb 2024 21:55:05 GMT  
		Size: 2.9 MB (2890389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267c9cb58073b29ad08f3bfe22b9248242542655f5079be2c0e05257bdaea655`  
		Last Modified: Mon, 26 Feb 2024 21:55:04 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a0d9b74f7ad20fd77aff5a217a742e04b3a8d85ac2c6b00856588a638931e6`  
		Last Modified: Tue, 27 Feb 2024 20:55:06 GMT  
		Size: 13.5 MB (13526706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0a25dcfc05801fd2b8b6cfb4818068a448f9b42fb8f56068b24e2e0e05a97`  
		Last Modified: Tue, 27 Feb 2024 20:55:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:3d71987cb377b326db2a34c4b2c01f49dcb5313e70314fac0b4f952e09590abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9095ca96a3f6f698bae27020d246144c5f252972dab51e8149aa19dd5cc3ce`

```dockerfile
```

-	Layers:
	-	`sha256:453b9544d954d7154d93d6aa31543caab87e45cdbdcd8ec17d4accb6463672f5`  
		Last Modified: Tue, 27 Feb 2024 20:55:04 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e6452fb28936eb23c0ffbfbee3a39185ad23f4f79f3c62fec8a37ca6c9e44ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51309829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a8abb63d1ffb44391106f1b82b1bfc45aeaae6ba42dbf8f15d7484f3b92311`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2244971bdeb0ffe951c062c7305fa9f47c0d38c610142a1024bc3988905d6c`  
		Last Modified: Tue, 13 Feb 2024 21:36:07 GMT  
		Size: 3.7 MB (3694014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c7dc76a82910bb57427f3f317178bd4c8307985fa6afb03a7cdae20b661a58`  
		Last Modified: Tue, 13 Feb 2024 21:36:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8739a617357d67644379e922b918bf810ebdb64281246c14bb5a3f8e45125298`  
		Last Modified: Wed, 28 Feb 2024 03:19:30 GMT  
		Size: 14.5 MB (14495268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6188966d8a05175fd8e804b69f71b3734f4839d8f6785dc5005d1e20e10be1cf`  
		Last Modified: Wed, 28 Feb 2024 03:19:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:96991708bad7a94ae9f8f4880b39a6c43473258374b5c92b338acbf62af0d548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3601966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c788d8bb415e988ee8902d487075b1be77df74d4197bd4a2557c4fad4abe909b`

```dockerfile
```

-	Layers:
	-	`sha256:0face5eb33a80a76962088ee23f7f34d99fcffad20a5f1d1ae0782273c9848f9`  
		Last Modified: Wed, 28 Feb 2024 03:19:30 GMT  
		Size: 3.6 MB (3580410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4114182e348591ec2f6b7c3bd092c7e2251d00d32f8a7c3442a0c15cc3d620b1`  
		Last Modified: Wed, 28 Feb 2024 03:19:29 GMT  
		Size: 21.6 KB (21556 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:e1578424a73b099f498d5e24ca4a2780c14a0ae5e2949948b52aba51884c67c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047067d558197afbe3b773077fb759160a96a4f71e4c448cb995cdd9ce879266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_VERSION=2.8.7
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.7.tar.gz
# Tue, 27 Feb 2024 00:14:01 GMT
ENV HAPROXY_SHA256=0d1a61161789c8ec50662955deffba50ab4ebe7efc6c0d947ff570ee7098e7f8
# Tue, 27 Feb 2024 00:14:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
STOPSIGNAL SIGUSR1
# Tue, 27 Feb 2024 00:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 00:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 00:14:01 GMT
USER haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
WORKDIR /var/lib/haproxy
# Tue, 27 Feb 2024 00:14:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428814e8fa5fb530cd5fc01256bc3b1e3b45313a40b33682a5b8245d645055e`  
		Last Modified: Thu, 15 Feb 2024 02:36:06 GMT  
		Size: 3.2 MB (3157133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5cd921306656827a23a5dd80d7cf072b01fe6762188e4b44fa4f897ad7a99b`  
		Last Modified: Thu, 15 Feb 2024 02:36:06 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec2c17ce94a191f2c3843cf935e994f71449961509affbf3dd2411e3bb3b4a`  
		Last Modified: Tue, 27 Feb 2024 21:02:54 GMT  
		Size: 12.9 MB (12897928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c7f80d77b2bfdd0a1defa7bdd9c3db97d3ee74957dc280c576d98e51c5fb3`  
		Last Modified: Tue, 27 Feb 2024 21:02:54 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ffea5883275522bf80227e9e7c46db04636af5bba416ab180a264ac7704b5865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c447eba510a643e80b7a16b56ca5543ead45c803a1e311c869ffac3066e44d5`

```dockerfile
```

-	Layers:
	-	`sha256:895adbd69ba284f411c23bd1d3c3df94809b70c6328317d8db76ebc90a2b3eae`  
		Last Modified: Tue, 27 Feb 2024 21:02:53 GMT  
		Size: 3.6 MB (3583021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa98e50c9a4ba922e71385d1573887d3964324964d988e4fd5d660d8e8e6c95b`  
		Last Modified: Tue, 27 Feb 2024 21:02:53 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json
