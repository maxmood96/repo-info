## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:9f6356a037268fec92910d2fd92539dec38526a4883651983ea50f2ecaf8729f
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
$ docker pull haproxy@sha256:be7979197b198119eb26e14e1177ea69ed75d520d71bf12109806399bb5d4d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41794223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f77122073e34d6e9cf2c526c912acaa66ce45717bda600b8bfd7a17afd818bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e82466095e8607b7bf5a662f43e26237bf351ed18d73695f0e478c2855659ad`  
		Last Modified: Fri, 12 Jul 2024 00:56:44 GMT  
		Size: 3.5 MB (3495529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ec32308b04eac071517b9b125a354ff8c716466eb1381997394e27778f5e3`  
		Last Modified: Fri, 12 Jul 2024 00:56:43 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5519d67c741fe213269d9b24ce30da579ecc76ce0e137ffe0cee7a4917ed47d`  
		Last Modified: Fri, 12 Jul 2024 00:56:44 GMT  
		Size: 9.2 MB (9170774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50adbd00958bdfd2100d132dad1336bd39454c4382f89017d886de3fb46e7550`  
		Last Modified: Fri, 12 Jul 2024 00:56:43 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7834e9c34ccea52d3441c8e1629e118228713c71907f01bc79c0c2d426e76f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42991f2880a86f37c7e6d469f25ec626096078932fe465f2d00de912553f21e4`

```dockerfile
```

-	Layers:
	-	`sha256:730b44d78e4a5acc2949d92a32b268396e2159a4cf17cd7ce0eb23ec29f5efa4`  
		Last Modified: Fri, 12 Jul 2024 00:56:44 GMT  
		Size: 2.3 MB (2341731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e9009398f7b0c908f9aefe9be49bbea01eca648f7c6300ee4fd3080328de95`  
		Last Modified: Fri, 12 Jul 2024 00:56:43 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:5fc859a98b169a5ee18e744e5ccac80228eb0449311f85734445985689c6170f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39073612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269ac0125441684289aca4bc339935b4763d306dabd9c7c6b14b3ce22c142621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:27 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Tue, 02 Jul 2024 00:48:27 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419b4f014b023339b460d1b06b72485f012343d6d81b783938689b243871f556`  
		Last Modified: Fri, 12 Jul 2024 00:56:14 GMT  
		Size: 3.1 MB (3071466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b415ffb3a96d3ab34279e68f2e059dafe5f2e7c02ef3f9d4115c282b3716d9`  
		Last Modified: Fri, 12 Jul 2024 00:56:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646ad5b459fecd91932f7ecb3c7dcb1affec56fd3559c4227af1520ee19ee256`  
		Last Modified: Fri, 12 Jul 2024 00:56:14 GMT  
		Size: 9.1 MB (9113219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb31f5ec8871981ce5ba40c0cc462080ce8097e9726d5a55c307fef7d2435cbd`  
		Last Modified: Fri, 12 Jul 2024 00:56:13 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1e9bd4a98b0e1666f3bce5427bc9f56bd6e7f958be6cbe0e8843abcf6dbced6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ac023ed2c0488263654b10dd13fa5b3da26a1e8995cdb18ab9823e356761ed`

```dockerfile
```

-	Layers:
	-	`sha256:04a8ef157f14c83010f790235068faa98e6d06e8268012f55abc5280ff8af75e`  
		Last Modified: Fri, 12 Jul 2024 00:56:14 GMT  
		Size: 2.3 MB (2345011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40c3e4c71d6e95a49748174ad45d9cd3af70cb1bea69d6c78a52009933ee69c`  
		Last Modified: Fri, 12 Jul 2024 00:56:13 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:ca5e0395eaf0c0bcd2cce053267636245a5294aed1e1eb804319aae8b7f05ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36572787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2622e7933a9ea053164f9eb3af58faf8da33464679c4416ce07bd5d0a351098`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea203fd35e82216129ac5994a221065d3f373c160a1e27a5527526f04b318a7b`  
		Last Modified: Fri, 12 Jul 2024 00:58:22 GMT  
		Size: 2.9 MB (2906260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240bc59a5f92c56a900302bf6d2ddf89f66ff83bad87ab60c50be46275ea901c`  
		Last Modified: Fri, 12 Jul 2024 00:58:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c731bb17fc310140b6c31df02f83c0b67c231d9f9bc3e37545ef8dc3993bd258`  
		Last Modified: Fri, 12 Jul 2024 00:58:22 GMT  
		Size: 8.9 MB (8946717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d95d92a0516ed9ec843e5219684bf941b50a112d6b188075da91ed79da843d`  
		Last Modified: Fri, 12 Jul 2024 00:58:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d6af146f9a39432ebeb258356df509bca0b158531f231f62a945484de09cac62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993a6e57e7802c0e9fb2225da3ece46fe5546889176e659a721ac94c67929044`

```dockerfile
```

-	Layers:
	-	`sha256:032e4aeffc7e3881f215d04f9e729f40578c8cd9aae5e630f935364985fe7be7`  
		Last Modified: Fri, 12 Jul 2024 00:58:22 GMT  
		Size: 2.3 MB (2343989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1e38c80538517e94389da3fb073cf25f9c5747eb693c9f68f3d2a60a1a4e6f`  
		Last Modified: Fri, 12 Jul 2024 00:58:21 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2cd021338def0d948ee7a8479d8c3ddb4aa4a04c16bae9ad3c0cae46127d7733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41639198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2ba40e44f8337913118e112ec149d7cd1a6304115843b290165f8c70125b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652c547cc81f93a744d1fd2d1e79d85326c60cd50215064e4b8aa72226ba7c0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 3.3 MB (3318940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8171de54bc15583c3905d9db008cd8cb12923a7b27832d135763c78dbd1780ab`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2990367f10f9ffb42d16b1257b13f150558bf228206a2459c2394fbd9fcb0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 9.2 MB (9162056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92482e0c2fcfced82fa7371a45d23984a7f831bd17e99a9e1bf3b913e83460a`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:03aea2cc1cbccc85caaf72a5aa4849dc2f0b90ef05ff77b0596aedbd49357964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91b9cb0ac8f37aaab6c3eaf6b0f38f15e2596aef356ab722de03039acb850a`

```dockerfile
```

-	Layers:
	-	`sha256:0098c3101e6c6e790d7f13c1451a57772c6664fd861d82fb755fc73affa985a0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 2.3 MB (2342037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7ef4cdb05db7ff665494c23abc8607d29c6916c63a80aecb9c28b882598831`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:3f6b73e167753230ebb42d7d9def5facdc162f0194d32439b6a53353d91a5786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42580652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cdb433e1e82eb330201f8ccbabde52779df395b1535cf354461b2678b6de70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def2fc3727d4361a281e4c76905ad9154c94189f43d76841485b2123bcd98b41`  
		Last Modified: Fri, 12 Jul 2024 00:56:52 GMT  
		Size: 3.5 MB (3500267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318632f68dc7f8d2bf1e7bf2379456705e2a6732dfbe7cf5d09651e9630b5d8c`  
		Last Modified: Fri, 12 Jul 2024 00:56:51 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcffa504dbbc764b9a716dba8a862dadaee1907ba705ade7939771a3087d3ac`  
		Last Modified: Fri, 12 Jul 2024 00:56:52 GMT  
		Size: 8.9 MB (8934467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba6e88fcf5d8fe9fb55174091b7f2057357f74657687ee2b5bc8c610568f6ad`  
		Last Modified: Fri, 12 Jul 2024 00:56:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b0df34b20498e81843664f61ee6470939c841cbc917cd3695e6cbf3bf261a961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c392812db21d5bdb4a6abeddd77baf1d977c30817c621b6e8cd17e650c416472`

```dockerfile
```

-	Layers:
	-	`sha256:ec51f4936c7507a63973e515fafb3c1a36aba1794a0afcf988430ae4a84a6850`  
		Last Modified: Fri, 12 Jul 2024 00:56:52 GMT  
		Size: 2.3 MB (2338848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0baa9f45c34be521e8559dfd2c8f5b9ea166b83812685cb4ba2d8c56ec4e44d`  
		Last Modified: Fri, 12 Jul 2024 00:56:52 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:79546924dc768c03f2c7666135c25d550eae06d71013f953ce886d69ef202a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41324788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8bcc09b1a084f20d526809e82a9c01cd177c2f2fe34d90e1bb07fd8b04e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aa09befb1657b3197ac829db488481d15293f25c37f219f41fde4bc0dca78e`  
		Last Modified: Fri, 12 Jul 2024 01:00:42 GMT  
		Size: 2.9 MB (2892398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dad4977e891ea367fbf53890a2c9eb734cccd7b6938d176fbbb44cb77bcadf`  
		Last Modified: Fri, 12 Jul 2024 01:00:41 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb172235e5f26c46238073a39006b3195cebac8d4d1f99f4088370f6db098ecd`  
		Last Modified: Fri, 12 Jul 2024 01:00:43 GMT  
		Size: 9.3 MB (9305816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8796de9d8230090c5a9d791039fc3c7d72dfb66407567e61e2ea7dd2b6bdbb`  
		Last Modified: Fri, 12 Jul 2024 01:00:42 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e21e663bf56810d0e56149bcf2ea1784fdcece506342a6cd8437c6842a3fd58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9822714cfef7ae36d582062c734691e938983ee963ae6d9306bc48bb9882ea1`

```dockerfile
```

-	Layers:
	-	`sha256:a4b5a58041fb97828f604c1760d60ea9d9e93748aade1bf43d0c5c65272ed7fc`  
		Last Modified: Fri, 12 Jul 2024 01:00:41 GMT  
		Size: 22.0 KB (22025 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3aa6470ec33de8a631e3103abe6c56a17ccb65cf7ad0dab5046d94340e2d37ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46508686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd51f1663450cd06903dd03deadd1faa0e914ca76cc201901538ccf28018c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25b5593fa1f79db3cb39c69b3df7846a0c53d768e2b70acbc2002eae1d7df0a`  
		Last Modified: Wed, 10 Jul 2024 19:01:17 GMT  
		Size: 3.7 MB (3698306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b15b4dd2629d9581e994b2553de8105f6f9315c7bde97702ec5027b3d2c70`  
		Last Modified: Wed, 10 Jul 2024 19:01:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ba721b9c7191d6ca4b6276d459f80c637866febd8437752d6630c9d1d373f`  
		Last Modified: Fri, 12 Jul 2024 00:56:31 GMT  
		Size: 9.7 MB (9686462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8836c9b79b32038ea4d2497cc477d543a28b7af663425092717cf84a99dc28`  
		Last Modified: Fri, 12 Jul 2024 00:56:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:c53664a58c87b1dc1e938451fe0ecc298fcd93c6892eda9a0574cead31f4cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d17c1c3e8105ce033526652e3aea161ef0f328c3c434c71d00b8077033b2a94`

```dockerfile
```

-	Layers:
	-	`sha256:9f754477afe500a458548a7d0d37c0b40f037dc02b7a0f5c23d4ee6e43a59690`  
		Last Modified: Fri, 12 Jul 2024 00:56:30 GMT  
		Size: 2.3 MB (2346056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0400836ec2f134c2fdca96a2e8de2fe6c97d653ecfd665502e177b44ea3b9f39`  
		Last Modified: Fri, 12 Jul 2024 00:56:30 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:0cd24279a9f3500e46feb54b97af64fc8040f1ee4f2bf9a6a7d58ffa3749aa12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a65c6d127e4c7e1b5a9352a1224aff468ac972c1eb5a866ec953dfcb958640d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2270d5ba958c6200e1f15acbeb3f761c5bca2adb13be71b766288108b30558d`  
		Last Modified: Wed, 10 Jul 2024 19:01:07 GMT  
		Size: 3.2 MB (3160191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dca5178a8df7f35afa756e90982ba85f4aad71a50e33bf22afb947598f71bb4`  
		Last Modified: Wed, 10 Jul 2024 19:01:07 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2664a1720d81e9e3c7c0b1cb9ef8203f00ced98bfb11f0c36575f2c244bb9c9c`  
		Last Modified: Fri, 12 Jul 2024 00:56:24 GMT  
		Size: 9.1 MB (9057042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2def1dc6ad9687777c85b67586841103dc2fca55fcd753f5a97ea58e97cabc`  
		Last Modified: Fri, 12 Jul 2024 00:56:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e694178fd1480c69d73941be69445416f43c1a13e04cb1acc26d102e9770cae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e745528ed5496807ef07df61cbea4e35dc1ce7b7e87e947cc4699ce3f88df75`

```dockerfile
```

-	Layers:
	-	`sha256:6cccc8cd971572c18a8e2da9e3a46a8013beaa2e314bbb099868290e6d897ee0`  
		Last Modified: Fri, 12 Jul 2024 00:56:24 GMT  
		Size: 2.3 MB (2341560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3728f29b063d465af119e3e7d731a1a14269de0c5f72ff1fd897efe539fd65af`  
		Last Modified: Fri, 12 Jul 2024 00:56:24 GMT  
		Size: 22.2 KB (22180 bytes)  
		MIME: application/vnd.in-toto+json
