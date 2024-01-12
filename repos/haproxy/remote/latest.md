## `haproxy:latest`

```console
$ docker pull haproxy@sha256:2358ee4ef1072ca23892697b8488ccda4dafa9f63c59fa23423e4ef82f55d85a
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
$ docker pull haproxy@sha256:e1d0edfdee9e39632a1fda3883dafb8c9268894849c1afd8afbd1fc6437bbeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47078457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e039e2b4b096e7d29b3d3b313d1b45b8becba4ead2eac726c47d78ef50e197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd43d38f1789e46d41ec604444a2b3be5960ed4c01d0e4af2c9744855eba8c2`  
		Last Modified: Fri, 12 Jan 2024 00:22:48 GMT  
		Size: 3.5 MB (3490946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c76cf16668b92cc1bf2eefe662e63ed51271f5f45e0313a71c6345ee2361e92`  
		Last Modified: Fri, 12 Jan 2024 00:22:47 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0c2082bfbbdf3697b1e2c9511d947a4f643d7e5bcde6ad600a39a7eb70c97`  
		Last Modified: Fri, 12 Jan 2024 00:22:48 GMT  
		Size: 14.5 MB (14459953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceda08f9ae6f6ea53e615a9596ca3b596e01540e3a1e1ebe2974ebc306ac6cf`  
		Last Modified: Fri, 12 Jan 2024 00:22:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:829d7ebfa83be5fbd073d28aafe1ac3f73ac1ee5a9dc17bd7d6f34962970a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b80aeb090c2c276f9da1e56a451598b8bca82beee9ac4143fda52b9a415f82`

```dockerfile
```

-	Layers:
	-	`sha256:dd8b671fd1950937dfe438be5be589af5b96cabd64d8e70a8256b83a69367ab3`  
		Last Modified: Fri, 12 Jan 2024 00:22:48 GMT  
		Size: 3.1 MB (3122040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedd7a5742cbf33d1f5c149dbf2069b8fcc0335c2168460a3e0b6d20f26d89b7`  
		Last Modified: Fri, 12 Jan 2024 00:22:47 GMT  
		Size: 21.7 KB (21668 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e513438a2571fd296db49bdd570d2a0d8ecef98fc118699032097cbc60f948c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42932189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093d51d1441f9115b3d53118eedd886ab223275c93f2b669562738ced9c73046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19a954f0ec3c5f770ad4d2b4f9896701c7e23c5dc4aca8b7a706a0103ac7282`  
		Last Modified: Fri, 12 Jan 2024 14:29:32 GMT  
		Size: 3.1 MB (3066626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff822f39cc6843f9eea99287581a8e15471d6370f9aafdf77bdd83357814a2`  
		Last Modified: Fri, 12 Jan 2024 14:29:31 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e454056dd53be7b9f952456b62fe8f101f8941fb3df7ec25b1120aba256b215c`  
		Last Modified: Fri, 12 Jan 2024 14:46:26 GMT  
		Size: 13.0 MB (12978438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b554d4adbd06b6aa264fbfccb0100cb8c5df03af594b2db71a293fffb77198c`  
		Last Modified: Fri, 12 Jan 2024 14:46:24 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:64a5aa1497e1a9ab61f51c7c472a4f2f084e26f73f85e91c69b9848019f6160a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6261feb9b3876ab6fddc9007d4b3d81375a9f891871af92765142fe1fe7b5d`

```dockerfile
```

-	Layers:
	-	`sha256:136d01af43d8cd3987940ffc7741767d401172f759f6e536a6f3c2c478f363b5`  
		Last Modified: Fri, 12 Jan 2024 14:46:25 GMT  
		Size: 3.1 MB (3096748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e87df32b8c5aea3773032c58eef1bceb4866f29f168761cadfbc6de6a8fdb6c`  
		Last Modified: Fri, 12 Jan 2024 14:46:24 GMT  
		Size: 21.6 KB (21612 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:be805c2213a36558152081697ff750ace46a2892df668f92db83920746395155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40198337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870f523d643ea8231eef1f7f7e40f5a87af5e9113639eb21d687dee8dd1680d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72699e14d5884fdb9c47f8e9de304bf9f9255c8b015ded71609d46db00c48372`  
		Last Modified: Fri, 12 Jan 2024 17:07:54 GMT  
		Size: 2.9 MB (2903597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08524ad81bbccfc9ffa2997a7d03ed0483e6690ebd2d17605297c268d8ee09b`  
		Last Modified: Fri, 12 Jan 2024 17:07:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed391c45cdc46cc4febc08916333828a0006752b6f9b465f57a5ac1a54e8d794`  
		Last Modified: Fri, 12 Jan 2024 17:38:08 GMT  
		Size: 12.6 MB (12574972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969494ac04126323fab567e5011527999b05392bcff3814ecf91024b7813fdc7`  
		Last Modified: Fri, 12 Jan 2024 17:38:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:37f70e4bd22b58d0ced3a117bc0941f9264ec5b36caad8660cd645499ab8bd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da63a27d12f3928504f5075c1a1e3071b7135c014b65d57451e193074acaab5`

```dockerfile
```

-	Layers:
	-	`sha256:b5480d9538c5c29ea3209d7f22257e5b08042642b9edf9f8f766545d4019688e`  
		Last Modified: Fri, 12 Jan 2024 17:38:08 GMT  
		Size: 3.1 MB (3096598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff3bd9974df9ee4ef07776b866842b689a6e08c06354841d257fee68bd967ed`  
		Last Modified: Fri, 12 Jan 2024 17:38:08 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:7697e4cb56f3bd2a1b84d09c6d546d3574d27b9479d311a2d71931f33afcc413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e156b9b20facb84a58d4f2b93a950e0c9b90cad73dedbe481cb3b7b8e2584f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c8a18e713b3a28061235191eb1f1b478e3841667dd3bdb83f73cb130cc4c50`  
		Last Modified: Fri, 12 Jan 2024 08:34:40 GMT  
		Size: 3.3 MB (3314079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6c57c5420ec601732ca3300622d3d85761d27edb62c4fb1ebc0238ec909b6d`  
		Last Modified: Fri, 12 Jan 2024 08:34:39 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a36abb480a84b846a1b6be5140ad0b066b42f91616ae4c7aa5a5e6208a17d5`  
		Last Modified: Fri, 12 Jan 2024 08:36:33 GMT  
		Size: 13.4 MB (13445274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ef995e37f7c4a3ab14c13a979de65e607a58d1ce080f63b9edf4cb546ad09`  
		Last Modified: Fri, 12 Jan 2024 08:36:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:954fbf6560e0f754a829d6fe96e316b6eec577882f4abc6abfb8c7eabc60807f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09970bfda6bc0fb7bf3fe7f8a69d831dd07bcd296e7256d24290d9a69017fc10`

```dockerfile
```

-	Layers:
	-	`sha256:0980aa80cf48bf8c5a5d3bd5b0e64889c5bae507eb57d3a7f35a8cf758da2cf0`  
		Last Modified: Fri, 12 Jan 2024 08:36:33 GMT  
		Size: 3.1 MB (3097219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4738fab9bb45fac4258acca76d3d3c076d37ffc85680133b5ca0c83d0c4d26`  
		Last Modified: Fri, 12 Jan 2024 08:36:32 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:d044a04023f925fd330d26f61853495cd7df5f46313e83c10fb0de0b772627df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6509fd33ec9184b31a6017dd3640bd3bc2a2eb1bb771db7cc9e35dcebc7c8b78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19fa670fd240d224f5028492dce524d75689ae9adf1ddd9fb6b6d2feb8306a5`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 3.5 MB (3496055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2268550a7b85d28f6fa9a669b329bc1b3a25bde0e79662947da70282f867963`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c03aeee8f6bfb1f1d2bc9a1853bad9b9414efc231a5b623b3c95495813aa0`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 13.7 MB (13688802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef9bf90f6ae061d348769e75abd20695d9d6cb755e562dd62ea1790a98038dd`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:31ff3331bd914568e563e781718776d2bcb8f41d76f75e3baf068e5eaad35986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e664964ce66cd43da5c575f37a5d55ccabcdd5ee73bfe5a8ed45ffcc38a6c4`

```dockerfile
```

-	Layers:
	-	`sha256:36ba6b9e41af0a9dfb534a3c8b5666d8c76f60ada62f8288b0c4e1f23f9a6bfa`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 3.1 MB (3116372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbdc6fd9738a6ae507955b1cedd814df5a5df0199109d71fd60faadff12a5d9`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 21.6 KB (21624 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:67092cd227d8d8ea95740517da566d07e384133aaebe86853b904060dc69a9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45857080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac95c1ed56531ecec590efe6b2d80f03e6987fb99dc7325c4ba0760ebf9d489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5982060e709e77d51e5b7dca82283d2a0b600d79e34c57331dc4fc91c10112`  
		Last Modified: Fri, 12 Jan 2024 03:06:15 GMT  
		Size: 2.9 MB (2890290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4adbf0e68553d76aeadeb70d7c15e1d871f2bd618b3430b55c6529785dd793`  
		Last Modified: Fri, 12 Jan 2024 03:06:15 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fd5e657b2549a4b1b3d8cd86326f5709992da5d0608863183e82feb90546c`  
		Last Modified: Fri, 12 Jan 2024 03:10:47 GMT  
		Size: 13.8 MB (13843754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fb8efadc01bbf456dfd8a077d63cbabd0a7a043412c5f7912804dac9d7859`  
		Last Modified: Fri, 12 Jan 2024 03:10:46 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:dd419117903bdf8120fbbb351b4b8bd97eff0864e623f74822720af7e9608a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13de86dd6f33225156f20eb2ef3964bae10712174eeb07ba8dc5a7f4abf629d0`

```dockerfile
```

-	Layers:
	-	`sha256:89dd0f716c823b738c73559c306b24e4c4050606efe570edd22ebfee5c53ecef`  
		Last Modified: Fri, 12 Jan 2024 03:10:46 GMT  
		Size: 21.4 KB (21366 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c2261cafdeeebf7c8d1daa010ab6a546e3f26b378a67c41880c4812f8be3f8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51632453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0131e6846edcc804ed1d5a8166c2ac8200b80668006cc19f0bc73fdcc0fb57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab16af157893f7fd55d11afb2288759ad4b28e03604e5ba64db4c4ff0390b372`  
		Last Modified: Fri, 12 Jan 2024 08:40:41 GMT  
		Size: 3.7 MB (3693928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247998c00b96e59aee946cbfd1f254f91c21f10056f4ffadf5a5e1fedbdc35fc`  
		Last Modified: Fri, 12 Jan 2024 08:40:41 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec2434837a55b502d0afdf9ab389896b53043258e1bcf0d5070b92a221b786`  
		Last Modified: Fri, 12 Jan 2024 08:42:37 GMT  
		Size: 14.8 MB (14816353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2648f43af4f63edd1ef330fc870560d1c29e511cb71ffa095b168e5df5fa27`  
		Last Modified: Fri, 12 Jan 2024 08:42:37 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:ecefdd2db834761204e91d4e55e21ae437aea601de47f1d672bf1511a7f64b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3ef90dcdb8e4a52b859a343eb4b33fed141b32fd94586870cc5760923a477c`

```dockerfile
```

-	Layers:
	-	`sha256:1d542a2b82fa7f6a46f05db816d569fbeeac8e8e9cad7a6c866ef86026626cf6`  
		Last Modified: Fri, 12 Jan 2024 08:42:37 GMT  
		Size: 3.1 MB (3110568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e693000f13658f7c860687f7425e90fd881053f28dd9e51021b4088a48fd5a`  
		Last Modified: Fri, 12 Jan 2024 08:42:36 GMT  
		Size: 21.6 KB (21555 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:e33f75d9dd8f1048bbc4af1ea9a1bc840b5831df608606bb6551e8569b87f16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43906504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6f1934112737b22fedf4988995485dac3305e0ada57a23ca8910d74463c951`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.9.1
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.1.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=d5801c772aab9c43f40964b7b33b4388d14b5b45750be4d2671785863cdb9f1c
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 21 Dec 2023 07:56:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2023 07:56:45 GMT
USER haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a431834551ef75fdc0ea33df86334a344614528c436505e38c38adbf57d4aeb7`  
		Last Modified: Fri, 12 Jan 2024 10:00:07 GMT  
		Size: 3.2 MB (3156911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc82f2eb894eb410618b286f301772fae340cecb2c924bc9e66adcbeb7967776`  
		Last Modified: Fri, 12 Jan 2024 10:00:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eef44d2ae45fc643f1d66f34f1ba74a98ab2249921289698f81d8dfb584f2`  
		Last Modified: Fri, 12 Jan 2024 10:09:51 GMT  
		Size: 13.3 MB (13256101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6becab2a7b1c16884da1b8b52880ee6397ce6a0216d927a5f36406313fd5fdd9`  
		Last Modified: Fri, 12 Jan 2024 10:09:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a6030bb366078d010cd4728a754ad91988eeb0726578d891f04e7d876ba48a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220134e94ca2cb13d0302ab88ae30ef98e513f36500774caa16ac6e812a8190d`

```dockerfile
```

-	Layers:
	-	`sha256:1d611562d6196bb999a750ce401472873f0dea4bf55d727fb36949f36e569b6f`  
		Last Modified: Fri, 12 Jan 2024 10:09:50 GMT  
		Size: 3.1 MB (3111589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e31b8c5cdf06fc3cb5736940419a0802f69a9b88ccf2b8cc054a3b5bc8ce98`  
		Last Modified: Fri, 12 Jan 2024 10:09:50 GMT  
		Size: 21.5 KB (21500 bytes)  
		MIME: application/vnd.in-toto+json
