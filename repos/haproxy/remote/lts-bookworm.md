## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:176291cf3c0ff4a144ebca2aeaf85e9f0f76bfb3daed9ba5b6d257c7fbefe220
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

### `haproxy:lts-bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:b9e027fd78cb8619c864630d5ad6d5acde26f65e7a61b170363fe2533062a2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42586243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ab311b1552d2972fea5340bc4f41230ec3b36d743088b6a9d13fa52d4a40e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db2e0c646c0883dd96cae134a094a57ab5c5941924583057c9177c087bc0b85`  
		Last Modified: Tue, 10 Jun 2025 23:27:54 GMT  
		Size: 3.5 MB (3500611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aafc8de00cc51abc1a299be1174f82854a4adca171545c4afa555e17083053`  
		Last Modified: Tue, 10 Jun 2025 23:27:54 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6e9599ba7f74bbbe1ff290a6b8ccfbdbe3a1ca8345625483532e5292ba506d`  
		Last Modified: Tue, 10 Jun 2025 23:27:56 GMT  
		Size: 10.9 MB (10853862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077204a435753099cebf3510c3c483b35ee3a5b04504d3a386f3e31af7e70df`  
		Last Modified: Tue, 10 Jun 2025 23:27:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:72b6da7ef223e5a5a3bf2c0762a0e6381cca3e5272484e116c5e964d4834a401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8663d7fa7f03bc2bcd612a0851f6a5e669cfe007586016a3a9a16147fdfeb4`

```dockerfile
```

-	Layers:
	-	`sha256:e507e81d13c65617ed6bdff66d9f69520647c58ce41e73755a9ecddb8a6a0ef9`  
		Last Modified: Wed, 11 Jun 2025 00:58:22 GMT  
		Size: 2.5 MB (2485127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c4255fcc8312ea17250154d0683bee329615d8c17e4a18e5ee4480aee60069`  
		Last Modified: Wed, 11 Jun 2025 00:58:22 GMT  
		Size: 22.2 KB (22194 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:577aee0dd0a23d953a844eccf602a40ca439eb4129352a2bd24da07f73911bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39752809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c7e06866e4eaa54e773f38c1270f8ac0b46811a47a833695a3aa2124f2b451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64aa76a1aec4ca5ec6b604ac62f2c56609b258965abd5c532f8af0ce5d922f`  
		Last Modified: Tue, 10 Jun 2025 23:45:16 GMT  
		Size: 3.1 MB (3074545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c02746ac98e49a538ff551c187da4b3e83c72ee9c5627091e1cce593b49cc5`  
		Last Modified: Tue, 10 Jun 2025 23:45:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8d5c7eb23286e608e476f0459d756000e5c3f0a080b0c770f9c2b50aae8b8a`  
		Last Modified: Tue, 10 Jun 2025 23:28:48 GMT  
		Size: 10.9 MB (10914230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0e9522010db897bcc0e50901c2255eecd66993f034ce3ac5f8d4afeae24196`  
		Last Modified: Tue, 10 Jun 2025 23:28:47 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:90b224da7623c554357e794e37b1a0ae215b292fc2798db3c0de199fdfba8830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694646276e87e6d80007991e433dc0a06951cb17cb347cf08d56c3553fbe63ce`

```dockerfile
```

-	Layers:
	-	`sha256:b78303bd307931f1646512a0273c1dcf300d6aeb07efc9f382d075c927e75f67`  
		Last Modified: Wed, 11 Jun 2025 00:58:27 GMT  
		Size: 2.5 MB (2488965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035c9f306410139fa909fff70aefecc191e8c4980677ff5eeac32f9aa9d7b190`  
		Last Modified: Wed, 11 Jun 2025 00:58:28 GMT  
		Size: 22.3 KB (22328 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e866cc171da1c55bf5d61dcaff49c8c975504d4dcd598f0601b4c58881940fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37561748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f546481a3c61c364ceb19d1fae40faaf5a26cafbc4c887bdf15e8113daaa01b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a77c0e85ff3abb156ce12029ae9cfa0546d098a2a64f08ed9bd47a6bd07d39`  
		Last Modified: Tue, 10 Jun 2025 23:29:12 GMT  
		Size: 2.9 MB (2910185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a152e7c979b5a6059b6941e022aa0ffb177ed5df470cdd7a62e5a05a7f61e00e`  
		Last Modified: Tue, 10 Jun 2025 23:29:11 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367d20367b5ac1ab6bc4a8986909fab41ce84a5e5aa02e5ee53054a7456bafea`  
		Last Modified: Tue, 10 Jun 2025 23:30:26 GMT  
		Size: 10.7 MB (10711179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6f4abd3899bbf6f57528fa1da3806346c0d09aabe37a59019ba181f4548a01`  
		Last Modified: Tue, 10 Jun 2025 23:30:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7435b5eba150c2f1846c1febbdf1188fc024cbedf4f6cebcbf0fd3bb09d0941d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da446072600c097245fa10341f36ffc447416d80be331a31d48864aff7345281`

```dockerfile
```

-	Layers:
	-	`sha256:df6a82bb1d6877eee0d44ddc36e32fc56c31870ffa24c0efefe1c89c8e4085f2`  
		Last Modified: Wed, 11 Jun 2025 00:58:33 GMT  
		Size: 2.5 MB (2487386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1187d2283822ed075ed7c9076991d5ee318c46e24df6ebef687ce1f6db2ba544`  
		Last Modified: Wed, 11 Jun 2025 00:58:34 GMT  
		Size: 22.3 KB (22328 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:1caf83cefc38a11c1f4ad94d526684d41ad76e1cc5a9e6ed31e9032423d78f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42233351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1364369005bc36747dee0438fa3a0d3c946bfee9bea1dd4d59c309de3ba7ad1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f935c4cd780c89b145a846545e3a268680ec723fd748fea3897de43631a324`  
		Last Modified: Tue, 10 Jun 2025 23:28:26 GMT  
		Size: 3.3 MB (3324387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d08078c9dcfd4477d776d39dac1c7f58ee38ede4b61ea6c854504ffcdffedc`  
		Last Modified: Tue, 10 Jun 2025 23:28:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67e27c74b6b7ac73ce2b63d488b10c174e17a44269fb75b6adef1d882ef52d1`  
		Last Modified: Tue, 10 Jun 2025 23:29:20 GMT  
		Size: 10.8 MB (10829651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe5135f165d4a4e7d70023fe96e229c82c0ea1939b53253dbb8588644a8bce0`  
		Last Modified: Tue, 10 Jun 2025 23:29:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1dfe27790d3551438910914e0628cede8223e19d829454b3dd0f8743340cbf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6090758bc982fba938c6e0c38cfe59c1a5a3b09c726a92487422d08a1397c41a`

```dockerfile
```

-	Layers:
	-	`sha256:3a827f0a167dbe4d01de8bf61b44c0a6c788f9ce29034c960c7f392799f50f9c`  
		Last Modified: Wed, 11 Jun 2025 00:58:38 GMT  
		Size: 2.5 MB (2485434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81f8cbb9be2b40f4692d23b024f8705979fdcf65f93e240f32d1a90955fb4ff`  
		Last Modified: Wed, 11 Jun 2025 00:58:39 GMT  
		Size: 22.4 KB (22376 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:8e3344c656b3a3d704602c3bab8d73e263e577490f73159a4b24ec6fd4c663e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43218561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569d035d923b280886f88e8faa3ef2676eafb30187f29257b31001265e4bb38f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee7d43cfa7b24f4a60c3c52b4fb7f39fc9f4868e9970f79619271369222efc`  
		Last Modified: Tue, 10 Jun 2025 23:27:47 GMT  
		Size: 3.5 MB (3506070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db402e0617bbc8dc53c9731de07b0c6d59bcbc4dd9fd6eed96b3bea95420481a`  
		Last Modified: Tue, 10 Jun 2025 23:27:47 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f560d315ac38ec961d51a39a38ba9f009a4b4c7dd8c89edc5cddc449bc49c74`  
		Last Modified: Tue, 10 Jun 2025 23:27:47 GMT  
		Size: 10.5 MB (10498419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ee9eeb721a9a351ca0fbcaf4957f5348f37360a72064aed758395b4152fcd4`  
		Last Modified: Tue, 10 Jun 2025 23:27:47 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ce68aadd06b17de297e96b4266369449900e6206341a980cddde6647bf431eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0d63bea205a8114ea5bc01d4b4649a40cb7774bf50afd4fcf12ea5314efd01`

```dockerfile
```

-	Layers:
	-	`sha256:82e8eb741c4928b581f8ff9bcedf302e2c618f49c62aaa171e1fcc664b3c8919`  
		Last Modified: Wed, 11 Jun 2025 00:58:43 GMT  
		Size: 2.5 MB (2482286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1d87454f9a62405a4ab26eda6dd2c627a1be71b30b495ff56f336a971d2812`  
		Last Modified: Wed, 11 Jun 2025 00:58:44 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:a0cb7c33edb01f3f87149808fdce3b8084e02584a9ca28d39052eb7f39194229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42448217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89e9e1a09dbc5e4f98310107febe1757daf757041dae4fbd0aeda93054dd86a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89de932eec335b5d31d5e7131daca73bd0655ac540c6f8a744824f46b50acce`  
		Last Modified: Tue, 10 Jun 2025 23:45:20 GMT  
		Size: 2.9 MB (2897316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a6f8b67bf7d7e7dbe2103a24db825833dff6d5088d4a681fd43ca590feff7`  
		Last Modified: Tue, 10 Jun 2025 23:45:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c429df77d1c2716a6ead3ae6f4bd5add8030a0adba669acab31bcffbc38e7`  
		Last Modified: Tue, 10 Jun 2025 23:40:19 GMT  
		Size: 11.0 MB (11032542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35644930ac7a22e62f5ac73d45684f98265ba9a6bdf05dee6da3457df03bb6c1`  
		Last Modified: Tue, 10 Jun 2025 23:40:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:869cc6d231b1abb6201d4f9154d9f1f512b285715f7871ea5b6514c06bd183b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43aac487ff88b76b1cef57fd7bb3babd48e2b1a1df4e43a221fc83f8f6483beb`

```dockerfile
```

-	Layers:
	-	`sha256:b88e33a7f944f9ab3e94a5571d9ef3e68255aa4896dd08b99acc7d764e9fffe6`  
		Last Modified: Wed, 11 Jun 2025 00:58:48 GMT  
		Size: 22.1 KB (22087 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e583677c92dc7fcf37946ec4544cfcb3b0ed4d1ba38b15f8dea130685d77018e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ff1deb1030c9ee2d98407847b480938e4e18ad5a7048bb0c9c731d74558b65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97506bbc7b8a39826962842cfeba6c645d07afc4a76b720da4b30ac0689a89d1`  
		Last Modified: Tue, 10 Jun 2025 23:29:12 GMT  
		Size: 3.7 MB (3705059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bcc7b722e8b948227bb0d10ffac50f27ae62cf77f21360df4ad5e82383186f`  
		Last Modified: Tue, 10 Jun 2025 23:29:12 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6309f8b9b94916cbf860a2b15f2900e8a83f450d2f32baa1d7c1267edf0b4`  
		Last Modified: Tue, 10 Jun 2025 23:30:18 GMT  
		Size: 11.4 MB (11448916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb4ac8f9f6f691e36872b93fbc978935115da00d8c65bc498c85eee729be6c`  
		Last Modified: Tue, 10 Jun 2025 23:30:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:dfcadbf73332315ad280bd5519f02e73eb77f44a0f23011a9cf4ed0621850cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a90bb3e76a2ba1fda7592e1384490e8c5788c06a5b31fde4c8b1eff2c7270`

```dockerfile
```

-	Layers:
	-	`sha256:38938d86d996c895a2e12269890ef885530f73402577d0a9fd28d9c0bab38f93`  
		Last Modified: Wed, 11 Jun 2025 00:58:51 GMT  
		Size: 2.5 MB (2489547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b72efd7ffafb62f5f5eb5cfc8352088aa95ea604e77390b85d6fbd11e27d20f`  
		Last Modified: Wed, 11 Jun 2025 00:58:52 GMT  
		Size: 22.3 KB (22265 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:23b20091e6cadee72c2641da7d55bb93372306536a19358e44786b1fc326d3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40870059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a31afc4b57916b0d62e24199bb57e1d745564e27e59defe9528daa54f7ad16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 29 May 2025 11:26:38 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fd2f706f8f1a993a631532c76c5c812e4efc1a98ac1534a31d6c1a7d4cb32d`  
		Last Modified: Tue, 10 Jun 2025 23:27:39 GMT  
		Size: 3.2 MB (3164919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9242b1ef5e7738b1ae023f7888373e446ee5c8da2c59801bf1f39e537a6a7c5`  
		Last Modified: Tue, 10 Jun 2025 23:27:40 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347c8cd6494c5c4a7398c5b87590320f8a1256be771c29b2f18d54b912e31920`  
		Last Modified: Tue, 10 Jun 2025 23:29:02 GMT  
		Size: 10.8 MB (10815650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ec436e48bf6b6665eb9c7d66c9bd717e66105bdbc99ba6844d77c41e8eba14`  
		Last Modified: Tue, 10 Jun 2025 23:29:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e44df01eb8dc85596fe23c814e68770d70e4e7dcc237c0352df16d8ef39e5703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2504151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46ba485c8782ebf94212fdb9e73919737e811c02273857e4464ad9fee0b5ece`

```dockerfile
```

-	Layers:
	-	`sha256:4513158967ede8d45efd8273186bad9dad98d9d95b1eca2ac30bcc8583619aed`  
		Last Modified: Wed, 11 Jun 2025 00:58:56 GMT  
		Size: 2.5 MB (2481957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b57a3fc2d241c0437da1edbe72f2ce1270fde35cd380a2f3822ed0ef8bf7dd`  
		Last Modified: Wed, 11 Jun 2025 00:58:57 GMT  
		Size: 22.2 KB (22194 bytes)  
		MIME: application/vnd.in-toto+json
