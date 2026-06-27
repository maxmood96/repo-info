## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:0f597665a2a6d57f5a52fe81166fa781281ef54a771a9f9b4ff0567725be637c
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
$ docker pull haproxy@sha256:b11da2976f89c1dd925c1c725688da3bf4e2d144466aeb37dd48ac65553ad82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47063570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41b098e4d2e69ab52ff30e642bac3bdf9d51366a7e475d2f8b0afffcfeab25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 23:25:52 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 23:25:53 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:37 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:37 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:37 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:37 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:37 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512e40f0b987ae6562fbb5c1ef8c3bde1291a77557095b5b417bd75cfb0fa6e1`  
		Last Modified: Thu, 25 Jun 2026 23:26:44 GMT  
		Size: 1.6 MB (1581343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e524b5f1eb34dc4f2c732184f1c52e59d492e7efa03549bb3cf345ea19c107a`  
		Last Modified: Thu, 25 Jun 2026 23:26:44 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dfb9061d95adf5de038d85273df3f4d48bc034d23fc732c34cf8c6caac3827`  
		Last Modified: Thu, 25 Jun 2026 23:26:45 GMT  
		Size: 15.7 MB (15695163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556bb8734093139232a741fd3942a9ae9ad1cc208f3c490c131b5412ae1964e`  
		Last Modified: Thu, 25 Jun 2026 23:26:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1f54ed541652beef8ebbffff2283a84214ddbe5dbe3db54b2b4d0fb022fa9746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba4bc7239de0119d5b3e5eec7e0d0f9707181944ad549a50d66d3a2c6e97d2`

```dockerfile
```

-	Layers:
	-	`sha256:4cd1f1797644a7f72c213e31bc579b70c4d6a62ad2b3b1012166c627b2d6d599`  
		Last Modified: Thu, 25 Jun 2026 23:26:44 GMT  
		Size: 2.1 MB (2114442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae441433f07d40b68047586d9ab0e86532b21a224b7d77b0125b2d651712e83`  
		Last Modified: Thu, 25 Jun 2026 23:26:44 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:5241eb52f56369373fee40c1fa6dbb66833efeb2934be727a19418a11308a208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45406549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54445cd61367d25d943a77f670efaa74503abf3cfee951441b16b32060609984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 23:25:52 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 23:25:52 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:58 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:58 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:58 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:58 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:58 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d9da04bd9a0209b19865378ca1fe05a318615849ac16be4219b4678cc93254`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 1.5 MB (1535945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5436b41f1025934ec45067b8e2fce9f3710b33f24fe2fe7de0e7d3d77d2b81`  
		Last Modified: Thu, 25 Jun 2026 23:27:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6c6bd18a5701b9db0fd30dfa08629fa8c99f873d5fcdb331df4fba3acc21fd`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 15.9 MB (15909745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf5346b557ae52dcc6da7c2898025ff5b7d81815a9c6ea33fac7f7ef66dcae`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:9b32eb385470e84a24b9683739beb6d03cca95fff79c37204770378f591847c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353181c21211ad056cc85016170a687f439447fac1985d9fe23d2fb843c5fcc6`

```dockerfile
```

-	Layers:
	-	`sha256:45cea245e787d8fac08b795787a589c375d4360fcb11c01f024445e8a67b4037`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 2.1 MB (2117438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e133553902f80cfe3cc2779f86ccbe53c261d56812ca1b0539232da422a91d3b`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:3499e4d724048e1726073b035900b8a5b687510dc8568fc9b2581e1a1385f83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43394894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89963985b5f70270084ea90d369926350ebc04718e4f4e902e3d4d49b0528db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 23:25:51 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 23:25:51 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:45 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:45 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:45 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:45 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959e778666866699f13ec077aae71d1f95b54a566b4a67656bb3f575ae7ed5ef`  
		Last Modified: Thu, 25 Jun 2026 23:26:53 GMT  
		Size: 1.5 MB (1489662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cc4d30843717de425a52e7a1ba70f24f8f75f000c4d9151e4b532711416539`  
		Last Modified: Thu, 25 Jun 2026 23:26:53 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d3b712d7b9e90c1e4caa0c9d3a624e7e70ffab3d582db888f3983c4244348a`  
		Last Modified: Thu, 25 Jun 2026 23:26:53 GMT  
		Size: 15.7 MB (15692543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b9fb1745eb419331dfdcf5f396e63a00efecec384b527808646ac4261c456`  
		Last Modified: Thu, 25 Jun 2026 23:26:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:405738f2bf0df5e5d522d32c8834f867177c492362fe5c66b938a419069da5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41ad99e6cddb060cc9d53bfc23b3c05411f48718ec0f67a62bb16e95b8f7f7d`

```dockerfile
```

-	Layers:
	-	`sha256:1586abf03eee7d51437a5e82cddaf208424a599f8ce43c1c94e008f4755ab8e6`  
		Last Modified: Thu, 25 Jun 2026 23:26:52 GMT  
		Size: 2.1 MB (2115881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06029514d0ba611644b37357b1e115ee746baabbd5448061b64e36014249d454`  
		Last Modified: Thu, 25 Jun 2026 23:26:52 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:9d5b061bae7c11690d3a47c3009ee26e0b6e469219753a712243821ecdf9b105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47281508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5532b357612fe10eee9997f5df8b40fb8619bdb55fbf3df6f6578895b611eb3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 23:26:26 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 23:26:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:27:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:27:12 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:27:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:27:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:12 GMT
