## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:e981214a5d74a26e0ade3425e0c0c24c8d5e4d9d16e1738268939ff7b4896d92
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
$ docker pull haproxy@sha256:fa0db0e3c87e6fdfe8d2f6f91e49d8ab9f4cd74d3d1ae00bc14894dc32356535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40681789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b80809121b95786502b7cb4fad33ccfe217e85a434d39778913a71557bffd6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e112df56777702f039f58ef45c089caa4d3df7fa20889267f17221d0f09e37`  
		Last Modified: Wed, 24 Apr 2024 04:55:52 GMT  
		Size: 3.3 MB (3299418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb05eeb02206ef05a09e6dd65c3dcdd3dab88a1d0833c81e245de22f6130644`  
		Last Modified: Wed, 24 Apr 2024 04:55:52 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22c358ff9442a5a97d1ddd824641ba9db4bd826290cf81896b828509ca461c9`  
		Last Modified: Wed, 24 Apr 2024 04:55:52 GMT  
		Size: 8.2 MB (8230250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7b6701fc0532658f84cf25cbd4419776b0d2bef6af1ea62de6af37c366a5b5`  
		Last Modified: Wed, 24 Apr 2024 04:55:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:107b5b6e1df24f2d0e8c9f8de6e6d40970926e6defdcdf5382e0361429a68155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08d121a8018658114ff649c95cfe1d081a8ab31b7ced748d31ef5c2a8d11a4a`

```dockerfile
```

-	Layers:
	-	`sha256:3540314939d76b3cf30b31c52b992c118d5b0dbcc03e2c11dbf0181b5f67bf5e`  
		Last Modified: Wed, 24 Apr 2024 04:55:52 GMT  
		Size: 2.3 MB (2341063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5ceaacc08ced41b3846be631634d62124e7a7d9e43833e482e8b1d54a0c4cb`  
		Last Modified: Wed, 24 Apr 2024 04:55:51 GMT  
		Size: 21.7 KB (21696 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:bcb492c7206968e7a0524ef34bfd050fa1df3365ef4f1dae6b2441ac856530bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37913653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbdae9996cc6cc2d2318ced5c9f16f07a6501e9a37c52ee8826fd61edc1f0a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b96bfe225c1480b4f89d723b1687c952dfc8149bd588238b1e4130505639e6`  
		Last Modified: Wed, 24 Apr 2024 17:10:36 GMT  
		Size: 2.9 MB (2874739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a040713da1cf4305b6171bbc6149c8b588a879da88bf58eae02490b33f0b5`  
		Last Modified: Wed, 24 Apr 2024 17:10:36 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5422abdb208bd12195aeb5316358e4320fe8bb484398e870c366937665405bc`  
		Last Modified: Wed, 24 Apr 2024 17:12:45 GMT  
		Size: 8.1 MB (8127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aabfa03a0e0daffa31c4aa47aa8837364f225512f5469acc57e9b1848f26f4`  
		Last Modified: Wed, 24 Apr 2024 17:12:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d45037d530c2d44b8d356d7782ac1777ebc562db4d4fb269af3e197a8256291d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c39647070883df4817f64c7501758df20574ea51f744f79ef3485c87e513c9e`

```dockerfile
```

-	Layers:
	-	`sha256:fdd1085152958c183d4c27a54ae695de25cbc888eec7d7508816a9f6b0b32e0d`  
		Last Modified: Wed, 24 Apr 2024 17:12:45 GMT  
		Size: 2.3 MB (2344327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5cedc39849944c77921a384e5be1a8885f00d6ad5519945842d04abd93b21d`  
		Last Modified: Wed, 24 Apr 2024 17:12:45 GMT  
		Size: 21.6 KB (21641 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7ae424c9b5fe25b4099d3219cc8efed79ad7b7a48694afe426bf13f0f44e7a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35431849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f0c9c53f0cdc7dc148cd9f1f28727519673c5f73b67e8f413a2e06432384ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d98b3e0f1e0e00c42be3ae7f63022fec3efa8ae8442c0352695fca8309177`  
		Last Modified: Wed, 24 Apr 2024 13:11:03 GMT  
		Size: 2.7 MB (2711044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86d9bedf9593f08135a02714b5cd4c81a01c93b37eee75e230e5c4e18185ef4`  
		Last Modified: Wed, 24 Apr 2024 13:11:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3923afcf62e97cfcd7893da052e46a4916c3e6aa2464d1cfc840411999b98f`  
		Last Modified: Wed, 24 Apr 2024 16:23:10 GMT  
		Size: 8.0 MB (7978726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f596561ff2bb6dc21929df068a95ea31500095197d5e649f5a9e2f390402919`  
		Last Modified: Wed, 24 Apr 2024 16:23:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:09a9d2095144519afc1e95d6e0548eaaf822eabfbe0f3970efa53c94c06f6905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54769b715ea2e7f1980b8d298d60e0ac541c797ec0aa2908cabced70bbe8925b`

```dockerfile
```

-	Layers:
	-	`sha256:a10e1a2084b690d029c5bbf778d57186c01f1c9b5d73471dfa5a319e6789b4d9`  
		Last Modified: Wed, 24 Apr 2024 16:23:09 GMT  
		Size: 2.3 MB (2343305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a4b0a856245be80751ef2858babcef65b38f0a1aa489c0a7033d09c4f5d808`  
		Last Modified: Wed, 24 Apr 2024 16:23:09 GMT  
		Size: 21.6 KB (21641 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fdeec807d9233f414ff6300439b7ad9faf3e64720b1c2351eeca7f4efaf161b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40461996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6faead780d6bf0debac90f598e389dbd1694b945e623494d1e9857212a5709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9b9f20116ce3dcfc10ab5e3ee29ff31e77416e1f052955953026f495957676`  
		Last Modified: Thu, 25 Apr 2024 06:53:42 GMT  
		Size: 3.1 MB (3122197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e87412c2035958c921e9ea04d613848ff667e2b64dc9d2da7d5fe564ff3d39`  
		Last Modified: Thu, 25 Apr 2024 06:53:42 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3fdee3f43e6bb537eb683583719dddf8c81dea200dc4f1b07bf714a40d6d44`  
		Last Modified: Thu, 25 Apr 2024 07:17:30 GMT  
		Size: 8.2 MB (8158224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8fd90c718be2f6d559b202cdb3a6e80a7e43538e50a9fdf876e17589e678a1`  
		Last Modified: Thu, 25 Apr 2024 07:17:30 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc43de1f14ef3ab5411646728bc1bfb24cc959f9f827614f85bc7c6cee903e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd82c46cce71f635638f366d854fc503522a90d6e7fc7674b5a4d7cbd487e06e`

```dockerfile
```

-	Layers:
	-	`sha256:f1df33c9034a8635afa441b78d17f391a21630915cb24ed832de7be3180c148b`  
		Last Modified: Thu, 25 Apr 2024 07:17:30 GMT  
		Size: 2.3 MB (2341280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12d2cefd0a403882e34ec82f6bb340848f8eafccfcfdfcf5a2a4cfc231c3cc7`  
		Last Modified: Thu, 25 Apr 2024 07:17:30 GMT  
		Size: 21.5 KB (21542 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:0fa86d8004114bcc2fa5c6e8c6d9b7b659f9bfd210c908925910c4f50a279792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41471915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a0411bd45779930903d80d77e500eac163c85cab0f9428d7dc981367fca446`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6261b3ecf30a14d51d16f09e1fc8b54c7b08329125a2f319fc7a9f69f1ace3d7`  
		Last Modified: Wed, 24 Apr 2024 04:55:56 GMT  
		Size: 3.3 MB (3304895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a41da4405dae3ab54950e3c55a09759ddf330f3cd0ae32d5aaa9a9ea50ab96`  
		Last Modified: Wed, 24 Apr 2024 04:55:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89746c58bd81b968387e8017d96a835e152589bc94b5916f7b61a605052d9a72`  
		Last Modified: Wed, 24 Apr 2024 04:55:56 GMT  
		Size: 8.0 MB (8002198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d33d6339c39460e28a50a562f55ae9059ec01fec2dbc7e32e901fd0f045908`  
		Last Modified: Wed, 24 Apr 2024 04:55:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:62669b962b497c42024fcd618de6c4485bf503df2c365f62829d04330bc5b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1095d74de23f5fae6c1de413c951ebcc1ac0bb248f674528885ae299528bc74`

```dockerfile
```

-	Layers:
	-	`sha256:d3e149ee91f411f491ca8192b7c101c2587712b8b7e89fcd15edd0342e1fb3f6`  
		Last Modified: Wed, 24 Apr 2024 04:55:56 GMT  
		Size: 2.3 MB (2338190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b2d817657010ef44093d24d50a2a5e11df99cf5a0d374e4f3299426ed0ed31`  
		Last Modified: Wed, 24 Apr 2024 04:55:55 GMT  
		Size: 21.7 KB (21653 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:9bbde31654af26c2ebc2a34368a66bcc090ad45cbe2aa7119fabdb438f56c149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40139246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65823a04095665fad4efe6af5e451e8146be8ba93a1a412f83e1104b7f45fb8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997cb0c5cb8925ca73db4dc1d7fb380498429e97aea27ee2dc6255b2edac80ac`  
		Last Modified: Wed, 24 Apr 2024 17:32:06 GMT  
		Size: 2.7 MB (2699073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dfb66628058561dc84dd66ce4c25ec13456d0e7173a92c64c856cd9c49e8f5`  
		Last Modified: Wed, 24 Apr 2024 17:32:06 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ecf20dbb05be4d2d8b27c2a05959746a3fb3183e2f8e88e32aad13c72169b6`  
		Last Modified: Wed, 24 Apr 2024 23:08:56 GMT  
		Size: 8.3 MB (8294351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cefc8a9388919834910620aebedcfd00534e7067644bd1fab51e810e11c1ada`  
		Last Modified: Wed, 24 Apr 2024 23:08:55 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d96070ba1a3340bb0b69282ff9d14837d1c3a521071f979db685802188574686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43e70d97b7b81ac0134cacb498df71e47927429eacd5c53df733c1a9db7f459`

```dockerfile
```

-	Layers:
	-	`sha256:09a4eea3db408142f7c4d1c4be09f0403a58900fa713efaa59c13dff89205e65`  
		Last Modified: Wed, 24 Apr 2024 23:08:56 GMT  
		Size: 21.4 KB (21391 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1332320e189514456365f0f55bc535149ef7a7cea170c42259a58adfc1d43cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c8cd2945d105f41e78fed18254573bc9ec9d2973243c4254578c3a5897a597`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f7ac9d4b9dbd057b48f42090de19b894ad15b30e97c9dbce7a651b7f5c59be`  
		Last Modified: Thu, 25 Apr 2024 02:56:55 GMT  
		Size: 3.5 MB (3501617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6e4800d3af0a16b245981b2794f85f6c08faeba0bdb59d9f0ef359041a2e58`  
		Last Modified: Thu, 25 Apr 2024 02:56:54 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a8a5cdd0874fb5a707ed21191ac806dafa403b81e74e6ad65b41025d16ee1a`  
		Last Modified: Thu, 25 Apr 2024 03:09:28 GMT  
		Size: 8.7 MB (8656593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d4f041689efcfa40100b7bc4eed9e4e4d1b8c51f569b6ed32cf8ef94867bfd`  
		Last Modified: Thu, 25 Apr 2024 03:09:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:22fe18bed98c7fa229bca199f9b297e442e88b15503bf3c2ce3ba4e8837db31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d51e262d7299c97e5469d893646d6909a566e2be1a1cd5064aedddd94df7785`

```dockerfile
```

-	Layers:
	-	`sha256:33ee8271d2cabb482a512e94a2a3db9290606c79d256689c72f05651c629d6b6`  
		Last Modified: Thu, 25 Apr 2024 03:09:27 GMT  
		Size: 2.3 MB (2345376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73522a5d5a8e8f18b8a67895dc173392e38225fe96dc4d1bccb4d095cc73b3d3`  
		Last Modified: Thu, 25 Apr 2024 03:09:27 GMT  
		Size: 21.6 KB (21582 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:7269f44e25fd3398fca12f1b9d242dd70db5b60d8ff1005a001a5fc8236860e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38562067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5132d313fa30067df6f961b51cbbbffcfa74feb35f9fcd61861f5547d0e7961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
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
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e130302681b810a6e31df758532a451a6887c4a0ca124355965c4d1080eb225`  
		Last Modified: Thu, 25 Apr 2024 02:01:46 GMT  
		Size: 3.0 MB (2964886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5d82f5fe0e6419c5c1c5635a4a8f7b6d898024d7145b5cd49ffecfab3bb2b5`  
		Last Modified: Thu, 25 Apr 2024 02:01:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208488e5bd0bd1cd2b6329331cd3335472c348ff4f53a9d6285c105a0da8c8`  
		Last Modified: Thu, 25 Apr 2024 02:22:05 GMT  
		Size: 8.1 MB (8083187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe1574b125a4cee873a89f246c2e1f5073b467d018fbdc65615a190f822e7ab`  
		Last Modified: Thu, 25 Apr 2024 02:22:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9dfe973a48586e87a4947aaffe9a68a3dd527c2c65f3a007b2f49ff308a54f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b659a30b70c6d44f0da76f8f7650f00f1e694d6b26067628d51509635317f598`

```dockerfile
```

-	Layers:
	-	`sha256:b52101938771112dd22a95acb2e51ee9d9319a5bc26847111afe5836c2fc716f`  
		Last Modified: Thu, 25 Apr 2024 02:22:06 GMT  
		Size: 2.3 MB (2340892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc730908c5512afbbac283a895a443b4f4120d89d84dce16c23b20a18ceda7bf`  
		Last Modified: Thu, 25 Apr 2024 02:22:05 GMT  
		Size: 21.5 KB (21529 bytes)  
		MIME: application/vnd.in-toto+json
