## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:94ffc515b57b9995882cf598d0ded6bb3160eea97d2796323be540e81adf9512
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
$ docker pull haproxy@sha256:5592c458d1f81bb002f799811966dc43170f8c0aedb528826839bb2ac0876f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46565409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6c601e9bf8a7048147196b38c25c305c29fd07a462a40572f21496e10745a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51019cd97814cd194722c3fc1d9b246ddd85c0c6c281dc16c13e99ea3de0a5e4`  
		Last Modified: Wed, 31 Jan 2024 23:55:15 GMT  
		Size: 3.3 MB (3299217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed682a7b427659c65e21bfdb342d0a2fe65c5677ab0d9e515d2b6e1f1c078872`  
		Last Modified: Wed, 31 Jan 2024 23:55:15 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1bbc0b7f1c06829438caf99e75e09c97f4116a61fddde7936a4d1817f86cff`  
		Last Modified: Wed, 31 Jan 2024 23:55:16 GMT  
		Size: 14.1 MB (14114087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047ae2484c633bad66d9a9d0c7ad184c553169befe6d5799023bc26508a52f92`  
		Last Modified: Wed, 31 Jan 2024 23:55:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:5d445235c37be97d5368f47c887eaab9ad270d03d5391e2d20b62828d65f7596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ad9ac760f7cdbf5928c1cdf9fc24e2caac12b609b3e0c0e4fd6f71783be18`

```dockerfile
```

-	Layers:
	-	`sha256:999eeaab3bb947190855598fa6f16a4e190f8f2e4bb81aeb692a4b4389999951`  
		Last Modified: Wed, 31 Jan 2024 23:55:15 GMT  
		Size: 3.1 MB (3122042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25846eeddd0e76e2e21a3dec8c530e7c63c07ab0fe7587c69e51622da3f585d`  
		Last Modified: Wed, 31 Jan 2024 23:55:16 GMT  
		Size: 21.7 KB (21669 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:62974c28d687fd675ba4c731a7ca666321b04bcc96fffbbd2e132f05008328ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42377435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca7176d16fe7b1f7e03a3ecf368c5f11083636ec4887bcebe57930bb650d191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae3932debb1bb76ad7429082b66becd7db0890710f001178ebe6f782ee3dac`  
		Last Modified: Thu, 01 Feb 2024 11:49:27 GMT  
		Size: 2.9 MB (2874507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9a50d0639f526664573d09f758fc725e20d4a405a86f72771686640c82b2c0`  
		Last Modified: Thu, 01 Feb 2024 11:49:26 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb869d048378a1f5b8755861e70d08f5a0f0534a0d0139b551af362d73da6be`  
		Last Modified: Thu, 01 Feb 2024 11:51:23 GMT  
		Size: 12.6 MB (12591966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1692c2a88d60ba9b6ee5061c91cfbb4a14c459dd1fa5cf08e9188b9a97d540e`  
		Last Modified: Thu, 01 Feb 2024 11:51:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7cd9fd4d03937861b8d30b948db9255fab6047d1209e6bf541775fbf28bdb17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0babed92450d46eed11f75208d4dfe778f410ee364bdfc5a3ede8e80c696f`

```dockerfile
```

-	Layers:
	-	`sha256:651683fe59579c728a28c91aeae2c269d2518bebcbee866f3f40aadb0e6f7165`  
		Last Modified: Thu, 01 Feb 2024 11:51:23 GMT  
		Size: 3.1 MB (3096750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcc95f4a3e1736b0de5dd1a841c3cf8266e1a42735c0eb1116a9ec31e760f42`  
		Last Modified: Thu, 01 Feb 2024 11:51:22 GMT  
		Size: 21.6 KB (21615 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6fa87c48787677154063fc388b605788e46ad8f1e457b0dece49e2ae3a933277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39819447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5cd90b2a85c66bd20dd855f4a3e3ee338ed1f471bf671626aa5885a0de71a5`
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
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:1cffabdc2ef7ec6624d5a62d3478bdc25eaf9cb49697fc2010043daee3555fc3`  
		Last Modified: Fri, 12 Jan 2024 17:53:30 GMT  
		Size: 12.2 MB (12196082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e38f6f7fbbf12cb1cfddc982ab870c5879fab7c6f8aecdaac591fe2ac39c78`  
		Last Modified: Fri, 12 Jan 2024 17:53:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:069bfac9679fa7b8bd3306b32cdcbb3dea031df340c68e12f5e06017c5ffaac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f6f0b152a560134861d10933761d85a1424bfc9aacf51649e0106857f198c`

```dockerfile
```

-	Layers:
	-	`sha256:9a272b99f1d6b1ad9a307abd833f86a5dae58749194c33a6a356b9969c5e8d47`  
		Last Modified: Fri, 12 Jan 2024 17:53:30 GMT  
		Size: 3.1 MB (3096600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4ca2807ac9e983c3cf3f4216eb347852d3c9ef8b91dadc63fd02b34fb607cf`  
		Last Modified: Fri, 12 Jan 2024 17:53:29 GMT  
		Size: 21.6 KB (21615 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:c87fd5ebb8c95006627abde7ba5e9692865bbb790651eb1ccf75c180dfc8e1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45350273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74b336b98566340f635bf4b25aaccebd7de083071c421c385826fee9c160f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db57d4409924fff3e9134b701329844b543fbbe5606744f2f9a5e50d3df0975`  
		Last Modified: Thu, 01 Feb 2024 15:02:19 GMT  
		Size: 3.1 MB (3122061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bc33b7bdb465a5bb80852a7068923cdbee23d13461dd66ee20252a7af24bc5`  
		Last Modified: Thu, 01 Feb 2024 15:02:18 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7baf3f6484967b43a0bc469cbb6eb523b7fa1fa3f174430946b18fb7f25058`  
		Last Modified: Thu, 01 Feb 2024 15:30:26 GMT  
		Size: 13.0 MB (13045741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f182b8d4a6f18affbc87ccc1b763da0bb6abc68b8b2fc81e5cec5f0055d96618`  
		Last Modified: Thu, 01 Feb 2024 15:30:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:14b36899b38f5edceeecd56797591f7f30c7c399f7e1664bf2b13ab07bf7768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ddf87ec184d3add25a6842e18ed7283bf42392de016da5f5ed0c484cc30cf6`

```dockerfile
```

-	Layers:
	-	`sha256:506a073b777c3ea192fe6381b583b95e9cf0b6f32060a3a1223954a358738d3a`  
		Last Modified: Thu, 01 Feb 2024 15:30:25 GMT  
		Size: 3.1 MB (3097221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8caf503f7726b55d4e873288a7836093e83fa34b506ba2f5609c70f13e23a79`  
		Last Modified: Thu, 01 Feb 2024 15:30:25 GMT  
		Size: 21.5 KB (21517 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:b97281a864f449ac627d33073a6ba456acd09e402fdf3df8feb6ad7a82e447af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46814824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c45bea8842dae94a91672204e6c2e2ebf2da8d2cef4a2cdb576b491e7a66065`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbb6dd9225d522ee11f51ddcc64c2c19c25c780400dc6cb31c10849b637329`  
		Last Modified: Wed, 31 Jan 2024 23:55:23 GMT  
		Size: 3.3 MB (3304759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d700a42cabb5945e25c9666437c3d06f349d660ace85f474ed4a8874507afd`  
		Last Modified: Wed, 31 Jan 2024 23:55:21 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d45c655b95c5dc08377b179f6d9c670d2c4ce096723ca72872fe845634225a3`  
		Last Modified: Wed, 31 Jan 2024 23:55:23 GMT  
		Size: 13.3 MB (13343411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65dab28e1a0430cff8454800c38118324822efa9a0fee76c9884adec39fe603`  
		Last Modified: Wed, 31 Jan 2024 23:55:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:67cd272a93791768a9e636a4fdea54b0dd237bee19facbfc1007da9381281424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946d8de2d2f39e15f898b2a21c7188ba4681406980841e44f2bab23af609d4c6`

```dockerfile
```

-	Layers:
	-	`sha256:5e82125d0e88af42e447b8b8a337366a5621d453f3504ae6a559492053e62e80`  
		Last Modified: Wed, 31 Jan 2024 23:55:23 GMT  
		Size: 3.1 MB (3116374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4cec71d276ac397c97267df37b23a6ebdc4ff8009ebc86f5dfbcdf89005dae3`  
		Last Modified: Wed, 31 Jan 2024 23:55:23 GMT  
		Size: 21.6 KB (21627 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:d079f615afcedc04c385e93ea0d01fad4b5c38a5cf9e7e14d671cc3898c89367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45302409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2afec542cbfc63ef08fa6ce2f4dc8bc6c4029c1cf37e1faeef0381a8313ffe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8956b6f23121167181118fba218bf9c7c47d13ac029aecca429fed0949d2869`  
		Last Modified: Thu, 01 Feb 2024 19:27:10 GMT  
		Size: 2.7 MB (2698803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274dd577b7c1ec37395744f1d64fb2bb7f0f1b7842402dbe25fdd70cae83171f`  
		Last Modified: Thu, 01 Feb 2024 19:27:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77da06963dbf6f9a2e1fbed41824ae3562b23f8be8069f7b87d9033a22b67a1`  
		Last Modified: Thu, 01 Feb 2024 19:36:21 GMT  
		Size: 13.5 MB (13459524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c320ed6f93a9b22987d82979343c03c0952150658c6299f88553b5075b56e00`  
		Last Modified: Thu, 01 Feb 2024 19:36:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:8b083fed4f9e4c3ad7e6099272eeb1a273f8ddd15c96660c4786b5f78445b8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bd81746346ed500b53f86e474ee356b4736f46924d09559ff5f539e7538fc7`

```dockerfile
```

-	Layers:
	-	`sha256:ea341ac52c530fa88aedddf0402a2549c2beb445755103a7eb2f5d5c08826c95`  
		Last Modified: Thu, 01 Feb 2024 19:36:20 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:322752f1ffc1314fd57d8973af3b5750969fa5b4f16b005fa3811f8d1f5e7a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51067270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4c9129bfebeb374a9a4309480028820fb376aae87f1ac277e3c45bec0e4871`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 21 Dec 2023 07:56:45 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
# Thu, 21 Dec 2023 07:56:45 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410845727ded5f900ee3452c226045e42284a20ca3d3496fbee010658de0e61b`  
		Last Modified: Thu, 01 Feb 2024 12:24:39 GMT  
		Size: 3.5 MB (3501455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f697c52c8337858337ee9b96542e0ee9af2640b925a54057b3e04bce2bb083`  
		Last Modified: Thu, 01 Feb 2024 12:24:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc23f1a96247f82c923dfed6b7616f38551baaccda815110345f56ac4ef81dd`  
		Last Modified: Thu, 01 Feb 2024 12:40:38 GMT  
		Size: 14.4 MB (14421253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9429d9dff5fb0574224a0c704b7072b192b43782b484bb51285b84e89f9c7ac`  
		Last Modified: Thu, 01 Feb 2024 12:40:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f65f015eea66d47ffb7dd62cc6dcdabb05c7b3efa87d72235fb7dfbb4116545b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a190db5496ee725c9e536ef4633ad4b62e400e1ed6293e0fb83963e1130106`

```dockerfile
```

-	Layers:
	-	`sha256:c3c830d2ccdf5905aa2ce8b558e3b7906aacb1d7dd891a0039ab9ab25a390645`  
		Last Modified: Thu, 01 Feb 2024 12:40:33 GMT  
		Size: 3.1 MB (3110570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57273db95a36ecd7562dfb2d6829f26249b2ce143f08eb0af825a73cc334c36`  
		Last Modified: Thu, 01 Feb 2024 12:40:32 GMT  
		Size: 21.6 KB (21556 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:dd155e2852ede1f2f8b3c05a2bfd1cf5c0019f68ae391036eda520fa83e931f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43521061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a48771a911b652da5e616a3077a693e57607e6f25c9d34d4db3aa5e91a14f1`
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
ENV HAPROXY_VERSION=2.8.5
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.8/src/haproxy-2.8.5.tar.gz
# Thu, 21 Dec 2023 07:56:45 GMT
ENV HAPROXY_SHA256=3f5459c5a58e0b343a32eaef7ed5bed9d3fc29d8aa9e14b36c92c969fc2a60d9
# Thu, 21 Dec 2023 07:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
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
	-	`sha256:5b43b2273dbaffce84fab183e030d2793e9f87fcb8989aac4c5402fbd08eebc4`  
		Last Modified: Fri, 12 Jan 2024 10:11:04 GMT  
		Size: 12.9 MB (12870658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de49a52afcdc43ccfc7e15df923bab809e498ee04909ee0aaf07c03f0099b6cf`  
		Last Modified: Fri, 12 Jan 2024 10:11:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:217297efb99d3ad55c384c47b19241bff4bcf717e467386c62c613d5e63abe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc95a87cc91103e2981b06cf93bdd5995c30462d727cd6896c7c09fcf83beed2`

```dockerfile
```

-	Layers:
	-	`sha256:712b1dfb06aba187e4ae7fe43dc02f4dc70863b01580fa97561a83539a5a8f3e`  
		Last Modified: Fri, 12 Jan 2024 10:11:04 GMT  
		Size: 3.1 MB (3111591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4db02a720718e43fedaa1088b2933c6246f79db98b92c3ef9d08f1369c7ed6`  
		Last Modified: Fri, 12 Jan 2024 10:11:04 GMT  
		Size: 21.5 KB (21503 bytes)  
		MIME: application/vnd.in-toto+json
