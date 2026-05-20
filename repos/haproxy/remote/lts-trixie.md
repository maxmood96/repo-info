## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:c19111ba5b32a19fb934475d0241e72ce9a9028ca83f63ce03fdbcbaa5666d99
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
$ docker pull haproxy@sha256:c3248b12c065026e2556ed7ccc20c286752667d8f304b942b414e034e602a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44532268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e40e6a2106e2be46720b1171271d88e3e492185d3be2ddd65cd2be6038e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:49 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:58:49 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:59:29 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:59:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:59:29 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:59:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:59:29 GMT
USER haproxy
# Tue, 19 May 2026 22:59:30 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:59:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9610ed6d000f9698c1ff2a518b6c9ea298f2951c9d7cb7b833ae661ddceeefe3`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 1.6 MB (1581331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb071eb697c9530e93db62171c7598f27e5fad3b2c207a2a4c7bb4804c95718f`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e7804bcfdb603d1c71a63c27f0aa847b9340895f297d3c2bfee916e2d6780a`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 13.2 MB (13169370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a9981686dc29904a86c3a57ad00c3926a65c506b27ba49934a9fea70ec503b`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:4bf6305ed06db255c9f2a8c79e2e0117a2969cd8fb548a2c753e2984ceb7aace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4674ed0e5a1731776bda928ff5760e3822bbb1307e9585af04d6d4963759c8e8`

```dockerfile
```

