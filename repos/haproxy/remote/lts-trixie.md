## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:5126fe31035ecd371a8317f955c2a224c6e01d506379427615a549139d0e1616
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
$ docker pull haproxy@sha256:549dc8fd74bcbc20355307de2953ed1924674550b9625e3a3a00bd2008cd75c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44493633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d3e55a8c702c548691b36b46ec7986bae43d2143df6a5c9ac99742d1b2de22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:33:36 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:33:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:34:21 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:34:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:34:21 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:34:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:34:21 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:34:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:34:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:34:22 GMT
USER haproxy
# Mon, 09 Mar 2026 18:34:22 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:34:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4afe7294798f837507a48a71c98043766c6c02be43cf12ab87f0e14bc6c69`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 1.6 MB (1580853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230ede694085ad331aef52af5559de272ebcbcef135a289f013e4064968d0d16`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a7a33f13e909e5052bd827981882fd55a0dfadc73cf6fd92ae5b02a67ee444`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 13.1 MB (13132508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6989172978a26c13e7b0d1b57c42e5514cef4fd5b13c2af97a67bce7b55a7de`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:db72de3145f8485dad91d0ec28f76641bf6563046fbfebbdafad033de2c3fb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782bbfc15ff20de9309d40d1669b711e0bced54fa768f04828e5f191c2d7eb05`

```dockerfile
```

