## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:61ba467b5bf76a78c2331754451e53c41faad1348da7b757e172853e093d4879
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
$ docker pull haproxy@sha256:de8c16e3a8dd86d196bf4cfce45b7d66d25f1c296c6dadc00643bc65e0c7ba08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41729285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2681e37e40604a8a90196cfe9d396f5d1044d3e73e808c0437d2387fe408683`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3678512963015410722f6ef7e4ca4bb868a9aec2b5db848b2209188de0bbc02`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 3.5 MB (3499314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8205fbb84bd7fc95546cf90efd63241cf3df39111022e1d7a560d5e11bc791`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952af004283cf191ac0d969db0cad7061467fb67a6a4fb73744f8daaa656436f`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 10.0 MB (10016026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579b18b9c6a5e9c417edbb2287f8e6af9fb36803aee8ca6adcd670810c926a97`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:36c9371472f5d87288e36ad7bce49b0750a1a5208a6dda9e473705bcf94193d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256e58d0251666506138410940a515d229afb97a2b9458b3e64a638fbf1c2e83`

```dockerfile
```

-	Layers:
	-	`sha256:594bb3844ac60a0cd0b04d157eb862f5d0589237efb38965b3c8c05e809e3bca`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 2.4 MB (2369045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d867cd4b0a4bc55bd02594b94f0bdb6634ffc6ad181b12e8916a3dc9585a4a`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2722f34cc4ab603eac4c668d8a725cf9464ef9c135786971518d755a2cde47c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38819786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215310b6e3e5af40dcb1b4c3bb25a76b7b02fe1b941d66cb9bf29965f6e6f47f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91504bc1c1e71105151322b732b30225ed4af99ad052b57083b0163bea0f5f`  
		Last Modified: Tue, 04 Feb 2025 04:45:07 GMT  
		Size: 3.1 MB (3073419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7a338ccecc85fecfce8047aca5f7767fe7aaa86eb4bdfdeb537eff825c9ab`  
		Last Modified: Tue, 04 Feb 2025 04:45:06 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3ad9a418d55f4ddb7808039bee9448c9a97f912a15fed503e06dcca181c2e1`  
		Last Modified: Fri, 21 Feb 2025 18:30:37 GMT  
		Size: 10.0 MB (10008182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ec54bd76c7e3b2a92f8489c8c66b3056cf1b161bf0efbdb6320825ad45b34a`  
		Last Modified: Fri, 21 Feb 2025 18:30:37 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:60c67f1c28aa06032212e25834ffb20534f2e2f09602d2166626ca18285282e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8e9ac6f659aec09c1e95b04222232f420c0594f0a2d6d865c1d9a46714d74f`

```dockerfile
```

-	Layers:
	-	`sha256:1d70744039d9ed972bd05e5c54b1fca5abbec6f342c620dc610509cb55d25479`  
		Last Modified: Fri, 21 Feb 2025 18:30:37 GMT  
		Size: 2.4 MB (2372559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753f06ff7d1fb30f259d7c3b60fc75a93e84c0b36e6495dd66dc83ea44d4afd4`  
		Last Modified: Fri, 21 Feb 2025 18:30:37 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:abb287916c52acf9b0f6ac82bd8b0af992cd84fd37e16f5241f12fb9af742505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36636667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f223ff72e72d195c81b627560ebd8c6f689e76c8cbc1c269071f157eef84094`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff3d026663dffd44eec785a25c9c3855a8164799a6d4e938e18090f914a86d`  
		Last Modified: Tue, 04 Feb 2025 04:42:04 GMT  
		Size: 2.9 MB (2907810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410de9ecf4a542e26da93e9f5b2ea2b6d9536aef95077292c0a18149c48bf57e`  
		Last Modified: Tue, 04 Feb 2025 04:42:03 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4c916a1a0388c8e00affdc9795b14780778f29eca9a8b0b56376550c1cd6cc`  
		Last Modified: Fri, 21 Feb 2025 18:31:30 GMT  
		Size: 9.8 MB (9812680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c86a7b12d45c7a88a4aae038bfbd856ca358fcdd9883cb263af117f05fc5a`  
		Last Modified: Fri, 21 Feb 2025 18:31:30 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:80cf2c8e35438057fbe660f988062e104ce49f9c6b5c9b8984d342a9717c7108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3ed3eaa2445acc370aba4e38cf9a40d6f05f46f6b6f456544cdaf4555408ea`

```dockerfile
```

-	Layers:
	-	`sha256:5aab77216868746386b5b8d5825bc1d469b73292aabc5eb7542d1452c94b716d`  
		Last Modified: Fri, 21 Feb 2025 18:31:30 GMT  
		Size: 2.4 MB (2371288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bab5bc6fd0db4cf3ea7671517be6157baf325edd27f7e2aab52cf17b2450144e`  
		Last Modified: Fri, 21 Feb 2025 18:31:29 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e4c7ab6a79515758dbbe643264863528214d289474c1bb446b9f8ea4955bbe06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41352533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4baa318504ed8b35f361ef557eb1048e28e82f72c8eec91ab874c35f48917d67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9355eed803991b5fe9184c36a38aef87f1551a975beed62f9cedb673f825072f`  
		Last Modified: Wed, 05 Feb 2025 00:41:03 GMT  
		Size: 3.3 MB (3322828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d706b5cc0cea06f04bfbbfd8f3b55c806d00f33f24374f9c69264aaa31bc1e6b`  
		Last Modified: Tue, 11 Feb 2025 00:28:38 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564cdb65e9f3c28414c344d9e58cca4bcaf80c210babeee16a50b47496749a6`  
		Last Modified: Fri, 21 Feb 2025 18:29:50 GMT  
		Size: 10.0 MB (9987180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ca58747a9706c3cf8befac0973f688c5d050d4779079434aaf59f535431453`  
		Last Modified: Fri, 21 Feb 2025 18:29:50 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:25a250fbbdddce5cc2b2b2ed51ae1f8882e84c36f28440eb1ce331bcad30e5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a6029c7f89b9ebd1240336ff4e0ed04faef4eeb783f6d2ff2f08b82e8d6323`

```dockerfile
```

-	Layers:
	-	`sha256:9e43ee4f4cddbe04a2566ec9e3897b10aff14002f7be01da2d2e6d22f40ac8c0`  
		Last Modified: Fri, 21 Feb 2025 18:29:50 GMT  
		Size: 2.4 MB (2369328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708caeb13c26562e9537253ffe18c8585cf902be1017498131c5b2f95a0134c0`  
		Last Modified: Fri, 21 Feb 2025 18:29:49 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:590324616a005a86499e3f92733667c82ddbe6a92533036217dcdcdd96d2940f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42441032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61a1e5d0c865ac337d54da02e8a9c724908ea5e6c23c4b653817891295ef1a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b93e8b0f58b003b73668e2638fd365110dce4bb3f466451b29e9b40938e28aa`  
		Last Modified: Fri, 21 Feb 2025 18:29:22 GMT  
		Size: 3.5 MB (3503449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8205fbb84bd7fc95546cf90efd63241cf3df39111022e1d7a560d5e11bc791`  
		Last Modified: Fri, 21 Feb 2025 18:29:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40826fb232c12564080b50ea83b1ce20942b4ab7255d48cb0bcc7a855fe176`  
		Last Modified: Fri, 21 Feb 2025 18:29:22 GMT  
		Size: 9.7 MB (9748485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f7d5bbf22d9b06c38437c05f60e09486fefd0b51306c6c10d3202ec0ee295a`  
		Last Modified: Fri, 21 Feb 2025 18:29:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7e30ac56da3f80759914655fceabd6b9c863d1099bb796c365461e097f1e972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b122b7ddd46a9a0b3599413165c7fd7cf67cc5e2c397c205153646b0d47a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a161772667cdc7344829ce76aa89ab56760539a9078337b8aceb081dd487b97`  
		Last Modified: Fri, 21 Feb 2025 18:29:22 GMT  
		Size: 2.4 MB (2366173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a98f87d21552c8ede057f958be9ce62b79b0e288c6fe7dd5bb52d3db5a22fe`  
		Last Modified: Fri, 21 Feb 2025 18:29:21 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:084155622bc0a672d310c927d292abdc55c086ad2511b9f2e2552b355bc4f6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41502272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31ccd9511567593ea546c0ef65778d46b8efc6007af0871117e956dbbcb6778`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5ae736b15ba52070d57c9f2039f035b5f96ccbf855651ef21412c7259f474`  
		Last Modified: Tue, 04 Feb 2025 04:42:54 GMT  
		Size: 2.9 MB (2895375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcf91c1f0861b051bcec907829878ff27eadc4e7e2fa16c489e3a5a22e888a6`  
		Last Modified: Tue, 04 Feb 2025 04:42:53 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a18d1881197579f7a29c585beba6e138a16bf97d01e754c53be5787b8dd0dc`  
		Last Modified: Fri, 21 Feb 2025 18:38:07 GMT  
		Size: 10.1 MB (10118672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3effcbf72d558c6a1a29a11e4fb946738958858836174664ed775a644eb81fc2`  
		Last Modified: Fri, 21 Feb 2025 18:38:06 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6183f7201b8bcf87cd72bc8ab39ed39d4285b9478e0d2c4889ef961b16d61505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a5029db714d67cfd9f4136b934dbefbc4c555f4d665f0b3ddf06c350942cf`

```dockerfile
```

-	Layers:
	-	`sha256:4479818e062ccd128b7d90a1ec1dc32b4c54ab1e4a02c76903a840a349e27cd6`  
		Last Modified: Fri, 21 Feb 2025 18:38:05 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1f2d586966f41efafd523bf6645b5d40dcb2b026c879423b5339219cb7f00a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46254550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1959ea7c57d537b7131a99663503125bc3cb82ff98ea4bf1e24cff5e8beea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebacc5e3bdcc5a17c104d34d0cb74196d470d1dfeffc22349f69a1740ad1777`  
		Last Modified: Tue, 04 Feb 2025 04:26:38 GMT  
		Size: 3.7 MB (3702957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4195a222b922ccb334052fac481019206a9ab633368d4c5505eca6c079d2d41f`  
		Last Modified: Tue, 11 Feb 2025 00:29:02 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddba58b097995ecc1eacefb9c953ceb9071f6bca23ff19efd8ff79b64016ba08`  
		Last Modified: Fri, 21 Feb 2025 18:31:33 GMT  
		Size: 10.5 MB (10505175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b8de3fc7263563a3e366ed7e3fa1c61ffc804906c84092fa4483982ea4d4d0`  
		Last Modified: Fri, 21 Feb 2025 18:31:32 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:c1ac3d75c62fdd631bba9a2e7e35add694fbd4b25cdfd764a4372b637fe5430b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef4bd475998e525041dea5667578cea0303221dfcd48c2f1a326ad9897f1dd0`

```dockerfile
```

-	Layers:
	-	`sha256:7453e4782f91c58d7b6ddbd99b66041e808505d267627123d708f4369807f54c`  
		Last Modified: Fri, 21 Feb 2025 18:31:33 GMT  
		Size: 2.4 MB (2373359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d247879cd0a47cef88e2ed857c35b84ae3722d6ba4a4cb0adb43eaa3e390fb`  
		Last Modified: Fri, 21 Feb 2025 18:31:32 GMT  
		Size: 21.8 KB (21832 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:a7390dc6564f25766814a1481a99fec073e2c52cea568176f55df4c9f8a55a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39915766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1b7146be8dca71b89b3bf5b71aa3b750388268eb0180fd51540d3342dee31c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883a687bc74bf7b86205b797cebd7311f5b71cf92c8fd3923ed5c7c41643f944`  
		Last Modified: Tue, 04 Feb 2025 04:31:58 GMT  
		Size: 3.2 MB (3163360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd38641f718184d4bae3cd0131f2897498c0fd5b49aa51ee314d961bce5b2031`  
		Last Modified: Tue, 11 Feb 2025 00:47:58 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b666e13daf95e9fc4b2e46e978b62fc665dbde5f0d51657f09cff7bdec95a148`  
		Last Modified: Fri, 21 Feb 2025 18:32:54 GMT  
		Size: 9.9 MB (9892136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e211a794660e331c75170800d315ec1c37e9f9b93ac2afc7047f7b870f4dd35d`  
		Last Modified: Fri, 21 Feb 2025 18:32:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6440e4e43549d69b4eb377d0698aa607b0d42593e4988c6c4588bd244f04c83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dccc43b0f41d53e5fc05f31125c0a043fcf92310d38348984a885510fe53beb`

```dockerfile
```

-	Layers:
	-	`sha256:5b580eb912bd094b21ee9dd5f0ff1d18cf6270050bb75ba166faac0312191004`  
		Last Modified: Fri, 21 Feb 2025 18:32:54 GMT  
		Size: 2.4 MB (2368767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36fa684efa031d5a4ad84838cc476a676b0d95d8b13688f71b7ea859a1d2088`  
		Last Modified: Fri, 21 Feb 2025 18:32:53 GMT  
		Size: 21.8 KB (21769 bytes)  
		MIME: application/vnd.in-toto+json
