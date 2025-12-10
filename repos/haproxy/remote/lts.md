## `haproxy:lts`

```console
$ docker pull haproxy@sha256:7eb80a6c4555dd64fd5b01c078b33637b1af1871d636570624ef0b079857527e
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
$ docker pull haproxy@sha256:3838c604db462857ae19cbb5a7513f2bf07e4bb543a8d7b20a56cd2795b16348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42389951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a31d244c9623d4843424c0dc2950f97a0abc61d2730587fce54277220d50cc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:52 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:34:52 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:35:29 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:35:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:35:29 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:35:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:35:29 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:35:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:35:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:35:29 GMT
USER haproxy
# Mon, 08 Dec 2025 22:35:29 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:35:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d468aaff80c70263740183dda62a8d12da3042fd6da44b8dbf82223895b92ce2`  
		Last Modified: Mon, 08 Dec 2025 22:35:42 GMT  
		Size: 1.6 MB (1580867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6474f15f0dd6b946bcb5b4abe8cc351c6e3808570da80f64da392f0fa85a4d6`  
		Last Modified: Mon, 08 Dec 2025 22:35:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c1e5c786b2366b52fa94eb8bd4f06da3042a70816700c617447d09c761d4bc`  
		Last Modified: Mon, 08 Dec 2025 22:35:43 GMT  
		Size: 11.0 MB (11030953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd96f6ca1a093de96d60b75ade4e0fe34224f61f332b5aabcc427dfad9949d8`  
		Last Modified: Mon, 08 Dec 2025 22:35:42 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:da0b9bcee27e4cbce38b85f9eb56a4387704c626059c0e223ff0e295e5a4df72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f30909cee152b4a808eb7380ee86c98ec956d0f1d8631ec078a2325cb2392b`

```dockerfile
```

-	Layers:
	-	`sha256:f6b2eb7b321ef01e24532fe5d45c14ae6ff542f3e0de8b3f7082533069ba9d97`  
		Last Modified: Tue, 09 Dec 2025 01:58:56 GMT  
		Size: 2.1 MB (2113702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec11f75e065960f73ad811d61c1fa3f81660e33cf003c0083e1894f5648a0b66`  
		Last Modified: Tue, 09 Dec 2025 01:58:57 GMT  
		Size: 21.6 KB (21602 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:da6b7e6806de1638a99426845af5ba2269d830b432d1f3e1134bd51943bd15e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40588749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf2fc1fc737a66a9c2f447b938cbc6c85bca5a49258d98abcfaa94920eed982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:31:57 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:31:57 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:32:48 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:32:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:32:48 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:32:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:32:48 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:32:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:32:48 GMT
USER haproxy
# Mon, 08 Dec 2025 22:32:48 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:32:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6740601d1ee7e0d906090ad6146661b17535a567714f5d90861095af624fb090`  
		Last Modified: Mon, 08 Dec 2025 22:33:02 GMT  
		Size: 1.5 MB (1534761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62bb7a90a516f3251082cab0c50aa1aff6e93af00e111d016fc41015a14157f`  
		Last Modified: Mon, 08 Dec 2025 22:33:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402bf86c2dffeddf69586267d831d8d421d5afd91df6b930c6d4a63554926b44`  
		Last Modified: Mon, 08 Dec 2025 22:33:04 GMT  
		Size: 11.1 MB (11108163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bd1fe7cdee245005b3a19df8c3e02970427f5660e421abb84a9823061a0ff9`  
		Last Modified: Mon, 08 Dec 2025 22:33:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:95ee571131af6b968ca512ec142ce0901a22e59ac72b8da18ce4ca80cf442ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f02d8bbb61a3d0345ec4f3f591406c1677781f5065df1f98b45314153887bd8`

```dockerfile
```

-	Layers:
	-	`sha256:459af3e6b9d6206aa8ee4b23d0096c35a771402e5aa7c36f5e70fc01412dd0be`  
		Last Modified: Tue, 09 Dec 2025 01:59:01 GMT  
		Size: 2.1 MB (2116682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f65f7fdc21396f1cc8afcf36d87b3256bdc9fd172519ecd880cfe9173e1319`  
		Last Modified: Tue, 09 Dec 2025 01:59:02 GMT  
		Size: 21.7 KB (21727 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; arm64 variant v8

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:15ae483e2689ca1c2ffcd4c245117fa227ef02ba9d711fe61d06a06ce2897280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43639199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf77b68b58b805fc23c090760cada0c1d84c3cd17e6af64fe4696923967f225`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:25 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:33:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_VERSION=3.2.9
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.9.tar.gz
# Mon, 08 Dec 2025 22:34:12 GMT
ENV HAPROXY_SHA256=e660d141b29019f4d198785b0834cc3e9c96efceeb807c2fff2fc935bd3354c2
# Mon, 08 Dec 2025 22:34:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Dec 2025 22:34:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:34:12 GMT
USER haproxy
# Mon, 08 Dec 2025 22:34:12 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Dec 2025 22:34:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c70f7892d5cb3665c373d6e392c0d121c9f1fc8225f5977e9e2c8501c4e88c`  
		Last Modified: Mon, 08 Dec 2025 22:34:26 GMT  
		Size: 1.6 MB (1603042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d43f0d8bdbc53d7e01d78addd1a0772b5e472181560644814b2579416f536`  
		Last Modified: Mon, 08 Dec 2025 22:34:24 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee55e4ca3abcc1245885883b85a6610eb9455a11a3720c5e7e27bdf387d7b65`  
		Last Modified: Mon, 08 Dec 2025 22:34:26 GMT  
		Size: 10.7 MB (10741455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109c66f1ca236d434f086fdf5be52453052fe469da19680899750a1e6f3cc5a4`  
		Last Modified: Mon, 08 Dec 2025 22:34:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:8f5a36c1ebee952bca676c1b8dcf2e399d5e2dcb2c9ba12381b0e7a402fa7a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ef9f1862d0331e29372d1df247e678682911b167bac89102df6eb71e6054d`

```dockerfile
```

-	Layers:
	-	`sha256:279e73c60d51dc57d8b0fcacd02c4ef37db61155435fd569783d5aa5184ecb57`  
		Last Modified: Tue, 09 Dec 2025 01:59:15 GMT  
		Size: 2.1 MB (2110883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fb0bd4911ac921c89d3a41ce6011eb35941dd8981ca6586092868ae1a00519`  
		Last Modified: Tue, 09 Dec 2025 01:59:16 GMT  
		Size: 21.6 KB (21559 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; riscv64

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; s390x

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

### `haproxy:lts` - unknown; unknown

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
