## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:4bfaf6249d52050a6a2f4a3b0fe97c5699b80324507f9153300413bc01f4b2fe
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
$ docker pull haproxy@sha256:2367d6dbf3d1fac21c77bfd6c1f6d56813271b529629e98b7a9a03b53942fa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41619218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a0eca74264e3ead34b5953d869b03165d78e7f58ebab7d71b1093b1db7c997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08500fa7cd4148f5ee07adc2edbc582a2327b41f7f74bb5a93bd078006df30ca`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 3.3 MB (3299427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6359bba6adc0c43dbd207c72cfcf1619bb11be8e64ae93a78775de58a6926707`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80314bf42844cba36df0be715e78f330ba23a4f726fac073bbddec763200e48e`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 9.2 MB (9167737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e988fd07b81d1e3f511637b67b128ab082ac80985acf587993e0da5aef33eeb`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7bf0ce3ba1bb9c6e8777fb059b2959c3d6d9bbb2d50cfb9faf993ae1b3c659bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e91720dc96862005249cb9c9594fe0032accfdb44f0fbeed00b29fcca4b7f`

```dockerfile
```

-	Layers:
	-	`sha256:f51bdd094f52ee003b3e7b0cea9ba6edff8f29bbcad4a22d69811414750c1b2d`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 2.3 MB (2341666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7933c028b04dc0fad5c0079fa446ef67f243b1392632411125e876c4043368c`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:cf2d46fc2af1fa6a6c71ccb9bf44162bad4b9c39c4956485b9413d8035dcdc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38896810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9621c9bddbbe6e4029f9da1b19bf57d0597cc6d701fd2abf2d75e2b4aad94a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5557f3a98f1d6feda9e8782c6742a836114942706a1de2059d88af00a7692a7b`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 2.9 MB (2874776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cff519ca6359e705f5718820428c1071f1d74a37b17a504c9f65548f50e903`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03097d66dec1114f4c47f6d8c95cca4540a8cc955a156fd882c82d1826aec58`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 9.1 MB (9110466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2552b543ac9351f14ba94c53b5fbf2f1f371854ad163b4ddedcaa3852d6e7f02`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ae5a685c3b59da43508d54a8627401286f534cccd364341a21707fb9ad02f765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef6607e53b3e17584f25f964babee0b38ba0e2a844da385108ad81d99bfbf6a`

```dockerfile
```

-	Layers:
	-	`sha256:878bfd3b4d5ffe65ae6b40fdf2e345bbb90ec9b8a03d3c6f3bb12abeb3342006`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 2.3 MB (2344946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f0edd2c05b718869d980c7e4dd3c4e80aaca9b44eda18ce2b082cf39642489`  
		Last Modified: Tue, 11 Jun 2024 01:32:19 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7e9eea26b8ada1d2854bf7399f0d43d5cd631dae2bb0382c9296244e02cec2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36396938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9e4424f70609d4bb800c439b1dcc23c2d1c0f386490363144f8dadd4f35cae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2519286f89d9a9b8016904bd4bfef2ecff70fe9b3be4c521f75b9df750f7f9a8`  
		Last Modified: Thu, 30 May 2024 03:31:48 GMT  
		Size: 2.7 MB (2711112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f15b2b983b01aea68b2d1b284dea58f64f9dd836901460d342d597d1830719`  
		Last Modified: Thu, 30 May 2024 03:31:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ef265e0832b0759e1f92ed9e7fcc659965dd79ede011095d221fd8f6cbc551`  
		Last Modified: Thu, 30 May 2024 03:33:34 GMT  
		Size: 8.9 MB (8943977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec94174792fae283117c3f8520214331921037d922dee43160c9a03e8f7528f`  
		Last Modified: Thu, 30 May 2024 03:33:33 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:59b1cd12f1077d9b4e5a357f1eded7c56a1a96d40d952367f873970e501a24c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2233306113100b9ed3bb2e0f03ec4e8a43b5e39b05ee572be119740b27fc62`

```dockerfile
```

-	Layers:
	-	`sha256:d3522b8283cba70a85bfb0f1a337303876dbd8fc0bbc1f123d48ef5ede60cc82`  
		Last Modified: Thu, 30 May 2024 03:33:34 GMT  
		Size: 2.3 MB (2343925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a94a46afd7deaaa6d49c6eed64f4a48742728c4f2e51048aa607eeef7a9dff`  
		Last Modified: Thu, 30 May 2024 03:33:33 GMT  
		Size: 22.3 KB (22259 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:aa6b478fbc150ee77e6106e3126b50e6c3991161c05b8fe071efb0a1a5905db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41460315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5486df871700d539611483ce75ca1fa5e8853489f41ee5d454c7e08fb68f989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a318f1988768cfb671a164b7a4c1cd76272152cb1ab3c64e2b9f5dc0a4bf5d09`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 3.1 MB (3122185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f0f594bb8bbfa6f0653d3a4e1aa82b9012f0b35e5107e4b87beaa474fddb83`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9a6edc851061b9d24c23f30ee372f6e64ba4a2032b5af60fb5e59f11a79eec`  
		Last Modified: Tue, 11 Jun 2024 03:34:36 GMT  
		Size: 9.2 MB (9156978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f567ec354fe55f27e3e24f01db03a8c8eb5186bdf3b585fd762461190109e0b`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9c0b8efc3424c3c9126030e1cbe87697d617fe6b18f53b37f43e94c382b3a00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82b007515adbb0cd9a1728e13661a404776fc95265abd60f6390e5f56a565fd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e327f24c88ec74ddba76f549ea6020c5bb55030ee49cda8be6beb0e6ecccf5`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 2.3 MB (2341972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0625281787f9444681bccc03de66a65dcce89e6826ff7c33ba160428f51082f4`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:e30bbdd9f6eee282a41ba851edd6c117dac6345ae4c6f226881e8103162a2683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42398485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4675a43e0f6be0af7acc2e404c0fc5c611e6fef6e488858a09607740f598ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a16bed6009fabd23f19c5cbbd658d79aef1c96164f4e54cfa11b8b096f3c39`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 3.3 MB (3304901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a8d30fc521843b6a3f9afdcc2b7b9d6e07e4f0180fb9fc630a75f35f6abf8`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1471f890df42265eced0e6690d8eaefa3f9513ffb171db21d128b075089fe9df`  
		Last Modified: Mon, 10 Jun 2024 22:33:40 GMT  
		Size: 8.9 MB (8929302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fca53eaa57160f958c30beb01a4596b00c5d579422c54e08d2fc2acdba33fa`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ecd138f4c2cbed588c87df685bc1fc88d07992267c532ce2ca070e1a3ba82278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5083d582745e8c8c18eced911243a29aa22c5a3663615b14c160dca7679a1b0`

```dockerfile
```

-	Layers:
	-	`sha256:87bdf0199d845871ca652191dc1d56738ed49c7a9baab9ee19873c7fc8f623cd`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 2.3 MB (2338783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e4d43ff83f51fc19e53c61d2b3c8b2c510ecbdb5cda10dc056af10c5149cfc`  
		Last Modified: Mon, 10 Jun 2024 22:33:39 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:d1fdf86afae35063859ecdaca65e7c17ffe0c1d89e73a4d667e8fcbdc8a8502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41144718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7190105d7f8d034456744e0b0958a694204c3254c3cdff6e537f01a4ab42dea2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cd683aef2186fc572268dd06430ebe8fb9e9f4b9c87a908ce9aa0f81c4a2a7`  
		Last Modified: Thu, 30 May 2024 03:03:39 GMT  
		Size: 2.7 MB (2699019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4011e38b613853b1998a5a6ac594c1a292c837eeca0a7d05a3c380eb4ddf4f82`  
		Last Modified: Thu, 30 May 2024 03:03:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405a72c261c303091020903540bd7d82b46239e72e3f689ab931f93bfd52157`  
		Last Modified: Thu, 30 May 2024 03:08:33 GMT  
		Size: 9.3 MB (9300363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91abb4f3704fc70f0cc105394ad32350806356345f53952676c0c876c43f2d3`  
		Last Modified: Thu, 30 May 2024 03:08:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc59f9b1685dbc24fa1dea53a611bcd821ee2e286202d19474fd2abdba309864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241d14b43b807e7fc40e59a4f68a449d745669a4bc9194c97db54493ba858894`

```dockerfile
```

-	Layers:
	-	`sha256:dba13fef77b12739734928a76112ecf5ffcc9b51275d021395b39134ffc9185b`  
		Last Modified: Thu, 30 May 2024 03:08:32 GMT  
		Size: 22.0 KB (22013 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1fff4f07012f94a6eb24480bfb4eb77d701a65625502a153562961b39c512f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46328075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18b214e75aaeb4dc44206869e7a1c7fcccf78f729bf2b7932c74b7b52759259`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3feffa4c231cfca3e7d2edb96f03676e7940f0cb579be3ea24c2949014af08c`  
		Last Modified: Thu, 30 May 2024 02:51:19 GMT  
		Size: 3.5 MB (3501568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660afc2ff6dc930a643d203d90f2e2ea4c2980c3bf098fa97515a184a5025c7f`  
		Last Modified: Thu, 30 May 2024 02:51:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e237b377782b1cd6b8de99456143fc1296b89825d1d315557dabfabf3b4d7e0`  
		Last Modified: Thu, 30 May 2024 02:53:28 GMT  
		Size: 9.7 MB (9683701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9511cfde46f060bfaecd27ede03b09b3f644e27ec26a8d2dc76f3f3fa1595637`  
		Last Modified: Thu, 30 May 2024 02:53:27 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:cf9a9a5c6dcfb291a01045253358987e3e7929928bb98da9414a12543cfa7769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e618d48c84ad00b2c6a27f05606a16d01db54f269ecfd6aba5b492439d5009c2`

```dockerfile
```

-	Layers:
	-	`sha256:d219d07f58ee1ef58d52adc8279e7c54d2084c6086e7440496edf080ed29dd6d`  
		Last Modified: Thu, 30 May 2024 02:53:28 GMT  
		Size: 2.3 MB (2345992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702482ef11e71da4bb79f9c47ef5c821409bf9ee0f3dd29e11259219f7f95cbf`  
		Last Modified: Thu, 30 May 2024 02:53:27 GMT  
		Size: 22.2 KB (22199 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:b2693556422f17371a63bf14b4e6ed62d7a5a5cb624edd20d48887052e4aeed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39532610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745059c0104b2c4b27d88fd0a0b7967ff90e281c04ddef55da24be3e800573e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975e5d47318dd2bb283ee263d251297b86c7b207116fa35f58e807f98c40be6`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 3.0 MB (2964931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5403381a776cf6a1c64702915d9f0157d991693bedc5064dab7fc8ca1b60a3`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c7f485844c019ea96cb15a2eecda1c7dc5f2f5335383bc2c8c483b1cf2800f`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 9.1 MB (9053634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acbbfff0bb305ebb279d9482b9e26ebe68ae8db3afe0811dacd838711394908`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:20c3159bd889f512c4d2df9466d4c6d1f7850980461c0252f0fe0690195b7f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae18d671c4c819df9bc2ebaa7694e870afee789a4f4453ebf82e20259a0c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:07fb838c23e9f3226a9dfb13fbd567bf1a47892aaadabfff47f314a6e0a44fa7`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 2.3 MB (2341495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bf0791383a3c73ce7fa073fc1f17f9c166a3e6dcf67ad37244aa4ee404cdf0`  
		Last Modified: Tue, 11 Jun 2024 02:14:44 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json
