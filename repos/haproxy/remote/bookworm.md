## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:0f3127e63b00982c3f12b2a9a17ecbd0595003a191ec1cb403741a692f7a39a9
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

### `haproxy:bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:c2e9911475f185f43a1e7b241de44c7fccf7391792992fe33ee65d3a5a2ce213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41908215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7852aa8a2d3552b38036af5ab96e9dde220aec59835ca23f670bbd839e647be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85e9add3e0089006e32148a43d9ce4058d76ccfba2d7e08c86eb9db15551b26`  
		Last Modified: Tue, 12 Nov 2024 02:17:54 GMT  
		Size: 3.5 MB (3499305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2675d15c3e9d415365c5ab8fac44ce8b6d0ef6d394d2c7fc9ea824e53707436d`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6580d764f7ad9e3d2c755bca294149de1cffeb1e8733ad182c1527bd40991381`  
		Last Modified: Tue, 12 Nov 2024 02:17:54 GMT  
		Size: 9.3 MB (9279277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6bde85958347aba5c2b8b123f555faf6cb74f86b8394f51aea24509ea9290`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:01a96e41f678d77a86790162f109e6dd5e74ac89705b1b2f6100dac0177ea567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610399e1a03fca795d1d2785e990d21d98ebd2b1b05113aef6586fe53deeaf42`

```dockerfile
```

-	Layers:
	-	`sha256:4c7d1e2524233b668d1c05755e0f2a873a5bbc61f9ab5dc670b6cb69540f365d`  
		Last Modified: Tue, 12 Nov 2024 02:17:54 GMT  
		Size: 2.4 MB (2372882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e772e695c83ec7d5ad7474dadd4a1d676650b1431252fe20a4bb44b934bae17`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 22.4 KB (22376 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:0c99b4c34242e89a31618e7d5772c343828bdca2ef0cf4d35123049446e34404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39199167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e9e36cfe0624fbc6412a009be053b9f84b6681a21166100e79eef67174df43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa1bf906711e7bea1dc69fe99693d7b0722fcf4c0b001928afd2a060e9a7cf`  
		Last Modified: Tue, 12 Nov 2024 02:04:35 GMT  
		Size: 3.1 MB (3073421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5ff3167f5d31c7e4b6298750b4bb986fd117f8e4b4a16656362fa67ced0ce4`  
		Last Modified: Tue, 12 Nov 2024 02:04:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9b4b37706475b59bb3aad77f4803a3b9c886b48789abe5c98a5c2da99ee66`  
		Last Modified: Tue, 12 Nov 2024 02:05:34 GMT  
		Size: 9.2 MB (9234049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ff6983288b3d95d13271d188676705ad6c8494032fc6f66db1d8b483619671`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:93d045b2fcb6dcf0c09c928dfccc0549e88127f19a9fd3ea289c0d70e8988ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5881b63d9d1bd6cf1ed241ea052236f8384b4781b21c6a64584fca9ad0be84`

```dockerfile
```

-	Layers:
	-	`sha256:ddcee77810270a1923d45e727f4af2ad2eada811aeda2a0ceca3add8a592cc4a`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 2.4 MB (2376411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573d11994e83fcecb456fff2176c0a2cfe5e7d8a839b713605503b1bbff7b117`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 22.5 KB (22510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b262b8d065402bb5b3589a1bb88d35d0f77a40ee85c44a3eff2e013815515a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36690611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087e5766a242830d285ee811873aa58a9df3e8d76ec4e427c51f65dcb0a600f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85326871e781c3d5670a80f3409f0a604826aad374f81a7e0c7e80d1d2a1b65`  
		Last Modified: Tue, 12 Nov 2024 02:24:34 GMT  
		Size: 2.9 MB (2907823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b001faf5164aec49fddcb5e18c350a1df454d1cca8e4a6d1f4bb80bcf3d034c3`  
		Last Modified: Tue, 12 Nov 2024 02:24:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f16de67cfc0f53b0c40fbdcad9fc47ccbf212235bd3f0ccd0cf052d183915e`  
		Last Modified: Tue, 12 Nov 2024 02:26:40 GMT  
		Size: 9.1 MB (9062239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05adda982bb9ced15a5ad1988de546021c957f63e09e372b6aa4da3d257073a`  
		Last Modified: Tue, 12 Nov 2024 02:26:39 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:3a09aeddbf2c19ce1b72f388d4636145b8fc6a36281fa6f26ea62554c2b1268c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91bf770621af5161505564bf6edd0f1177f6f15d1da73169df5d234ea629257`

```dockerfile
```

-	Layers:
	-	`sha256:644de188b605ef00c22d5e241a26045703fad93eb84b28d875313426e16f6dec`  
		Last Modified: Tue, 12 Nov 2024 02:26:40 GMT  
		Size: 2.4 MB (2375140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eba94e04b5e6c03445b7d7a215b9c34a3c33dad74b689cc930b4c140a4275e2`  
		Last Modified: Tue, 12 Nov 2024 02:26:39 GMT  
		Size: 22.5 KB (22510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4d9c99656c491733b2367a6e2ebfb137abe72e2cee403fe392e4401dacb92a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41740859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af4c3f46543372c6ac96ee4f711c49108cc9b61592ae6bc66d97bfe16e794ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a74791b8c7a4669886fbb4ceb0cf7e1d1f8abd9961001320bf5d1d1cadb2510`  
		Last Modified: Tue, 12 Nov 2024 02:42:28 GMT  
		Size: 3.3 MB (3322863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dabe3d24327d843d1e610cd7650de8ad6908b252d946201c5d8c3a40554136`  
		Last Modified: Tue, 12 Nov 2024 02:42:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ae80f895ccb57009c272d9e379eb7df803611035f6953da0bf71b535266f61`  
		Last Modified: Tue, 12 Nov 2024 02:44:10 GMT  
		Size: 9.3 MB (9259003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff215b0baefcfa70cefbca8224cdeb7677e1a166dea1091625d129123c1d2854`  
		Last Modified: Tue, 12 Nov 2024 02:44:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:16bac2a24e72fe7ccb47a0e735e768329e76ba95f14df385b92fed05283f922e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c02902225c7c88fe3f6b989555ac0af6404c0bd8d64d25ec0ee602390da911`

```dockerfile
```

-	Layers:
	-	`sha256:2218ced8e94776796d181d667cefeb4a4b7e44f57d087e22faa0ff04f91ec4a4`  
		Last Modified: Tue, 12 Nov 2024 02:44:10 GMT  
		Size: 2.4 MB (2373188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b065e82bc7730bb8c643e959c584b54b582c782664d21e8df22439565e59be`  
		Last Modified: Tue, 12 Nov 2024 02:44:10 GMT  
		Size: 22.6 KB (22557 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:e79a25b74aaecc6c657a27207f6205ceef48650126da52fc40ff3f8035f4b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42686012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07102225b1cd184a0d97b86891eb1d3c1f4ca592bda15654c37e79603fd65c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5ca0e4b58e4f2e13a99422c7acf75a51cbe1e2a65d364158d67a2c38951ab`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 3.5 MB (3503443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab049bf6950ac0f50146430b222c322bde7f0ab64af8b0878cc5d5a1a51ae26`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9229f14adab890b82384cee9a8bf38659293ef3933d63ab8f52f986560563880`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 9.0 MB (9035482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b032fedcb1cdd68c616974ee545e30c9e78edfe0651403c2f43b65531d44170`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b40eb8e2933bfb2334b8d76abfc9b63168da2d8b00d1c46e2b5008dd8d782750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd6046aeecddb1a737f703d508e17971a367e9934bbe07b4e5ca5994b5e1082`

```dockerfile
```

-	Layers:
	-	`sha256:bcfc75599ffb55dc00314d19e93a32311cfade8112a0059cdc85de227713984f`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 2.4 MB (2369999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d020fe2d77882dd396cd60d9d7a0f9f385cccfb728b3710f4b9d9e2d82dec025`  
		Last Modified: Tue, 12 Nov 2024 02:19:41 GMT  
		Size: 22.3 KB (22320 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:7d46bfd730bf6c71a2f69332ecbdfee39d394de8d253b4f61f893227ac511129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad86d9b7f429f805b8f379c7abefd6796599bdc6b5fd95f91a0f7c3ef4dd474`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:01c6d0bf10848996e396c89b66742849d41fd852c3610146badf9f612e62945b`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 29.1 MB (29127365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c450c12094e9d507070704bc1c3d5d54037e8ea7c8ed631e21479778e0600a0`  
		Last Modified: Tue, 12 Nov 2024 02:11:50 GMT  
		Size: 2.9 MB (2895381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b91bcbeff5760427c53ea6e4a90026ea783356d0f9a7c8c51b03b0da885f2`  
		Last Modified: Tue, 12 Nov 2024 02:11:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d059d3ca3d5bc12827ca53d8de507ba25f4cfed1a90843b26cde60f52406b1bc`  
		Last Modified: Tue, 12 Nov 2024 02:16:58 GMT  
		Size: 9.4 MB (9393057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e1062ab709e429da573550aae21a961ef1acca5088cf7b80869e9228ee97d`  
		Last Modified: Tue, 12 Nov 2024 02:16:57 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:a1aca5d4f8b2c4bef7e75dc4381d094801bc833c8132998a1b83e4246f3bcd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 KB (22269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564d77df76fdab78c9130c65e20d145c3c53f99afb01782bf27b97bbf4619dce`

```dockerfile
```

-	Layers:
	-	`sha256:1bdf0c1bcc83bf052ffa574b929add9e5b44c5882fa65157925a5f003959bb12`  
		Last Modified: Tue, 12 Nov 2024 02:16:57 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6402d387aed12f3bae69f28a8c5f82bf3af45db548f28e98b0853f85d06fa606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46609118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0504779b91af9086d183dea5d5d7788bd29bd47e280d3e9dbc7f073ef5155a66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372447efe90f3a2d36afbc64ce6ca7c91e1761784d425574c9d624cf7fcf1be`  
		Last Modified: Tue, 12 Nov 2024 02:30:47 GMT  
		Size: 3.7 MB (3702947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3420be081565b3562ebf1e2211233a9db3333dda378906870cec31d5b89e005`  
		Last Modified: Tue, 12 Nov 2024 02:30:47 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a77746e0be12665459b49f98667bb1ca5dae282eec803d6d42e8d8d7e567f0`  
		Last Modified: Tue, 12 Nov 2024 02:33:28 GMT  
		Size: 9.8 MB (9779183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d4affca384bfde9bae8a882c7fb88f3574f10d3a6018732b1e8897422cca06`  
		Last Modified: Tue, 12 Nov 2024 02:33:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:dbcbb5440defca72ea75054f6f800480a0fedd516e653d57256276df7b6e2894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0ba1dd759277a15d0e6a49110f8fb67dae3f706dc068812bbdcc835effcc69`

```dockerfile
```

-	Layers:
	-	`sha256:a7e55261586d45acfc009f2bf65ba58547e1576e3af4acbae797647bbe492e20`  
		Last Modified: Tue, 12 Nov 2024 02:33:28 GMT  
		Size: 2.4 MB (2377207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d671ac61657058b36ecf39b9e78414c1eb1584ad9cc581bb2cf496cb3cb2600`  
		Last Modified: Tue, 12 Nov 2024 02:33:28 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:be7dcc92cb9c069155a676cd5fda29a910ed120d7dec8505db101b91395a15e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f94f5f53e4a148be9e240ce3a76f09a26e0e96217bda71515d56d85bea483c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 07 Nov 2024 18:13:31 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_VERSION=3.0.6
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.6.tar.gz
# Thu, 07 Nov 2024 18:13:31 GMT
ENV HAPROXY_SHA256=cf1bf58b5bc79c48db7b01667596ffd98343adb29a41096f075f00a8f90a7335
# Thu, 07 Nov 2024 18:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 07 Nov 2024 18:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Nov 2024 18:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Nov 2024 18:13:31 GMT
USER haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 07 Nov 2024 18:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b10a8c9a575c8fd924f9952fb66e6bacc807df1e72458920b69db269f86bbea`  
		Last Modified: Tue, 12 Nov 2024 02:28:17 GMT  
		Size: 3.2 MB (3163380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2016ec34b446c4f498753cabda5a1458c96f292f934ec488d42dd41cbc57fa40`  
		Last Modified: Tue, 12 Nov 2024 02:28:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cce68722f8313a0b29ae5d14eb28786cf277903ecc9bb68d6248085ed10367d`  
		Last Modified: Tue, 12 Nov 2024 02:31:03 GMT  
		Size: 9.1 MB (9138403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b06581f8dc48d1fb1ad9235b51918b57509340c6c1c426162291d157c3a04a`  
		Last Modified: Tue, 12 Nov 2024 02:31:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7bd280a307f9af917c6a9add44e0910fac9f1594641c90b913f3aeddb95b0602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f9189736b250fa6cddca1f10ac2367c875cb247dc8ea3984c0d25c1bab5e21`

```dockerfile
```

-	Layers:
	-	`sha256:a6504d450504fd54e19a351cc696906cc1ca74de3f50b8e5d08f2309cb382d46`  
		Last Modified: Tue, 12 Nov 2024 02:31:03 GMT  
		Size: 2.4 MB (2372605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b8a8716d73e34a8f2b1a9812bb2cbc087a4417bef513c689f1c0ab9b0d6834`  
		Last Modified: Tue, 12 Nov 2024 02:31:03 GMT  
		Size: 22.4 KB (22376 bytes)  
		MIME: application/vnd.in-toto+json
