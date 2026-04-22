## `haproxy:latest`

```console
$ docker pull haproxy@sha256:ca564bba966e6e4b6052c76689642875dfcf8c47727519956a38e7a40098864b
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:abc1c81214bb2390da39c11a75da6b92e83882f12de98636714a34ba74851dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45874764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cb647e017eea29046a21215877aa62f2b3776b635067d4148f1d30edeeac11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:17 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:17 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:17 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:17 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:17 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15facf1b894faea938ae7a6c7d48fe21d002872eb967615ed3be527ad09d959`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 1.6 MB (1581106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd363d41c660ad045047c89092947ed4ac62491b211f931c74cba26fab455e2`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b73834a37a949afafb620a46324faad9919fb0b27b18520040a9d5bee7aaa3`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 14.5 MB (14511845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007334ce8d7dc57c5d0def543820dcf4541d31cc8591c9ef1b8c2339a03d3dc3`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6f00360adc8f3f2f212b1442f58e26f05ce812b4f55ded69063288c8fac7f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e118e28f3562d82c55105efb52449402d7a3b9b46e425595aa36f03ad10ae9`

```dockerfile
```

-	Layers:
	-	`sha256:219306021088d9a9b798014fac615aa9207937873b771eb3ee3617bff6657be3`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 2.1 MB (2113798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0beb8c6c6d8c7b9f9565aaaf31785a470c1d03f516b15437c887fa9351050444`  
		Last Modified: Wed, 22 Apr 2026 01:16:24 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:3276a8738c4e316c0789bcd53201f9f4175cee4fd2715bef7b0a34cf5fe6361c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44186912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aa2e4a0f9229573dc87f691ada22efc331b5515e9dfaa2f61a71866250758a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:33:23 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:33:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 07 Apr 2026 01:34:24 GMT
ENV HAPROXY_VERSION=3.3.6
# Tue, 07 Apr 2026 01:34:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Tue, 07 Apr 2026 01:34:24 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Tue, 07 Apr 2026 01:34:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 07 Apr 2026 01:34:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 07 Apr 2026 01:34:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:34:24 GMT
USER haproxy
# Tue, 07 Apr 2026 01:34:24 GMT
WORKDIR /var/lib/haproxy
# Tue, 07 Apr 2026 01:34:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f403199416424c85e44d5c50497ba7a25325941a4e0ac7f1ddddfa6791ec0ef3`  
		Last Modified: Tue, 07 Apr 2026 01:34:32 GMT  
		Size: 1.5 MB (1535773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a141915328709ad8feab154d72d5ea8a3afa5faca2039fc8acdb666b0307334c`  
		Last Modified: Tue, 07 Apr 2026 01:34:32 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ec262ca486812f4098c548f47559e483bf23f64aed198091298064211bfba`  
		Last Modified: Tue, 07 Apr 2026 01:34:33 GMT  
		Size: 14.7 MB (14705689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099259cd31c439ebb666882158955fad73ef2ebca87b94ad10dfe864fc70ddf5`  
		Last Modified: Tue, 07 Apr 2026 01:34:32 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e3889ea6bcc55ee648b68920b9cfd256ad90171272c8be66a14f7b28d3d9850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d95bcc7eef6cd48597b95589e0c745c063a1c99e2076b9ece5a3f030fd58647`

```dockerfile
```

-	Layers:
	-	`sha256:1d67bc9715170f69cb3f5dd4666a6b30eb223c87dc9f47b57232dd07246b150a`  
		Last Modified: Tue, 07 Apr 2026 01:34:32 GMT  
		Size: 2.1 MB (2116778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e78f62b8eb13878568b6e636775a9a0ec74e5ad7a791dec17b05868389c1833`  
		Last Modified: Tue, 07 Apr 2026 01:34:32 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:90415f06aaa45d3ee835d05be6bd80e023a4f334f5aed7ec9e0be4690b7f418c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42212540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8a59c5a91812058970ab8551d6ca3a9fa362c1f3349c75d02e0efed6b7d139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:40 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:31 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:31 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:31 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:31 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:31 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defbe821d14b3f28364898a1d70673faea0aca3b9ed3079787022b8b6db29b49`  
		Last Modified: Wed, 22 Apr 2026 01:16:39 GMT  
		Size: 1.5 MB (1489523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ebf4acadcfc7021dda4726f78edcb5da6978bca957e53a67f15f365f4076d1`  
		Last Modified: Wed, 22 Apr 2026 01:16:39 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bfb91b08de25571ef776221ab9643819b035217cc85af353aa7bf8cd42c742`  
		Last Modified: Wed, 22 Apr 2026 01:16:40 GMT  
		Size: 14.5 MB (14506539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35811bb890f1c5bf9f2580df90e8188903b90bf18aa3ea0a56b566795a3aa0d1`  
		Last Modified: Wed, 22 Apr 2026 01:16:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:632e57b44476c4b9c8c06f816612758818604e40e095904aae3ca8a4a2298fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb17975564c25a4d019c70c5ec4e03f3f160f310345cf2a6cbac69f102a9ae`

```dockerfile
```

-	Layers:
	-	`sha256:9c90e65029329f3de53f6de08973096fe8b254f3ed00d0575929cb1fd48ba3a7`  
		Last Modified: Wed, 22 Apr 2026 01:16:39 GMT  
		Size: 2.1 MB (2115221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c640623aa73a9fad3e1d2bcfa8a644ba86e163051b3f5e5d12848ff255ccb850`  
		Last Modified: Wed, 22 Apr 2026 01:16:39 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ec8c7ae2e803dc2d69888e2f0e42bed191a6c59530016169c93be934b56323be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df00b49cd3ae7305551287c612b09a2dfb5c2876b096025c0adbe59be679625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:26 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:20 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:20 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:20 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:20 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:20 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c93d77d43ffcaced3d3a3252d6bb1afdf92a7e088e7f47ddea5d03f676332`  
		Last Modified: Wed, 22 Apr 2026 01:16:28 GMT  
		Size: 1.6 MB (1563652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e7fe5667fcea7ec998bf4d2bf27e90348081f8a98f91a89f3a2539885c194c`  
		Last Modified: Wed, 22 Apr 2026 01:16:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b572c52c4f633af51aa1532990b283ee97c874325289c3a3f2aa6a76848fbf`  
		Last Modified: Wed, 22 Apr 2026 01:16:28 GMT  
		Size: 14.4 MB (14388775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a89cfb4635d664c0d3c34c9a6a1dbb242b3407db44e93c21fa8004354deecf`  
		Last Modified: Wed, 22 Apr 2026 01:16:27 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:bfcdfb2e0f2a3e6fbe45bd1bb6c75fe7cf21a6cee3c99d59a60492d32fb02941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89636dea2df4a4fe33a5ad94af98883481b1fdd36072c5892693f37f0cf480b`

```dockerfile
```

-	Layers:
	-	`sha256:cab8631bde05092b66d6b3abe4ef84c057e659f3d9dce385324dcc35ea73e3d7`  
		Last Modified: Wed, 22 Apr 2026 01:16:28 GMT  
		Size: 2.1 MB (2114083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0169362fd89cf4efe3d83159d86153a7de24ea6aa0ab4c527ddc8899ee3a760c`  
		Last Modified: Wed, 22 Apr 2026 01:16:28 GMT  
		Size: 22.5 KB (22495 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:c4c0c7b3aea7a0945a5519676db6d7b9051dba29141d35ca05eb0aa712b8214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47187037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a094b09851e00df2ad02c4d84ffc796d82e8b96d7aec3625df34a144a8a8d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:22 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:16:22 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 07 Apr 2026 01:17:12 GMT
ENV HAPROXY_VERSION=3.3.6
# Tue, 07 Apr 2026 01:17:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Tue, 07 Apr 2026 01:17:12 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Tue, 07 Apr 2026 01:17:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 07 Apr 2026 01:17:12 GMT
STOPSIGNAL SIGUSR1
# Tue, 07 Apr 2026 01:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:17:12 GMT
USER haproxy
# Tue, 07 Apr 2026 01:17:12 GMT
WORKDIR /var/lib/haproxy
# Tue, 07 Apr 2026 01:17:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d7ba11a481c7e8417b1186bab54ae7bceb28e90f87c4b975bc5b1b29865f6`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 1.6 MB (1603358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27885a5bc92cae45e1297aa55b70f16e1bdbf82379498924135c57fda93e6c7e`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d595eb14b303c79ed681b7b7b0b21b51ba0885715f0c33358a2f10e52fc89246`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 14.3 MB (14290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525ba651b69ccbced7eba877ea423371242ae92b438f259c2244c4c744aa3b73`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a7b394f893799411dcc10ba8f3146967ebd3bcbcb6f12242985f62b86ba9894f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb69a88069d9fdf528bca963802442b86ca31a7ae6512d679407559bff2aacd`

```dockerfile
```

-	Layers:
	-	`sha256:e9c7acf4228276cbf1f3a59a1ccf38bc50817fc1c22a0f42dfaf4a444073fdc2`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 2.1 MB (2110979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874e9c7e2140460042d7d120a5e2fd2d9eccc24b1b03a908c8441f31e3e83779`  
		Last Modified: Tue, 07 Apr 2026 01:17:20 GMT  
		Size: 22.3 KB (22292 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ec7ae83a9f9f1296cf08bfda66cef4d07de52443729fed4dee4815e4320a7fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50467398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c1ea8f8e651ff95569f8d0d98f066d5159501b470b46469883c6f0bb31897d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:18:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:18:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ENV HAPROXY_VERSION=3.3.6
# Tue, 07 Apr 2026 01:20:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Tue, 07 Apr 2026 01:20:28 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Tue, 07 Apr 2026 01:20:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
STOPSIGNAL SIGUSR1
# Tue, 07 Apr 2026 01:20:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:20:28 GMT
USER haproxy
# Tue, 07 Apr 2026 01:20:28 GMT
WORKDIR /var/lib/haproxy
# Tue, 07 Apr 2026 01:20:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32904ae8fc2c23a770d7f1902b1cd135d3b2f31af0972d233885cc36f6267936`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 1.6 MB (1639112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006f77cf07422350f2e4ecb462d4dcc5ac80e6622e19d9562c351bc8fe21733a`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a045f5afe1f651e08244e72bd43020ca734c2cca5298878812e79e1fac4535b6`  
		Last Modified: Tue, 07 Apr 2026 01:20:50 GMT  
		Size: 15.2 MB (15233623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dbc506b0f7f340056d9fe124227009a3dd890dec47dc7851db81b62ff8a164`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:52ee213ed211e3fd6e02f37a5530ec4a3348b01edd5b17340adf414621186ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e252d61f899f188ff64ff1b33f9caeaf40b57d21468c027b362707ae25fc2514`

```dockerfile
```

-	Layers:
	-	`sha256:e2e9ccbb1b9228bfc87ed194dda9bef4e845a3d3a27c4bed168f27f4c88168db`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 2.1 MB (2117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:257c3a0da2b43814030039adb9e6a22698892c3ac6974890d3f84ff41da0682a`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:c66d1e6790b9e587a88097c385c0e6b9dfc7b50402bb50ae4db2cd7697217d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43792345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e334e51bbdfbd3466734d16159012f6f6dcbf329484cbc4efd844b7137cfbcb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:38:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:38:32 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 07 Apr 2026 03:10:24 GMT
ENV HAPROXY_VERSION=3.3.6
# Tue, 07 Apr 2026 03:10:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Tue, 07 Apr 2026 03:10:24 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Tue, 07 Apr 2026 03:10:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 07 Apr 2026 03:10:24 GMT
STOPSIGNAL SIGUSR1
# Tue, 07 Apr 2026 03:10:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:10:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:10:24 GMT
USER haproxy
# Tue, 07 Apr 2026 03:10:24 GMT
WORKDIR /var/lib/haproxy
# Tue, 07 Apr 2026 03:10:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607981e7ed06fad93d791ad253a598525a50953c77c4fa91bbe931fc007c2b96`  
		Last Modified: Tue, 07 Apr 2026 02:55:08 GMT  
		Size: 1.5 MB (1535466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f830de6efdf414ce66750ab155608fd1126ada0440ecb14570d62798f489f8ef`  
		Last Modified: Tue, 07 Apr 2026 02:55:07 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0280f736a9e433dbf4509da3087009f6353d2599be42aa61e77ae7c4eb2d9b1`  
		Last Modified: Tue, 07 Apr 2026 03:11:31 GMT  
		Size: 14.0 MB (13979454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc27d388a438aa9d78288470a4051eb4f8e9e0eb5b6cc37f3ec23ca19be5e9c`  
		Last Modified: Tue, 07 Apr 2026 03:11:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:ff7b668b7b3b051106e763d30b20d108fadc5045d09b481421ee0f3891dddc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971844f5a49f0290556fc0b0dd93205e806590ab06be85acedcb07f430d1ea52`

```dockerfile
```

-	Layers:
	-	`sha256:c20dab43918e34b564289c1a270a0964dc0ab585b0219aeadee75242d4331284`  
		Last Modified: Tue, 07 Apr 2026 03:11:30 GMT  
		Size: 2.1 MB (2107735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479b60d1f7dbf09d0848ba50922781f62d9f9492f379c94bef121d896615de04`  
		Last Modified: Tue, 07 Apr 2026 03:11:29 GMT  
		Size: 22.4 KB (22397 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:bdbddb87db061095618e6ffb58bddf9a97493f47a9e103b7b4a360513f66c71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46335305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b6381a4c04fa1fb437751398fa9284570561fc26ee78be5619da212bfc34e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:13 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:13 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:52 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:52 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:52 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:52 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:52 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eadd13bb01ab3a6fed22866c1c97a5abc38da434d91b6217dd98297720b3273`  
		Last Modified: Wed, 22 Apr 2026 01:17:06 GMT  
		Size: 1.6 MB (1599883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33729a351d90960a3d2fe1e7ad67c4896650b088738df67640231d15bc106c8b`  
		Last Modified: Wed, 22 Apr 2026 01:17:06 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eb69db1911e4be9eb1faaa763aa2daa5ef0709f5eaccfc4b14a0f76244cc6c`  
		Last Modified: Wed, 22 Apr 2026 01:17:06 GMT  
		Size: 14.9 MB (14893484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d177d06f71124f9f2df3b9e64f5a473a4f4cad89e9a0807d85c86d46bdf99`  
		Last Modified: Wed, 22 Apr 2026 01:17:05 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:9d69bdb8dbf76d26abed39c6a5227cbe9a1d46536850e3abfffa45815876b16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc56d4c41372499518834beb1de5d4e3706af568aa8a6bd05c5bd8f91e30415`

```dockerfile
```

-	Layers:
	-	`sha256:3d2d6eaa829bd215e6ccf7472c1302e5b0f001ffdcc889a739624415d53b1cd7`  
		Last Modified: Wed, 22 Apr 2026 01:17:06 GMT  
		Size: 2.1 MB (2115242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1822446aaadb8d2d07eaab7af3afdfe6dc960314dd715d463c6649fef98544`  
		Last Modified: Wed, 22 Apr 2026 01:17:06 GMT  
		Size: 22.3 KB (22337 bytes)  
		MIME: application/vnd.in-toto+json
