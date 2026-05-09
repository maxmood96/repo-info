## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:99b32f9f1056eee6f01f19b4914d22116d32f7baf757b91bd92f45d342ff9350
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
$ docker pull haproxy@sha256:82e6a4712ba090d0025152a81b1dfb1382e0950416ac2ec481fdd8ca76c97302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44531631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906f4415e1ab34a3a55656d5464a5538a6dc2df2b255138ba59caf8f7180b65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:41 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:15:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 19:16:23 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 19:16:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 19:16:23 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 19:16:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 19:16:23 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 19:16:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:16:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:16:23 GMT
USER haproxy
# Fri, 08 May 2026 19:16:23 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 19:16:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fd62cba5654bf05603608000f4e5723fd66291a54f4a7159fdec91809ff04a`  
		Last Modified: Fri, 08 May 2026 19:16:30 GMT  
		Size: 1.6 MB (1581135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539532484422992e647bbf47ca65d3b8f6a0453e0f679c4473b0a6186b60a748`  
		Last Modified: Fri, 08 May 2026 19:16:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8288dedab843910354bf21968789f6efd8af83f69328fcecc7a158de03bdd5d`  
		Last Modified: Fri, 08 May 2026 19:16:30 GMT  
		Size: 13.2 MB (13168629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24aca07c65b02391365eab13942c7f8e55c7a76975b9bf6545743538b021c2c3`  
		Last Modified: Fri, 08 May 2026 19:16:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c51223cf02d1f7a5f4caa19466f3cf2c58192cab6d9982f1af201d93873a5166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7611cf5950b172220357b9d3d939293e7cbf5e8907efa632ac64b55bc705131e`

```dockerfile
```

-	Layers:
	-	`sha256:a4253c14c2b97555482f03a36657c1ff665a30665915ee8dd28e7cf7e9084904`  
		Last Modified: Fri, 08 May 2026 19:16:30 GMT  
		Size: 2.1 MB (2113806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8b26335a9e0ecd4147bc3a24e0a70532b12fde51c11a8bf2c512fabbc8f3d7`  
		Last Modified: Fri, 08 May 2026 19:16:30 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:927fc80604c750e6b7c239ee763e4f00343728505c39476312db7b850d60ae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42795897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d24e55332b183008d40362b1a83121ecf3c30307878111802f30fc53a021f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:25:42 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 20:26:38 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 20:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 20:26:38 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 20:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 20:26:38 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 20:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:26:38 GMT
USER haproxy
# Fri, 08 May 2026 20:26:38 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 20:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a5e937cb0ed532c3ec54d4345fdfc3439b3250b471bf550ca1b47a6ec32fb`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 1.5 MB (1535744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b30e2a4916fc583c262976003b436568a814648401e55637f6b5f4fad128ad`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29d9822ddf84e5676aba6b16e4ca474cff2f7d103b026515f459525463aaafc`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 13.3 MB (13310309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f3d9a245b5223964556a1e6be1a87f5fda02c295e340bcbf9030737fbcef1`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2dbc336467dad7643c4d1d7d6b9afcb34e1a7f5749f46275d6eb899a51a2d604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd496b427d73be2ed981cc7bbe20f9cc00cbe861c8f5d444e984b27edf22ecb`

```dockerfile
```

-	Layers:
	-	`sha256:8f799a799516a8929363d09c1d61b6461bc28d5249e3e6e1e3103f0b84890a93`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 2.1 MB (2116786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a117045c43675c287e74ed6d78ee2a496452303d8ef70aaeacd48c82c683dfa5`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b9213aac80c8999418bdf3b204e26b88c78a3af3a10feb916c7687552eb68f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40773554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ca373ac9af0ec265a773ae5a3a05491630a102a37ae4c08238b79e323eaed2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:14:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:14:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 19:15:55 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 19:15:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 19:15:55 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 19:15:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 19:15:55 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 19:15:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:15:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:15:55 GMT
USER haproxy
# Fri, 08 May 2026 19:15:55 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 19:15:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1dd55ccc1bfbb566f99369706253dabece0185da7e26a6e06782f899b266a1`  
		Last Modified: Fri, 08 May 2026 19:16:03 GMT  
		Size: 1.5 MB (1489517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408504b9ee1dcc53a7a4f3d7a864bad6d7b95942ccc8782184b61b51926ce0d3`  
		Last Modified: Fri, 08 May 2026 19:15:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1881407f52c95c277659e0c9c956da2d907432d45a6acdd9f0f73092211fe9c`  
		Last Modified: Fri, 08 May 2026 19:16:04 GMT  
		Size: 13.1 MB (13067482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e041d3df4205a07a6be177ed12a215ca337d76b43e120c1263fbd223a8fd7`  
		Last Modified: Fri, 08 May 2026 19:16:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a723382bc7b299f24bb516dcfaaece2be432fde753a09101b0b2306b7084f3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729b6fdd4dccd16f1e59ed0917cb0e0b3213ef5f5432d11eb66199b7f96e953e`

```dockerfile
```

-	Layers:
	-	`sha256:f94084c9fbe7b98c0591952f9b2d6dc9cc40e0c037c7dae4f279681762f46b44`  
		Last Modified: Fri, 08 May 2026 19:16:03 GMT  
		Size: 2.1 MB (2115229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c0645edbe3836ecc0a3a79d342d388ae7315a9a8fedbb0acfa28e7c9e8fc0c`  
		Last Modified: Fri, 08 May 2026 19:16:03 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:598fc5468be0a6edcc5c8741bcc5b21cd49fb91a4bb5ce59fcaf94a02125196a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44780902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5733a4af8b0ddf5ddb9f84f270b2e7c24c16b6a6e54fbfe7fb99b978489545`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:14:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:14:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 19:15:39 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 19:15:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 19:15:39 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 19:15:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 19:15:39 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 19:15:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:15:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:15:39 GMT
USER haproxy
# Fri, 08 May 2026 19:15:39 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 19:15:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86883b58c4c8dbc19f1cb9afc3fbd846032cd31d0120b0fcf6c95ae3afb41f`  
		Last Modified: Fri, 08 May 2026 19:15:47 GMT  
		Size: 1.6 MB (1563689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408504b9ee1dcc53a7a4f3d7a864bad6d7b95942ccc8782184b61b51926ce0d3`  
		Last Modified: Fri, 08 May 2026 19:15:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a16a1fca54fa18029ba249eac7ba0bf64d6daf7cc4e09ae5f17d626e226a65`  
		Last Modified: Fri, 08 May 2026 19:15:47 GMT  
		Size: 13.1 MB (13071930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3354f6a5f4b7436461eb089fe95470421714bdaf26c8da70e88c1b5e9dd2214`  
		Last Modified: Fri, 08 May 2026 19:15:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:79fb10dfd573e2f86210c5834e59a60dc925b394fd0fafd48b61396a423b777e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386371719ddb3cb9284af341463938532ad384b3fb7120f554de54e0c48e780a`

```dockerfile
```

-	Layers:
	-	`sha256:693e8dee47f78045b8527f826d63af8d34dff59ecfba074ac3bce8d808295530`  
		Last Modified: Fri, 08 May 2026 19:15:47 GMT  
		Size: 2.1 MB (2114091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335546b2f0034eaf5c53b21d13908d3f726806f960edc6092edcdb8c7b42f040`  
		Last Modified: Fri, 08 May 2026 19:15:47 GMT  
		Size: 22.5 KB (22507 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:262c4835f4eae192cf34831abdb3d0d6a8f8321b5c3af86694b78acf86347e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45761120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5316c1d3e312da1be08201676705774a46a788cec26a1e61cea66b4043af371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:15:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 19:16:11 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 19:16:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 19:16:11 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 19:16:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 19:16:11 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 19:16:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:16:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:16:11 GMT
USER haproxy
# Fri, 08 May 2026 19:16:11 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 19:16:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6f334b4a7e3db3521263d8f876aa5f018978da744690064f42c630d0570752`  
		Last Modified: Fri, 08 May 2026 19:16:19 GMT  
		Size: 1.6 MB (1603361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d210046063a5b8ae55cbb9913dc2bca8aa0d98d44b4a182ad984705fe342259`  
		Last Modified: Fri, 08 May 2026 19:16:19 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4121c44bf5a1f83a764e5ccbb2867117213c6b5e2429441688cc25f2a42cc5`  
		Last Modified: Fri, 08 May 2026 19:16:19 GMT  
		Size: 12.9 MB (12859714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7c7fe5dc8660922e6683b17b315211c69a626cd68e6f5b6962c3946062788`  
		Last Modified: Fri, 08 May 2026 19:16:19 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e23953197d2e23df76a032d335c08ddcd7f6f6900155ad18b920056fc915e70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e9a5da2dd682b1022d4c6db272fa3acd73d0bc51c0a307aab136aacad903c3`

```dockerfile
```

-	Layers:
	-	`sha256:f2c189146bbf795046a192ea5c1a63bc5e27a5ed522fdd7209dfdce97d1d5004`  
		Last Modified: Fri, 08 May 2026 19:16:19 GMT  
		Size: 2.1 MB (2110987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba7c5b6a1fceebd9c78ccb68d62f27d0299d3f748abb3ed829e0f2e23d25237`  
		Last Modified: Fri, 08 May 2026 19:16:18 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c77d68a86e96e2b4ee492933eb1eeff5de937ed10c133747e8c4fef9b9f67f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49092857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32379dcdc7a5bacc75d236e8923b866240b293b2a83228f8c5f9922900da1dd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:21:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 20:25:01 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 20:25:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 20:25:01 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 20:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 20:25:01 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 20:25:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:25:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:25:01 GMT
USER haproxy
# Fri, 08 May 2026 20:25:02 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 20:25:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce439d82ca41d44acbf9df3ed0c15fe33df6ee2baf00b6b017579376d9c3859`  
		Last Modified: Fri, 08 May 2026 20:23:03 GMT  
		Size: 1.6 MB (1639074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46b41a4d8a25e8f50a6a5d7e21caa314cc572fcc1915de0dc72245edfd0ed7a`  
		Last Modified: Fri, 08 May 2026 20:23:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b3fd0fc14d6c6f89786c5c50bdaa1f6fb5b8e5951de716a00743b7a16f5a06`  
		Last Modified: Fri, 08 May 2026 20:25:20 GMT  
		Size: 13.9 MB (13854053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031c06a3226b760666f1f92c804a7c31b4be796dbe9504a3e42e3149eb036635`  
		Last Modified: Fri, 08 May 2026 20:25:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ae402e01719e47777a048e5e891ea773160d3e59a866d0d22ef30973137a728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38678ed4e48ecf230f1adc184d1364ca8422a141b093f22a286eaa36b5c78cb4`

```dockerfile
```

-	Layers:
	-	`sha256:12ee4b4c20475ef2feb020cb859884b8feee67f17b250c6b297e94ecd7d23e54`  
		Last Modified: Fri, 08 May 2026 20:25:19 GMT  
		Size: 2.1 MB (2117352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0c2b3e733ef79247b6c271ca1f54c92b040891ac12e6c64b79389330edda1d`  
		Last Modified: Fri, 08 May 2026 20:25:19 GMT  
		Size: 22.4 KB (22409 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:a93684a75dfa0dc424097654eb903dba12bc65fb7160133f49f6b12e1c247d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42583058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0744751c76ac6eccbbf9ffc04687c6585ebbfdb74e4b3aa69ec874f073263b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:07:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:07:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 06:20:10 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 06:20:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 06:20:10 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 06:20:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 06:20:10 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 06:20:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 06:20:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 06:20:10 GMT
USER haproxy
# Fri, 01 May 2026 06:20:10 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 06:20:10 GMT
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
	-	`sha256:066b0de7c750cc6920eb31e89b8e3942fec76496f206dca684e472023d56edf1`  
		Last Modified: Fri, 01 May 2026 06:21:16 GMT  
		Size: 12.8 MB (12765779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afc3c19362d5c265e95719fa3b937005c667b238f1fe267400fe94ddb6fe19e`  
		Last Modified: Fri, 01 May 2026 06:21:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5dd54fa8cbf32a6257f735054002b741f4d4164fceae7c4895e0651ed9e99603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4128ee6203844b9b323578a9325f54315034f8953847693db7044139efe819`

```dockerfile
```

-	Layers:
	-	`sha256:8e952508464b6168f104cd163e6b2a08257129d730605cb9f6fc979cf1e6201f`  
		Last Modified: Fri, 01 May 2026 06:21:15 GMT  
		Size: 2.1 MB (2107743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8eb4c080c041abfbb8a470a49268e5a17ba290cc08606bac4a2c29cfd0616b`  
		Last Modified: Fri, 01 May 2026 06:21:14 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:bec6812328706ccf3c90a82c3e54795b5cd077996a439aa77e42f316a3e192a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44909505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3aa5e36b79f4c95503765fa37ad37eea2940e901db27ecd742c97e34cea6d59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:06 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:15:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 08 May 2026 19:16:30 GMT
ENV HAPROXY_VERSION=3.2.18
# Fri, 08 May 2026 19:16:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.18.tar.gz
# Fri, 08 May 2026 19:16:30 GMT
ENV HAPROXY_SHA256=da8c1486d418e11188febbbb90a3a64690ed9e5c882c711b688b82fd4907143c
# Fri, 08 May 2026 19:16:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 08 May 2026 19:16:30 GMT
STOPSIGNAL SIGUSR1
# Fri, 08 May 2026 19:16:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:16:30 GMT
USER haproxy
# Fri, 08 May 2026 19:16:30 GMT
WORKDIR /var/lib/haproxy
# Fri, 08 May 2026 19:16:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ce30412c10dd9aa038fa21b38baee56528e7b7ea7db27db60aeb56d920db6`  
		Last Modified: Fri, 08 May 2026 19:16:43 GMT  
		Size: 1.6 MB (1599882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df3b9516adf9e0e67f509db58c9d90feab438f77a64aae3ad1923ad493a4826`  
		Last Modified: Fri, 08 May 2026 19:16:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a222ffb365a34a935d8989f78601ec591ab4a0ea2eb9b2ddbbb104fb1f606`  
		Last Modified: Fri, 08 May 2026 19:16:43 GMT  
		Size: 13.5 MB (13467634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957ddb2ef0c5d1bacff002e1b948ee0f15ced7a8ad3eb3d27cf587653375b066`  
		Last Modified: Fri, 08 May 2026 19:16:43 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:9a3aacf30fcf1d0a3c95da9d3c2385e8b303230118a26d662755fc9d248f1e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d868f62ef8f70ffd4d178dda2e969ea133ab3146c87cb391beecdb94c9e14c99`

```dockerfile
```

-	Layers:
	-	`sha256:74610573b759fd9bc5e8ba5106117e4647ca2fead4aeb7becf34728b2ce7cf25`  
		Last Modified: Fri, 08 May 2026 19:16:43 GMT  
		Size: 2.1 MB (2115250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c702d9b0ef508068afce6be683786fffb44d920ae00f5852a37f019a076cbd67`  
		Last Modified: Fri, 08 May 2026 19:16:42 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
