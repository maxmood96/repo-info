## `haproxy:latest`

```console
$ docker pull haproxy@sha256:3ab695ae94fb960da08947bb6d9ccb12e8237d7813c711beaf93a5310d150474
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
$ docker pull haproxy@sha256:564c872e11ce437531c07f735be3f6e57b7b89a8665f83ab071d0f848e84f172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41794155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5bebb0fd91397c696f2406999242c603c6c08e1dccc8c5f8284d949b7c1cf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f35aa9cdd9515fb4a2ef92a897757b941bc4127f0b3ebe59d32d8c5886f04`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 3.5 MB (3495517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decc7eb61c9b053770aa1fec827559ea09ff542263159885d259c9dbcb40e814`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223cfb63f5dcbaa98771cc4aae90b7e7d97225e3d037afa8ae18c43c5af5880`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 9.2 MB (9170766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04890a5cc25b9ac8828df32bb77b85ff55235ec92de4158577b90876393395`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:260b032ba6150ee2b6cdbd5ad4bfa6f700b27ff312e0a14ac736a08ce529159b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107f661270e8803a123dad664754335c1bdce7790a98e5f443668ba230d3cf4`

```dockerfile
```

-	Layers:
	-	`sha256:7d0332eeed4c0869b1ccd9552ea50233165124d03b555b356ff832bf1485f664`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 2.4 MB (2360692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7a472fc4e327582a81b103ef9675b3c1da65d257f430683fc0e3011b9c5209`  
		Last Modified: Tue, 13 Aug 2024 01:17:53 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:42ddcd933747017dfdcfd1ab85f8661ac7f292ea5e763a7a78136e39f934dfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39073707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965e383eb5b1d57fb54eae195c1221cce789cf33388dafc816afb5cc23690dc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:89bc2bf4cd4c77e84f215d138f8c6071575bf3a174ffb503c439a96984ec4317`  
		Last Modified: Tue, 13 Aug 2024 10:29:34 GMT  
		Size: 9.1 MB (9113267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f3cde12e35e456fba1bddd5b0b69f7e7c0b0361ecdda9fd2acd0234521ea8`  
		Last Modified: Tue, 13 Aug 2024 10:29:33 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:254c0b2fbd2903f76228b3da75788dd6edeeedcfb2ed869d7f25ac7f695cbd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4ba6fc451073345707b8406c9cf9249334fc0f715ae4f10569b14883161d37`

```dockerfile
```

-	Layers:
	-	`sha256:6bb39f2f9c9aa715769419b4058740d2b6d2ab70713a0e8c34e157a04cd5e307`  
		Last Modified: Tue, 13 Aug 2024 10:29:33 GMT  
		Size: 2.4 MB (2364115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2e09f5a88add9d593a8125ad98137686e49772f436af616db6a7a069deb5df`  
		Last Modified: Tue, 13 Aug 2024 10:29:33 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f60bf21ec3b24796947c20eab67c0c4310a5c937d5fbf2f2692e34e55aefc061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36572730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477e4bc2d63428ce81834d4ea59c03be8e63381e137be07b0b49664485265dc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:b3ad161c15de4f549ed5d30561860bcc7084a278b359733ceff0ae70bcea4619`  
		Last Modified: Tue, 13 Aug 2024 11:38:42 GMT  
		Size: 8.9 MB (8946702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aac3b5c3d5ec695147f53830a39cb7c8031ff093a656c768aca413ecbe08b1`  
		Last Modified: Tue, 13 Aug 2024 11:38:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:4853964278de19e4c58082d4ec5532443e59ab448cd77a5b976a8b3a0cb68e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f67d0a09afdeeda53df98a59e7a16e637f80ccb790a72a4f01d16343b5a4a4`

```dockerfile
```

-	Layers:
	-	`sha256:07a89276f001679cc3ae4101adb524064efc31a5b7f9a4ede385dbe8b4a433cc`  
		Last Modified: Tue, 13 Aug 2024 11:38:41 GMT  
		Size: 2.4 MB (2362950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa19dece4b1e854fd26f42dd4ae68f7b51314fe340bf35f4cc6c8a68ec1b361`  
		Last Modified: Tue, 13 Aug 2024 11:38:41 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:5397be04178357a7fa373a548aa14c9a3bd6ccfee5801120e12733f61cb3311f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41639106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b943118473c0910eebe66c470b621d8094c0f939182a9cba2921ca9a5c19abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f549a12d7916ba8d128faaba9540a4269006ead9ebf0341ce188fcb83e1eff1`  
		Last Modified: Tue, 13 Aug 2024 07:12:18 GMT  
		Size: 3.3 MB (3318911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edf3ea8324ba716ed0a346e0c30135e7cac60f9d5474df9c3dd27801d848d1`  
		Last Modified: Tue, 13 Aug 2024 07:12:17 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ab71c19ba0beb899588d0c8410cb16b57361e4616393d19a61b8006806aaaa`  
		Last Modified: Tue, 13 Aug 2024 07:13:09 GMT  
		Size: 9.2 MB (9162028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44502e7024e302b66cf3c702f8edcfca0fc1735df02e316f03ae9d63c173ed73`  
		Last Modified: Tue, 13 Aug 2024 07:13:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:8e5c12d9a0d000d2d0150ae83fd2420b5ec0e32c4e26893f051fd8fe0f9b1428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ac72f26aa4b18ca8f1767126a815934fa77757bc050bdb0586cb6efc38df6e`

```dockerfile
```

-	Layers:
	-	`sha256:e159a956337e9e856c6153f9df31a41916812bf2aeebf24f775efb19b995c46e`  
		Last Modified: Tue, 13 Aug 2024 07:13:09 GMT  
		Size: 2.4 MB (2360998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d063f7bbaa47d14a783adb0f3caad0f3fa8abe219e61c64e994e76fc069eb2e2`  
		Last Modified: Tue, 13 Aug 2024 07:13:09 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:c97f3f38436e1a95dd522edffb8c7541c8f5434164e7424dd46c335bbed5e624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42580682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecece8e6d235e91d722cc7ea73924ac22dcfe970c7c5183af760492992bdeca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca25659ed55c209ea270285143f965232d673c4b30b5ef6b5b3802121504c40`  
		Last Modified: Tue, 13 Aug 2024 01:18:18 GMT  
		Size: 3.5 MB (3500306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e153c6b8a0155346c5627d21564e8ed404b7581089b49fdae7563aae66eeee9`  
		Last Modified: Tue, 13 Aug 2024 01:18:18 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2d8f301b3ab3c2b34763fa4751910366277a51d1a154f1599ae00cc43b2ccf`  
		Last Modified: Tue, 13 Aug 2024 01:18:18 GMT  
		Size: 8.9 MB (8934457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6407535b71438848d9bc94bba8a12721a4f2ef7d9f7140cdf81164e987622d73`  
		Last Modified: Tue, 13 Aug 2024 01:18:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:c8ff197a1032a5d2db144e0779d594faa0f1ef8cc028c6592ede533e44f62127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b37ea8a6c795a48691914d75ebd6935eecef6d812a9ac7ec9f56f9b849749`

```dockerfile
```

-	Layers:
	-	`sha256:033c8509acb0df445793fae2d7d039ae069bb49b1a57e6db2ad0f62c20b97eef`  
		Last Modified: Tue, 13 Aug 2024 01:18:18 GMT  
		Size: 2.4 MB (2357809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3be7e75b8e41bf233f3796a1f300dc9e7c313974b634b10a226d540fa626a1`  
		Last Modified: Tue, 13 Aug 2024 01:18:17 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:ad55bdae39180ed8edb44acb95002e9cd04d9f3be40cd8bffc8aa263a92bd703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41324665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f146e6e87d92741414c8fcaac24ae4a64d0da4e6e6f11939440b80a8e7f2786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:d973de1c4845a44016e5170b311090c27f1d13567d58a101faa29dd735739144`  
		Last Modified: Tue, 13 Aug 2024 18:47:21 GMT  
		Size: 9.3 MB (9305744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204a101392944a49da236a8de01e4e419bfd158dc8ac521bf72612a47e74d65a`  
		Last Modified: Tue, 13 Aug 2024 18:47:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:3e5f319254f5c169c02607dc1c5ccc36a6691fbbe2cbb4aa578a74166dfd7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a013f8336459e2eb5297edcb982dbd935ceba5dc8c7451ef0d087ff272cc4c`

```dockerfile
```

-	Layers:
	-	`sha256:cdc62a5870accccf58de2a0e384e82c7b26857cc327ef4b2ac74405cc61383e3`  
		Last Modified: Tue, 13 Aug 2024 18:47:20 GMT  
		Size: 22.1 KB (22061 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:5754e228209f6f253539658dae9e6f689c45e9aca9b6584adcc51b1f591f921f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46508753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34343342e7812d816d7ef69bb75e4c96265898006005b59fe0e0bc9f451a86e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e25e379eebdcbb90f85e7ab7034a60f1558f7de7b035d90bf87f51273a25b87`  
		Last Modified: Tue, 13 Aug 2024 06:32:42 GMT  
		Size: 3.7 MB (3698349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bf984ac60e85c75bb4845b682e6aeca531b2baa8dd5baabe750457653d0060`  
		Last Modified: Tue, 13 Aug 2024 06:32:41 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7b885c0d54407b53e9f22cba64a372d74b61d54d4c8353b7765af773aa9f8a`  
		Last Modified: Tue, 13 Aug 2024 06:34:18 GMT  
		Size: 9.7 MB (9686462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb898afa0845ba54276a811017304cbb81c1e3ee7a95171b0d22ba88e0bbc4e`  
		Last Modified: Tue, 13 Aug 2024 06:34:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:3336701e69a7c1f98e97363d53b5800ffe51e15e83ac39f3f019d09cf997e42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c865fe2705adbcaff64b367955ae3dd6079e06ac3ed2b37ee20644397a3a418`

```dockerfile
```

-	Layers:
	-	`sha256:15cf60556e2a8663612acd6d0bdeccda1eafd0c3f99ad832dd8b2b176ff4f76f`  
		Last Modified: Tue, 13 Aug 2024 06:34:18 GMT  
		Size: 2.4 MB (2365017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1224f40bca51a3360ca557fdb24ae8484ace7ac8114552db63987ff7506f8e7`  
		Last Modified: Tue, 13 Aug 2024 06:34:18 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:7c0c8810380530096a7a72cb50e238dd8d9805874e99a48f37694955d3399fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39708980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ed6ddb284cb73f065b1d6162e226a38fd5b64e73b0356f107ffc0d59288b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
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
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638471d2bf528874c613f16b9ea134036edfdc6719ddbe6c3162c26d6cd0fb13`  
		Last Modified: Tue, 13 Aug 2024 05:11:08 GMT  
		Size: 3.2 MB (3160184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b53b10d8179b818334a7baebe155a74de47f7f3545172dcde2c418aedcc1cd`  
		Last Modified: Tue, 13 Aug 2024 05:11:07 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b30926d6abeee866960f8d7875dd62a079a35b409bb61db69b4473b8a5993`  
		Last Modified: Tue, 13 Aug 2024 05:14:46 GMT  
		Size: 9.1 MB (9057061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcd62914a69eca8090e013242062638030c4ce1614a072468e93fa5846f2c32`  
		Last Modified: Tue, 13 Aug 2024 05:14:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:51b9e1dc768bc7dbff20e94d86bf185b3946eb8658addd4f927d3c31fb6a7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9e52728e2c387d550d3d47e556561074f7d4c7c0b2372b1938638a00ea319a`

```dockerfile
```

-	Layers:
	-	`sha256:6a3de09ff0dff5de7a5e64476d7c22fc59151794eddfea50596b61507f6fa8f1`  
		Last Modified: Tue, 13 Aug 2024 05:14:45 GMT  
		Size: 2.4 MB (2360521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331aa4ace386c0873b3c46c8c7ebf1045c4d4f0a0d98b3d4bc82d249c4b1937c`  
		Last Modified: Tue, 13 Aug 2024 05:14:45 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json
