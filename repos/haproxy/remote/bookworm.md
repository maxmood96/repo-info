## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:ef017d32270c1455a0e395869441f2397a1d4773a46e9cc38bc350f6208a0672
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
$ docker pull haproxy@sha256:4c7f18a809a54236d33bab07516d621cadc8c0801ea2736c7e7a47944a64db1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47998576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c7b581ea7d303250fa13230f006d71ebc79f07d7a98a8c407fbae8ebd8456c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1cf0dc1a75c3d9b7d5d8317dbbb28b90427d0ac2972d01910652754dc27918`  
		Last Modified: Wed, 04 Sep 2024 17:59:17 GMT  
		Size: 3.5 MB (3499027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f4f3db7ce55d1dcfe448bef071383f1b6180fca16664c8044cffa586e3b16b`  
		Last Modified: Wed, 04 Sep 2024 17:59:16 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c15f1c95253c7384ebfef1bb4df54b863ffee7d8193cf3f0e744d3c0f91dd3`  
		Last Modified: Wed, 04 Sep 2024 17:59:17 GMT  
		Size: 15.4 MB (15371675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0af1d647b62bc0237936b98336043bce133172c4a23117a986eee2dd6eab09`  
		Last Modified: Wed, 04 Sep 2024 17:59:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:814fb69b0b9ac0d74631c59bb585e6163bf08175cfbfef6b2c85bcdaa927f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1ff0a8f817d05a4b4ff49ea58316af29c5cf194d28c3d61065de73350c8226`

```dockerfile
```

-	Layers:
	-	`sha256:e17f9bfde42752fff7219b6552105cdc75e330e2570c0c05dd34b615280e88bc`  
		Last Modified: Wed, 04 Sep 2024 17:59:16 GMT  
		Size: 2.4 MB (2360692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc0f9645e520df9c23a04cb8a385f7a8aa5fe5128d3389c451b2028f419f241`  
		Last Modified: Wed, 04 Sep 2024 17:59:16 GMT  
		Size: 22.2 KB (22185 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:c3a51a9ec6e7305ed5923d1229eab6bf8b7c4efde5bbf693234a5ec226872d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46449408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cc517485be35b33e50d2dec01c065511de296221b5556f182f4772dca585b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:29 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
# Tue, 13 Aug 2024 00:55:30 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1bc90b37f777aded897944b0ce596c103432c1b84f7b626b9fd4a53356f006da`  
		Last Modified: Tue, 13 Aug 2024 00:58:27 GMT  
		Size: 26.9 MB (26887303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1267cffe86459b67db582161a3264dad20476ef0918cc3f35670dd8ef7e412c`  
		Last Modified: Tue, 13 Aug 2024 10:28:17 GMT  
		Size: 3.1 MB (3071498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bf679eb99a5f8d020fa4a241ef2837d2f21f5500941f3c91cfa32914f1e482`  
		Last Modified: Tue, 13 Aug 2024 10:28:17 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f2a65bae606bf32c01136f2c0e248f01c8dfa420ccc1358c2b5aa612506700`  
		Last Modified: Wed, 04 Sep 2024 17:58:42 GMT  
		Size: 16.5 MB (16488967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbb55152cbc977f03d2d07d9decf1d067f077201b0ae09ea6e7c4ca5d7fd8b5`  
		Last Modified: Wed, 04 Sep 2024 17:58:41 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:3d7b8e71a698eac09f3e43a20dbf706f4437132704a21e3f7fd5eef0450c7c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cbb58ddefff42abbc074b2550c442a9e608a84606eff4b1fbf260599de3236`

```dockerfile
```

-	Layers:
	-	`sha256:61daa677759d8c475a375645a7b7ca959759a91d5f485ed0e06bd83b873859d7`  
		Last Modified: Wed, 04 Sep 2024 17:58:41 GMT  
		Size: 2.4 MB (2364115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e524ccfc66aec4d323d46bf8d45f70fa063b1b8c4952e158ed2248b93ad9ac`  
		Last Modified: Wed, 04 Sep 2024 17:58:41 GMT  
		Size: 22.3 KB (22313 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bbec48ef34eb4285ef3bd8c6cfcb51dabd43e187215871047689e867c05c9998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43504316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6242bf401830fc37adb9f9a3acf63d46f70da1096e583edc674302b6a16463bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12098d491018703244c3d05972605a540871945a79b8f23467edb2fbd2e9fe`  
		Last Modified: Tue, 13 Aug 2024 11:37:31 GMT  
		Size: 2.9 MB (2906251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5482cca959d7e023a5e5e84f979d20f9b8fd90f6212ff82e45f97cdc0ae24a9d`  
		Last Modified: Tue, 13 Aug 2024 11:37:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5706b7a99b62e62d0959b70eff5d3116bf5be0cfaab058609d37351dff86f0`  
		Last Modified: Wed, 04 Sep 2024 17:58:46 GMT  
		Size: 15.9 MB (15878286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715a88f0a014644917b1fc44908b15f7bb9ff4fb523bf069a7338df7f5370d7`  
		Last Modified: Wed, 04 Sep 2024 17:58:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b836dc59a3e893a1188eeb5221f122bbe466d4c7f4855876a18d9e83a7f91509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e19ee411245a7f08933f453498468e01e993edb3a9c11f67c24784952cf87b`

```dockerfile
```

-	Layers:
	-	`sha256:aa825ef3201b42f9171286b73697b03bc77d3db307f401d3bce0b213dc72fd76`  
		Last Modified: Wed, 04 Sep 2024 17:58:46 GMT  
		Size: 2.4 MB (2362950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a12ceb84d5fc3f7e4bbf17f4d3b7c811362080621382e82b21023f8d367199`  
		Last Modified: Wed, 04 Sep 2024 17:58:45 GMT  
		Size: 22.3 KB (22313 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:bed2548d554a0b6b53b23034cf823cfb75b61e935360290733da7d7835d00384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50388542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a4f952c9fb63441b776a4ced54d981214052a50e0105a129bd4cff7554e084`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00a7c086ff922bbd687983a530861ab85e12f4e86ed7570e0eb6d308f8a1982`  
		Last Modified: Wed, 21 Aug 2024 21:03:22 GMT  
		Size: 3.3 MB (3318926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c110c227884ff56144c010a0f45de283a21e37bf5d0bcbd7151ba22feba5d35a`  
		Last Modified: Wed, 21 Aug 2024 21:03:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bce4708dc23497ebe9fa33c93c86fbf8ff55f59ba7ba0df7ceeefdf0a394701`  
		Last Modified: Wed, 04 Sep 2024 17:58:24 GMT  
		Size: 17.9 MB (17911447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffc80b65ef821ba6a47da1edcf50544f9c4b03ca978e1423c4dbd44e0b53a4`  
		Last Modified: Wed, 04 Sep 2024 17:58:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:c3f4aa3604c492f3f4b373030a8d4e0b8bd6c119e4140deb61cd093d9c828083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e599c4e824c676997c224772baab6ed24fc11deb73e868de24a57f06c5c5b`

```dockerfile
```

-	Layers:
	-	`sha256:360935978b54716edf5cbf9d5b54534bcc75a801c3eb27b1176129f20da8e12f`  
		Last Modified: Wed, 04 Sep 2024 17:58:24 GMT  
		Size: 2.4 MB (2360998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b553ab848ee757a3e5e80c5b148fd9f770313337539145e15c43784bc7c71a33`  
		Last Modified: Wed, 04 Sep 2024 17:58:23 GMT  
		Size: 22.5 KB (22542 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:ad1925e8630ba182180df4fc1de77ee8ed5416244272d4ccc9fd4fc3fe55b871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521644f097a877ae7852ce01c311497547df43a58b32df68f0372646a3eba85c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:56 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Tue, 13 Aug 2024 00:38:56 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac03f6f5e55e30a2270bb15d50ac36a55766b2424c74ac055baad474cd3d848`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 3.5 MB (3502380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3c844b3809a334fbc035b8e4dc8a4fd09ab9f4bfb570b02def5d744b24cc59`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030cbd32147920432909fd4e4805929243e518f15f2072dfdf240c07934d243b`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 14.7 MB (14726933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bbf3f9753e9dab4c6356b8dca575e3442bf2ab2bcba22d415300d278b85cc2`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f7216b3fa539e06e992e4bccfd768c415b996b3e59d84ea23cdd39c2591d9f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721c09ed1dd4ddb5ebcba9cc49bbb75e4e5e5187fd5099714062cde0b327802`

```dockerfile
```

-	Layers:
	-	`sha256:2a8910a2795e1822d64979ea42f3e4c8da77ea4cf3d264cb85147593aa44e1f4`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 2.4 MB (2357809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9049875870847c6867529cc18d83c88c2b248e03cc4c09b14a5dc661cbd720d9`  
		Last Modified: Wed, 04 Sep 2024 17:59:02 GMT  
		Size: 22.1 KB (22132 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:9aab489d3c369a78ccf715cdb33c04b78f3bb7d95f7ef21727212c264a0bc278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a847c82c7e476b0c8638ee92a9e60afd8992d9f68c172535d4f42f693c95d0df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:09 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 13 Aug 2024 00:11:14 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8d1b1bf4e2ab963e6440240e13a2ad63af49c05eceb14b69154cd24380b349`  
		Last Modified: Tue, 13 Aug 2024 18:41:54 GMT  
		Size: 2.9 MB (2892342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa936e21e97ac879207d17ff144d3ba5ecee1c68009fc324837bc299a7a1415`  
		Last Modified: Tue, 13 Aug 2024 18:41:54 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbf166e81c8fbee2149ab7cdecb6f84a925e7a70e3f9630f62236c88b2849`  
		Last Modified: Wed, 04 Sep 2024 18:03:34 GMT  
		Size: 17.7 MB (17704039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead97c9d36dc0ddc3dd79e83216bcae3a26966b867351aeff05a7d7ab5ae3082`  
		Last Modified: Wed, 04 Sep 2024 18:03:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:2e0239bbbff8d6837d79e59173fd06a2640fd7bae53b911355a63f074516399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c823930cc66710176dd43adda5f516d39e3f7681ee9ef8d2db78b9b209fc1832`

```dockerfile
```

-	Layers:
	-	`sha256:5f3d3bb18f849694109a822b92935f90d34b9bc7b399765ebb47f3dc3b12ef68`  
		Last Modified: Wed, 04 Sep 2024 18:03:32 GMT  
		Size: 22.1 KB (22065 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:f0a9b761d1515eeb33ee3eb0f7c03ac32fa62e1f051d9296469fe1a3ec21be74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56512917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7d9003bc66b408421c2ce7035ca09d684438887b80d42fb2ae7feb69f1dba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:03 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 13 Aug 2024 00:22:05 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbfb1274366fcc0a0ff580c033e5f4c792826bd633a319058b4a8cd99361a99`  
		Last Modified: Wed, 21 Aug 2024 21:04:10 GMT  
		Size: 3.7 MB (3698350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3fb057bc7c24aa70322ed446a370cda9395dda0943d3c0f178a06fac741c69`  
		Last Modified: Wed, 21 Aug 2024 21:04:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde50f1695a4ec08fdb0e17034c60c28113a010952e25d3a7422260b040302d2`  
		Last Modified: Wed, 04 Sep 2024 17:59:39 GMT  
		Size: 19.7 MB (19690618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f914586fa6da32594b06ecd6931c3b738e2959f5c39ddf9a17d554d3bcc3053`  
		Last Modified: Wed, 04 Sep 2024 17:59:38 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f13d0989aba4ae8ccc48647e860ce96e470e4b9e42e128183e9b9cab0603b8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c892663524af5b6e1280a88f058b27fa136b628331b3248a4fb6f17b71382977`

```dockerfile
```

-	Layers:
	-	`sha256:d24fce6f624e3743c470c67de7ebd0b801f17791b05887b9f1c085f2efa527b4`  
		Last Modified: Wed, 04 Sep 2024 17:59:38 GMT  
		Size: 2.4 MB (2365017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4e4f200fb6d7456591243da1118e6e8a53923f7328566859920f1ae7d0274a`  
		Last Modified: Wed, 04 Sep 2024 17:59:38 GMT  
		Size: 22.2 KB (22250 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:017b11a1cef1e2f5ce53fcf04b47f74c964a9d1e4c472c4b5168a071dfa59dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47398518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8967f7989d3a4720e665ffcedf6c9ae12a5f35bdc5b328f5c42ecf436faf5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:39 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 13 Aug 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7be8316b97e3a1b645faaa487049ac621b293bb22f770ec35ffc93baec78f`  
		Last Modified: Wed, 21 Aug 2024 21:04:55 GMT  
		Size: 3.2 MB (3160198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a37db44ada7fb6ca6952dfb68226272239492846dba552a59abea8463845b99`  
		Last Modified: Wed, 21 Aug 2024 21:04:54 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cfacb26fc1f0175ead3964fa15dd0de340f488570df7ebbb320638cd53690`  
		Last Modified: Wed, 04 Sep 2024 18:02:58 GMT  
		Size: 16.7 MB (16746578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403506b02b1bdd873e6e23c1eb37aca500d38f46400688c9b12a8a23005db9d`  
		Last Modified: Wed, 04 Sep 2024 18:02:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:fca7c96a3dc13b43e10054cec9baac46b6beecad27bb2990b9096ffe9933198d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d75c39e92bf53a1a242db6cc9864befb1b28f09792689a227aea037407ec355`

```dockerfile
```

-	Layers:
	-	`sha256:185044b89166f8b50bb6c0f529c26f2d61611919df0b8b90df913c88db2db113`  
		Last Modified: Wed, 04 Sep 2024 18:02:58 GMT  
		Size: 2.4 MB (2360521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d75db7dd4425c10a23453e4e8e0984ab6f2f8c66df27c9e93324d4a16243a0d`  
		Last Modified: Wed, 04 Sep 2024 18:02:58 GMT  
		Size: 22.2 KB (22185 bytes)  
		MIME: application/vnd.in-toto+json
