## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:011a9e9706551ee3eebdc4272546c440f19b1d8d135d7e72d7aac501b3c1ac11
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

### `haproxy:trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:a3ab9b3dcc0e0ef75532aaae57102cdeeec9b733e5fb82e31e7962a9b17cb51d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45892832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96750b4aa65fa2baadfd9436602dd4505532bb8a600b7802413c7bb859f30ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:12:45 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:12:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:13:28 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:13:28 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:13:28 GMT
USER haproxy
# Fri, 24 Apr 2026 18:13:29 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db0e8c3eaa182ab2ba011aa86b33fb2568c6fec5613ab6c0a1ecfd7584e83a`  
		Last Modified: Fri, 24 Apr 2026 18:13:36 GMT  
		Size: 1.6 MB (1581077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb6e062633eec76cca3d6bf5d7fb838e2a002b10d9da6d81b3972249aa86a28`  
		Last Modified: Fri, 24 Apr 2026 18:13:36 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71844910dce361dc6d0f48687fb35f3de9dfbde5d5448330cb611a01f837e53f`  
		Last Modified: Fri, 24 Apr 2026 18:13:37 GMT  
		Size: 14.5 MB (14529944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76873b41ccc9fbc97dbb60167e08177de850843e4ee9adff5510993c65eec55`  
		Last Modified: Fri, 24 Apr 2026 18:13:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c70de330370aa8e544da7b1f6a764ed3188b7b516d1f9ae2038ff3dc83f5d10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c8850a5b59d711207f86ac10a89d50d46e014d04b38560dc7ef741e8e207d5`

```dockerfile
```

-	Layers:
	-	`sha256:32efd6a1cb2927eb6662d8b697baffa868f699fa03601484593851f4f002d6a5`  
		Last Modified: Fri, 24 Apr 2026 18:13:36 GMT  
		Size: 2.1 MB (2113798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf7086811dec4c9b4018001694e4b4368e2ea94287317baf3ad27022974081e`  
		Last Modified: Fri, 24 Apr 2026 18:13:36 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:b5eb564dc0f220daee90afd177d832e45f4f70956871466f9e23e8e4814d0925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1a305b51fa966681c6ab05196fd0a0854cda10c8286ab7034eccf1275ebc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:57:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:57:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:58:11 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:58:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:58:11 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:58:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:58:11 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:58:11 GMT
USER haproxy
# Fri, 24 Apr 2026 17:58:11 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:58:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381079695b3cb6cfbd3aebfe63bfc1d10f5a3c3b63836c5a2a61c3edfc088dc3`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 1.5 MB (1535722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d8ebbb9d3f21c7a96ac57fa74a110928d92dfeec82d45191bea478d781894`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47e746ad1f6721b3db2b4520091e657d4953e813c5ae40c996100b1fa133834`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 14.7 MB (14724213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e2309734f7ef5d75d44e151c9e55691c7868212e62f21047cbeec3cd01d911`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:b3b453671a9e3cd2559be7386c0882a134909f39a72007d7efa779226a7dc176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8a2a6bed606f853657de1507cfbe68954df8a56e853e10b576e5c161400329`

```dockerfile
```

-	Layers:
	-	`sha256:cec7cd8532a92ff36a66ae04002b1dc14625ec784984651b7a46ac7e38fd4eed`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 2.1 MB (2116778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02355cfcd29a5e23df60171f7456c5a32556b65efbce68b45cb77b1e7ac1c345`  
		Last Modified: Fri, 24 Apr 2026 17:58:19 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:77890d5dbd5023ca3ea975ec43f572aa49f1235324ea2777a1df07cc2e15801b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42231019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8affe3c1cbc67aed1a0567fd3de6fbd2a944f91ba632ca7fe0e32fd4cfe85e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:56:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:56:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:57:50 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:57:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:57:50 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:57:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:57:50 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:57:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:57:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:57:50 GMT
USER haproxy
# Fri, 24 Apr 2026 17:57:50 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:57:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454bb4c47c52728c62aaca02e8ef47df2db102f442952a84f17a1dd8f4531682`  
		Last Modified: Fri, 24 Apr 2026 17:57:58 GMT  
		Size: 1.5 MB (1489553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ebacabf00e7f6bb79f0178e3b158c859c2fc0791755675e1d4901cb385186f`  
		Last Modified: Fri, 24 Apr 2026 17:57:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c6471cf22f52f62005353e96bbcfd55f159a7684f8a8a3f4b82d48fc8aae38`  
		Last Modified: Fri, 24 Apr 2026 17:57:59 GMT  
		Size: 14.5 MB (14524991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eab52a10f606f1fa65ee5c32795301ad9d2dfe82faffad30f9055e28bf29f3`  
		Last Modified: Fri, 24 Apr 2026 17:57:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e505430972708a25de7805d854be7d5a0910a76ea7004c9c61a5599cca160c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7543a97420709baa953ba8fc5fb05e0864a5c2f21849aa7960b3685da70a4a46`

```dockerfile
```

-	Layers:
	-	`sha256:7ea9caec73b957f182e42bcb4cf18e29112720480452db8a750b4b8650450234`  
		Last Modified: Fri, 24 Apr 2026 17:57:58 GMT  
		Size: 2.1 MB (2115221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5585e3ac02f65136d488f7ca643cc79eb906d373be923363c2e9530ca4eea93b`  
		Last Modified: Fri, 24 Apr 2026 17:57:58 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:5f03d2c24f7c60aa74348b14544ac45b4bb991e012e2370af31a469e35691295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46115142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c711a77c6bbecd24b63059a06eda3bc3fa4af28b44db9c8005c57698ca8621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:55:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 17:55:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:56:26 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:56:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:56:26 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:56:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:56:26 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:56:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:56:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:56:26 GMT
USER haproxy
# Fri, 24 Apr 2026 17:56:26 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:56:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5739728aff950a56f34e0d954e1a9495171374a4aa15f520c047eff60ad3c46a`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 1.6 MB (1563673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee8eba575fad48849ab02c4fb4f1cc50d98ba532f47efbd1f802db823211c3`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ba0e0f7c85c6f09647da73ace7f60dc1fa6ef18d55f68173f488206669ea3`  
		Last Modified: Fri, 24 Apr 2026 17:56:34 GMT  
		Size: 14.4 MB (14406224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ce816b1da80dcc4a30e64de65d8c338aff63a8b71f3f34bac39ee5ea6dfa6`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:22af0a8676261df791450a94d0cd8e91afe9ba8b1928c1ea7f054b618fb2b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8f32b49ae9ca033f63573ad2e0f00ac3ddb5310d71482e1af9d3c22814b36`

```dockerfile
```

-	Layers:
	-	`sha256:cf53550fa483a2c74f8a92bc9d71a1d67d9c10c98d4fb9f0b32851b088a7620a`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 2.1 MB (2114083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e618eebffbbf756d5923634a8aeb2dd5199373a7df5f9bd1b59cd58fb7d216bd`  
		Last Modified: Fri, 24 Apr 2026 17:56:33 GMT  
		Size: 22.5 KB (22496 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:cd6d06f0f4a9814dddf4626b24c36131766fa9e7808a85bdf2a118f6f685f34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47212443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dffa9826956e788af3c158dd5ba31af154621dd2e440766c13642f4422dd10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 20:20:04 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 20:20:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 20:21:00 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 20:21:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 20:21:00 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 20:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 20:21:00 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 20:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 20:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 20:21:00 GMT
USER haproxy
# Fri, 24 Apr 2026 20:21:00 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 20:21:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98946e31e8f1c34fdca94af4f80703c21fa18aba564c2a985680f2dea5bd9bbe`  
		Last Modified: Fri, 24 Apr 2026 20:21:08 GMT  
		Size: 1.6 MB (1603349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d715f61b51857526d0a8375c3228fc0ce54e26e1da465db4e56256654a40a18d`  
		Last Modified: Fri, 24 Apr 2026 20:21:07 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ae83e4b1969f92bbe23e206b6ac7dcd7465146a0bf8331d7a324760ee84f07`  
		Last Modified: Fri, 24 Apr 2026 20:21:08 GMT  
		Size: 14.3 MB (14311127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3afc1d12100c6c053ec13b9b9b210831a5c5f89c0922a042f463de75ce8177cf`  
		Last Modified: Fri, 24 Apr 2026 20:21:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2a4428ee523851c9e8209ee98cd6135fb7571d5d0d13a374e93f262b515cef54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dabfe35508de66775a880ed3a8a6b27742e1d4ef65d04097b269e501a5f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:1202364904fb32705dc266a88ab216a38d9b864e11bc3640e88a284b9e7d0ffe`  
		Last Modified: Fri, 24 Apr 2026 20:21:07 GMT  
		Size: 2.1 MB (2110979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a988d86ed2d8c2687f948bf751b6eea46bb614920730dee3f77b4d899b27b8`  
		Last Modified: Fri, 24 Apr 2026 20:21:07 GMT  
		Size: 22.3 KB (22291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3a9409ba12df8870450dcb731c4512c996c4f8d8bd19b67a723d3c3c3705b0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50497715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3eacdd02ab356269e93111c5bef592133076767bb824192da9ea4fe12cdddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:23:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:23:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:25:04 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:25:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:25:04 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:25:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:25:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:25:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:25:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:25:04 GMT
USER haproxy
# Fri, 24 Apr 2026 18:25:05 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:25:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53858ab18906b009afa91fe2a7cba690938b22794d14059026f0942586a70709`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 1.6 MB (1639154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d6554396b0420fa4d7815e5d17c727debcfa279f4cebb40c0ec276f650d7e6`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a3f22fe189cb74ada5781c94c7b3af611c31f2b5898f598fc8fda68d904a94`  
		Last Modified: Fri, 24 Apr 2026 18:25:21 GMT  
		Size: 15.3 MB (15258887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cab690bf421412a24995705175433da461598447181941ce6f6690f22779889`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:41bfd9e62ec810eaa9f322e33a7c6e319f325bbc80a1f31dc570f14d9bc66e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dd407216f9fb34c9dfa974db3f4a22c41585f6bc560e7a470272577a54c629`

```dockerfile
```

-	Layers:
	-	`sha256:042159e621a7e53aaaf18cc4c33f9ef6f9832c183a9bb8cf66c02c07dc7a89c8`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 2.1 MB (2117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67892a2b9c7bbe324e6f9cbcf7c6e323e95721a62ee3706dd89c1cf33840cb7`  
		Last Modified: Fri, 24 Apr 2026 18:25:20 GMT  
		Size: 22.4 KB (22397 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:22ae7529bede691f212d7abf69703412e404f171af504a711af027956be25a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43823127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd18165f2eec7c4c00166dd9eb66121a415175a83578d6bade8ed5fcf719b0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:07:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:07:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 20:18:06 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 20:18:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 20:18:06 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 20:18:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 20:18:06 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 20:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 20:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 20:18:06 GMT
USER haproxy
# Fri, 24 Apr 2026 20:18:06 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 20:18:06 GMT
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
	-	`sha256:af811d6e3515e4421fe755ff54d0d7cca3de3fb0bad5d57917f1dc55ec3ae501`  
		Last Modified: Fri, 24 Apr 2026 20:19:14 GMT  
		Size: 14.0 MB (14005851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f16dedef0c5a4d47dd1d411f2f7d2357e1f282a0e4a7548d9b5d09e6be133c`  
		Last Modified: Fri, 24 Apr 2026 20:19:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0a64eda023d3a11ea3a0cbb01ac2197492fbee508dd63e738a8ce1f9c26deaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304ea811e25a3ec72f3a83ba8eb789d1209abe0f82abf54893f0928f4c022e17`

```dockerfile
```

-	Layers:
	-	`sha256:8509afe5d8fe654510a0f68626b5113241f48701e40882ce50b1b8a13cfb5978`  
		Last Modified: Fri, 24 Apr 2026 20:19:12 GMT  
		Size: 2.1 MB (2107735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6eb04cea715eeb1bb7919ddd13196e60e3039cf09c786afaee5d6b13b57b54`  
		Last Modified: Fri, 24 Apr 2026 20:19:12 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:2db9bf621a36641ee74477598e9d9f7eaf0bf1791b07677f1c1b4708d691d72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46354205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15068951d95461cc924af88fde264e5c65421a665fc6f08689b0f122b753e9cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:03:40 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:03:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:14:16 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:14:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:14:16 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:14:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:14:16 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:14:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:14:20 GMT
USER haproxy
# Fri, 24 Apr 2026 18:14:24 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:14:24 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449ad0c4a3e8c1d968592901eac2abab390dfb2e78e63715a0e225e1726670aa`  
		Last Modified: Fri, 24 Apr 2026 18:15:27 GMT  
		Size: 1.6 MB (1600010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd484bf870db407e1c8ce1453939cd2de80ef74de30a46d72097fa4bc02c335`  
		Last Modified: Fri, 24 Apr 2026 18:15:27 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445970596b298edcae9ca19bfa4bb4a40c610e988d43d5cf6fe017594ce4050a`  
		Last Modified: Fri, 24 Apr 2026 18:15:31 GMT  
		Size: 14.9 MB (14912244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92402b6cea94058404e12286cec56ac9c6ea58ec43296543b9d996e9baf9a623`  
		Last Modified: Fri, 24 Apr 2026 18:15:28 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:13e2c344e25245cef27783e281674c757f66f2fc2bbb481e4d048449951dc259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77dde4450703ea58d964cb1b3236f8e580225a038dff782f11d038f468b1870`

```dockerfile
```

-	Layers:
	-	`sha256:7efb7d449e83df6bbaa761b57fadeef1dc3faa6146436fb47a59182ca77ed37c`  
		Last Modified: Fri, 24 Apr 2026 18:15:27 GMT  
		Size: 2.1 MB (2115242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb292b439e647de7a8213109f50925f3cfb593b09b24e6eba545ca817ae6f5ba`  
		Last Modified: Fri, 24 Apr 2026 18:15:28 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json
