## `haproxy:latest`

```console
$ docker pull haproxy@sha256:c3ca2f50e701297770a358ddcf62c432da11dc72e9a2054fed695cb6795d01eb
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
$ docker pull haproxy@sha256:68ce363bbaa1d341b31be70a71fe3dec4c4cfb1f0ee1c935c1617bdcbc5b581b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41736325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb8e6b467213e8a8142b77ab8bde1a647d85eaf225e280736e5d5e60ce3624e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91433623ff3c53adb1ee960afd9263c27561cbc41446f1eae5163d2dfdf079a2`  
		Last Modified: Tue, 25 Feb 2025 02:12:49 GMT  
		Size: 3.5 MB (3499334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e287bd2da5bba514071065eb6015a16119cdcba447174f11aa18de380c50f`  
		Last Modified: Tue, 25 Feb 2025 02:12:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad3316688a9d67cb73494ea94b457a884f6e35df81b4899e228023f944e29f`  
		Last Modified: Tue, 25 Feb 2025 02:12:49 GMT  
		Size: 10.0 MB (10016049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836d977af65b63adb492589273fef5b78ccbb06e35ef878473bfaf51b0f949f1`  
		Last Modified: Tue, 25 Feb 2025 02:12:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b946ffce0e6f4fa7cf3293e46d5b255dcfc1cd0723f7d7c37b8b880359f4068b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52670adc3339483b7dcca8129007736497229410b8eff33802b71dc9151030eb`

```dockerfile
```

-	Layers:
	-	`sha256:89945f35a21caf6de076b22652798666eb6dd2774cc2dcd99a63ed14165539c1`  
		Last Modified: Tue, 25 Feb 2025 02:12:49 GMT  
		Size: 2.4 MB (2369063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b2f4a28e936a0430d0e74d57cbe2d1ce3e6e209aab9788b4f0b02ca3b360fe`  
		Last Modified: Tue, 25 Feb 2025 02:12:49 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:b9a83f583dda28fa0c1c77e26e2832f4d9bf86e1e2f21707906e3047ea57af46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38823860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c04157b10e253f278c2b3cacbbc598fe70e6668568336f6f9f2c40a4f21b58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb796b4078c24eacc4e96fa6314434576ef2cb38939712321f810114f707a3`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 3.1 MB (3073429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6633fcbfc99e037dd82e82e08e6061be81aac16e1a6cb5d6dd8beacaedc3f80`  
		Last Modified: Tue, 25 Feb 2025 02:22:54 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e27b3cf879514e338ec1eace1841ed731896f9bb656595d1801504b2f4a1f27`  
		Last Modified: Tue, 25 Feb 2025 08:10:47 GMT  
		Size: 10.0 MB (10008156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc987ab5299ede5d5e7b84903d603677be17722013d165eb2c89915631baffd`  
		Last Modified: Tue, 25 Feb 2025 08:10:46 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:f254cc1fe0fa058fa5ae537bef8128ed8a59032cd00efc461533620eaea60d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e47e73a42b740ec6d028afbcdcaf8df880aba8568442cbb731becd6caea2fea`

```dockerfile
```

-	Layers:
	-	`sha256:57beda376363735f3a9ce095b16b61634dc7f6c270a182022f6d76acd69c7780`  
		Last Modified: Tue, 25 Feb 2025 08:10:46 GMT  
		Size: 2.4 MB (2372577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7154f2e7f6c950f0f4091bb74ab014b11d6d77ad97ac066859cf627c4cd152`  
		Last Modified: Tue, 25 Feb 2025 08:10:46 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:487e136076ed52a878cb90588f3c58df489224d65ad92f77a07ae6694de26762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36641863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4102aa654069b66714520c6beb715c9496d2c0869bf4006bf3574bc3d196fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404fdc0fb57d39a8e26e53fce5df0d8735e863f965a6f0adb560d70a9cb5e793`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8952bff13ffb8acf33f0841d7fa8293820556d9084205ad6d23f7eefdc1da58`  
		Last Modified: Tue, 25 Feb 2025 02:19:13 GMT  
		Size: 9.8 MB (9812693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51cb1bca945b9f19da8d0a8a774a16deff37ec0c9791ee6dc4d8af6d9ffd373`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:004387e7eab4799e06e061a2d63310a8ab37e0395e89310cdbf8e0a5b931f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd731e1f9de26526cd71270e5511508d01e956dd9a570871221af79630b36ce1`

```dockerfile
```

-	Layers:
	-	`sha256:a8a6831deade886ed3b41a63982284e33af95ed4a555a0e1bbf47e28d5862f61`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 2.4 MB (2371306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa7786a21c4799a0fb9b8c1039eeb1f09ce566b39a50d81eca5471b08629962`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f71049073870c7facd9ad8495bd3b02d655f0cc1ddeb7a2cd527cd40f6fb87d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41360105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4584d972ae771f5054c18199109eb03cc22172b75e978952907c0171d3ed2dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7b4ee7e951b37043152ade0847099b1f46f92e07b958859030ae0f10fb4e9b`  
		Last Modified: Tue, 25 Feb 2025 02:20:00 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed0f2753c8f1c99271ce1642d4a8d155dcd489e0a4102ee1bd09c63fc4967d`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 10.0 MB (9987155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafecde205479d1ebb01ddcec3cb9393fcc385a48ed08f22a6095e62c6ce0717`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:38e6f7db7f2ac6cb80662c24b2639fba8e8e2f3b5c19f352b16e289d630be1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36adbc453da45054cdea0e2efbdc52a5af7c794ce8e292de36d0c3e187da4f6c`

```dockerfile
```

-	Layers:
	-	`sha256:896781d59317d77bb4d5974122ef0ae7a064eaa5d96707022c72f907c1668d90`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 2.4 MB (2369346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed52e1ba5576e3d0259b9de206d292d04088af1f718ee05f9a79efed93a0782`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:4faabb9cc2e958b307312115c153e6e3718c56d53d52d79015dcbfc123cab5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42448186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e54b60cf15f69327eec8046aefe1a80def48ee8af50ff23db087afff0a304da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f5b3b8dc12240cbad681502a239127df8a74a741f9b28dc78950931781eacf`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 3.5 MB (3503443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90864b6d269a77a18e5c9b555c935b11511437315ddf0957b1fab70d5b8c5c5c`  
		Last Modified: Tue, 25 Feb 2025 02:12:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983be85759becd4c0bf47cc99500a8c80a9d9faf7e4bd965a5f6a21c50f0cad6`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 9.7 MB (9748514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b74f8cd52372205d8dd0cece05487de821e53d686cf218c4944d0b0a3aef20`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:564e0b13990000b87d717fdead4a01310681a4ba4080688f67e56828acf2234c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518dca4630dca32b5a5622ce34748bd60476d69c4fcb72c6f401b4070491517d`

```dockerfile
```

-	Layers:
	-	`sha256:9e49bba81fcfdd64786b1a9333b6674d51159dc6371f34ffa5409723658dcc36`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 2.4 MB (2366191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02514c79b6b9027a5b96dc83e971f0055389fc982cc3e65afa84e2f45a525cf5`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:e2553890a6593771a39d1c4d562d84b8b5a91433d9dc0f9530c2199fa1730b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41509321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4b60d948de552e03fb9b27aa7651c06e343e0575b138e9fc5e3c0e783bd12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c82bfc1c2f5e4b0dc4b532714b8582fae92d04a9d4c6e432252fb2e247fc44`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 2.9 MB (2895386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d134d9bfb627f1719193c98a83137b618b72692f2b807ec8b91ad1507959f317`  
		Last Modified: Tue, 25 Feb 2025 02:24:08 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f168b861087b1b2a2c03f310fbd49ac0e75a6a89936860f6a0f2863778567860`  
		Last Modified: Tue, 25 Feb 2025 02:29:04 GMT  
		Size: 10.1 MB (10118607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f4ebb43b12fbbc6d5643e518fbd11072ac9a954d204ba438fecbf4965109d`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ebea310c156e07c3d68c33246d876a42c2ec2cd4ad233c7b301b66bfa0a181e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1fcdb5b0571500c693cc3c525d581930214dfc2abc86fd5b8c1a74f666569`

```dockerfile
```

-	Layers:
	-	`sha256:8546480388ca37acd62249f8a4515d23d7586c0b96b4f9822731e206ce73d58f`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1792f02dcbcc34de6458dadb5e39199f3965c4408aaff6f45745a59d8f507162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46262142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413668c3df1aba4a1f3d3cc591373b984d056698f576cf46224a25d457f741a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bc6f29027769d00b506a51e73aa8c38c1b8573e422dbeec27479d1dfca9308`  
		Last Modified: Tue, 25 Feb 2025 02:18:31 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad995f48b4827fb8c2b9a18b10d730e429960a4d94d72776a49085676c5f2f12`  
		Last Modified: Tue, 25 Feb 2025 02:19:46 GMT  
		Size: 10.5 MB (10505208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbd4a91ddc96b9f0e28a0e755001d1620bc707cf2fbab1b3bb18b800980148b`  
		Last Modified: Tue, 25 Feb 2025 02:19:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:110f3f1b1d7914da7abc3c524747ad312db261fe734ead0025d28febfa97f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7335c854c46f282f0d306ad99e83d789cc5ac72abb6e7ae5a02dc42ca2875`

```dockerfile
```

-	Layers:
	-	`sha256:b7d11ece7b28e5aa2a6934a9a935a6c8fc35709dcdd9c155059a8e207f131523`  
		Last Modified: Tue, 25 Feb 2025 02:19:46 GMT  
		Size: 2.4 MB (2373377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea21f774fb82101e5e78be05a4504a680befc3f700b9126f5ae50e859c2295fb`  
		Last Modified: Tue, 25 Feb 2025 02:19:45 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:8491465dcd065d8c4284e966a9c00f2d63b643b1aefbbc79a833dfd7ccb35b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39921946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74df609b612636c6d888847f10b52a62587a038a2964787fcdce0f600e3021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec25f4589ffdbb577c0bcfd5ad87b05e2df25d8b5ef48bf8767cdfc6d5ad8f4`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535f5c181709b7dadd1424615ca8fe7ec29bc2ba93007c40a1db551ed750c44e`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 9.9 MB (9892070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d22c44d1e43c1b10c91fb4e34070d09a242ffdd0d389b3ef9e011c79ac4f646`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d29910aff021cfbf311685b50038ca7063e95aba2cdc3f573efa9798b74851e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7507deb1d9db7a7837f07c2ef04bbd7286ef72fff3c172f0af9f0009dad4fb11`

```dockerfile
```

-	Layers:
	-	`sha256:538a16c55e0dcf2e853cc6e2fa6a010f473ac1c5bfc90609dad6569c66814b07`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 2.4 MB (2368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9048839e1388dd1381ef0739023b2470da17abe4f99949fc7f4ce8747b4a7328`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
