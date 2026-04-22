## `haproxy:latest`

```console
$ docker pull haproxy@sha256:e3794c185be0f5ac3180298e8416e9953cec9cb26f422f96d497e38a8a856ae0
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
$ docker pull haproxy@sha256:87f9fd211707a72da1b32d2c16fed64a5d37edbad83363cac1c7e8c1365292f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44191293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2af2eac694bdf173eec1e52b8610c50da9d2fc70f36cc1076ad92cb0812f6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:41 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:40 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:40 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:40 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:40 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:40 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b8f48e0720b43bfa28bb7e097794ebef0716ae6712f51795fe3e45c5081e2d`  
		Last Modified: Wed, 22 Apr 2026 01:16:48 GMT  
		Size: 1.5 MB (1535727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3124cf4179a08d94096dab8720f7a471773ebfefea56d1f10955707b5e223a6`  
		Last Modified: Wed, 22 Apr 2026 01:16:47 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561cce1de41520b5254d981161be68e38efb8b61b2d8f8174972eb7ac5588c97`  
		Last Modified: Wed, 22 Apr 2026 01:16:48 GMT  
		Size: 14.7 MB (14705750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965ec2465a63cecfd02293a2e01eee50faa2aea9ba89f175a8990b42c75d19e`  
		Last Modified: Wed, 22 Apr 2026 01:16:48 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:fbe87639d32155215fdcdad6ed38c0ec8cc8d338939448bef9dabef9b3a5a441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf10e8ecedbbe58ae5334f32202f0cc13e6150660a0d86055f48f67d3b218a9e`

```dockerfile
```

-	Layers:
	-	`sha256:254baa633db19c9542ed0bed66f19512563622b4a6c2b1f01ac981d0c881cebc`  
		Last Modified: Wed, 22 Apr 2026 01:16:48 GMT  
		Size: 2.1 MB (2116778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68baac95dfd583851ee6c8806181d8540bf17f76b48049346b5a1a0d1ce13cd`  
		Last Modified: Wed, 22 Apr 2026 01:16:47 GMT  
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
$ docker pull haproxy@sha256:337e1d576c543c1d70e845783c9bb89106b912a36ee598234138fa2b571cb81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47192019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f99b35032a0fceb1793547bb0b954de3a733cad29408dfc25f0765d0ade6666`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:16:11 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:16:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:16:11 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:16:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:16:11 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:16:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:11 GMT
USER haproxy
# Wed, 22 Apr 2026 01:16:11 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:16:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46706487ccf318410d3bbc56c553e6715d01c4c8262a35586298099431c85d51`  
		Last Modified: Wed, 22 Apr 2026 01:16:19 GMT  
		Size: 1.6 MB (1603290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15cd2d08b86a3e875456c83f7bdbb368ad0fc35d2ddc19b329bbf1196804fb8`  
		Last Modified: Wed, 22 Apr 2026 01:16:18 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c86be1cc0ff5ba0dacd51aea1e1746e09f82f17800f60e35ac3f9933a059bf5`  
		Last Modified: Wed, 22 Apr 2026 01:16:19 GMT  
		Size: 14.3 MB (14290762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5463f5bc880e43edce493e5193dc6c89f7bc5c411c3449e473bc48643b58f01`  
		Last Modified: Wed, 22 Apr 2026 01:16:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:772672dd032870ae0aefa772db1e858287f23f4df05ce9566a8004930a2aada6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074993fbc6a5f2fc8868efde604c432ff0f758a14b75cad784649d85dd19304a`

```dockerfile
```

-	Layers:
	-	`sha256:23536dc22822e46167d0164c0f397f09179f991735be56a0b9c8956f50cd4c16`  
		Last Modified: Wed, 22 Apr 2026 01:16:18 GMT  
		Size: 2.1 MB (2110979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d4f02aaa4b0664cb8dc009be9c976ae99eec75fdde3943192444e9eacf98e8`  
		Last Modified: Wed, 22 Apr 2026 01:16:18 GMT  
		Size: 22.3 KB (22291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e0729c03edc7bddb30e8204f31cf19bbe46b0fb69bd70579b0a72a9e974ca006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50472452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3ccfeb622852210352af9b8c8cf0b5eb19dca09eb5e99d1d8aabcbbbd2f120`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:46 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:17:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 01:19:29 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 01:19:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 01:19:29 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 01:19:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 01:19:29 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 01:19:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:19:30 GMT
USER haproxy
# Wed, 22 Apr 2026 01:19:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 01:19:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495aa1c13c8e8c3040d915f35a96a4407c3697667fa9b6e95fdf55995ae31666`  
		Last Modified: Wed, 22 Apr 2026 01:19:49 GMT  
		Size: 1.6 MB (1639122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f263bf3a91f543cf4b9c667cc3657f612e3b82a276249a39f092018d3970710`  
		Last Modified: Wed, 22 Apr 2026 01:19:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50aeedbdef260fb9d3a81dddd5989e8698d11e1d82d7cae9e0415386615ab77`  
		Last Modified: Wed, 22 Apr 2026 01:19:50 GMT  
		Size: 15.2 MB (15233658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6bd2fe1a32bd2fc99ec80275e519ffc78bda9a0f7cbfec633c1b1f1f4dbc23`  
		Last Modified: Wed, 22 Apr 2026 01:19:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:fb65e11ebae5bbe6bdee5abd77072f59ed017e4b3aceccb1882dc218a71d3bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675684a1cedc86becae9f0a5d80ba6395e3756e8bb7b48a1265a779296c82c2a`

```dockerfile
```

-	Layers:
	-	`sha256:f17650ee931b75955525e90dcd194dcc774b48b40312d5f23b9468f0f2fb1558`  
		Last Modified: Wed, 22 Apr 2026 01:19:49 GMT  
		Size: 2.1 MB (2117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9d33436d1515a2ee8895ee8ea33179d1a4a783f9c399ae469d4244202994f2`  
		Last Modified: Wed, 22 Apr 2026 01:19:49 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:b8a22b14ffb87b2e06d0fe5aacd707039142566a51e61915fcec5daaab2e95aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43788362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79354a57259fb3532f8e060cd2f8fe31bf1cbe5ed4ac1869422b9fe31d86525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:07:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:07:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 Apr 2026 06:39:52 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 22 Apr 2026 06:39:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 22 Apr 2026 06:39:52 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 22 Apr 2026 06:39:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 22 Apr 2026 06:39:52 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 Apr 2026 06:39:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 06:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 06:39:52 GMT
USER haproxy
# Wed, 22 Apr 2026 06:39:52 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 Apr 2026 06:39:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc623a92fa73e7fb55b6cbcec224c9a3d5617dafad79c6a3703ff556e2fea34`  
		Last Modified: Wed, 22 Apr 2026 06:24:22 GMT  
		Size: 1.5 MB (1535443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec766d6a121a8aa9a11c026443ab5b5998bfc0876dd46f9f7ad98a51d65938f6`  
		Last Modified: Wed, 22 Apr 2026 06:24:21 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08736aedbab0998afdfaec518fb691c12b576dec0344c1dddfe363f8d9836b01`  
		Last Modified: Wed, 22 Apr 2026 06:40:59 GMT  
		Size: 14.0 MB (13971082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2bbc31760b7b0372a6a44c854db9e856892bdf9379d20f9969fda21f5161fb`  
		Last Modified: Wed, 22 Apr 2026 06:40:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:33803d3bf5fee07a6980a682210587031683dc839f8d24e13d5371023a276da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04aaa3ef16da33a14dd0034b92e8a8cf5273e6b20ad0e9426379de9131fe42b`

```dockerfile
```

-	Layers:
	-	`sha256:fd018878a817b25604000f477766c60bb2ed2b9bfc720b637e4b266bc0926a38`  
		Last Modified: Wed, 22 Apr 2026 06:40:57 GMT  
		Size: 2.1 MB (2107735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58db1615e6225e431388cb5fcc107509adbb7f3ee70015373ddc3c0b122f5817`  
		Last Modified: Wed, 22 Apr 2026 06:40:57 GMT  
		Size: 22.4 KB (22398 bytes)  
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
