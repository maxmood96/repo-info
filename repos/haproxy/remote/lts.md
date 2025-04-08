## `haproxy:lts`

```console
$ docker pull haproxy@sha256:8239905ff3a4d91d1cf7cd1309ed47361714077d093b158f2b11e14bddd7e7c1
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:de90d122b09b8be08af4713aef4f31dfd9dff06e2e360cb31435bfe9f0839442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41124271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bf9dbfbbcf630f6cea8393fe12859ae77d2b3151c4f209da572d80941ed189`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3af28c2edb571dc1acf5b3331a07414ae2c247e1502420b10f9580e98b5fdd0`  
		Last Modified: Tue, 08 Apr 2025 01:12:53 GMT  
		Size: 3.5 MB (3499343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99eea4f549c2de99b89b8cbe4f2bed73a1980474d8d50d88658b55451807cff`  
		Last Modified: Tue, 08 Apr 2025 01:12:52 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8eab3e3e5fe0bd6d0112aa9769e7460d6001ed87cb7b6c14e189221cab5b35`  
		Last Modified: Tue, 08 Apr 2025 01:12:53 GMT  
		Size: 9.4 MB (9396026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16960a0e35b93f933fc882c1ecd28dd1779f18453c3bd0ebee8ba865a40b281a`  
		Last Modified: Tue, 08 Apr 2025 01:12:52 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:eeb00416dcf5ff252784802a5aa256ed70dde6e8502d8d206c2c74f3ffe597a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea1b2a5b18f92a0a65fa458429274418d10772115961cf0ee8dde117ff6e7c9`

```dockerfile
```

-	Layers:
	-	`sha256:cbf3f04d0f917fd21de4d2a90f6c252f20934a69e13a1868c370150cc98f336f`  
		Last Modified: Tue, 08 Apr 2025 01:12:53 GMT  
		Size: 2.4 MB (2370409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d3582575a177d8e1c1935656940b4041aff9f5d3eb696055e36f2e28f3cfbe`  
		Last Modified: Tue, 08 Apr 2025 01:12:52 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:ee593912e26233edb13cfa0e6c964b896b5276fa2c6e1c3eb95d541c215e67bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38187342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032c001148ae965affde46284f9751229633c88498bb186d45d91a41337a0e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab545fcf5aee846efc6cba753da45cc34479d11f27cd91a73b4d9791ccec82a5`  
		Last Modified: Tue, 08 Apr 2025 01:15:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd27028e510811e6d737fa3d264adbdc36abc7d9c9905cc8cc6c964af931690`  
		Last Modified: Tue, 08 Apr 2025 01:20:02 GMT  
		Size: 9.4 MB (9354422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c20534c2c2ea5db75bc4831026b12b64537ea2512278f1b7ba91e97a5408896`  
		Last Modified: Tue, 08 Apr 2025 01:20:00 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:41ef159961273d0ac528f1b353fb2008e48a7bada3f6ecbda48bfade8edd1789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74113b5a7fb94c307448656bfe3310c3aa6b77e70b088166e3c3df3865d53da3`

```dockerfile
```

-	Layers:
	-	`sha256:8113e24630c65d38919389159cddb4edcc5668458cc7c48bdc335f6146c61fb9`  
		Last Modified: Tue, 08 Apr 2025 01:20:00 GMT  
		Size: 2.4 MB (2373923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8ed3a2e6b73a31a5a7ebd18884265e73b8335393ad849f03e3e63a551b44d7`  
		Last Modified: Tue, 08 Apr 2025 01:20:00 GMT  
		Size: 21.9 KB (21890 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0fcc9fe6447a5c9fa86c7c57959e5109de472aeed553fe56dd700dfeace32249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36023253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cf4f407ab63affb2fc250baa7bb8554a511270908234650355b2d3d18400fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c335d0f71373bed2334812b2451b30088049a848c153af540562a7ffe26d439`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c0646e2f5855156940c79bd716644ead0b9fb69517b27828629b82cc75e6ef`  
		Last Modified: Tue, 08 Apr 2025 01:19:45 GMT  
		Size: 9.2 MB (9175967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d8063df37725265919bc05323bb202ae9522184bb9eb6b58c2e7779d92ff2b`  
		Last Modified: Tue, 08 Apr 2025 01:19:45 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:0000acccfcce82a10201748424cbfb171351a224ab45402b6ff22bff868171b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b87092e61e3ff9f02b1ebbc86504627f0af6dc4745012b8c26effcca7f92233`

```dockerfile
```

-	Layers:
	-	`sha256:2a47d6594a40220cc863eeca562e5e7a606ac1c11ac4550b4453b9c1887ced66`  
		Last Modified: Tue, 08 Apr 2025 01:19:45 GMT  
		Size: 2.4 MB (2372652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0372b4f8aba18511a234941555b60fd6e28bffc600024cace6c1ca0785c468ae`  
		Last Modified: Tue, 08 Apr 2025 01:19:44 GMT  
		Size: 21.9 KB (21890 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2254d88fae94b2de8d892d151079d5cd3792bfacc33696f8ca10dfb3489af27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40770456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728dd416533f416ff54548cb26e87e963911fdf86f2e0d101afa4636d9e7a0c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dad2f5675b0cdf464e63a9b48c409ac612b17f996bbf7b338c749f6fda86c4`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963a0c7819694f41c1af2e3bdae32d705940d44e7d4118409bfd1b112f122cd`  
		Last Modified: Tue, 08 Apr 2025 01:21:27 GMT  
		Size: 9.4 MB (9379609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf441789d2aa17117262e7aab8dabbd5dca1d919d3987b7588f3fe3e27a23e3`  
		Last Modified: Tue, 08 Apr 2025 01:21:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:46ca709d1e6bf4d467b43d230f1d2c8a4b88be698be449c101ef003b09df7b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8523af0a17fcf1a060823294f6a940e24be438a917ffd3863ecc036030d1214c`

```dockerfile
```

-	Layers:
	-	`sha256:5942a696f992bfa8f0e1051cb5c684342d75d9a93b92ba81661e54202ddcb3cf`  
		Last Modified: Tue, 08 Apr 2025 01:21:27 GMT  
		Size: 2.4 MB (2370692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c42c6d0413cd415a3f77cfaec3cf0f347ece830c5826061c3f698744746c6d8`  
		Last Modified: Tue, 08 Apr 2025 01:21:27 GMT  
		Size: 21.9 KB (21929 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:92a573ec00a90a51ca71032fd0187102a90cd4b3430c413f9647e798370562f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41860549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d2e1fed92f671b4da27e27d4d4d6a437f5197440e4199e327f816fdf8fbd05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a312648b54de393712ae2e9542b5e228a0a98df31de1a6555e09620ee9aaf`  
		Last Modified: Tue, 08 Apr 2025 01:12:57 GMT  
		Size: 3.5 MB (3503457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63785bcf0143345bc3407b89757eface42f8d13a28d78bfab29d1d17f6da159e`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42273ceb96b449f7a425f509ac08eab30785ddce34e93b28cf75d30b1bdbbe`  
		Last Modified: Tue, 08 Apr 2025 01:12:57 GMT  
		Size: 9.1 MB (9144719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028368e594ab91e2fd4686174c6620b0dcba2c477ec74c99983798ee9cda200`  
		Last Modified: Tue, 08 Apr 2025 01:12:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:67d2a825f25b46953cfc7d276c74121b4db0b87e1c14588d94c73f4ba505069e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040152686db9272347c0bcfd9e32a4ea2e9de9cae8fd43ea03a013d2d0b4fe91`

```dockerfile
```

-	Layers:
	-	`sha256:55456f5be1ef5e590acc8d6b5626efde9130514ff6fc4241e3be4d569960aa2c`  
		Last Modified: Tue, 08 Apr 2025 01:12:57 GMT  
		Size: 2.4 MB (2367537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfcad5634a00e7d0962dfc5d71c7951496d2c68339f22e90149eaa7687650e8`  
		Last Modified: Tue, 08 Apr 2025 01:12:57 GMT  
		Size: 21.7 KB (21726 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:b89f662d87462896c9f2d5c46e611a52012c3689cb4921967ee80f76e726b42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40916298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c697599d544ce1d85230c2decf7176e48c84b89e43d38b2c1555c68fd1cbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949d2412d1813d925526134f33bbbd4b60e21f566ca57a9d89acc7ac2b8b0d6`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 2.9 MB (2895366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b52f5ed8e1f10c8be219e38ade04f17a5c6e6f88d0c36e73271efde31de0c`  
		Last Modified: Tue, 08 Apr 2025 01:29:31 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff495b93a8b891a8fda0e157c01bc69c932caa328fca072665e6afbf4907758`  
		Last Modified: Tue, 08 Apr 2025 01:39:49 GMT  
		Size: 9.5 MB (9505330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851bcedf31b057ea96a116fe8493742da09f5f8851a2b594d7e0f7f563dd7b4`  
		Last Modified: Tue, 08 Apr 2025 01:39:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9049209c5e8505e58d9f2e6626a597bb033b4e0783bb6e9300ffda11d526cc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb01708e34b06fdc4e4c481291eb70a87829460190eef2bd18b56dd6d52da19`

```dockerfile
```

-	Layers:
	-	`sha256:0787621e4eafd60993b0b4c1082be08df9d4c93bf180ef325e44c270b4504a57`  
		Last Modified: Tue, 08 Apr 2025 01:39:48 GMT  
		Size: 21.6 KB (21647 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2f313d2546d5f84d17f6da466c7f9697c995975906ce4284e2fd93988d52f3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45658035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1846b48234b2124b3c0a86095a03d10950eb292f095a38a90c14f549b48ddc3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e733c236b1c36a34f8989c83253cc91216e17a8ae4d8df75664f2bf82c25fc8`  
		Last Modified: Tue, 08 Apr 2025 01:19:16 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd330c614d3f28cce2b0ecbdba3ad0b1829a685f2a05d13bebe794981306b03`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 9.9 MB (9885245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecfb56143173e31976808118e78fa54925da1aa2fd717c923fd33c84ef9c8cf`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:01ac5d418041cc5ebb623c760086cd343db1125bfe6d70dba33b183c352e2317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c12406c4d9722558c58db962ac18442d3c61ad94fc9c49b330401c0a0482781`

```dockerfile
```

-	Layers:
	-	`sha256:f72624857d70242bed8e65fc22b1e74f1afb0a6ab1c3adfd37f725ff6549037b`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 2.4 MB (2374723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a170050694ff7c22d01fb1e96f499820b8e047c374f075645b43f07d39d8971f`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 21.8 KB (21832 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:81c398ebf6573fcd1aacef75f93b6d4158bac98658b5801b61c592b2d5a95289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39306594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e458cfd23b261dca326b296562800621b45722ab167c90915e06bba77ce215b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Mar 2025 17:13:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfffa6b73ae4d5d069267e9a17062dd54eecf9383eca25920655be9d759a569`  
		Last Modified: Tue, 08 Apr 2025 01:15:41 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f64b93e410d9828ddb02beaa0a081fe7be17fdf07e9feeebcdce47acc8aa3f`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 9.3 MB (9256982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3439cd08f7a14f7728dfa5d0b0ce465f179b6c56cd5c879cf01a7456befa67`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:fa8c64366f892caf398c3dabfd36e3a4e626d80bcf959643d89bf77b2bdbbc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c762b846de60060d4b78c0511d83f97447ae2128cc9dd334ede3331bd03580ff`

```dockerfile
```

-	Layers:
	-	`sha256:d7406d4d9969892b11a569c666b58bd1cb655c22af6eb9c3690c5e64e6a7ca2f`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 2.4 MB (2370131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192e7516b1e21ebbb402df61d0568f9a882693e7ec9ba405ab79e293d215b121`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json
