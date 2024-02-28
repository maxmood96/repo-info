## `haproxy:latest`

```console
$ docker pull haproxy@sha256:89f428704a9dd15cf71c58b122340734655ef0de24762d686699ffb40ba219c9
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
$ docker pull haproxy@sha256:f35edd237c4a04c1834265edc1d406c975e8ace8580895ca3c3a39945a1b7b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47075307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53657d3341d61956861f38616ca838aedcb83514811535fd732ec24fa25cde6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bc70689575ced3f7e0509175ba360428963632978cfb1c9e0a45bdbb256868`  
		Last Modified: Mon, 26 Feb 2024 21:52:20 GMT  
		Size: 3.5 MB (3491109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46eb488dd74f24dadb65d63bf2165799d993cf5a3828b0c3f5189be394dd36`  
		Last Modified: Mon, 26 Feb 2024 21:52:20 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a0e61ee6fe1e8e58316a4dc80710fdde93b20d823a1d293fffe63fd257f89e`  
		Last Modified: Mon, 26 Feb 2024 21:52:20 GMT  
		Size: 14.5 MB (14458468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9cb8cd484554c728f74e11fb3400c47f60f3a7324c53868da86a5b66de080f`  
		Last Modified: Mon, 26 Feb 2024 21:52:20 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:48bfd281245e1347b38be8895dcbcfc40f12be1d932f259c07e4cdd7fe76bdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1022a451527b0b7543717206c0ad983aa6acb18c743f7e5f7cbf39afc0f9c15`

```dockerfile
```

-	Layers:
	-	`sha256:08ae6eec2fa51df1525aafda13b8feeacd31452bedda8177d028fc30ea5b01b8`  
		Last Modified: Mon, 26 Feb 2024 21:52:21 GMT  
		Size: 3.6 MB (3594742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a167d26c1b8abbf003d26b4c29b5aec45d481ab054c77a3763dd1fe0dc1c7050`  
		Last Modified: Mon, 26 Feb 2024 21:52:20 GMT  
		Size: 21.7 KB (21668 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:842b6bb23bc118521e796812eddb84278ce51212d0854acd0b1b9d86bfacb696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43049808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6852a7c3ea6b7c36ae4a6fe3266cf45049dac7782d7a6c25bda338e0ab27e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93250c55b4e76ea7df49c4f3d33908606f353b792be0a7b579571482fb6d4730`  
		Last Modified: Tue, 13 Feb 2024 13:08:25 GMT  
		Size: 3.1 MB (3066716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd191230532aee92f6b2f05ee877c37201168254a79072e26e6715cd8d4e5812`  
		Last Modified: Tue, 13 Feb 2024 13:08:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384302e4e093c3ed2e08b3653b54be52280b8ef5cfb3cf7e78423dcf7570ad00`  
		Last Modified: Mon, 26 Feb 2024 22:11:31 GMT  
		Size: 13.1 MB (13097551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6e5a919e625106b16a8982aa6cb912d2edbd491b2e19e1bd8ac033ed8078d`  
		Last Modified: Mon, 26 Feb 2024 22:11:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d3cd06e6b5f138f7b72505187ebd9bb816568dd3d973831f4cc669b703621724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536b9dc903f52917ff38374912cd7586efaf3aeeb6abbbc597773603124f9895`

```dockerfile
```

-	Layers:
	-	`sha256:2859819ef1392a28d016f07d7e8b7a9f7b42612c0acdafb9bea361e248186b87`  
		Last Modified: Mon, 26 Feb 2024 22:11:30 GMT  
		Size: 3.6 MB (3564998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a225172d625e8a16a555957b64f6a295423f8c7777ff33417d961b3b36700f16`  
		Last Modified: Mon, 26 Feb 2024 22:11:30 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:923ee3ede9b2b78815d3c645bfc4d9a95b23acfda83195f4abc2d7446beb7771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40307534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ef6ee659c2dd6112259fe078b0db66fbe631d09cceb19eb5db91c4dedb36b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
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
	-	`sha256:8b1631827817cfa9d74231fcac358b8cc2e7cc4cc2b823cff85ed9eaa989226d`  
		Last Modified: Mon, 26 Feb 2024 23:46:31 GMT  
		Size: 12.7 MB (12685536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4efbe677dfe6b977c5ca0f650132cb41019b6dddd9b15f41e1a6b0da400bdc6`  
		Last Modified: Mon, 26 Feb 2024 23:46:30 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:086ad3fcc8a4a19f9fa749f1b1903b9bd62479fe3945eed866df901a08f8f8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3586355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487bc6b296fb030717883feb9811b7fb17be42da531c176b83298289f1c6c0e6`

```dockerfile
```

-	Layers:
	-	`sha256:49847588441fdee4e25069146c1f290c92dff475786314156bbbd9d3c17c98ca`  
		Last Modified: Mon, 26 Feb 2024 23:46:30 GMT  
		Size: 3.6 MB (3564742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fced290ffed68941e4cb98a8c2841a57a13fad7fd7effe9df1a1e42750ee72a4`  
		Last Modified: Mon, 26 Feb 2024 23:46:30 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:8895d831bfcb44387605f2c90113e2c1c14fa8e97148fa25ddf8ef2ae53e6f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45938823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94637c786fab9e05dfc9eed98231bfb47bf0daeee47ca9b35b4279185987133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e9b063990eee029df7b6c394a1b21265a48c7e4af8491e730783834270e6c`  
		Last Modified: Wed, 14 Feb 2024 00:00:42 GMT  
		Size: 3.3 MB (3314250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c590571812615054febadef038f8df80f006f94650ae6e99535701a0f6cc57d`  
		Last Modified: Wed, 14 Feb 2024 00:00:42 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db3a04c832f7453abb337062998ead5a08cf7807b46e80ba5732d0e458b9c1`  
		Last Modified: Mon, 26 Feb 2024 22:04:22 GMT  
		Size: 13.5 MB (13466573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d2ddab97bb1c888f8a8a641c0cc3f6c3927f74823c511be9095e697ba48bca`  
		Last Modified: Mon, 26 Feb 2024 22:04:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:1fac6a0e0321cbb5da47753a137cd7a71819bcedc755d5ea0363e805b20b738b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b2e34c68874e4b84de43bc3e04242e18956d260f1bcbf04c89d32c3069759d`

```dockerfile
```

-	Layers:
	-	`sha256:28079c482e9d5be4a6cabd97c43b6aca58dde69ed7c02fb2fdce405ea030d5a1`  
		Last Modified: Mon, 26 Feb 2024 22:04:22 GMT  
		Size: 3.6 MB (3565893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196f354928b9dce94f4a73b302d2bb1e26b8d5313bbf2616bcf05d1123afca0c`  
		Last Modified: Mon, 26 Feb 2024 22:04:21 GMT  
		Size: 21.5 KB (21514 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:d8837feb4523fd540a5be4b0bc07e044e51eab67cb60f5e4c074c9ee0c5ce2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47331268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d79dc91091d36eb1e6e2bb200b872261eb4c7fd8c5e7ef038cd232d879ca8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad9c2e24cb05aed192c0d8affd5d167951118f4dcf6635444c04441dca8fb7`  
		Last Modified: Mon, 26 Feb 2024 21:52:35 GMT  
		Size: 3.5 MB (3496198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f48b5614e8c5ebbfdcb48d5b7bf0a47604b70c68556dd068bd251ced69f432`  
		Last Modified: Mon, 26 Feb 2024 21:52:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d6a5df3081f9e3e9416661f22641a85c7a00f9bf7395e994c6a8c9df02455`  
		Last Modified: Mon, 26 Feb 2024 21:52:36 GMT  
		Size: 13.7 MB (13691622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4b928433090230df03290462eeb615a953e7cdc7f32f60a6c60224da1ff4d9`  
		Last Modified: Mon, 26 Feb 2024 21:52:35 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:5060cb12e0417a262251e053e1f45704932d3837c647d3dd62b6908293ba6f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27eaf7cd3b454c44cefb947ce71bede255098d41d761b8c0be66d87fd7fda25`

```dockerfile
```

-	Layers:
	-	`sha256:999a18b16338b2b636f6ef0c08d59de3e407f2ccb8be4394904e1960d4fe3a5d`  
		Last Modified: Mon, 26 Feb 2024 21:52:35 GMT  
		Size: 3.6 MB (3588650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3b6f85937f9307272e10478df49f7a6e82c7083b27978ba062f9038adf9346`  
		Last Modified: Mon, 26 Feb 2024 21:52:35 GMT  
		Size: 21.6 KB (21625 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:5aa4c55c7f6f1b039be23d3b772ccaec422847b94e1c1d50e248485061e1817e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45933806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f2ed0549d97346044e5f024e6410708220a0983a89bd0b8e87b9f6b62899aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:14 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Tue, 13 Feb 2024 02:04:18 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
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
	-	`sha256:abc0bef471f2caa9738107ad851da44a5e7a39b141b1d55d7214d0977c491c21`  
		Last Modified: Mon, 26 Feb 2024 22:00:13 GMT  
		Size: 13.9 MB (13922682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cab02e916bc1e020eeb2b348e99cee5c4d9e7aab750e6216995d6ff455b0cc0`  
		Last Modified: Mon, 26 Feb 2024 22:00:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:5fc96c6fe10a56e0340c4adb3dc958cc53079ff8f429542848d519b909fc46ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ef02229106cd2533fad018f0d76dc4232049435fa6b80e29c9d2306546c76c`

```dockerfile
```

-	Layers:
	-	`sha256:8fdd063a2a6e1ccc939281080424315900824dc0a137b805e59b3ede3a318dda`  
		Last Modified: Mon, 26 Feb 2024 22:00:11 GMT  
		Size: 21.4 KB (21367 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8728705179ed8fef7f7c5bed4dae0f7f350de567fe3b0f6208cd76f135af5427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013224220f23c025cb17de7eea9d2e837e6716daa913aaf5fa00ce082b2d53ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
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
	-	`sha256:8d01098a61029e36fb6bc39db2b1a8d74e1c6efb3f83f7d02fe1bf0eefba1b1c`  
		Last Modified: Wed, 28 Feb 2024 03:17:06 GMT  
		Size: 14.9 MB (14895880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ae79e60dd7bde5a83b0d0c9649408f21360a366057cc187aa2b95e266915cb`  
		Last Modified: Wed, 28 Feb 2024 03:17:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:df93a91f0a32700d89e46a59d3e6c573fe5be2ca9df6a2fb8e40b1609d043597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3601963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0714ad0ba4e95b85297055f1c733fd8202e8a87de34e5e29fc8ccb63915aede`

```dockerfile
```

-	Layers:
	-	`sha256:8f902e7213cc6ddc629835484545a13d5b1fb145c5140c45923d3ddbee1ce588`  
		Last Modified: Wed, 28 Feb 2024 03:17:06 GMT  
		Size: 3.6 MB (3580408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b60c37b2ed5bc16cd247d08e280fbdbba5ab619113e4cea4f9017c5469e1370`  
		Last Modified: Wed, 28 Feb 2024 03:17:06 GMT  
		Size: 21.6 KB (21555 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:d043085abcca1db33b4cf8a08c2dbd8b06dba949078bbe2eb9a305aa97063fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43928474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b98fe3756abd2e3826bb441c997cbfe323a1ad74ae3e896b9435b5665212fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
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
	-	`sha256:e5c750b24b0c868eeae3a6154390887631825b3d2b23a6af020a3590d64914e4`  
		Last Modified: Mon, 26 Feb 2024 23:01:04 GMT  
		Size: 13.3 MB (13281118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2a450eee9ac643041d4c65cb2c1361500d416aef1ab471f966829be442abcb`  
		Last Modified: Mon, 26 Feb 2024 23:01:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:c3d78979f8c0177ef0f3ec136f147324ff0c8d458fd80b20a54b881692bea283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbf832e4e7017f9f275bad87a0d11b7fc6ba0db51199e21935dc3f2c413195a`

```dockerfile
```

-	Layers:
	-	`sha256:b74e0bb0b5d0c2ce3c6523d3d37817bffe74b064b9f40ec9b07f399031de9d99`  
		Last Modified: Mon, 26 Feb 2024 23:01:03 GMT  
		Size: 3.6 MB (3583019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a70ea7c3e6f9641f03897c9da466bcc1f7d388c4850e4e33716f5c3baebf9c`  
		Last Modified: Mon, 26 Feb 2024 23:01:03 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json
