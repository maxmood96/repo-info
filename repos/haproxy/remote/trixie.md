## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:2872964b3c356c91a193282d66d7cb623c95f16e421fb305e461268ea23bc846
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
$ docker pull haproxy@sha256:4182ac20964b95525571c0d4ec5b7426bc16a0df7e0c69f92d40a2dbfb450e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45709180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cf5fb48f1b25b955d6f5407066a5a8bdff42a795744ff6218dbfa5fa5e4eb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:57 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:52:57 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:53:41 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:53:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:53:41 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:53:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:53:41 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:53:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:53:41 GMT
USER haproxy
# Tue, 24 Feb 2026 18:53:41 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:53:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8efe1202b0f1326eb239d7c090957b35caadf62e4dc23b7a86f6d1f04ee31`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 1.6 MB (1580888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf6ff5eca99c0c22a01fb03cae2777e7b8194afa73754fd7995149aa4714616`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a855ea611497d7cd578641f6a9cbe81580a69b429c602cfaf892c15bca54fe0b`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 14.3 MB (14348020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25983eec19c5a9ae9f5eaa709e16a6256f7a023c8d0d4b42ee5652a41e762324`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:8796afc61957cf081d0941221fa6a05f3c0f3377534e4f157a2a82bb6c7cee21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abab67c1761c2fe7139865ea4a169dc79d17b86e7c1fd71750d3a5cf3b2c1fdd`

```dockerfile
```

