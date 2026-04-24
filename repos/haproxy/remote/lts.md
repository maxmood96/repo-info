## `haproxy:lts`

```console
$ docker pull haproxy@sha256:346e6a02fd646d5dd449e2c94aebde3cc7cac32ca6dc8b7b0ddadc9cb423d471
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:7d4ca3c0bfb759cc430c0d217700554fc745b1e4b2ecf37a5d390b76b762872e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44525512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e3d8f9ce5ac2e5c95102b834f8787e21f35e13c376c12fba5740f18c874caa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:13:47 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:13:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:14:30 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 18:14:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 18:14:30 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 18:14:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:14:30 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:14:30 GMT
USER haproxy
# Fri, 24 Apr 2026 18:14:30 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:14:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3e94e7dbc274bcebdb8d8b651e32d353f0b4e7dfd299079d28065ee83c848f`  
		Last Modified: Fri, 24 Apr 2026 18:14:37 GMT  
		Size: 1.6 MB (1581139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4d48f5af158f85935545bdb2b7718497521045ea138c21b0d8064b46ab3e60`  
		Last Modified: Fri, 24 Apr 2026 18:14:37 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3752def8f9b819784d98174f013dd378c98fd869c8ab417d4ad9f235d19c1dad`  
		Last Modified: Fri, 24 Apr 2026 18:14:39 GMT  
		Size: 13.2 MB (13162562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d25aba0bcf1515b1c46e1001a92088fe476400a931d4ab331d4bc49ee730bb`  
		Last Modified: Fri, 24 Apr 2026 18:14:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:67ed26ac97d6a5d25f3a731a46587c4932418c41736bdee829f76397e52817d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649d21c77e1faa6c3d2cb6b9a2baa88e12c7fc672d4b344c688d378df08fe9d3`

```dockerfile
```

-	Layers:
	-	`sha256:8fb65bce8b8f39369f9b811cf1a6d063a05c943fd655fc293002fcb6587d0bb8`  
		Last Modified: Fri, 24 Apr 2026 18:14:37 GMT  
		Size: 2.1 MB (2113806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b20671a11578ddc1c9dd4baebc6ef414a154cb6131b6c5b8da6979aafb0315`  
		Last Modified: Fri, 24 Apr 2026 18:14:37 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8d12d2b51f29968d6bed5bed29fd71bcf0a97806e466881830979f7d690b431e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42790330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78481ef6a3b187a83641071f3a060d6ddfb2b598a0ee21aec7acd1a461828cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:57:38 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:57:39 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:58:32 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 17:58:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 17:58:32 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 17:58:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:58:32 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:58:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:58:32 GMT
USER haproxy
# Fri, 24 Apr 2026 17:58:32 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:58:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d29a39fe7c610777784ff533d22398182b2b79e2f609a2c1030739cb458dbc0`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 1.5 MB (1535711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aec7fad06810a2297543607a6627a032c9eeaa104664fe40fae3ff86d5c8d5f`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac0cfbacc4cf88770983d22b59e0b54c2742aad5afa5a46963e9a7305f40193`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 13.3 MB (13304797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080dd4f4f87ab578b32c7259077603429f60fdeb924bb527f7e7747cb4877002`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:d4c7cba006ae5994ba3ecf88ccc1d7fca46ed144482e4a3035e778d57e031b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03431fb15b2acb9bb5eabe01f8c97ebc46173f9d7a867a380873fdf56e275320`

```dockerfile
```

-	Layers:
	-	`sha256:c90b655a0d0a591e28041bcb0345bdaccc43ccd74e083561421d7e3499bafea1`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 2.1 MB (2116786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51700b31e94ee1c1b76032e3f5f105398b6d298106b3d8d8daff29e0e657b7f1`  
		Last Modified: Fri, 24 Apr 2026 17:58:40 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:eba7806e9d789d0a6b59557b0e03cf6ea657e0fb8bfb906dee12314598c18594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40764413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5af92092177e092624ae9a19bf44c8a404f06e25964bc747694002e936319a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:57:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:57:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:58:05 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 17:58:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 17:58:05 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 17:58:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:58:05 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:58:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:58:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:58:05 GMT
USER haproxy
# Fri, 24 Apr 2026 17:58:05 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:58:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba722a929f1f00451b1798db66f9ac9fb5ae5aa33b3ef543df134b14e6eb7d6a`  
		Last Modified: Fri, 24 Apr 2026 17:58:13 GMT  
		Size: 1.5 MB (1489527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c10cf97ce78a3dbcd9a6f60662a8ac1eec7cd05069cc573d2011ac0671f52dc`  
		Last Modified: Fri, 24 Apr 2026 17:58:12 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1aac00ac387f841a95805f4ed94ed1e193731d623122bbe278fcf43550f540`  
		Last Modified: Fri, 24 Apr 2026 17:58:13 GMT  
		Size: 13.1 MB (13058410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec556a2f3191251fb9aa27d59cc54b59497d7d2bd295cdc4da5c1ee7c999f8b`  
		Last Modified: Fri, 24 Apr 2026 17:58:12 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:4472653836b52b156dec6050690b712664987ff2749d434f2b096f8725af3390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97962278c7d787abedd93de7dc7a6c26322ec81941b2c949cd07d6b2697dca9`

```dockerfile
```

-	Layers:
	-	`sha256:d5071e454eb12e8770bb59d2d30b6289d82dbd1a1a8e199ce92b0f6e34497a36`  
		Last Modified: Fri, 24 Apr 2026 17:58:13 GMT  
		Size: 2.1 MB (2115229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba0de0c812c3940e718335004bca195ac841975a57772102ddf848308e9c87e`  
		Last Modified: Fri, 24 Apr 2026 17:58:12 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:daa888011d597619179bee1dffea3a9089743728a7e0584ac89d7d087aa2e31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44775304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6494d5f9f2aaa401aa21400f5c8e968033b3f4854d39b5398d147369437f345a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:55:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:55:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:57:22 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 17:57:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 17:57:22 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 17:57:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:57:22 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:57:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:57:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:57:22 GMT
USER haproxy
# Fri, 24 Apr 2026 17:57:22 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:57:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739728aff950a56f34e0d954e1a9495171374a4aa15f520c047eff60ad3c46a`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 1.6 MB (1563673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee8eba575fad48849ab02c4fb4f1cc50d98ba532f47efbd1f802db823211c3`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e9897cf64f4dba7431f6f4c21696814ed2587ae14f9cb5047344f526f79a6e`  
		Last Modified: Fri, 24 Apr 2026 17:57:30 GMT  
		Size: 13.1 MB (13066387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ade36fd44e32146bc26ad5a17ffe83a8f6d18b58537656c66d87c5ba0824a4`  
		Last Modified: Fri, 24 Apr 2026 17:57:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:cd441651bc60df899b3478e0e34de0a0282589371f37591b683aa8dbcc1520f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75214efa118dfe23f4894bd3a2d165bf354251d28a6ae41d6fd80071198a42bb`

```dockerfile
```

-	Layers:
	-	`sha256:8462c579f77b03062c410c6955c603c7304267522768e516997728428245e07c`  
		Last Modified: Fri, 24 Apr 2026 17:57:29 GMT  
		Size: 2.1 MB (2114091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477118af07e01d5607f6a5b6fcc5ba07c7f9f7aa3a7395cddb8830a030b92212`  
		Last Modified: Fri, 24 Apr 2026 17:57:29 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:90015e4483e7de479943f2b89c0029f1dc98e950cae95a17bfce2fe3c19517d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45741001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1ba41878c6b9973090a8ffc25444746d788704b441da64021bc1aa4a0870d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:56 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:56 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:42 GMT
ENV HAPROXY_VERSION=3.2.15
# Wed, 22 Apr 2026 01:16:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.15.tar.gz
# Wed, 22 Apr 2026 01:16:42 GMT
ENV HAPROXY_SHA256=117e408aff544c9ad758c2fb3fd8cf791a72609d3ae319b2cf9f2a0b035393c2
# Wed, 22 Apr 2026 01:16:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:42 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:42 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:42 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f0fa3ac0efc856456e71be0a8e73cdd75fc1a02c3068ccae91b97315b4b51f`  
		Last Modified: Wed, 22 Apr 2026 01:16:49 GMT  
		Size: 1.6 MB (1603295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8acb2321dd2d8d40bc9578f73e7a152c846cd090d091594c33e73545a551a2`  
		Last Modified: Wed, 22 Apr 2026 01:16:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001258e602bc76ce398281ecedd0c86290cc37693761ff564e3645d54165a96`  
		Last Modified: Wed, 22 Apr 2026 01:16:50 GMT  
		Size: 12.8 MB (12839740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cf486d153ed4f422f0348a5b88bc1bd6be7a5c8b2b9b89d04880c29753d9d`  
		Last Modified: Wed, 22 Apr 2026 01:16:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:254c4be104f712dfc128f030a7bcf5c89747f36f0e20932ea7c11b9490b2529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4360f45d18560eead3ac3890a2981c2eb06768d99c8bbe85f1a3351e6822924`

```dockerfile
```

-	Layers:
	-	`sha256:51057d30c50bc16617bdaadab01dda47409944faaa3dd2465044fcd23d3ffcce`  
		Last Modified: Wed, 22 Apr 2026 01:16:50 GMT  
		Size: 2.1 MB (2110987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bb0d4209c717a6a1042fa7dc98a41aad2f68530a5b8cb4f193ebbff73ad554`  
		Last Modified: Wed, 22 Apr 2026 01:16:49 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:831c98ac3aa27cfe553cb8ad5daa5b8fc6bebe88567e2eaa7edfc8f22ff492d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49086636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce51e3eb64d18c0cda278cd0ae87774e9af605383cee0cac294947296c52b77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:23:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:23:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:25:51 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 18:25:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 18:25:51 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 18:25:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:25:51 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:25:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:25:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:25:51 GMT
USER haproxy
# Fri, 24 Apr 2026 18:25:52 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:25:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53858ab18906b009afa91fe2a7cba690938b22794d14059026f0942586a70709`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 1.6 MB (1639154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d6554396b0420fa4d7815e5d17c727debcfa279f4cebb40c0ec276f650d7e6`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a357336fd6549879ab1cd2b9439c240f06fec4233d8411493993c4d2263d45b5`  
		Last Modified: Fri, 24 Apr 2026 18:26:09 GMT  
		Size: 13.8 MB (13847810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492b407caab2763b511e1813f2b79b7c3850935c00ea14823acd4b53e567fa23`  
		Last Modified: Fri, 24 Apr 2026 18:26:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:b685342d79a7bf1f9c19d44ade4ff1988ce2fdf719f56174a36cec41f74cbc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3ac7847ea89989618bc7bb57ed424ede628de1bc47e9eb17c7a1c2995b9e6f`

```dockerfile
```

-	Layers:
	-	`sha256:021f4d6c8e2d7f12970fac3c3025e4cf478472926f43b0e7e24ed23bc18d7e15`  
		Last Modified: Fri, 24 Apr 2026 18:26:08 GMT  
		Size: 2.1 MB (2117352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c70dafd11628ccca5aed7217a248156776cbef5772781e7584fdaff9978ce4c`  
		Last Modified: Fri, 24 Apr 2026 18:26:08 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:42097577a01ac86e0cb98184267e3deb6255c54f387bbbbf440a1dc6fec06b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42550771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60c24e14ac3e2da17dbbe54559ce973428f56cfc026ceb44d463513627a0871`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:07:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:07:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 06:55:03 GMT
ENV HAPROXY_VERSION=3.2.15
# Wed, 22 Apr 2026 06:55:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.15.tar.gz
# Wed, 22 Apr 2026 06:55:03 GMT
ENV HAPROXY_SHA256=117e408aff544c9ad758c2fb3fd8cf791a72609d3ae319b2cf9f2a0b035393c2
# Wed, 22 Apr 2026 06:55:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 06:55:03 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 06:55:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 06:55:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 06:55:03 GMT
USER haproxy
# Wed, 22 Apr 2026 06:55:04 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 06:55:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc623a92fa73e7fb55b6cbcec224c9a3d5617dafad79c6a3703ff556e2fea34`  
		Last Modified: Wed, 22 Apr 2026 06:24:22 GMT  
		Size: 1.5 MB (1535443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec766d6a121a8aa9a11c026443ab5b5998bfc0876dd46f9f7ad98a51d65938f6`  
		Last Modified: Wed, 22 Apr 2026 06:24:21 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6dc44477026c298aff0173e0aa9b9461b571f0af8a5951f4821e36f3b12330`  
		Last Modified: Wed, 22 Apr 2026 06:56:09 GMT  
		Size: 12.7 MB (12733491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e0a425d4b345280c43c66dae6b60c5f0c92dc79279449bf058fdc9b35cc13`  
		Last Modified: Wed, 22 Apr 2026 06:56:06 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:00ee85be9547cb5d8a91c839e91def516f8abe3c6c9e91d141f0b8068511abd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b427fc54ff6fe44e4c104046ca2b2d8ba339dd195fca13665b27d669996baa`

```dockerfile
```

-	Layers:
	-	`sha256:2586f3a40a93d0e9e6f40700ca3928a1893e6b1af97fdde4c1d628745693c39a`  
		Last Modified: Wed, 22 Apr 2026 06:56:06 GMT  
		Size: 2.1 MB (2107743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2e99302d954b065b8384db2997b24a9537ba98ef1f087584c654ce2f1d64f1`  
		Last Modified: Wed, 22 Apr 2026 06:56:06 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:ff3ef8ba662c4fef2fab26432279dfa06f33125f2f0d3e10cd68fed06bfbe3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44903522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32d371461e93ac831f5a3d5d95938337a99402e8dc2d15519ece3f189f63f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:03:41 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:03:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:13:26 GMT
ENV HAPROXY_VERSION=3.2.16
# Fri, 24 Apr 2026 18:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.16.tar.gz
# Fri, 24 Apr 2026 18:13:26 GMT
ENV HAPROXY_SHA256=2ed807f2a8742a4c1ec64906fe857bc53472d521aea8dcc453c82b8e5b1ecb02
# Fri, 24 Apr 2026 18:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:13:26 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:13:31 GMT
USER haproxy
# Fri, 24 Apr 2026 18:13:37 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:13:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcf38f09588edcdd8a55ad4ba7070b738ddbcdf1b418e86b7a8291e28ea2673`  
		Last Modified: Fri, 24 Apr 2026 18:14:46 GMT  
		Size: 1.6 MB (1599996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33deb27a01db3f1e7d917ca3122b3cc52c80e5390e142c6a54ead91205a1e725`  
		Last Modified: Fri, 24 Apr 2026 18:14:45 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7ab323f6ed1dbd2f2a0db03aca6f8af3b124d8741631739fb2915a615d734`  
		Last Modified: Fri, 24 Apr 2026 18:14:50 GMT  
		Size: 13.5 MB (13461577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87887ee9ae579011462dd115a2bce834c0a193cbdb44b70af3a0571c82456889`  
		Last Modified: Fri, 24 Apr 2026 18:14:46 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:a369d0b256f51f07f7123a1e411737f1b542daa460c605773b5cae81bb5aad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f490740d3e4e811607a13ddcfa8695f9aa015a89d627511d2a904b805ada70`

```dockerfile
```

-	Layers:
	-	`sha256:f3515c2bae37c71c8c239f2e20483417441802fe46094c4a33cb7e975ce6f291`  
		Last Modified: Fri, 24 Apr 2026 18:14:47 GMT  
		Size: 2.1 MB (2115250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e2e089920446d9d9a248a1e409b2e5b98a2e04cbf1b23d36e67bd2f17dd4b5`  
		Last Modified: Fri, 24 Apr 2026 18:14:40 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
