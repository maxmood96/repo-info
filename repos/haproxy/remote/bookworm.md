## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:da8a89fbb5a081002aad8f3c05fd9185646d6bc2c10d8d68943390f8f70cc74a
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

### `haproxy:bookworm` - unknown; unknown

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

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:1daaf85bf6470c780c4ecd56512bbbe63ba7b927954b142a7d442077338b7f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39073648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83095605e7ad23c45a745bf625964dc6e1a6aaecd18d739169b228073a2b5898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
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
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbdcc7ea3438c1cb10f3677e1d27d2e729f24896d15e18ddc8b11c73ce76788`  
		Last Modified: Tue, 23 Jul 2024 07:43:18 GMT  
		Size: 3.1 MB (3071471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b70f1fd4b164ab5d2f735b52cfa09bf1099705fa06ca3a79de73590be44240`  
		Last Modified: Tue, 23 Jul 2024 07:43:18 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8295099d5908489660d95e8df2fb53370ee351d3908124a11ba2837f18163a5`  
		Last Modified: Tue, 23 Jul 2024 07:44:44 GMT  
		Size: 9.1 MB (9113236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9ab3694d176598c8f6ce37361beb7d999aa8b7c377381b7b1cc74dc6266f3`  
		Last Modified: Tue, 23 Jul 2024 07:44:38 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d08a65e079a5c5150b87d408be291501bfc20db0d3cc45eec23326072b4d6c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e122a853b5a9db63c5449bdd6ab07451145aabb901705f96bced14d1217fc25`

```dockerfile
```

-	Layers:
	-	`sha256:b58c6365eab2ddda6f1afc4df162ddd78ea4135e4bc0cb35a97ac5f2b9b251e0`  
		Last Modified: Tue, 23 Jul 2024 07:44:39 GMT  
		Size: 2.4 MB (2364115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4deabd719f4364194cb21ba27fc417a8e4a8c7c9eb514793a3d38670fa7cf0`  
		Last Modified: Tue, 23 Jul 2024 07:44:38 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:702e40d70512c87a7392652864f07b5cf2457bd3c62b97c82ad087d00ba193ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36572856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcdc7af328bcfa29ffd11a30aa31cb9946d9e1db08ff40578ddb1161cdb2125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578321af5215cd54501fe4c4cf84286f40b41c7b6cee3c2f276720191b9e726b`  
		Last Modified: Tue, 23 Jul 2024 17:35:49 GMT  
		Size: 2.9 MB (2906302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b15e492026aab67d1cf4eb393cef17be680cdf971bf81a839003e6713d495b`  
		Last Modified: Tue, 23 Jul 2024 17:35:48 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b509a26b04db69ec13f5b30fd1256a93e8a534b1ba00b2720987132490848a93`  
		Last Modified: Tue, 23 Jul 2024 17:37:57 GMT  
		Size: 8.9 MB (8946713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b8fba7a24a5d3bafef4200d62bf89b8c89ed50b3a5397f124300e713dbe885`  
		Last Modified: Tue, 23 Jul 2024 17:37:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ded6c650c5f7815dab4240faa5e4fcfb7308a063d0e8a94b565cd840c790135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a2a40eac2405ee8cbaee5eac71b7eb990e209142a38f78c8e1488abf923a9c`

```dockerfile
```

-	Layers:
	-	`sha256:4bb41b6d2ab45402e78860c92458ea06c265badca59dbdb776e194e01fe91c41`  
		Last Modified: Tue, 23 Jul 2024 17:37:57 GMT  
		Size: 2.4 MB (2362950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d530a11971e73fb8ffc9fe90434bdb7225ae8392dd20a2db4363ca883ea3159c`  
		Last Modified: Tue, 23 Jul 2024 17:37:56 GMT  
		Size: 22.3 KB (22309 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:14f8a2f802d2bcdcdecfb22c5aa90c9908a5677a27930fab5c50cd62c6d9535c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41639202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2be76b7da9c998f731e35d43ff3f44091b18a28316c569e8f76ce620400856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321e9271d6f32e3cc986a11cab64d6f4ce39afe4a17186a9f0eb474735acc78`  
		Last Modified: Tue, 23 Jul 2024 17:52:00 GMT  
		Size: 3.3 MB (3318957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa762249bb46d6584b8b980a1ff4a51abf550234d05a1c0f788253bdabf0593`  
		Last Modified: Tue, 23 Jul 2024 17:52:00 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176f662b135d0bdb0523cf865d54ca658f174b007872012ddda3084b607f11f`  
		Last Modified: Tue, 23 Jul 2024 17:53:42 GMT  
		Size: 9.2 MB (9162034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08274234bf798be15b9d59552a1efc351008f643fdcdf114d9db407ab5a4419`  
		Last Modified: Tue, 23 Jul 2024 17:53:41 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:eb6b653c1b4a69fab6d44098c5a63f3f7d470e1733273504f6d30291ac32cfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa551344667949f401b148bef25023beb9b20530c699fd9ecb4d33fb265ec06`

```dockerfile
```

-	Layers:
	-	`sha256:2176e04a2216d59d75cc06888a545d003fc90b1f328ea6860912938657f01af7`  
		Last Modified: Tue, 23 Jul 2024 17:53:41 GMT  
		Size: 2.4 MB (2360998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f3f802fd67db760d42a28ded963f8a415155b1df63e4c6719fe5fe3337c067`  
		Last Modified: Tue, 23 Jul 2024 17:53:41 GMT  
		Size: 22.5 KB (22538 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

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

### `haproxy:bookworm` - unknown; unknown

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

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:1a1dc49e0164eade9cde5942aa5dbee6deababb9cb6389ef52b490d9ee6bf30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41324706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21dcdc9b6a48467154fcc869e6e9c8007046d5751998637c774687a0c257287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
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
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68bcbfe05cd35155d675c5b464fb9bf1ff9021c3292327950b7acac1cd10e5f`  
		Last Modified: Wed, 24 Jul 2024 02:58:27 GMT  
		Size: 2.9 MB (2892378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd2da8c4e47e72cf08005d9ed1138a1e91c5c2eb8ce3eb7235e8fe0f63857cc`  
		Last Modified: Wed, 24 Jul 2024 02:58:26 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ec752c79048c10c60a7595e599193306b606dba0b01b4da21365287bf43c62`  
		Last Modified: Wed, 24 Jul 2024 03:03:30 GMT  
		Size: 9.3 MB (9305761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c7eaed8290e89562bd5daf7c612844b8792ccc227ea81981e2bc82affa6f2`  
		Last Modified: Wed, 24 Jul 2024 03:03:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b982b4ff0851022beaf2d257dc8a7f4e8a05e04dd74e93064815bd4def641fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850f210334b6f3c163a0129c6a62b1aead06bc519dfa0ec0123de76e664f84e6`

```dockerfile
```

-	Layers:
	-	`sha256:15e0e2cf94ca168115f9190bd4d57abbbd524a0d8e39d1eb07007a04c767c379`  
		Last Modified: Wed, 24 Jul 2024 03:03:29 GMT  
		Size: 22.1 KB (22061 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0c504b8a053d40ee04e5de71001990d6541f2d0a90c4f70657e6e57d04a5fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46508709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb89be86128f911c3b437a59c8f4a58e6357d7bdaa0410caa223ee5feb625ff5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
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
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b42bbe9382623778c38223fcb890ddc47c82077ad84ceb56f081e0a13fb80`  
		Last Modified: Tue, 23 Jul 2024 16:56:44 GMT  
		Size: 3.7 MB (3698357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaac5fc26399514413cc23851e2c7fb907d60c90e52136d69b861cc67914bfa`  
		Last Modified: Tue, 23 Jul 2024 16:56:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a23c3454fcb264d10af98683ea3424beee2054d0ff03b8587a0eaf1e877e6c`  
		Last Modified: Tue, 23 Jul 2024 16:59:08 GMT  
		Size: 9.7 MB (9686441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712a4881f3c7f64b2be6d4ae5011f727f76e1c6b90eff35c13b6c942d25270e3`  
		Last Modified: Tue, 23 Jul 2024 16:59:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:25b418fec154262419132f081764e9e6a76959b5e5010675479c381e21b8c972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093259edc61d16e126816fdcd5adf886edc446322050b4805f485df710751de`

```dockerfile
```

-	Layers:
	-	`sha256:e956e6c44d70ff990312ad941a44eb958a096d19be6edf102eefe5b1db3825f3`  
		Last Modified: Tue, 23 Jul 2024 16:59:08 GMT  
		Size: 2.4 MB (2365017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88bd82618f51df1875ee723cb0f9cb48cd29cdba3d77d57f07e08a87b372272b`  
		Last Modified: Tue, 23 Jul 2024 16:59:07 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

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

### `haproxy:bookworm` - unknown; unknown

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