USER haproxy
# Thu, 25 Jun 2026 23:27:12 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:27:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69f821234b456250fd1a4b18a3929af94e4d0c0a98262e9c853c0563c667daf`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 1.6 MB (1564020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a492d55289bdbb31332f5647403272c1864c443901f3e4a6d1b9f20fadd0cee1`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b7163e0cd6eba22c34ac7ae0682367f8bcb7b742cc1182cff57f56af529ff9`  
		Last Modified: Thu, 25 Jun 2026 23:27:21 GMT  
		Size: 15.6 MB (15567297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4919cc80b12a345813998179fe412c1758ba316fab7887b539bd66b0350a3479`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:33d9cab4ed351ffd3a279fe220406257436505fca05fe185f64a6e0a73133983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cb7695210ea8d3b126fdd0d792f195831db6b50c953d9f06fe2666fecaf784`

```dockerfile
```

-	Layers:
	-	`sha256:6f691a173b1f9cde3f525b6169c3e90ab6abb1eac143b58e3de44518dbcf5669`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 2.1 MB (2114743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76b136b8d88ad235b543170e401c7293866e84e469f636d03fd1409cecc0db5`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 23.1 KB (23121 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:44202459d6f6b3eb0daaf7bd6feafff85ab5f1349b55a2c26cc1f2fdb8cd3277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48362821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d2a9cd10f4dedaa917bc65c2f884dc7fbb6488b2b6a8e7a072f97643b53418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 23:26:04 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 23:26:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:26:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:26:55 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:26:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:26:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:55 GMT
USER haproxy
# Thu, 25 Jun 2026 23:26:55 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:26:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e051adde237bc9e1ef512a349de4985074457059bb8773567ee0dc3877d76`  
		Last Modified: Thu, 25 Jun 2026 23:27:03 GMT  
		Size: 1.6 MB (1603827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54c37161191ccdb2d0111eb10fd9df5c6ff21525dac43c34dc5dd510e737c8f`  
		Last Modified: Thu, 25 Jun 2026 23:27:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed411e40053cdbf12a705df223d309c17f246f9b26fc4aa5983d86d6dbc2dfd1`  
		Last Modified: Thu, 25 Jun 2026 23:27:03 GMT  
		Size: 15.5 MB (15456143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89def55740db1cd055508760438c3e6fbae9af3f5479b3135f4b79c070f49408`  
		Last Modified: Thu, 25 Jun 2026 23:27:02 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a3d4212334017b7e0aca9f4ebee2c16120537c93d0b4a14a1cc49333dbfe2eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee5ab9edb59edb2378267ba726eea3727b34685f7df9687404577cc856a504e`

```dockerfile
```

-	Layers:
	-	`sha256:fabc583c1e90f7e03159d191e7ef997a31672c4c83f94ece32b12654d4fbb0c8`  
		Last Modified: Thu, 25 Jun 2026 23:27:03 GMT  
		Size: 2.1 MB (2111613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d2a13e29ec90b1562ea8bb38f0778fa83d9a2b1ac6ba83a9349375f8c23d07`  
		Last Modified: Thu, 25 Jun 2026 23:27:03 GMT  
		Size: 22.9 KB (22884 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:76f65697a9ae53c810d627e0f51aefad70a489b592e54ad8d2eb5596a46b74fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7294d2e97a5170d1c4a06031e2dd9853a19af174e4b9a3b2ebd9b71d2a91afd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:32 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:16:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:25:57 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:25:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:25:57 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:25:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:25:57 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:25:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:57 GMT
USER haproxy
# Thu, 25 Jun 2026 23:25:57 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:25:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdf48770d2ce4f6d2ec7fdca2214c67bee013812202b7495a65f8975916b4cb`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 1.6 MB (1639536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f20c5b6c932d79067aaf227b5db380011b0983b51497f83f05ba19c64c6c68`  
		Last Modified: Wed, 24 Jun 2026 01:18:44 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fe2292e8b00c8d51af50d19cc2412f982864a6b6195aaf8f0d5aa5df62ac8b`  
		Last Modified: Thu, 25 Jun 2026 23:26:11 GMT  
		Size: 16.5 MB (16474064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e5d13602f9aa462b4358499830c5d6a5a0dfaf83534cc25f8b292fef55108f`  
		Last Modified: Thu, 25 Jun 2026 23:26:11 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:32aa56cc91f2450e549d53872e740e69b9c17aef0c4edae87ab15ef4dc270e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0829454fdda01071351cb15f10e218b02e23841cae1739da44d54f20a23f2dd4`

```dockerfile
```

-	Layers:
	-	`sha256:793b033a67fc16c2ba7f9ba3ad9a550dcb14051fb099686b57a915ae6c639a2c`  
		Last Modified: Thu, 25 Jun 2026 23:26:11 GMT  
		Size: 2.1 MB (2118000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b1d81f5b48f8e0c8d9bea6e2a69e04b120f0647bfd40281f94ede9865f5c11`  
		Last Modified: Thu, 25 Jun 2026 23:26:11 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:476520058784dc3af6ee19fb1776df58eed2f1967999a3d595f24755863c2678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44950272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c62a18b6b58c59db3881b118b4c072fac8c7288df20e3941815c964285fa8cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 18:43:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 18:43:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 26 Jun 2026 22:40:52 GMT
ENV HAPROXY_VERSION=3.4.1
# Fri, 26 Jun 2026 22:40:52 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Fri, 26 Jun 2026 22:40:52 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Fri, 26 Jun 2026 22:40:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 26 Jun 2026 22:40:52 GMT
STOPSIGNAL SIGUSR1
# Fri, 26 Jun 2026 22:40:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 22:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jun 2026 22:40:52 GMT
USER haproxy
# Fri, 26 Jun 2026 22:40:52 GMT
WORKDIR /var/lib/haproxy
# Fri, 26 Jun 2026 22:40:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37465baa1f8cdf556a89cc741727534d7616ce29ccd10dc3358664061d0bfa9a`  
		Last Modified: Wed, 24 Jun 2026 19:00:49 GMT  
		Size: 1.5 MB (1535641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59c90bab2f81d28789abcfb722db18b66d9294f43e5afa2290cd87e1e4cab6`  
		Last Modified: Wed, 24 Jun 2026 19:00:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5ddfaaad1fac2048d57b6664ce40c63e967cb430e342d1a93c0437a0842d3a`  
		Last Modified: Fri, 26 Jun 2026 22:42:06 GMT  
		Size: 15.1 MB (15130610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a352d5364833364748da2e076a992e17eb6955ae348e03923089cb9eac6e0b58`  
		Last Modified: Fri, 26 Jun 2026 22:42:03 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f2a6587cd683c8744d91b99b11d3a589a87b0284276f47c619a8e01ad717bcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd83bdbe1337045f04579d7bf6aac84c5e75d39104a55199a41e973b3a5787c`

```dockerfile
```

-	Layers:
	-	`sha256:e6f73f5aa48d1a1881ed5f163ae26144c0d77a1d38de4ded5013d28382051988`  
		Last Modified: Fri, 26 Jun 2026 22:42:04 GMT  
		Size: 2.1 MB (2108391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c62b8d21363d0f7fa1958bee77c7e3c3e47f9c2db503966247f8460cc94f21`  
		Last Modified: Fri, 26 Jun 2026 22:42:03 GMT  
		Size: 23.0 KB (23012 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:ab5ae72bbe91efc1e7a8665d346a221db0d88bbcd3b74c7c119c3830fd8614df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47570309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c98899d7b74e2e1e89e29914ba586aa0c89e9ebe764052c47c6dd6602f3ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:14:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_VERSION=3.4.1
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.1.tar.gz
# Thu, 25 Jun 2026 23:25:43 GMT
ENV HAPROXY_SHA256=2e62c4ce4fd77d3bc7cf17e586431663454456a078b7c8465b8f0125b5bc22f8
# Thu, 25 Jun 2026 23:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 25 Jun 2026 23:25:43 GMT
STOPSIGNAL SIGUSR1
# Thu, 25 Jun 2026 23:25:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:25:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:43 GMT
USER haproxy
# Thu, 25 Jun 2026 23:25:43 GMT
WORKDIR /var/lib/haproxy
# Thu, 25 Jun 2026 23:25:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571fe387244ece97a67132849be88945ea722f7cf59012e29a90cfeb8be37cab`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 1.6 MB (1600048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b6aaf775d0d4d265485a3b1df8a681a624169b326101b832c46f2aeaf75e9`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f14a5a38251b5bc9fab8cc61cf64a0beae1a8c37545171571f96cb26cdd99`  
		Last Modified: Thu, 25 Jun 2026 23:25:56 GMT  
		Size: 16.1 MB (16117239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffe5a6ffd9199f068979994600ce144db863fe6eb9a4ccb63e5cc6379037ff9`  
		Last Modified: Thu, 25 Jun 2026 23:25:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1ff884e3d266eec4f3fbbdc6ec2671cb30cc9b959515427c27a59386302c27e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fbc6ce9e105f7e8519cc9660c3d142af56d866ac6fa47ad83c22096b26eebb`

```dockerfile
```

-	Layers:
	-	`sha256:41adc1169b8739038e7b57c67ca4727d39f68da16fbc63a0664a54aa47efbd41`  
		Last Modified: Thu, 25 Jun 2026 23:25:55 GMT  
		Size: 2.1 MB (2115886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568c3dcdc20cc2b7853e7ac88af2f636fd7b1aadf86fcffadf116e36d17ad786`  
		Last Modified: Thu, 25 Jun 2026 23:25:55 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json