-	Layers:
	-	`sha256:d5694770a35e5425ac7421b5b28f6230723e862e6031806fe2e103ad47861c8d`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 2.1 MB (2113848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:286f2091d8b564b0e253f2e353b794b22266a20a4e3f2a2cd97dcfc7393bf757`  
		Last Modified: Tue, 19 May 2026 22:59:37 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:eb025ca0ebfc723006d3567b4156ad706c33e20a38f05ad6000a988b76c94d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42800695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eebec3f0298307328c7d393c58dda497f0e7b788ede16aa3c0e1217f833a0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:26 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:58:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:58:26 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:58:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:26 GMT
USER haproxy
# Tue, 19 May 2026 22:58:26 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c11c222633cd4f304e6faf78b280fe275ba1b9513eb507d2ffba706a04e5feb`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 1.5 MB (1535880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6ec9134525b3b6f981fa7fd028d7e5b4284b7e0f23ac2f79f95c8c47ed1ede`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489fa6f1a23cbc8b0c115878bce938eec096d646875e76fd3e0a24a914184389`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 13.3 MB (13309307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb50f6c7edee8b27fbd126e01bbe2eb567b9980887eb000f45ab6c0e495cbada`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ca3b93b5b0b084b9b6cc9fefeef4c8814a19ba391d17429f949ce2faa1132045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dd6fb870a4269bfe9271e07bf26afa7a296f01e70cfbf1938bd6a7fe49ea49`

```dockerfile
```

-	Layers:
	-	`sha256:dceb6b5fcfef2183026bd6e57a6dfacbb6135feea2cf33cc86cb94c5bc03288b`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 2.1 MB (2116828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4dab612f7a4bd171942fd18e815f87a52fea423f73103f4f5c758d7d63f9ea`  
		Last Modified: Tue, 19 May 2026 22:58:34 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e7917de18b5c6cc6df70b0bfeb042546f8a046f1dfdb6d6bc977a2ec0cef20d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40765004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5a4147f19aa3a59f93509969bd82bb93f22fe3a775c8d9d32156a21e7ff5b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:39 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:58:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:59:26 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:59:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:59:26 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:59:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:59:26 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:59:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:59:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:59:26 GMT
USER haproxy
# Tue, 19 May 2026 22:59:26 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:59:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ba632ba0cc86c404f6ff75bab046f81c9a1748ac1dfdf5dc500f44aa0a04a`  
		Last Modified: Tue, 19 May 2026 22:59:34 GMT  
		Size: 1.5 MB (1489588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e8022ef3de489eec7864ce51a9fe0f6197dfeb9243b1386dd859236c52ee0b`  
		Last Modified: Tue, 19 May 2026 22:59:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb039b6836b375ae3abaf022c15216af34ffee2ba232223a1f896e4fca884a51`  
		Last Modified: Tue, 19 May 2026 22:59:34 GMT  
		Size: 13.1 MB (13067943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd5780a60f63c0b1b0ba1fb8ae3ec3985227a1270f9bda9de8137adf72b51f`  
		Last Modified: Tue, 19 May 2026 22:59:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:bef2bf0797630a6f87f001a6c88c02b49230a87aed7b1d6e8b24c57caae7c43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6478a0e5c41f07872d8ab16fb9aaff601f5f727fe4deddf681da41629ec41cdb`

```dockerfile
```

-	Layers:
	-	`sha256:b59f521918f927f474e08ab5b0b0ec2a6efd7043eac29096035cc7d8276e218b`  
		Last Modified: Tue, 19 May 2026 22:59:34 GMT  
		Size: 2.1 MB (2115271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe72b8ca09ae803f3576032ef8fb12f1d4ccd7f20c7525ebccb4c24c5416d644`  
		Last Modified: Tue, 19 May 2026 22:59:34 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3286d48a16fbf941ff145527241d3db984aa76f8e1b6fb83850acb537845238b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44781131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff238250a8029e07ddeaadcd453d57131f393f2148d6b1eae75aef4fb64591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:56:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:56:52 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:56:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:56:52 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:56:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:56:52 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:56:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:56:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:52 GMT
USER haproxy
# Tue, 19 May 2026 22:56:52 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:56:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334039c2af163c51de28c0562c87634af03500d4a69d93a57d7b89e39359105c`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 1.6 MB (1563994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449c0985a203c8fd3dee9a5693fd8a9e823ee91f5206838c7c4d4afc81e24e8d`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bda7960e7927fc295e3b8146fa66ef86f0dae5596854aabb2981c094b12dcc`  
		Last Modified: Tue, 19 May 2026 22:57:00 GMT  
		Size: 13.1 MB (13073580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6a3499b061d280ecc4f45fd4237c6ab4d16238cc22fc86516715442670ee1f`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:bf936898134e89757169f64e5580e4c9736c3d341aeb390175ef6e32a7ca185e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800830a70a794472b5452fe1db5cb3127ce8d85fcbc7dee7f6b5b0e703328934`

```dockerfile
```

-	Layers:
	-	`sha256:79f4863f5cb640a10cb1b6759174a6f9d0f78a9a92b113d289ea3e450705d6f0`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 2.1 MB (2114125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce32ffed893ef9e74cc5e0010dd78b21f3e0270394f1275b3505fdc687263f4`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:7ed1ed695ced12566305e2e9dec7e74f1cf38735d2b09b29473faf6c3cbd5225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45760770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baacbfb2b05b7b214b188db4f43ebf778ec25701d1f03b313b3b69ceac33ba9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:18 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:58:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:58:18 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:58:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:18 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:18 GMT
USER haproxy
# Tue, 19 May 2026 22:58:18 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5758313ec2fbfb69e689f9039a08365760d63b4d5811f3dc3083adae726db`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 1.6 MB (1603816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65405b424bcaff45fa18c8ee6f2dca6e4f8b3bf1d77c3ae345fccfa3c669bce1`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be9ebb53fe47a078e39b14a22a282cfe3f354b07ecf03354b03b622f4b3b0a`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 12.9 MB (12859982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b204d607ed480c996f747fb57a263cb2b03d0abf59bd7e8afb733d261982ac`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:fa1f55624b56b6b12c0b4cae354ddd6ec455f384019ddec358ff9504229012ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672faa9fe0d5c617c5d17bd39facfa1870d96fd238dc06bcc3d3f81d5f449f9`

```dockerfile
```

-	Layers:
	-	`sha256:4e4f4f4aa0528dfcb0e1983fa740f213d812289c8e0a0316b6ef787491e297cd`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 2.1 MB (2111029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a644d1a6306afc70a14bea07203cb0e7c2555710f898760c164cbbe78b9a1f0`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 22.3 KB (22303 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ecd5012fa2ce0901acffe544a9892c665afc1f1dd9c808051fa5eeddacc8c843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49095274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496177bb28449a36614fc0d3d5ede48c2e4698f03cc364c934ea9dc1a205546e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:35 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 23:00:54 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 23:00:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 23:00:54 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 23:00:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 23:00:54 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 23:00:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:00:54 GMT
USER haproxy
# Tue, 19 May 2026 23:00:55 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 23:00:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2682f083b1ebf5bd4e4423d2b37efeb458f008ac7b2800f061f4abeb082ca07`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.6 MB (1639553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada36dad28b45f88ff713f4189bbe40d949a14533ac18d07a0dff0cd73c3dc50`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccb62ed162fc4ef7ceb1b116f7ebcbf8a8c410e53a9db427cddd4e8980f202a`  
		Last Modified: Tue, 19 May 2026 23:01:12 GMT  
		Size: 13.9 MB (13853629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337e241fe595bbda83d5e19c535601868d55b4cbdb3eb841e806d356c8b27e75`  
		Last Modified: Tue, 19 May 2026 23:01:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b2358a5e89c5bf0e459c05c522a6db0e3f9824c465b7e556a975166e1dc7511a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20962620486924ada77d1b2717be094536d6e163c5a8050ad0800663adca27e`

```dockerfile
```

-	Layers:
	-	`sha256:9064b08657741d020c62f313adc699ee5e521f02fe138bf896fee1b4628c3099`  
		Last Modified: Tue, 19 May 2026 23:01:12 GMT  
		Size: 2.1 MB (2117394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7145b3bc869afd7d67095ccb80ae7bbe5f36ad31e818877cf2a56f9ece99f0e`  
		Last Modified: Tue, 19 May 2026 23:01:12 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

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

### `haproxy:lts-trixie` - unknown; unknown

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

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:b971cbd230275d41b899235514d7116a035a7311ca4ef7c3b67ddc894a8d1f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44915292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b477d195cf7ed6eba54b5776f5015f2cc3fe9850272e412a9404f629e553f4c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:36 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:37 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:42 GMT
ENV HAPROXY_VERSION=3.2.19
# Tue, 19 May 2026 22:58:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.19.tar.gz
# Tue, 19 May 2026 22:58:42 GMT
ENV HAPROXY_SHA256=b08ebbd57f575012e4a5eb5b772721531fbacf6913ffd334f0281736a1ad78b6
# Tue, 19 May 2026 22:58:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:42 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:43 GMT
USER haproxy
# Tue, 19 May 2026 22:58:43 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72bcfcf925c64bd9d9e48ac69879ffce51a26e18e3f393e5603452f6407d285`  
		Last Modified: Tue, 19 May 2026 22:58:47 GMT  
		Size: 1.6 MB (1600065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdbe3f32165baf6e63da13d9339c0f7b6b2260a9f99191337a16a0aa7e51368`  
		Last Modified: Tue, 19 May 2026 22:58:47 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea615c182de7173324f5573402dcbe4bcdeadeceb97e43a068920e9a2e9b4f`  
		Last Modified: Tue, 19 May 2026 22:58:54 GMT  
		Size: 13.5 MB (13467656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6927e269d1db1b7ca97627aede1fef6e599f4a57cd3df6b3d122d34684001f0`  
		Last Modified: Tue, 19 May 2026 22:58:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e8b44836c1ed5bab578a379aed9130c86b736bc2ab368f46648e4d03e7b33a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da814c4dd949841c2d054cba99f24a3cca56c3c50ef99926429eeb72cdee19c5`

```dockerfile
```

-	Layers:
	-	`sha256:34d8fd61ff3430d34c8c249453040c7a9fdbb68b14b568d46aa1023f8a01e002`  
		Last Modified: Tue, 19 May 2026 22:58:53 GMT  
		Size: 2.1 MB (2115292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4327f7c309c75182a19548bd3f8bfc70e05ec0b5a5263812449af8b118dee343`  
		Last Modified: Tue, 19 May 2026 22:58:53 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
