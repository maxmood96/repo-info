## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:54f5b44588fb56823995510feb0773d24899f3995a4e9963b8b3a85506aab1b9
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

### `haproxy:lts-trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:f719f14db6b3b820c4f29c00773823459df1253ffa43523122de134ac3c9d697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6f12a9122ee67718f7cac6d054cb1cc029ab0e4e41aa88e0d58f918e0e9859`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 18 Dec 2025 22:19:00 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 18 Dec 2025 22:19:00 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 22:19:40 GMT
ENV HAPROXY_VERSION=3.2.10
# Thu, 18 Dec 2025 22:19:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Thu, 18 Dec 2025 22:19:40 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Thu, 18 Dec 2025 22:19:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 22:19:40 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 22:19:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 22:19:40 GMT
USER haproxy
# Thu, 18 Dec 2025 22:19:40 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 22:19:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6203240651e303f56e71bf5ecea184c8db0297c5a9266713d6bf39eb54114e`  
		Last Modified: Thu, 18 Dec 2025 22:19:58 GMT  
		Size: 1.6 MB (1580910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51eb0937284e6e107f680bdd35cf6cf2c7601d6ff0066b4dd6e4ceba2df44`  
		Last Modified: Thu, 18 Dec 2025 22:19:53 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4857e589cf7c26fe4600516079fe7c893a1599f4a45a9658ceffd60aad6834d5`  
		Last Modified: Thu, 18 Dec 2025 22:19:54 GMT  
		Size: 11.0 MB (11031468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e25c081bb9a5086895bb571a4b92018bfe034437f8ceebefca1d5c7381eba4`  
		Last Modified: Thu, 18 Dec 2025 22:19:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:aa8b1e579d4a6ca4f77e0efd6ee5b582b69d65c8390eb1fd96ed12740dcc74a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dcdaf77a81100560230d7c87d164f3f76a0567151bcac7e22ee67a4bfc2556`

```dockerfile
```

-	Layers:
	-	`sha256:34f0699cc87ed39468a75de3ff727704539daa81e424428b09a7fbb38d9072bd`  
		Last Modified: Thu, 18 Dec 2025 22:56:36 GMT  
		Size: 2.1 MB (2113708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00815abaf3fb6954c999a3f724568ea863137bbd58f1317ef9c82b1324e77cd8`  
		Last Modified: Thu, 18 Dec 2025 22:56:37 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:a794dd7ba4b13136d46da923bf3acae764d2c2b90799281bfee221a544b5c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40592195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7929dc29e612fe5627c17aa13bd9fa7cda746c06f372bd8e6e96aa800bf7c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Thu, 18 Dec 2025 22:30:02 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 18 Dec 2025 22:30:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 22:30:52 GMT
ENV HAPROXY_VERSION=3.2.10
# Thu, 18 Dec 2025 22:30:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Thu, 18 Dec 2025 22:30:52 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Thu, 18 Dec 2025 22:30:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 22:30:52 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 22:30:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:30:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 22:30:52 GMT
USER haproxy
# Thu, 18 Dec 2025 22:30:52 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 22:30:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e59c5c7ad40287d8e93f52f085e614be984d2176ff423904031812356d378c3`  
		Last Modified: Thu, 18 Dec 2025 22:31:05 GMT  
		Size: 1.5 MB (1534772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c31e9c30ae5573545bb1a312a18a8ce0c1503c050e9d4f4d831d7cfd86963d`  
		Last Modified: Thu, 18 Dec 2025 22:31:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085a5bf56694dc581d998b6a68a426d912936eacd5fa9570819ef99d2bec8e36`  
		Last Modified: Thu, 18 Dec 2025 22:31:05 GMT  
		Size: 11.1 MB (11111594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4314f8040458400518e90887b5b0b4cd7a9b32b75ae29ec52334fe0bea761e1c`  
		Last Modified: Thu, 18 Dec 2025 22:31:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b98153e430d2a082728d4b14f3c04cf49114e954782de30e46b354b4ec42467a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47e3cdc15111707f5a1ef7fb1b14e7b3f6640ce45047ca8c6e17f94b71119d2`

```dockerfile
```

-	Layers:
	-	`sha256:9eee7ab7ab2946f126a5b5c3634d74035daa56803cd7585f1328030fe773d1f1`  
		Last Modified: Thu, 18 Dec 2025 22:56:16 GMT  
		Size: 2.1 MB (2116688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf16affe4d079a6c7f9c9de0b482d0cb8faecb6eea1863a8295224af60f3452b`  
		Last Modified: Thu, 18 Dec 2025 22:56:17 GMT  
		Size: 21.7 KB (21733 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5bcee0d60c6a1251fd6ea99d9b1908e6fe4786e34c630408f76c2e272492154b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38600142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d04e6c320d224eadf5184be5718bc3125dae464d103887ea8577eb161421fe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:34:04 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:34:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:34:04 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:34:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:34:04 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:34:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:34:04 GMT
USER haproxy
# Mon, 08 Dec 2025 22:34:04 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:34:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2ded4dffe2687dbfe4e6ad75d3c682649cc0953e611c27f488c518cf00be3f`  
		Last Modified: Mon, 08 Dec 2025 22:34:20 GMT  
		Size: 1.5 MB (1488827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db714c343c5a504e4add45a2501f4b8e37bc395481f7de84a216bb29a70bec3`  
		Last Modified: Mon, 08 Dec 2025 22:34:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c14bf14a70744daefe32fb74e4b35b338f7e00c3b876daf71d7e518b650902`  
		Last Modified: Mon, 08 Dec 2025 22:34:20 GMT  
		Size: 10.9 MB (10899664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db443a07c2435948fb752651778c36e1f2caa44b058ec46471ca2098643fb582`  
		Last Modified: Mon, 08 Dec 2025 22:34:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:7378ce7d6702ef2ae31376557ad243ba9c1dd0525641d0ecdb90bf9e6c0e2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd74879fb029a4523a8ed3dae8136db6c62b8c42b9c86ef68a446e6db3de2d4`

```dockerfile
```

-	Layers:
	-	`sha256:5bed92dc23d294ccd684c7d31d330ac87085575128ac98ac0cd66644568e41a1`  
		Last Modified: Tue, 09 Dec 2025 01:59:06 GMT  
		Size: 2.1 MB (2115125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76598125b32c9bf4f9c7f1bced510cf54f73bce1e486a5380b53eb59b2f5a75e`  
		Last Modified: Tue, 09 Dec 2025 01:59:06 GMT  
		Size: 21.7 KB (21726 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:abf985c7f03a4f2bf50a2f886cd1fe73b7835f64ca3ef77eb0d29764368a206b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42664909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af63580bc095e7189b74814f32a9629e6d07d453ec25f442c9c9f09536d06d18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:33:55 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:33:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:33:55 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:33:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:33:55 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:33:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:55 GMT
USER haproxy
# Mon, 08 Dec 2025 22:33:55 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:33:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce90bbb3dd7df4b5e976471b87cb8d226c679eb76b33f77984ef05b290a13b9d`  
		Last Modified: Mon, 08 Dec 2025 22:34:08 GMT  
		Size: 1.6 MB (1563646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abb51f56186f0beb7bca66140e9a1444362f79b2fc5a194b85aad200c59d3c5`  
		Last Modified: Mon, 08 Dec 2025 22:34:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c19d5d96564af6fa0657eace78c3bedd08782e89f2145c7d74ab4e8be05cb17`  
		Last Modified: Mon, 08 Dec 2025 22:34:14 GMT  
		Size: 11.0 MB (10960997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7967f1b36a09ba49e23686769157d93eedebb0bbe8a2c1d1ada382d1b021bea7`  
		Last Modified: Mon, 08 Dec 2025 22:34:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:21d6c262a9e555c96ef141dbf2e46caab0612a2f0cd005375adf6beb83bfd16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfe2e71cb464edf06e97a168f8dc7565389c2081fe137e3f6f128451a5eaf26`

```dockerfile
```

-	Layers:
	-	`sha256:7416ccd548f12be3364d593c6c27d83f4753893206d8b1200cd96a0af714914e`  
		Last Modified: Tue, 09 Dec 2025 01:59:10 GMT  
		Size: 2.1 MB (2113987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d277a4f0f22c9d5962906b99e3c1837a95e8e54ea4c79dc8540cbdfda8f54f75`  
		Last Modified: Tue, 09 Dec 2025 01:59:11 GMT  
		Size: 21.8 KB (21763 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:9742e983bc1263f2a0233361c088c55ec9a5758b5800d8d1ce15cfee00af20c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43641217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0468717aeb1bb945224ee1ed73a43d79222dce462b8a85b7249df98dd0557853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Thu, 18 Dec 2025 22:21:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 18 Dec 2025 22:21:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_VERSION=3.2.10
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Thu, 18 Dec 2025 22:22:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 22:22:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 22:22:25 GMT
USER haproxy
# Thu, 18 Dec 2025 22:22:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 22:22:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc574a74b73ba1971b73aaa4f4641968a284b411f108b53a5492b3ee7e7dd4a7`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 1.6 MB (1603066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610105c15b35d2ff6b946cc8599bb940c72a03da5d2febb26f9280c63e8743a`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813e44e556842af058f5b6bdd7c3772fa65d69a0c1e1bb953a8f87ec5c077043`  
		Last Modified: Thu, 18 Dec 2025 22:22:40 GMT  
		Size: 10.7 MB (10743441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe1c439d65f40eaada0bef870b9fd32d5333fd0bce1c5b6b116b710a11d1e3`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d511fdb8ac816a6e9c26bb56b0f7d761f77ede5fcb2d4b88911da41b637fe910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5f7eee5a548f7da9b329f59ece2071a5f11c5f0631eeb83d348f88e59923fb`

```dockerfile
```

-	Layers:
	-	`sha256:23ed9a054bcf1549443225ee5fa5badc52ee3f86e5ee9ca600d1955cb76d09a2`  
		Last Modified: Thu, 18 Dec 2025 22:57:06 GMT  
		Size: 2.1 MB (2110889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c332b5b464ca4d2a96ce001a321e170a768c557dd6394e1923bdcdd9a3e762bb`  
		Last Modified: Thu, 18 Dec 2025 22:57:07 GMT  
		Size: 21.6 KB (21565 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:fe6a2c3e0255452c2b87ca0c4e32d73cd82b5d661cecb9c732456561de9ee297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46914285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bdc727d162290efb9d809058684fc9937dde902d367400e9aad0672a6a130b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 09 Dec 2025 00:21:11 GMT
ENV HAPROXY_VERSION=3.2.9
# Tue, 09 Dec 2025 00:21:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Tue, 09 Dec 2025 00:21:11 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Tue, 09 Dec 2025 00:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 09 Dec 2025 00:21:11 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Dec 2025 00:21:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:21:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:12 GMT
USER haproxy
# Tue, 09 Dec 2025 00:21:12 GMT
WORKDIR /var/lib/haproxy
# Tue, 09 Dec 2025 00:21:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185480bdc18ea021a0fc7f5119aae641bd26bbb0177eb9faf2ff183fe47f022`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.6 MB (1638932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c1fe78578524cbf853cfaafa2576e0205722868fb7fcd5b0011a9d050049d`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88619a7bb9087714eec44f1b6504e43304fc6ff976cd0f7e5b8a44872ac7aee`  
		Last Modified: Tue, 09 Dec 2025 00:21:49 GMT  
		Size: 11.7 MB (11676822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbed3530991b04b27de27b074740ce4664d4e2ed2062d6fcadff2c652a08dc1`  
		Last Modified: Tue, 09 Dec 2025 00:21:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2e9a6a98cf7fd9d846eddfe51a2b01f42f3d8b1dc00c08430fc45365db24ad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500f859c09dd3e58019ba58d38717c7082932f058e3495a37021e57cfd89b76d`

```dockerfile
```

-	Layers:
	-	`sha256:5bce0ca45623acc1a329d7c665feb26ead3b91a026c18de1a6b1277d7cc8d489`  
		Last Modified: Tue, 09 Dec 2025 04:57:23 GMT  
		Size: 2.1 MB (2117248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d13eb2160ae5a86ca233c857e64b34cb183a91583719c4af4460327913c840`  
		Last Modified: Tue, 09 Dec 2025 04:57:24 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:789ff043fdc3970e1d426b6365f46b444f0982c621002a2257f5459863c5d042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40485508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b10ea55949b4530e01d7456be610512c892b69cb77aab2ddc6bbb681a180c58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:15:22 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:15:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 09 Dec 2025 03:56:52 GMT
ENV HAPROXY_VERSION=3.2.9
# Tue, 09 Dec 2025 03:56:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Tue, 09 Dec 2025 03:56:52 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Tue, 09 Dec 2025 03:56:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 09 Dec 2025 03:56:52 GMT
STOPSIGNAL SIGUSR1
# Tue, 09 Dec 2025 03:56:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 03:56:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 03:56:52 GMT
USER haproxy
# Tue, 09 Dec 2025 03:56:53 GMT
WORKDIR /var/lib/haproxy
# Tue, 09 Dec 2025 03:56:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764214954a48097c0e9e75920ec71940c64da22d529cf119465be01a382f7bf`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.5 MB (1535074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8e3b90d2e358dca114fe7f69a507e4f358fbe2966b2f6df9510975fe1daec3`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220c88484611c0551954e08073992ac751108e0e52edcef8e7a2320b7c773cb`  
		Last Modified: Tue, 09 Dec 2025 03:58:01 GMT  
		Size: 10.7 MB (10675641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5d98c8154fd9999e7afa4c04b6e70f8ecbaf91e411eb1680a531c3ab8a0950`  
		Last Modified: Tue, 09 Dec 2025 03:58:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a09efe16e194f7981ba4c3c3d482ca71fb677625ad3eb99b1c74aff19ad9ad8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17840d61e05ea3ad2273330a3c43d6bc9b51577a21785b3c599802f1bbc9cf06`

```dockerfile
```

-	Layers:
	-	`sha256:30465a8d5998dde7c71266c2956549ade7c514a3835fba8f8c283850460f258a`  
		Last Modified: Tue, 09 Dec 2025 04:57:28 GMT  
		Size: 2.1 MB (2107639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f3f620960770759e267cf490cd2de86293e85566bf19a5c104687a33cc788e`  
		Last Modified: Tue, 09 Dec 2025 04:57:29 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:8cb944c19cc5f4cfa58664714b364d43aa0bb02198d3e959dd3675452748d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42758720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2253fcbd7d19171bc425a0ea6319882aa89b7bf9b9b0ce7f2c7a3ec770d0a34c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:29:46 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:29:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:30:49 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:30:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:30:49 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:30:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:30:49 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:30:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:30:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:30:49 GMT
USER haproxy
# Mon, 08 Dec 2025 22:30:49 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:30:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3c68105d562e6e1e2201401f6f7ba3d0d73c730d4cd3cd1fff86f0138002f7`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 1.6 MB (1599483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0052d8eeab3ea5047d4a29c92e67ddb241a0670e49d355f08539023ddd65b`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4fbb2a57a425bc052b5139984e5b8821acf6c49641381652eb7051bdfb9c7`  
		Last Modified: Mon, 08 Dec 2025 22:31:10 GMT  
		Size: 11.3 MB (11323198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97f5081bc46012a06472678413193b0b41df6868f20d3d9af4b023584a2071`  
		Last Modified: Mon, 08 Dec 2025 22:31:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a8684ea7bc84a56a027620a2681d8161aef547adfa6bcd7fe9b0e8641c3a3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb032a1c3e5d0302c361b0452781283759077eef26854e988aba3407f15a721`

```dockerfile
```

-	Layers:
	-	`sha256:2dceb46c945514fbb1919f4463f875ed2c58730d946517e3bef9406f39f957bc`  
		Last Modified: Tue, 09 Dec 2025 01:59:26 GMT  
		Size: 2.1 MB (2115146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d0375676dfa78d41a6a71a2ade4ec9e1508aa827d0fe0342a7e57dea732e21`  
		Last Modified: Tue, 09 Dec 2025 01:59:26 GMT  
		Size: 21.6 KB (21605 bytes)  
		MIME: application/vnd.in-toto+json
