## `haproxy:latest`

```console
$ docker pull haproxy@sha256:f14a1788b56894e7ec7b5cb0ca09dbb959b674cf3c980f92139ec008167d4a91
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
$ docker pull haproxy@sha256:e5879dd340b64acf51ccf0b894e04548bf26f28b7ff5f4d2f8e333b02da6d02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45900918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927b5433a8bf78e709f89a6315ee8b66eea98036ce3d9b3c9cc3c97724d0321c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 05:30:13 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:30:13 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:30:59 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:30:59 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:30:59 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:30:59 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:30:59 GMT
USER haproxy
# Fri, 01 May 2026 05:30:59 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:30:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b45a04c0acc7d8eb214bb042bf086d4de542e0b06fd68b8143d55f095e4437d`  
		Last Modified: Fri, 01 May 2026 05:31:07 GMT  
		Size: 1.6 MB (1581124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba706fed6bfe59b2922c8b34259c2973f042ae66ee62493172792a47a189421f`  
		Last Modified: Fri, 01 May 2026 05:31:06 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4005f621d867c6554d567fe19cca7766e084cca7dad0bf50d7195e4473921990`  
		Last Modified: Fri, 01 May 2026 05:31:11 GMT  
		Size: 14.5 MB (14537977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac085a9ea70bdf2387ca8706f37a757153c339376715d5db89ffa7712db65e0`  
		Last Modified: Fri, 01 May 2026 05:31:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:4e349593836cc7544d12d48ee73fbc6ee8dd34f796f99373f2573df322f5c249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e7bb9d9b9536daedf61401b349da8bc8da5a5f64a2abcccf7f514cf68f5d1c`

```dockerfile
```

-	Layers:
	-	`sha256:1adb4e951700e2177ad3ef0c393b57225ff33120ba02d570827955e6c4371fce`  
		Last Modified: Fri, 01 May 2026 05:31:07 GMT  
		Size: 2.1 MB (2113798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd17f0426488128d2ae0ff5de52ec9a98b1d94d16e59ea58c9f43702430ad648`  
		Last Modified: Fri, 01 May 2026 05:31:06 GMT  
		Size: 22.3 KB (22337 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:35c8b14989ea9dee843eecdd4f8399ec5cecdd90637faf9b6ff4a287d6fcc214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44218504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94627e30295960fed99f739fb5af6e666d8f6f17ccc0d634cfe39d2b86258805`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 05:29:50 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:29:50 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:30:50 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:30:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:30:50 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:30:50 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:30:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:30:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:30:50 GMT
USER haproxy
# Fri, 01 May 2026 05:30:50 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:30:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cedfc7b52ff7562b4cd75d4ba02c2bb91c99489e46f5be8b8fa067675e9c018`  
		Last Modified: Fri, 01 May 2026 05:30:58 GMT  
		Size: 1.5 MB (1535707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc14e067c6ee7b331677be620a48137028fde3e4a842dd3a564513cf89e0541`  
		Last Modified: Fri, 01 May 2026 05:30:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579661545a23a498bba77fa53d8cd6bac96aed544e4a4a170ab72085364d5d96`  
		Last Modified: Fri, 01 May 2026 05:30:59 GMT  
		Size: 14.7 MB (14732979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6294be738580071f60a38f4a2d38fb268ab091f97aae5f672307e095892dac`  
		Last Modified: Fri, 01 May 2026 05:30:58 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:9aa9d3ef50b0cf3c05b0e86ccdf192423e34b6d0e2060f179338d2a36c2a5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc023771143d9aa16af6a031742b2c64191a25e64fc69459140c2ee529218eb`

```dockerfile
```

-	Layers:
	-	`sha256:571d3ab8919ed5450bdb955567496e710325be70be5fddfdd8d2ee2bad9bfc47`  
		Last Modified: Fri, 01 May 2026 05:30:58 GMT  
		Size: 2.1 MB (2116778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b500e145af33f75c8a663610b431cc89f96e5eab29a29b8a5099199ba446d95`  
		Last Modified: Fri, 01 May 2026 05:30:58 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:9af60ee24145a6bcb4c908971c6fdefdbce46bdf4f9e76489780b3d2535bd89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42235836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09cfde24698204066704cb67881944352087217b97e2605c0b1f6ab2f9dc5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 05:29:46 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:29:46 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:30:35 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:30:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:30:35 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:30:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:30:35 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:30:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:30:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:30:35 GMT
USER haproxy
# Fri, 01 May 2026 05:30:35 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:30:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc711532817ef4432af14019cf27aa5bf6e7af1680ce6a108d70abcc92056f`  
		Last Modified: Fri, 01 May 2026 05:30:43 GMT  
		Size: 1.5 MB (1489536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca06105d60d930ddbdad77df80ea7894bb28bcccf6d6f58e8b6f0d7793a55d82`  
		Last Modified: Fri, 01 May 2026 05:30:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14e2c1687d7079b638992eeffc81792d0d0cc79faa3bf885a7167fb43f2dc1`  
		Last Modified: Fri, 01 May 2026 05:30:44 GMT  
		Size: 14.5 MB (14529822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ec07b6dafe853bef4ad89258a6b8c2a9bd84b5e0ccc443f047ef53e5f176d`  
		Last Modified: Fri, 01 May 2026 05:30:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e30b3a0e84e9714e57cf47d4163650afff71f14672f1ee68d8fd6ea81ff411a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cb6b624147d0d642a8153ac0ae944d45e462fc0fb24862dbcd4c30011c1cc7`

```dockerfile
```

-	Layers:
	-	`sha256:96f740477f04464b7bddc648343140aab97cd601eca8e8166e90671fce7fac25`  
		Last Modified: Fri, 01 May 2026 05:30:43 GMT  
		Size: 2.1 MB (2115221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e735431cac360fec2f64be35ddef18159632dd99543153ee0d48136b0697dc7`  
		Last Modified: Fri, 01 May 2026 05:30:43 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:5491ddf35d08b199aa0bd2a58e91129f6ee6e100469c9e11a0567f4a0b341c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46119196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c573c6e59ee002e4bdf1185594143c5883fce99ebc2c0153224678c9a6f0e7f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 05:29:52 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:29:52 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:30:37 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:30:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:30:37 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:30:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:30:37 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:30:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:30:37 GMT
USER haproxy
# Fri, 01 May 2026 05:30:37 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:30:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0db86d6e9097047f96a9f00d753f485f354aa0a8dcdd51e3930aaa61e3961c`  
		Last Modified: Fri, 01 May 2026 05:30:45 GMT  
		Size: 1.6 MB (1563768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049531d146cacb5bc1c3c174556e0aed0fa59c53826e3cc0a087edad96129c4f`  
		Last Modified: Fri, 01 May 2026 05:30:42 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a4182642893da51e9ca54b1e545fc1c6be81f0f9f611f3611f3d3e0365d347`  
		Last Modified: Fri, 01 May 2026 05:30:45 GMT  
		Size: 14.4 MB (14410184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9373d0eeae288b6182af6f3c1adf34a0ebf223f0377d096ea47c72063af4bcaa`  
		Last Modified: Fri, 01 May 2026 05:30:45 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a1c833dea1d61588d35aae0714bff62555b4f895136eb8ba5b3a8e6237c025d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43b3e728c139a3d7f84b9b21912c9365ecd3049f1a3d4a0f46a815eb9dfa2f8`

```dockerfile
```

-	Layers:
	-	`sha256:f6afdad37c20cb7f4e0a4bdef78c6900e10ac5e07a479cf1e8fc320dcc0811c4`  
		Last Modified: Fri, 01 May 2026 05:30:45 GMT  
		Size: 2.1 MB (2114083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5a62324ff1a6830068f0e523f322d415c373629a0128e3a07fef51e75d817b`  
		Last Modified: Fri, 01 May 2026 05:30:45 GMT  
		Size: 22.5 KB (22496 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:0ecd6a7f5882d248bb3872f17c77e62ad5107d70db37994a358bf850a94c7351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47220143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7886988f96c94d7ed30bd5b9cb972c7ae99db76a84b29b5ac5ed7816c0974c0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 05:30:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:30:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:31:07 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:31:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:31:07 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:31:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:31:07 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:31:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:31:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:31:07 GMT
USER haproxy
# Fri, 01 May 2026 05:31:07 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:31:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9089443bd01d44e6f07f6f567db67ad5007df1281e7b7349cfbcdda75e7a8`  
		Last Modified: Fri, 01 May 2026 05:31:15 GMT  
		Size: 1.6 MB (1603358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0f288b94c3329332b1e7a15c11aa4c001d1463c4c02dd610cd76d1b385e028`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e14a47418aadc620d4c6cd17a94866fc97b5865fa3698611c5cb6a44197419`  
		Last Modified: Fri, 01 May 2026 05:31:15 GMT  
		Size: 14.3 MB (14318818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bcce627ef6ed1b251c1010f54f31899e880f22d973b72d3d93a48ff4a0acb6`  
		Last Modified: Fri, 01 May 2026 05:31:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a20024a378f5390bb2725f53319865de9a74d8cc5f723691a227d8be28a338e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bfe7c0d8228e05aed7601216f7e2429c57aa6da9289dec071fb28750214380`

```dockerfile
```

-	Layers:
	-	`sha256:b650416eb36c11d16fce6cedcfc2cee656369c5307e9f3a7ef097383c015a599`  
		Last Modified: Fri, 01 May 2026 05:31:15 GMT  
		Size: 2.1 MB (2110979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b751e8ba257aa7e804b9c4c39fd5a0adc30c89c1147ef56be667dd9ecd1c2d34`  
		Last Modified: Fri, 01 May 2026 05:31:15 GMT  
		Size: 22.3 KB (22292 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0f3be9d8d891edb5672857e142da734e40dc9b7d1b585c6a0c294b723d9c8e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50514682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2b5f2098d51c42eacc8ed1dd9bd1fbbdaccfbe3eabba696a542481828f39be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:23:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 24 Apr 2026 18:23:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:40:26 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:40:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:40:26 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:40:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:40:26 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:40:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:40:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:40:27 GMT
USER haproxy
# Fri, 01 May 2026 05:40:27 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:40:27 GMT
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
	-	`sha256:2362749b88184676c9bc4442b55261ecbe50d18a6a4fd8aa81daf440dc1134ec`  
		Last Modified: Fri, 01 May 2026 05:40:43 GMT  
		Size: 15.3 MB (15275855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98296a643997457eb62e0e07c9e215ef24b66637700ad262c496f16a2396ba1c`  
		Last Modified: Fri, 01 May 2026 05:40:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:3c2f968049559cde79434e49b5abbacd6c622b9a1740e4f127bbcc4a8703212f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02c27bc8ac5208c5816693c56d7903361f1daecb2b92878dc4a3d67d46301bc`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf7ce8978013852b46a77a70a9f7f390c03deb7ec5dd5f28a7e5c7d39b9e08`  
		Last Modified: Fri, 01 May 2026 05:40:43 GMT  
		Size: 2.1 MB (2117344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481195562da0fbc6b320d71802a7ae1fdaf8e3d909b37f5b36289d007d6b8761`  
		Last Modified: Fri, 01 May 2026 05:40:43 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:97062e7a2bb397866ce449f9409a46415f340a36a6a4aea861d3bc8398cb2b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43827902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88317d0105ca19581f1008194cd43525e54b49cfbc2df6f161475c1e8f08a5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:07:34 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 06:07:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:47:02 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:47:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:47:02 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:47:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:47:02 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:47:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:47:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:47:02 GMT
USER haproxy
# Fri, 01 May 2026 05:47:02 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:47:02 GMT
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
	-	`sha256:fa1c1e3e409a992cfffc6d145091d11ee059934d721a8e950b397830b2fa5d79`  
		Last Modified: Fri, 01 May 2026 05:48:10 GMT  
		Size: 14.0 MB (14010622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ac42eeae1a57278c03a9ba722b3efa61bb2086fee3bfd4fec697188e9b6469`  
		Last Modified: Fri, 01 May 2026 05:48:08 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:92c3799dd8f5646687ffe7910af3339ee01a15a3d831cbb2f660413ee2d4db7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15e21d5635e2e61011db818d61523aec1681d4ed0759b69742cde18e2230e1`

```dockerfile
```

-	Layers:
	-	`sha256:814761828e310a517a256fe87e53b3726d505cc55cfdb20f8abec52334e6a3a8`  
		Last Modified: Fri, 01 May 2026 05:48:08 GMT  
		Size: 2.1 MB (2107735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd374bc8ee4203548e8e7260740474902417f42d5e9483542f08e206741a603e`  
		Last Modified: Fri, 01 May 2026 05:48:08 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:0796de4307ab6cf6e8386890729850668d158fa481e14e17dba27231cdfb62ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46374637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2e18201a11a5ad2769c76d16840378646bc67bd6ce47047e6ec9efb57d766d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:03:40 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 29 Apr 2026 23:33:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:40:08 GMT
ENV HAPROXY_VERSION=3.3.8
# Fri, 01 May 2026 05:40:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.8.tar.gz
# Fri, 01 May 2026 05:40:08 GMT
ENV HAPROXY_SHA256=89b1fe73d54d5990f74997da837f5fd0da1627a1baa62b26f5d358a6f3c48295
# Fri, 01 May 2026 05:40:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:40:08 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:40:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:40:08 GMT
USER haproxy
# Fri, 01 May 2026 05:40:08 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:40:08 GMT
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
	-	`sha256:84ecc08350b91c4092b6ecb7113adecd96a3735760b6c66d25346edd0cb1000e`  
		Last Modified: Wed, 29 Apr 2026 23:34:21 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55597864ee617b754447112e0b72408cefcfcf200a826dc3d3ea076b245f497`  
		Last Modified: Fri, 01 May 2026 05:40:20 GMT  
		Size: 14.9 MB (14932691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460408dc9436354eba1a0124b081e0e70b1753c6cb438255cb884418710123f`  
		Last Modified: Fri, 01 May 2026 05:40:20 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:9ac65c0c22147dfca86672f72e52894709c7bed8c9f1b27a9a7b490a636ba402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f01fd288144181d498ff87bd6aabc1523b1d1ea2a8d9be3dc506da5718f13a1`

```dockerfile
```

-	Layers:
	-	`sha256:01e73576e3b3a72a66b35db0e00b2d314fdbae956c66e8ced6a1b422683dd6de`  
		Last Modified: Fri, 01 May 2026 05:40:20 GMT  
		Size: 2.1 MB (2115242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1af34719c46c226358d294dceed40a47adf329b8660b8994e4fdc63a901f13`  
		Last Modified: Fri, 01 May 2026 05:40:20 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json
