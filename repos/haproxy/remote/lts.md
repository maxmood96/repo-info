## `haproxy:lts`

```console
$ docker pull haproxy@sha256:984a7e9d3c4c5f5c72af065ec0d702cf7763e3015901c9d7e1e0761649fb358c
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:b8afeba530a0e53e7d84e09caad7b56313748440e44d0085e5f87c94b23fab5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44532440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab750fcea072ae210c54024a60a6c0380dd3f4c41dc71d2cc4c40265a77453ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:48:27 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:48:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:49:12 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:49:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:49:12 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:49:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:49:12 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:49:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:49:12 GMT
USER haproxy
# Mon, 11 May 2026 23:49:12 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:49:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0c8aed3ba05cf511146a11a6474890bd4f412dbc1464c676935ad61bbcde2`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 1.6 MB (1581118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de7daff94a4f13a43501a8e18f82eb3f652f00c3a7d079ce7bc44d3bfa42e`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036df420f5fdeb7eb873315c7c1b913a82024c8a6ec8e39cc5e768011ec5bd41`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 13.2 MB (13169451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c72e280bd6407bd9d4491dbb5cd273430c5c9f0afe62142db2cdd30484aedf8`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:f260c095d85eb504e1416f92bcc6015c283352a42f131423d5353b606598e414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40464e0d8a398071cd5d21ee1d4e696e0673dfa72875e3b06a194b7eb03b14e2`

```dockerfile
```

-	Layers:
	-	`sha256:4473500ae02dd5f9e69a168e75ea0b07a864b2245cff83772e91307b83ed1d97`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 2.1 MB (2113806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d3043c05e721befe88564780cecebb46359c2cdc0289990ff0014f28f01c3c`  
		Last Modified: Mon, 11 May 2026 23:49:20 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:31e71b7a80090c8d6c639b18f6cfb043d0083b393d9867f516a2126dcd0f1d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42794933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bed39d19766785d3f8ad2566d34f0ebfc66b79931fcb9c6355fc59d0cf23265`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:49:14 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:49:14 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:50:08 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:50:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:50:08 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:50:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:50:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:50:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:50:08 GMT
USER haproxy
# Mon, 11 May 2026 23:50:08 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:50:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e808b0e66120e3d07f10e05324b9ca99847a3453d43c735c13e33de705800d9`  
		Last Modified: Mon, 11 May 2026 23:50:16 GMT  
		Size: 1.5 MB (1535732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b800750dd63d518c846283f5b01b2fb04265cbdd65e90445e405d4237ffdc59b`  
		Last Modified: Mon, 11 May 2026 23:50:05 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999904696b115788a197dd434d9ab2935e936958e632651ca9ecdd5974ca2d65`  
		Last Modified: Mon, 11 May 2026 23:50:16 GMT  
		Size: 13.3 MB (13309356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6c3f4755a7ae3aa3d049a2056799e1182dcdfc79f451fc295a31e893ec19c7`  
		Last Modified: Mon, 11 May 2026 23:50:16 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9911852678a93bec39d5562a008362fe8f17bda72512c07b60b026391a4341b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2977220763e3a4b674adb9482df44907b8cb65d4706b1c4a1b7d1d7f4cc3b032`

```dockerfile
```

-	Layers:
	-	`sha256:6ace0a14dfa87efb13de886d570f31dab8c1b5131b2fdc0a4d1d41b1cb575f8c`  
		Last Modified: Mon, 11 May 2026 23:50:16 GMT  
		Size: 2.1 MB (2116786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8fc5a4288405576bc785078d39a3de423be35d0454fb208c53ecf30a1d62af`  
		Last Modified: Mon, 11 May 2026 23:50:15 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f22796a6b039783a7c23025e561b087a994b3d1bf0545617e1e1fd493b626265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40774230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fa8b97cf9f10a0ec88a4dd5462e69701da9dcab98372970b2db87a186abe58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:50:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:50:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:51:07 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:51:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:51:07 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:51:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:51:07 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:51:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:51:07 GMT
USER haproxy
# Mon, 11 May 2026 23:51:07 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:51:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0a5115a6abf40cac2aa91e75348d54df30fac06c7bf0230ed0568298fd7130`  
		Last Modified: Mon, 11 May 2026 23:51:15 GMT  
		Size: 1.5 MB (1489566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca01003a9896048ae8423c8b4bd790e2e0c8ae42aca38847486cc97b064e5f`  
		Last Modified: Mon, 11 May 2026 23:51:14 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4293e912e77065ddc1f72fbccf27f20ce0d918f4c62f8dfb1e04637d6dbea17`  
		Last Modified: Mon, 11 May 2026 23:51:15 GMT  
		Size: 13.1 MB (13068106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a76de3abfcad191dfc93134319fc0f1f45935c4065c33c67ae22030c864bd7`  
		Last Modified: Mon, 11 May 2026 23:51:15 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:062e140c2dd06cb7b532ac8f928f0cead5bfb4d07fdc3661e7cc071c814d88c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bb64e6e995c6462fdd123859fc64e1964b7d92491d929006e3a95ee69b0b4`

```dockerfile
```

-	Layers:
	-	`sha256:762a5bf4c03572dca2695c1522dbfbdc09bf3ff7fb0d450ff530261ef7211526`  
		Last Modified: Mon, 11 May 2026 23:51:15 GMT  
		Size: 2.1 MB (2115229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a00aab2cb0b5cb8d3af237a9a58c68a08f39f89ae74c9dd3b766f47a029e48`  
		Last Modified: Mon, 11 May 2026 23:51:14 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ae91cac090e1b9c52b1b21c2d561c0ff12cad960818fa106faae4cbf8f7bb637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44782683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35de9598bdd15023b946ca0a170bf569902c9d217ac7c2dd5776f04b44b4484`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:48:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:48:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:49:27 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:49:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:49:27 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:49:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:49:27 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:49:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:49:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:49:27 GMT
USER haproxy
# Mon, 11 May 2026 23:49:27 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:49:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15b47322fc8607754f127bbd54857e77590a7c79c0745a3a1749745a4ca4323`  
		Last Modified: Mon, 11 May 2026 23:49:35 GMT  
		Size: 1.6 MB (1563714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35744dea1ba990f16222afdbe4f3481c72d4de1d4dfddae4f873492f47a86f3`  
		Last Modified: Mon, 11 May 2026 23:49:35 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5743f7cf347aa7389e0d2802872935f67f0ec82f67d8d69aa1aa3a466f6cda85`  
		Last Modified: Mon, 11 May 2026 23:49:36 GMT  
		Size: 13.1 MB (13073680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbec78cbfa8e04f8b0ee08484c0ee4f222c70555f0a17baa136a0eae351d847f`  
		Last Modified: Mon, 11 May 2026 23:49:35 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:fedc0ba72ddcde3fe03484a67de383aef2119125768e3464c3f26e889f1748b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a8ee7ac6823c0070656e540a6a9e1a5d592f54a98cea69bc9deb794a5c6356`

```dockerfile
```

-	Layers:
	-	`sha256:b2614bce4950f17957aed1c8676d99dfa50dc07e915a89be1ddcf547e259860b`  
		Last Modified: Mon, 11 May 2026 23:49:35 GMT  
		Size: 2.1 MB (2114091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2869e554df54a4e7311488cf122720661f689a39a2282307203d3eac439b44`  
		Last Modified: Mon, 11 May 2026 23:49:35 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:02d04f00699b7ebe49bab3ac82ea6a7870f71cb4c36b8a3a6ff4c6506821911b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45761490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006c590bea577440554c1b8fea5b627e0d9aed43b30da2545bc310f3cf04ce08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:48:47 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:48:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:49:34 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:49:34 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:49:34 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:49:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:49:34 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:49:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:49:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:49:34 GMT
USER haproxy
# Mon, 11 May 2026 23:49:34 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:49:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e1229022ce8cb38c002ee78b0ba19958be37c54b75bd6bd84bee2bd7fbd478`  
		Last Modified: Mon, 11 May 2026 23:49:41 GMT  
		Size: 1.6 MB (1603397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742cd90e5d0aa29b7fe3e3fa3fafe7c60e769fa5440e7efb8b443c454756e9f0`  
		Last Modified: Mon, 11 May 2026 23:49:41 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8644b95ab945fcab3c88ba851009415f310c3aeea7a1c5848ce8a700308bd92b`  
		Last Modified: Mon, 11 May 2026 23:49:42 GMT  
		Size: 12.9 MB (12860047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be679a96a0d54be21bde070366284d862bc62588ea1ec8531306fd6f7219d5d9`  
		Last Modified: Mon, 11 May 2026 23:49:41 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:1f189186d7696486cf97a2e6e0e99fbc29bc8a3695a8f8a09b7519b69aa9ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689b4275d0085f7928439183ddae024573f534ec0054d8916deaf28840a698e5`

```dockerfile
```

-	Layers:
	-	`sha256:fd6ed6c79da2d945dfc9c65498ba66de91e1483b211c9713a69b3802291f6f97`  
		Last Modified: Mon, 11 May 2026 23:49:41 GMT  
		Size: 2.1 MB (2110987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f48619510282efc4c817110a7f89a00bdf18f9229ee9d97ee29947368cda044`  
		Last Modified: Mon, 11 May 2026 23:49:41 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:edf58d4a1ed1fe6e232f21d98925affed93f75dd361c60235a06472d9bc7bf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49092707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686d29ab8002d1be9562af4a3b0e1ef9134d5e7531ef7060afbac04ef0df04f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 00:20:30 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:20:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 12 May 2026 00:22:57 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 12 May 2026 00:22:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 12 May 2026 00:22:57 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 12 May 2026 00:22:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 12 May 2026 00:22:57 GMT
STOPSIGNAL SIGUSR1
# Tue, 12 May 2026 00:22:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 00:22:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 00:22:58 GMT
USER haproxy
# Tue, 12 May 2026 00:22:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 12 May 2026 00:22:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b9ac38ddd9b997f362adef6cd05d077f03259b3f6083a3bfb4095da08e9bc`  
		Last Modified: Tue, 12 May 2026 00:21:52 GMT  
		Size: 1.6 MB (1639114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf2997fe19a81d470a2457e4b1f5d19d381e1a120e12220e9caaebe89d18f7a`  
		Last Modified: Tue, 12 May 2026 00:21:52 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f67666886520c5b36c513da8859758cd068c482a957ebd321b8c77189f09b`  
		Last Modified: Tue, 12 May 2026 00:23:14 GMT  
		Size: 13.9 MB (13853858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf35d1110164947490db85e734524f75c5c96addc69e5a8678b1dacab3f735cf`  
		Last Modified: Tue, 12 May 2026 00:23:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:94aee13444fa51d9d35a3ce084bbd7ce8c62055e8f3fee9c4a187314424c1126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542e53fcfe641148c92e9d291c37ec410f5bd1b0aa570cf65ebe4a2473fb9424`

```dockerfile
```

-	Layers:
	-	`sha256:a6e24afcd1fe86997af2da448e46a9f1717689e90662ffb4375faaba4ab610d7`  
		Last Modified: Tue, 12 May 2026 00:23:14 GMT  
		Size: 2.1 MB (2117352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8178cc989d2d4889fba0bebe36706e21915e0fc9e72cd62c98b6f9db49337606`  
		Last Modified: Tue, 12 May 2026 00:23:14 GMT  
		Size: 22.4 KB (22409 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:1901996df589fa3fb84210b309e247443fee4b2de9528ae94dd58de91c853450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42585331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8d3d5a26fbf90070ab95d40f5e307576703066f2852ca5ac3d404cd5b64d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 14:01:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 14:01:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 May 2026 10:37:09 GMT
ENV HAPROXY_VERSION=3.2.19
# Wed, 13 May 2026 10:37:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Wed, 13 May 2026 10:37:09 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Wed, 13 May 2026 10:37:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 May 2026 10:37:09 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 May 2026 10:37:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 10:37:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 10:37:09 GMT
USER haproxy
# Wed, 13 May 2026 10:37:09 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 May 2026 10:37:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83a54c5efc36f3f9f88a6d2dcee7620466feec5bfdaede8bfc6bb7d9926189`  
		Last Modified: Sat, 09 May 2026 14:18:33 GMT  
		Size: 1.5 MB (1535425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40aab834e7d7ef2a4744f04d82c68a628a97d62496c8cdc8af8a35f0e113a1d`  
		Last Modified: Sat, 09 May 2026 14:18:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300e3fc9fd1b16e250f575e4e52adb7017eba6c7f182bc9f79aa3bf5ebfe6a5e`  
		Last Modified: Wed, 13 May 2026 10:38:14 GMT  
		Size: 12.8 MB (12768030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3281711113124bd0f76c4d46fe736e45c5f836e51b1dfbaba0905986a05231`  
		Last Modified: Wed, 13 May 2026 10:38:11 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:6262cbe576dd93d3fefb463c031c0abedeb3f78f44ccb28ee4fa931752847187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1779a65cbd016a686ab7302cb6ba5b7b5e80734a2d683e78c07f02f73c15eae`

```dockerfile
```

-	Layers:
	-	`sha256:61e2f2d7a4a98c0b1bf679fe66551c4a1a3b9c27698ca660b09b832b37ae1093`  
		Last Modified: Wed, 13 May 2026 10:38:12 GMT  
		Size: 2.1 MB (2107743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5021d6abb0251a9c891e3b70a38299b2ae7f544d502bc8d254103e2a6e9a537`  
		Last Modified: Wed, 13 May 2026 10:38:11 GMT  
		Size: 22.4 KB (22408 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:e716577127efa41a71ba8105ba8007f9cb790b47ff0b73527925b90ef9aa236c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44909521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173830fbfdaedf30f2714c252429a133e858eb721aba098ec79b9454eb991a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 23:47:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:47:53 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 11 May 2026 23:49:08 GMT
ENV HAPROXY_VERSION=3.2.19
# Mon, 11 May 2026 23:49:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Mon, 11 May 2026 23:49:08 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Mon, 11 May 2026 23:49:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 11 May 2026 23:49:08 GMT
STOPSIGNAL SIGUSR1
# Mon, 11 May 2026 23:49:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:49:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:49:08 GMT
USER haproxy
# Mon, 11 May 2026 23:49:08 GMT
WORKDIR /var/lib/haproxy
# Mon, 11 May 2026 23:49:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd3f1367f2bb2d19e6228dbe7ef9513a91dce48219e0a53565dbb0158fd4e7f`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 1.6 MB (1599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace6207ccb27b4343692e0892e3ce0b1765287b0cdd56f441e2918a4daecdf3`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f11d9e5ed90689f9f0eb46741553b8a685c80a5fbd89762a4cd03398f6291ef`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 13.5 MB (13467657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b3707c466b91b5f6e7f56af79a5e94d8fdfeb8d84d0cb0925f2779c363a5a`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:792123d661f7fb9e93aed2e4de811f5ad130c31f6b90e61edecae52b982d5449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a517e54b20e18e90aa548a95c6567ee2c9056ebcfc97f8e5ff686c81805321`

```dockerfile
```

-	Layers:
	-	`sha256:3a0a54497f76df4071df2016ccde6b4d691e4b7b494f4a4c2d3391b1c18200fe`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 2.1 MB (2115250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db76f9bec38797223ec9abc329e65439cb2143ee7ed820a5fd6d821d8788fc7`  
		Last Modified: Mon, 11 May 2026 23:49:19 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
