## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:93c9b04bf974ebefb5ccecae05af3c224a229c07168fcaa2d8a3602bafd32911
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
$ docker pull haproxy@sha256:0b57196505f061e567af04cd081b403179e4162fd71498e992091b3c51807403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44490983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82890af16ce407d85f50ce39edf68bba734db1c46b09f05337600896256c2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:37:11 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:37:11 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:37:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:56 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:56 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890165d2bb7b27065d70bf0e07a83bfe76c94b520de4112e91133b58182291aa`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 1.6 MB (1580908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2f1a8e88c2f5768f6824d1d0747af40521736d06e03a9f818d7f3f214f2883`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee8cba91ff581d10b321a3b5f77a415f12a3d804bf2ed575d4fbcdb86d96cb2`  
		Last Modified: Thu, 19 Feb 2026 19:38:05 GMT  
		Size: 13.1 MB (13129836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db31c7759c0f6f33b1f39c9868c779f9dcd7c2cd135756807dc3e12250a58c17`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0e33b0448b195974bb0a37924e8ca0b2560936bcb9c9d821e6fd7d88357bda07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da382f7f0e4d7857317588b130e09a168362b0baa01999da114a62898550bdde`

```dockerfile
```

-	Layers:
	-	`sha256:cd6ca5ffffdc83d2ccd261b21ff1c80e1fc58f3aa2409109c7d022d194bce414`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40f6fdfd489ac3b4d52967f2ed78bca41cebcf2b8275fe491fd3d249bd1caae`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:5a6557fcb4298b98d3d7016d8608ecbf41874819d685f1d7cb3111ea9d3e7c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42757930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84dbe4ccf90b2a3dd97554a6fc220b9ef838fa05fe41206f75c0bd73987987b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:36:02 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:36:02 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:01 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:01 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817753681725b5233ef064b907c687020124e6df0f9aa993397fb263e9fed5e5`  
		Last Modified: Thu, 19 Feb 2026 19:37:09 GMT  
		Size: 1.5 MB (1534903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4931c2f00b855a5fa3271e99e67403308584b821b556dec6be784ac43057f4b3`  
		Last Modified: Thu, 19 Feb 2026 19:37:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b0e5611874860a88d3b08c21e350265caf21aac8b5434e60fcd7b2e632f348`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 13.3 MB (13273828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3474a6e76dd49b29037a695627a526bee713c29f3222957dfa8b34baffb6a`  
		Last Modified: Thu, 19 Feb 2026 19:37:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:99ffb6ef5bd8422dc8923a8a4826de021ec48284138f1a4ccc94875504416c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0c09519a99bf0ebce2bd4dc9013c201eb68c0dfaa89a381e721e717df252b8`

```dockerfile
```

-	Layers:
	-	`sha256:fbfc2d677a49213abf9ca109aa23bc1d98d5513e75aefa686600a2485c84eaab`  
		Last Modified: Thu, 19 Feb 2026 19:37:09 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807bc75498b0d24bf08530623a01d7e89c0be6ba5ecefe113867db28958f1e93`  
		Last Modified: Thu, 19 Feb 2026 19:37:09 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:cac41b29e38ce6ec8b548b8b9daf96c6ba33c2c8443423f77ca6397fa549023d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40729464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda617623f67b3e87be90a3bf1fe68ed99bc6b708696d379c317e44653540973`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:38:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:38:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:39:07 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:39:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:39:07 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:39:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:39:07 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:39:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:39:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:39:07 GMT
USER haproxy
# Thu, 19 Feb 2026 19:39:07 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:39:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95388d12fcc8ab0cba2fc23d30b5043898996047cecf53f92a3d2d75836db36`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 1.5 MB (1488875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08aafb5f3956d371b58b02c3b44b5f718ac602502fe884aa648f6cc58fac58e`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88a71755b7cb55dc3a04c8fe669de1561cd3f8e8977c57439dec30584c247d`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 13.0 MB (13025196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc8f2e0715d3f70608120f9740383da80ca860051a9b5f0cfc076bd9f4d8296`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:cd4f7afca0d004c4f09f1f9c128189f76e142532b32197436dc299a42fa5604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c003f293a09281be32ac011b1e48670a81aa02af9b1f20b07c9070bfd408465b`

```dockerfile
```

-	Layers:
	-	`sha256:133a12ef5d11dd21d01c2e1fd60fc09252d8157d1e5e57d3cc3e02b25f81d2e6`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28923884bdd94126f102bbcf08a430197e6dbba7fc30f9b2be41cbf83af9cc70`  
		Last Modified: Thu, 19 Feb 2026 19:39:15 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9e255447a026654926d46ad58f5a1cadc87cc8b829a00ead669591cbedcb7af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44742325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6bd9870002ec936c5b476c34078fc71e1534c56c59840b7d028c508a1aee30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:36:20 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:36:20 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:37:01 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:37:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:01 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:02 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:02 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758b1a4efb716962aef6c4b81dd691cba4c65b6c1a7db57d8a1864a1602c88c4`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 1.6 MB (1563185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76f0f6ffc726bb3984b0727d21548a6f9af08dfd090ea5fd30a97641975826a`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e346a6bdecfc69558241435b1df09270607249b255c152a8c2a2c4ba5d3c1a6`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 13.0 MB (13037431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce352d384464979bb206efa2e443541948a7c66b4601411a9ecd6c1095db43f`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:88c180ab4cbc85ad8ed055ecc54c442617f2f64459b8d827020fb156411cd880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47736231b4d1d3983da61caa3108413773e8ad6bebc7c459930e8b5244aa670`

```dockerfile
```

-	Layers:
	-	`sha256:a47c04e0f1f707e8d640fa142f1635f109842fed2c741168315a4b9a80389e00`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c367d60c48c51ae96626adc7c94cbb65e2b89b9f3457573030c844f289e172`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:92070c7624392438ecf578f96fda4eeb5463f42270b0139c361e3cd581b15d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45724805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2305cba35fe40fb1310e93e3cd8507ad846073ecd8e17af9e2cf575a7012a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:37:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:37:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:38:09 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:38:09 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:38:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:38:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:09 GMT
USER haproxy
# Thu, 19 Feb 2026 19:38:09 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:38:09 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af90500d335525b46509020e73a346dd9192674c7c78e4480b8e88b47c10fe6`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 1.6 MB (1603205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13644dd09cd1cb9dc6b4805ea05a93f7057af8f11492cf2ade24b0f1cc0d7f`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f50771db154461c9fe85cbf1ebc4049a3bdf2e6637af7e58d9244ef7d68e5b`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 12.8 MB (12826103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24159f2feea0b9b506c5addd22936c2a6f29c76afb38cc46b3a6290cc2927ed`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1349ac4c69549d553d8368270a94fa791266affd4eb9ac75546b207d4c8694e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77867e809a6a4dcc024456742cd8ebf7c971baf116c6496ee616c43ae1ef5c0d`

```dockerfile
```

-	Layers:
	-	`sha256:f7208da3ea111f75e47e0f9227242f8cb2a4a016baa5b2828256602d5dd000d2`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce94a5acc97647f63fd5566a6d24410f90992e45dbff532df6a6d0622c18d64`  
		Last Modified: Thu, 19 Feb 2026 19:38:17 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1fd1c1bc18b76f48ab848391194fdf02c9a23253e85499191fc0d88421ffe4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49067303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4666f0d04db306f4966d63c00b3f7901eb8bf6fb4bf627a9bcfb2e1cc34d6a4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:16:32 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:16:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:40:40 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:40:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:40:40 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:40:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:40:40 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:40:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:40:41 GMT
USER haproxy
# Thu, 19 Feb 2026 19:40:41 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:40:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb771c91e68e5c0b2810027274efd76c7432c5f533c9a2accab194ad66eeb7d`  
		Last Modified: Tue, 03 Feb 2026 02:18:36 GMT  
		Size: 1.6 MB (1638768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c41ab1963e36afe1baceadf478dee292e798dd968ef46b581c8352941f3ca25`  
		Last Modified: Tue, 03 Feb 2026 02:18:36 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be1f68be3f07c6987633ee9ab7884be210442a57390a15ffeff3e287febf050`  
		Last Modified: Thu, 19 Feb 2026 19:40:57 GMT  
		Size: 13.8 MB (13826710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6218dfd48e31e8120064b56b0b71852d8ee9527b020767a5371286d275d229`  
		Last Modified: Thu, 19 Feb 2026 19:40:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a56531952b1fc0689d1461938352993a5e0ea87f0a45c95154d78a20f0d10c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384f5fb189dd107580c34b062519d2aff1bcd4c21d75cebecdd1e205461bdabc`

```dockerfile
```

-	Layers:
	-	`sha256:baaa77c2bc276e16192d4baaec4a2c9edf2ba85d9483d1d55a00be52e61e875a`  
		Last Modified: Thu, 19 Feb 2026 19:40:57 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c663b29ae5bb60b1d5d9710a8a84b45845ee8fedfc55afccbf95b74560ce00cd`  
		Last Modified: Thu, 19 Feb 2026 19:40:56 GMT  
		Size: 22.4 KB (22409 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:edc0bb74759aeb51263e8fa382c8897e03a5ada43fdc2d8f85c2bc9527cc8511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42549123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfcaa38f48533b4432b0229e9a93b1f55967695aa74269ec1fb3d0e71e01ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:08:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:08:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 20:58:14 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 20:58:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 20:58:14 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 20:58:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 20:58:14 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 20:58:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 20:58:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 20:58:14 GMT
USER haproxy
# Thu, 19 Feb 2026 20:58:14 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 20:58:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eb4b4bae0113a5278f60bc47c5cfdbdf082781e28b7db61e12b38eee51040a`  
		Last Modified: Tue, 03 Feb 2026 09:24:50 GMT  
		Size: 1.5 MB (1535077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e454af7c4c927ef608ddfccaa21c486176a61afccfd5e9be19a4b93000144`  
		Last Modified: Tue, 03 Feb 2026 09:24:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ed93faa048ca818d6d08d1a396307328fb3d3ddc7497cade1cade330372574`  
		Last Modified: Thu, 19 Feb 2026 20:59:19 GMT  
		Size: 12.7 MB (12736014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3c7fa90a89eb61c26dc400408f89914da41ac0dc6fb51aa87e46ea9404568`  
		Last Modified: Thu, 19 Feb 2026 20:59:17 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:fed02d7ae61a54bb9eac68e5a456680fac2a085eec48ffb34d38954f9f133292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448ea0af98040b518f373e67c564e09458205971e918ab4273fd248bd84f99e7`

```dockerfile
```

-	Layers:
	-	`sha256:06193d67765b59f428c5a099f996da6b735c9ddb9eb1a4300b4889b26c8ec16a`  
		Last Modified: Thu, 19 Feb 2026 20:59:17 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce282af2411b5e09954368cef53d635b1afe5bdf6eebb9a48afa21e7ff2e8572`  
		Last Modified: Thu, 19 Feb 2026 20:59:17 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:9d13294b1e9c3dab1d8f4f61fbadc388d952022c27a50e59c7f3566ff7b99c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44868779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2300291d1411235f5da8961c150093539cd14a9e298774e20ce1892f7e9e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 19 Feb 2026 19:35:33 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 19 Feb 2026 19:35:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:38:52 GMT
ENV HAPROXY_VERSION=3.2.13
# Thu, 19 Feb 2026 19:38:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Thu, 19 Feb 2026 19:38:52 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Thu, 19 Feb 2026 19:38:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:38:52 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:38:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:52 GMT
USER haproxy
# Thu, 19 Feb 2026 19:38:53 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:38:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68d4270f78368062aee0a07969819af72ed8e7ccde9d87d5bf00241afff703e`  
		Last Modified: Thu, 19 Feb 2026 19:37:49 GMT  
		Size: 1.6 MB (1599755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d19613513c99c1aea40d7488c3aad7f255e52e54b637a6fc4c630afdcc588`  
		Last Modified: Thu, 19 Feb 2026 19:37:49 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee46e64dc11c2b45f34e6f744357f91f91c04ecbbaae572533fb37757e2332`  
		Last Modified: Thu, 19 Feb 2026 19:39:11 GMT  
		Size: 13.4 MB (13429229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0435407213ded75d2fef6ea2d9eb999f0c52b8c276d6fceb2fcb561af0bf345`  
		Last Modified: Thu, 19 Feb 2026 19:39:11 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:59798761d1bd6b03c3e5c122f93ae8bc85f2d13eda23665cc46412cbb8b13dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f6a744e9ca6e796f1ed1f85dacc3aee04855cd257415ee41647e6c4e3b4a23`

```dockerfile
```

-	Layers:
	-	`sha256:570a24d8b7795797f2ca553b8446c66bcb092ef648bab46bea85e9f825d266c5`  
		Last Modified: Thu, 19 Feb 2026 19:39:11 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147530b4e03b180953cd8d8c35e698ffe16b1efc06af763615187230b62d140e`  
		Last Modified: Thu, 19 Feb 2026 19:39:11 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