-	Layers:
	-	`sha256:43002ab12250fce5d88920f0e14704c127addca5a1ac711567b30166c28a7daf`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 2.1 MB (2113762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c1d6b48b3fadc420e999bdd8379191e7a99ab112343515e7ff82373df00938`  
		Last Modified: Tue, 24 Feb 2026 18:53:48 GMT  
		Size: 22.3 KB (22338 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:84822fe4ac4283ccaf919c16f2a0e442c1effde894a863a9dd5ec84fc0b6e5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44023126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9854cd05fffce7278b65302c8d2d1e8be8162c2d11bf20fe546406a2585b747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:54:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:54:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:56:46 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:56:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:56:46 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:56:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:56:46 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:56:46 GMT
USER haproxy
# Tue, 24 Feb 2026 18:56:47 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:56:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4367fd6e303c94c5fa797249cfe00066d083e97fc095e1dc46214c312ef37b46`  
		Last Modified: Tue, 24 Feb 2026 18:55:42 GMT  
		Size: 1.5 MB (1534896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7742ca66fb05f78b354df1cfa40ecaae732e0ec972a6ef688112d5a47df31ec`  
		Last Modified: Tue, 24 Feb 2026 18:55:42 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b6ace0cde49c189fd6e1d538deddd9ef353038a0a56d8a2f90d74df9011d11`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 14.5 MB (14538982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f833964a67f563cf498ed9a8eb645cbd88e036632b1333bd0e59f567fd476e`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d6e92b48594e4da97d4849ef8d59564bc6d30106a44bd887d66eeea8e70ca185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c509968fc7666a753ec15a7d2ad6e2a2b62c1884eebcb4f118c310a847e477d`

```dockerfile
```

-	Layers:
	-	`sha256:be310d0193e92a6119c85ceeaf0d62497b75e13ee6c9368a0285c388e08ae84b`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 2.1 MB (2116742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85748419d0b3102366778080cf0e2dd40231cbde393f246f9b84721b85e2d66a`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:e5fdfbc6d59417d66d479b616f010ed3fc3a64c641f22116ca4a16df86e05a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42045252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7de3becabe8772ea8e9cb5cb1e225f1ec9280c3d44d5ae841c9d2f649f7f5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:58:21 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:59:10 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:59:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:59:10 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:59:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:59:10 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:59:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:59:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:59:10 GMT
USER haproxy
# Tue, 24 Feb 2026 18:59:10 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:59:10 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c70fc8661993025e908c849593b0ca3f940389b7674bea8758d130db3baceee`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 1.5 MB (1488922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8851aceeed9483de352617ab16035b878a9776ef42bc9f97e1916edf825d4d08`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e592332dfe88e2b1c0192a0059b495c26eee378da567664b3b2f49c453b4eb4`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 14.3 MB (14340945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9522f0f3db85fbc9ff65e986127a9e890a0afd8995b4da2d3d0ef5862fedc4c`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0aee983ab079e19e1c8c51d1f8795e2720d60ccce9f6f5e4838174f4e1b64486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349b9bf6aa9ac9dfe318d006adb41146e45df845f656ecd8bc90e4cc1308928`

```dockerfile
```

-	Layers:
	-	`sha256:f8cae9d56f0faa06865053a26bcc9ad9ca9dc05f55aa5c189d6071dbea2df9cd`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 2.1 MB (2115185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29976cd6717f29b7afd7e2c92744284bc124e40a4a7da41fa6066a964ea82b47`  
		Last Modified: Tue, 24 Feb 2026 18:59:18 GMT  
		Size: 22.5 KB (22460 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b6a649c6931d4baf970a1500386203d77d4a2495e12f722e25136f5a2efdc95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45924628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69562458114fc86e8bf6d9729d1393ecec3a4756c24c626378287548bec11ef6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:32:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:32:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 20:33:03 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 20:33:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 20:33:03 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 20:33:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 20:33:03 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 20:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:33:03 GMT
USER haproxy
# Tue, 24 Feb 2026 20:33:03 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 20:33:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1349c74063ca7523693cc3f847d8dc880fabd0181a0d92ca7e41edff2c6f6391`  
		Last Modified: Tue, 24 Feb 2026 20:33:12 GMT  
		Size: 1.6 MB (1563180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bed29864982e44f9c1c5f3dcc2bd4f900343ff7e01db45365b48ac45609a3a`  
		Last Modified: Tue, 24 Feb 2026 20:33:12 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313e5f147ea1e027d5ff48215922eb218fcbb4620f17255e309eff8266412c09`  
		Last Modified: Tue, 24 Feb 2026 20:33:13 GMT  
		Size: 14.2 MB (14219710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0840811d400a0b8740a358d819639e0951de0cbc6205ffc1d019e75872dd41b`  
		Last Modified: Tue, 24 Feb 2026 20:33:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:bb166a2cd887d2948ec786f77ea7256c93349ad0518d27752831e0953773c332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7161677fdc74d2f957af0d17c891b2ef418da9bd429a07050300292638f9d7`

```dockerfile
```

-	Layers:
	-	`sha256:a3af084517f758c579195b1e4b1ef7fba87dbab4570e391625738c0de698a3a6`  
		Last Modified: Tue, 24 Feb 2026 20:33:12 GMT  
		Size: 2.1 MB (2114047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e923dcaf899dcea382d8be69f2d98fa83fae08b1e6f70ea042b539e0126a4bf`  
		Last Modified: Tue, 24 Feb 2026 20:33:12 GMT  
		Size: 22.5 KB (22496 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:8c4e05aec72710578dd48286e357ec01713326a7f6bd8c86c1c2262d2a199fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47035166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d498d43da391bd1e7b15b0020570e9b765047dc8dc183f8bfa6d0d8e36f8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:55:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:55:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:57:16 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:57:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:57:16 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:57:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:57:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:57:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:57:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:57:16 GMT
USER haproxy
# Tue, 24 Feb 2026 18:57:16 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:57:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85360dfd1b11c93374cbe7700f51c052e50f6178f4669a5149d11a9c61a279a2`  
		Last Modified: Tue, 24 Feb 2026 18:56:22 GMT  
		Size: 1.6 MB (1603151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1b124d943b510a88d915a6264aed3fc16c0add7dd19428c409a933f7f3ea2e`  
		Last Modified: Tue, 24 Feb 2026 18:56:21 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd070a6ce37b0e4299f05629d6043b68f051bf206442e1e2dc6521da9a7523c`  
		Last Modified: Tue, 24 Feb 2026 18:57:25 GMT  
		Size: 14.1 MB (14136454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5e7ec5491b3af3de0a53f9980b9646b37992a3f4c422721d1e242a09027056`  
		Last Modified: Tue, 24 Feb 2026 18:57:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:af5758d36fb57583774ac957971129731f61de06b148125cd5d4dae13d990d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd51b4d5f14ba9f44e15d907f7263a54125b3d0beb5e808f1567bc9e383ef71`

```dockerfile
```

-	Layers:
	-	`sha256:08f2ae1411d0e5b2a008c9b692fc72b84122b3d4d79b7e3dbe7a211f2f7f71ec`  
		Last Modified: Tue, 24 Feb 2026 18:57:23 GMT  
		Size: 2.1 MB (2110943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd291e5fc6a31016a5d2170ca0296a811b199f47d67980c4fe654c1fa784e2b7`  
		Last Modified: Tue, 24 Feb 2026 18:57:23 GMT  
		Size: 22.3 KB (22292 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6b1aeecc15f93cd38c60abb13605380ee631e02dbb84ff740a38b562515885fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50312628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6f9bbc82e3e058557deeb0c496bb53cf8d3a88b9ffb81dea8bf58bdd8f14a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:56:45 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:56:45 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:58:29 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:58:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:58:29 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:58:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:58:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:58:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:29 GMT
USER haproxy
# Tue, 24 Feb 2026 18:58:30 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:58:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb569d4cdf73275b0f9928916fc94fc9f6bed23e006ee4fe505204c8ba710fd`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 1.6 MB (1638813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aad80bc3253c69fac51646fff38bb785f1a5773e13a6c0151f2a8b102491d7`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e956a1942b4dd15bf16d6c4fdcf748f41e8763f2517c1bd91fd5964b42671985`  
		Last Modified: Tue, 24 Feb 2026 18:59:04 GMT  
		Size: 15.1 MB (15071960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b461eb8cd67402d32a9bb0480de8cc9cc1fa72b7f6447344c326809be316114`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c2d24b4ba25a8cacda439c31b32d6e746555e06ee6158747970d3ce5f005a9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e488eb7c194239b3488c7c31a207b6f3c95794a48c7a653262c9ee3853605da0`

```dockerfile
```

-	Layers:
	-	`sha256:3f4c70e09e7f25bbd3704d42faa6f1c8aeb121619167a4073e962b74d66d0053`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 2.1 MB (2117308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b1257a8ce71539980bd16bfa141fc803bb6af93d2cce9dce2583615a3cc363`  
		Last Modified: Tue, 24 Feb 2026 18:59:03 GMT  
		Size: 22.4 KB (22397 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:53ff08bd976ec4a09f03d7e9d22ae61a81d9ddc3cead8bd4e0f99e7f9a6bca33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43621398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348c59878ecec3cebd105ced610f14f1425a720d1b0279b64ca91e414e7f0efb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 21:27:27 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 21:27:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 21:27:27 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 21:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 21:27:27 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 21:27:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:27:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:27:27 GMT
USER haproxy
# Tue, 24 Feb 2026 21:27:27 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 21:27:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96667720c6f66d54c4069d1f4a90a9b99842eca810ad17a3c151ac557902e5f5`  
		Last Modified: Tue, 24 Feb 2026 21:12:01 GMT  
		Size: 1.5 MB (1535095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1449ff18173ad675507b1278e800bb7a82b1db725d4424087ede9e6b7dd711`  
		Last Modified: Tue, 24 Feb 2026 21:12:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa910afb86572958160e30ac107aeb52ff05573c9c33e773360927249e4f4e1b`  
		Last Modified: Tue, 24 Feb 2026 21:28:36 GMT  
		Size: 13.8 MB (13808242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13839f94563246773217a5e2ef9a21c931bce8984165207c528adf7fb3e83b3`  
		Last Modified: Tue, 24 Feb 2026 21:28:34 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:44c467296190ebdf64c35a6164973ef160bf19e5455a28428b1f42d18a091bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559cb85294735fe4844c40901ed507910e516d6e606b9cfa1c16fe945323e1e7`

```dockerfile
```

-	Layers:
	-	`sha256:1535c51b01062b64bb8a9ba0b65e604a57e1c820c2e8bd8a5addc025a2286c2c`  
		Last Modified: Tue, 24 Feb 2026 21:28:34 GMT  
		Size: 2.1 MB (2107699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6ea197d95475382cb14e0862a668c95f8445da0702d16c5f35fbcb080da267`  
		Last Modified: Tue, 24 Feb 2026 21:28:33 GMT  
		Size: 22.4 KB (22398 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:a7cd995cf784475648c1e8c4cc4270641def1846df3f7c5bbf4035dc11fe5e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46169927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c00dedc21fb0e1d78eaf2a8e290a2e653e46bdd0f8dec174498f37830a0dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:54:57 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:54:57 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 24 Feb 2026 18:57:25 GMT
ENV HAPROXY_VERSION=3.3.4
# Tue, 24 Feb 2026 18:57:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Tue, 24 Feb 2026 18:57:25 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Tue, 24 Feb 2026 18:57:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 24 Feb 2026 18:57:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 24 Feb 2026 18:57:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:57:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:57:25 GMT
USER haproxy
# Tue, 24 Feb 2026 18:57:26 GMT
WORKDIR /var/lib/haproxy
# Tue, 24 Feb 2026 18:57:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0ec2935c71a494d5f132306e901bbf22107471f29bcee0addd2d6daa55edfe`  
		Last Modified: Tue, 24 Feb 2026 18:57:52 GMT  
		Size: 1.6 MB (1599702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d1ef72ccba8f0f83834877ca1cb19df89b7979e6dbbf52ea58c13db210765`  
		Last Modified: Tue, 24 Feb 2026 18:57:52 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d9e0515e8c8a69e2480834be9fa1781d749367f4063d367b8f16c31e9ded2b`  
		Last Modified: Tue, 24 Feb 2026 18:57:52 GMT  
		Size: 14.7 MB (14730406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd2b404cb962694f27e5e609c9d8ea6c100f6ee5e72971e56de07fe65fed79f`  
		Last Modified: Tue, 24 Feb 2026 18:57:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e243a4ae89929ea7d217cbed4b25baa6f615cabb22daafbbe9e3ae3a15c710c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8657fe1b64189f74bf1c838aa2cfe9c590288cc3c838e7b67b4db8a0222e80de`

```dockerfile
```

-	Layers:
	-	`sha256:454170611274071d09149f93599350b6c3cda452e561b80d3348b5a5042a9ef1`  
		Last Modified: Tue, 24 Feb 2026 18:57:51 GMT  
		Size: 2.1 MB (2115206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e12bf459658472eb7bc91acae076382e215a1c9b2ce228b0409d0ddf5e5c08`  
		Last Modified: Tue, 24 Feb 2026 18:57:51 GMT  
		Size: 22.3 KB (22337 bytes)  
		MIME: application/vnd.in-toto+json