-	Layers:
	-	`sha256:6ae3e37adcb832b11e55a12cd93b5cd4043ca7967275855193c6dae3c8dc094c`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 2.1 MB (2113770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6e517f1a0e4d4350635adb281c38e2fa53340afe21c25915b5bf8dcfaaebf0`  
		Last Modified: Mon, 09 Mar 2026 18:34:29 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:09738f1af5c5adde20a1cf246ce0737f17715860558e8df26deaee1f74cb58cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42762195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf71e6d13e58eb00e728c7d58b7037f852da7ef924b77f4c709c7d561597e93f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:49:19 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:49:19 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:50:25 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:50:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:50:25 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:50:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:50:25 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:50:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:50:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:50:25 GMT
USER haproxy
# Mon, 09 Mar 2026 18:50:25 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:50:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5ca60452d87a212120c43d96d89a6cb57ec7e84327deb7a6b3445103cf1c48`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 1.5 MB (1534851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e8343b3e789af821355f891bba262ebbedd429663353c3e2ad34683c38e1b0`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266a5960a06e23fb3695a36774e92f0f3e8187c10781635611f2ab53e8afba3a`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 13.3 MB (13278094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92132155c168356bd2a8252273f2d66f62a9659ae5f336d539dc616d1849f09`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:59925ac7e610bb3b0aa5c816b909f258961a3ea3869f3a62be5ee58fbe96b587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3885ff6c09a9a600b093440508edb3b2f249b4b02755ff0159288325c8b448`

```dockerfile
```

-	Layers:
	-	`sha256:edbcf9dcddfadaea3a6f6d87a29a4ba2a9bd5770ed7143a725d695eee414f966`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 2.1 MB (2116750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fc430fd575605dd933a06a0b7d03e6fa0ac8e895d8714d1a81e9ec09ab0e37`  
		Last Modified: Mon, 09 Mar 2026 18:50:32 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:2eef36d2ededf7b629073a8bd795f1aab038afa85b6a3bdd55377f7b2ff6e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40739119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a894eb0664f794e270b10d9d7937f4785e81bb783688452263d5abe486869c7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:50:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:50:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:51:48 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:51:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:51:48 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:51:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:51:48 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:51:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:51:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:51:48 GMT
USER haproxy
# Mon, 09 Mar 2026 18:51:48 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:51:48 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a545b3fc51b8aab224259967b39a7812ed08a9601d194ece163397c9ea19c3f8`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 1.5 MB (1488920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b01589178e3605e275d5e8fcad6d0dbc121e9d1c4efba0fa338a11120b2b1e`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4f520756dbf78253183f5f13dd92fa64fb9ac7f3c05895885dd2fdca0119f6`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 13.0 MB (13034811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a329ed73175b4ad57bdfe492b84cbae6bcae461b25ce66fdfb4c51b81ab0c7e`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:97ac45a7cd3805ce99dbc17faa8e91b1272c8f0543e94bd86382551f2b62dc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9dfc55f9860315f589e8408bfe8f8be4a4b1ed6337b297c5b1cab84a73edb5`

```dockerfile
```

-	Layers:
	-	`sha256:0d6d3f072c1f6f7698cded759541f2d632a79ffdc913ac4e71c3afe465dfea54`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 2.1 MB (2115193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3d06510a0e71ec3ed9551d2b732350f167fd151cd342a0ed31e1f08b39024a`  
		Last Modified: Mon, 09 Mar 2026 18:51:55 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:af8efd8a0b1ab9b4f0a532f4d23ce4ad4e05c83696414e4540c47794910ed4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44746136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaf25e7c4721988fa375c257e30e60e8de0ac32df18c18776a23c519abeff56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:34:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:34:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:35:42 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:35:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:35:42 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:35:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:35:42 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:35:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:35:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:35:42 GMT
USER haproxy
# Mon, 09 Mar 2026 18:35:42 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:35:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d011e0e6ccca79c932818cee0244c125fd70b0f2f952a204182b2f4da5ed01`  
		Last Modified: Mon, 09 Mar 2026 18:35:49 GMT  
		Size: 1.6 MB (1563197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1492fefb468192a8ad389a0954ce07cc7469d6825e439fea4def243a8319839`  
		Last Modified: Mon, 09 Mar 2026 18:35:49 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2a9715dcf075b68b8ef389d813f127f6e686df7049b1ce606d77ed74e43378`  
		Last Modified: Mon, 09 Mar 2026 18:35:50 GMT  
		Size: 13.0 MB (13041198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3dd765d4f0de2ec2c08f3baa393ed9a7568599f952307a9051d1a9785f532`  
		Last Modified: Mon, 09 Mar 2026 18:35:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:be3544daffc7715fc273d4462488cba152be9147e061e3b0696e954651241aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872540c4e15d2ded8498fffca87cda1ee22753a3244a4e34798ae6f4f79a4385`

```dockerfile
```

-	Layers:
	-	`sha256:596304e9e1a5fa723f96a303e6d1e230e6e158971cb7e46d151d5b40d5c7bab2`  
		Last Modified: Mon, 09 Mar 2026 18:35:49 GMT  
		Size: 2.1 MB (2114055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5885fc9fe565085fe61f8763e4177b49ba94f81e8baa917922b4b72803e99a1b`  
		Last Modified: Mon, 09 Mar 2026 18:35:49 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:7b577817a3213bfb2260c031e52413b1651d412da793a5cb71487d0808af0f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45724776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f794bf66166b45946a1fab0cae4846ce24d2e8776693bacfe2c9650b535d31f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:20:21 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:20:22 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:21:14 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:21:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:21:14 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:21:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:21:14 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:21:14 GMT
USER haproxy
# Mon, 09 Mar 2026 18:21:14 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:21:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f66560545bae7a6445dbb47897705e223beef207f5aff16e5174bb38dfc548`  
		Last Modified: Mon, 09 Mar 2026 18:21:22 GMT  
		Size: 1.6 MB (1603150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fbe780f68b0736b4d0a9ec72d14fe16fef4b3bc274d7479edaddd4364a054d`  
		Last Modified: Mon, 09 Mar 2026 18:21:22 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044b999daf538d2b40b829f6928031eb6dd9123b57f740f56feea3de63de93e`  
		Last Modified: Mon, 09 Mar 2026 18:21:22 GMT  
		Size: 12.8 MB (12826061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b2def541d5025e30b64a7206fadb2b83592f42f04734177fa95a93a4b521d9`  
		Last Modified: Mon, 09 Mar 2026 18:21:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:04bbda38e7f64444c2a3541773e88876753eaeea827fc3378a243970c4bc669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab60fa6143adf4adad231c5cc66a84eb5df011a6f5370ee94376d90f283b5196`

```dockerfile
```

-	Layers:
	-	`sha256:9acaa5eed529f9a809c5cf4401dc84b99b95a324d85506496ebc51e37e2c3a6a`  
		Last Modified: Mon, 09 Mar 2026 18:21:22 GMT  
		Size: 2.1 MB (2110951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62084740394b5fd5d53e87a9633a38add51f326a6d47b1c5e54b6580d9a247b`  
		Last Modified: Mon, 09 Mar 2026 18:21:21 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:f21f589dad2a6c7c0ffb4fd94f8c23d45de5aa137436254ab50758d9faec7501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49072348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd421501cda9daecded15f29579e39a35dca1f56429bc5f6ae97a6dc76498acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Thu, 05 Mar 2026 17:51:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 17:51:55 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 20:16:40 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 20:16:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 20:16:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 20:16:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 20:16:40 GMT
USER haproxy
# Mon, 09 Mar 2026 20:16:40 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 20:16:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a512800400158a521cd6324ecbeca708089d7bda87efc9521342ea8da8b39`  
		Last Modified: Thu, 05 Mar 2026 17:53:28 GMT  
		Size: 1.6 MB (1638778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80dfee41595e422fd3eb516690027fa831c5e35f049040fda219efd0f3225a`  
		Last Modified: Thu, 05 Mar 2026 17:53:27 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17745c8c660d55926fb1b4fe5107256ed6cb734959ed8fb41ccd80881f662d5e`  
		Last Modified: Mon, 09 Mar 2026 20:16:54 GMT  
		Size: 13.8 MB (13831710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa071e7e39f72070553df304309ae80d25da980b9d4c2ca337f2704fb878e56`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0dc04c618c353cc142db7456c1fd0083c46d05a2e98cfa827ae895f27418d814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e03f2cd52fd27ed1212be8b0abde86d6c37eca7fcfd1e80080a0301c91ee867`

```dockerfile
```

-	Layers:
	-	`sha256:c8c88dd796e540d9f34c1d552befb4fbde876c90e94dc9826853901985689ef1`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 2.1 MB (2117316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96da89a6901f17bdb9c81c5f5c6b89accbcb2400006c30885c603b723caf6f36`  
		Last Modified: Mon, 09 Mar 2026 20:16:53 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:e870b4daef72463826d43c8da73b66af4ed53fd3b9071e78fde0ce9fc9cd9b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42533656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f5429104f4a7db92ca1bf1551515b6df9ce532b492031052178705511db6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:55:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_VERSION=3.2.13
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.13.tar.gz
# Wed, 25 Feb 2026 01:38:11 GMT
ENV HAPROXY_SHA256=9cf45dadca6899908049d4c098d29ad866d89ba8a283d78a9c10890e157f6185
# Wed, 25 Feb 2026 01:38:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
STOPSIGNAL SIGUSR1
# Wed, 25 Feb 2026 01:38:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 01:38:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 01:38:11 GMT
USER haproxy
# Wed, 25 Feb 2026 01:38:11 GMT
WORKDIR /var/lib/haproxy
# Wed, 25 Feb 2026 01:38:11 GMT
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
	-	`sha256:a61ab47a6c70b7a65e636a636d15300bc8d806b38dd094e41f4dbcc9430146bb`  
		Last Modified: Wed, 25 Feb 2026 01:39:17 GMT  
		Size: 12.7 MB (12720500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bd827a7e8595336e82551bdbfb85d2d23cc86779421261d3696d99ce6b14b5`  
		Last Modified: Wed, 25 Feb 2026 01:39:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:4c40f3954b546a9dfff9c62f9d5fa93d6a001509e572a909f0fa2feb0c5665bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7809a2b2aa6c3c55f805657b4902f3b131bdefa07f7016926d33454f93dcd6c2`

```dockerfile
```

-	Layers:
	-	`sha256:cfdd89364c3f6a310d4bb3ea52b0d35e00f269cdd141e2979cc8b94f03534ee3`  
		Last Modified: Wed, 25 Feb 2026 01:39:16 GMT  
		Size: 2.1 MB (2107707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dadd11b970339f4f3dbed7540a8f59b22426818567d76a16c6fa4d9c8ba1ac`  
		Last Modified: Wed, 25 Feb 2026 01:39:15 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:22f0439b00ccf96fff1e68f2809d68abd7db52f2c75ca95f3dbf550315909d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44872322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309b3ca6dcd0ca3acbb46aba1d1d0323e7ceadea1f7f27594728d4b3d6d48a6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 18:57:26 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 09 Mar 2026 18:57:26 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 09 Mar 2026 18:58:37 GMT
ENV HAPROXY_VERSION=3.2.14
# Mon, 09 Mar 2026 18:58:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.14.tar.gz
# Mon, 09 Mar 2026 18:58:37 GMT
ENV HAPROXY_SHA256=b21f50a790aa8cb0cf8dc505f1f8d849799eafe4d31c14b86a34409ccf4ae5e4
# Mon, 09 Mar 2026 18:58:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 09 Mar 2026 18:58:37 GMT
STOPSIGNAL SIGUSR1
# Mon, 09 Mar 2026 18:58:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Mar 2026 18:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Mar 2026 18:58:37 GMT
USER haproxy
# Mon, 09 Mar 2026 18:58:37 GMT
WORKDIR /var/lib/haproxy
# Mon, 09 Mar 2026 18:58:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192b2bd70eb8e0a153c4db4f73033a944eff656835793e6f431b0d1461410c30`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 1.6 MB (1599670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68426fe057d46f6825cc9c0c74722ef4bead351fd24595c6b48772911c074afc`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eefb3e11622954866a98c831c60c94207a2a804474876ca1384ae7fa793b200`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 13.4 MB (13432828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89991cc70d9b183e30c6be5fb5d855d87faf6d1b5c7835f7a88856f9ddc36137`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a9c326d8dec4030a204019709a44a6feed868e8afd96cf96c81d7acfaf07d877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91c5f23125f5a7e5e57e576c79bc0cfdbf02cdab5f461398c2b33d4716f5b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5eccd80c5b2fa34a956f5df2261fa8e779179629a8a5d361b75bc95b700a857`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 2.1 MB (2115214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1baf845062344124539817eb5790caf70f203b6a4d3b47fa2183670448764d6a`  
		Last Modified: Mon, 09 Mar 2026 18:58:49 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json
