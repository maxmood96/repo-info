## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:db778ac434b0e9c45862b1229eb4490a6a2f2703426bec0d135663da3b7d8cce
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
$ docker pull haproxy@sha256:f8acfc8a095098e0cb495b3e45fb0478e6b0d26b19d01d5535059bbe2ea6e72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42387876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72118e9b4bdf777d273b3287eee52efc0b3c60a9fbe1af57dfda66e95fbb1195`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 22:36:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 22:36:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:37:30 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:37:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:37:30 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:37:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:37:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:37:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:37:30 GMT
USER haproxy
# Wed, 05 Nov 2025 22:37:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:37:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b9f3c547d8579771d598f3cbc81718608b90fd993031e6135518e27f60b66d`  
		Last Modified: Wed, 05 Nov 2025 22:37:46 GMT  
		Size: 1.6 MB (1580948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4443d903fcda372cbed79baced2ee7cdeedc893ab003c2e2d87f50be63a3e6a3`  
		Last Modified: Wed, 05 Nov 2025 22:37:47 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecae1ea9f2ebbd82999d3414b246cace4a40af92ab69ce1c94687ff8e2593aa`  
		Last Modified: Wed, 05 Nov 2025 22:37:50 GMT  
		Size: 11.0 MB (11027185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900c86069c6e760c9d21d4b3a869e32af88a1b0b611ca2a218f98efb681ee97`  
		Last Modified: Wed, 05 Nov 2025 22:37:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:38ff7d97420724caec65274c9b354ffedfc52b1c547bbc14e40a7e1e0337e628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b9fe9fcf3726f59c942e8f60dfb48cb2eec773e5d318a342be84ada5c04574`

```dockerfile
```

-	Layers:
	-	`sha256:cea5652b2bacf457afef1b242795755be4b1e50b2b5a5cbacd3a302ea67aafd3`  
		Last Modified: Wed, 05 Nov 2025 22:57:34 GMT  
		Size: 2.1 MB (2114308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb84cb31874340d899f8d64737b4bab7d8dd8667f8faf68cefe60844ead3572`  
		Last Modified: Wed, 05 Nov 2025 22:57:35 GMT  
		Size: 22.2 KB (22205 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:4acaf31c83b3374b529af0f1c466177ca977bad992101b41f505891db0766b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40591596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61edc2958241bd92e05808348219fd542310322ee96452b5d5ae346c7d7defec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 19:43:03 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 10 Nov 2025 19:43:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:43:54 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:43:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:43:54 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:43:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:43:54 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:43:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:43:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:43:54 GMT
USER haproxy
# Mon, 10 Nov 2025 19:43:54 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:43:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b440211c3be9c73a4e8e0eebb3b28b3cdf01c9283f25afdb84e201538645cd`  
		Last Modified: Mon, 10 Nov 2025 19:44:10 GMT  
		Size: 1.5 MB (1534896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807a9a0dc8785321afeed8baab6a1a26b62ea60ea16d0060e0b12a3b7d5ab2e4`  
		Last Modified: Mon, 10 Nov 2025 19:44:10 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9bcf12202539ccde6f0e7c2a86eed1297591566dbbb2e9cdf25427038599fa`  
		Last Modified: Mon, 10 Nov 2025 19:44:12 GMT  
		Size: 11.1 MB (11108621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d858edb8b5274b17ec1a69fa42ead44ed512532cc3062dd4dda5f1dc6609800`  
		Last Modified: Mon, 10 Nov 2025 19:44:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:6e2d4290c95799055e33bac14a29fca908fbae69b2c8b9c0ba0cab418cb459a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56670ff19dde3ca6893f781d3d9c4322521486c56c7ede2503fac0f4c47c798`

```dockerfile
```

-	Layers:
	-	`sha256:49dd43bcacd2a425b8e32def9498631f0917e5cff21008862839ffd6e403a649`  
		Last Modified: Mon, 10 Nov 2025 19:56:36 GMT  
		Size: 2.1 MB (2117304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4867d943531331fb10adfa1185192e76dbeab3c8289d303cb74f80f17dfc3b`  
		Last Modified: Mon, 10 Nov 2025 19:56:37 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6fc4ed3656f279fd0e9ceb90f844e1fb8f39b0a433983422e24b5d55f0fab151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38600986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917b2b8f038fab68c7da3ad671b7dff17aa51bdd1513adc90b96b6a62bf82731`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 19:43:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 10 Nov 2025 19:43:42 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:44:26 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:44:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:44:26 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:44:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:44:26 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:44:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:44:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:44:26 GMT
USER haproxy
# Mon, 10 Nov 2025 19:44:26 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:44:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162541918d365ef1c719720ad7cb6eaf9a3040de64773ccde513c60ce70db30`  
		Last Modified: Mon, 10 Nov 2025 19:44:36 GMT  
		Size: 1.5 MB (1488901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6719b2950e7a3bf858f5b51b2d435c2a8a58ec643888446276493b92ed0dea9a`  
		Last Modified: Mon, 10 Nov 2025 19:44:36 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c7103cae3f09cfc815bf6b72cdad0d022b1e7582a6c51a4358891f336aced9`  
		Last Modified: Mon, 10 Nov 2025 19:44:37 GMT  
		Size: 10.9 MB (10897408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ee824488cbabe6c1bac8526c0887118bbb98b1be2bea06d0b152dbd0fa048f`  
		Last Modified: Mon, 10 Nov 2025 19:44:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:dc680dc74ccf1706df090670a1c786d7e8f3f1b77476172a0c3fbe402280a5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55071368b79fe02881c56facf28f198106964e398aa96d4ef80ca1029148d046`

```dockerfile
```

-	Layers:
	-	`sha256:73d2685575f1310415a0c7cda526f9dbebbeb3d96de7bcee9a346286e4ae333b`  
		Last Modified: Mon, 10 Nov 2025 19:58:28 GMT  
		Size: 2.1 MB (2115747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928061cbd9395a13f1a30d71efde13d8c788743f9a6187936c0259128bca3bc2`  
		Last Modified: Mon, 10 Nov 2025 19:58:29 GMT  
		Size: 22.3 KB (22343 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:31ffe60bca4bf9bec4f8530ad49eb8887832a495f18bcd8ae869bcf7bca0f7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42662527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee9d166f73868ed6fa7ad9f81b01ea31a40d6479ac59d31bfd4b874e56d553f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 22:37:17 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 22:37:17 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:37:57 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:37:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:37:57 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:37:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:37:57 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:37:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:37:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:37:57 GMT
USER haproxy
# Wed, 05 Nov 2025 22:37:57 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:37:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9944186d35efade8ab033189d7fb66d99dbb77f0b82eb1724ad6d6209326d`  
		Last Modified: Wed, 05 Nov 2025 22:38:12 GMT  
		Size: 1.6 MB (1563336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90687321a820a4ba56e86e6caec9c8deda0f8df0e68433405d7a6aea1deeced8`  
		Last Modified: Wed, 05 Nov 2025 22:38:12 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b93b08dc6fe18c51f4995f39a428952a2bbe790e71ef87b7fb341d6acf7c0`  
		Last Modified: Wed, 05 Nov 2025 22:38:13 GMT  
		Size: 11.0 MB (10955256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dca91b63ce061696316150915374559e3ed9be1539b9db2aded93ac3fe9a5e`  
		Last Modified: Wed, 05 Nov 2025 22:38:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:76041cd8400ef74e167e8a1ad31e887243a44fbd3a9f48a1b756602dd05d23cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d2c965387f70187e2fb6156641f5ac4bf06d562128a632200e26d0cc23c6b`

```dockerfile
```

-	Layers:
	-	`sha256:1c54fdb64f4d7d8340cbd731df25d49eb0b96cf78877c5ad4fddd5e90cd10ab9`  
		Last Modified: Wed, 05 Nov 2025 22:57:46 GMT  
		Size: 2.1 MB (2114617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b66cab298ac98fa487c5208d2791197ff6260d9a8e6779c49606c30fc8dd42`  
		Last Modified: Wed, 05 Nov 2025 22:57:47 GMT  
		Size: 22.4 KB (22387 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:4bbf118a5fc9ddafa8602c645c3b9caad3504239053c27f37368d775a412937a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43637782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe97458230399584591d1c5b2c28988ba2c72d56c198fcb216a0bf2cfa446f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 19:45:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 10 Nov 2025 19:45:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:47:57 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:47:57 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:47:57 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:47:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:47:57 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:47:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:47:57 GMT
USER haproxy
# Mon, 10 Nov 2025 19:47:57 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:47:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a6ee68b7139e2c936074577e5ff63e1de63a979e2384803a5dea551f0fa561`  
		Last Modified: Mon, 10 Nov 2025 19:46:12 GMT  
		Size: 1.6 MB (1603163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ffad79e1aa90a089534c677507a5f68a587a02758d1828844ddddd045e8c59`  
		Last Modified: Mon, 10 Nov 2025 19:46:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306ae11f2e9cb0aeefbd590f42a7e52d31dc04fba040e3107cf714adb1481ddd`  
		Last Modified: Mon, 10 Nov 2025 19:48:16 GMT  
		Size: 10.7 MB (10738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36e42b32cf4518ba244b92b44e6c822f1544613a8697f94070c60497e7aa887`  
		Last Modified: Mon, 10 Nov 2025 19:48:16 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:9a26a472bccd7324ca5e0a08ead9397a38e5b015f90b730b6133da40810410f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae630e7b60b13b7fe483c03dfa97d27418c2f087902e51d7fd1abc0a24f9f05f`

```dockerfile
```

-	Layers:
	-	`sha256:0b3cd221e19ff9c2fc5a365c62044cdd4eecd89a90aaa3d34c06a57d7132b41b`  
		Last Modified: Mon, 10 Nov 2025 19:58:40 GMT  
		Size: 2.1 MB (2111479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3219f58b875dc94626d1016b32574581062cb5a26c143d21c2638672172439`  
		Last Modified: Mon, 10 Nov 2025 19:58:40 GMT  
		Size: 22.1 KB (22149 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:71063ea0ee62c8049928a0f4a44ff43c0e2cb0616bf839c793aee79da956c6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46914112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814557f3840fe8230db2fd9748ce4bcc5f4d516df6860405501741db306190ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 22:34:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 22:34:56 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:36:07 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:36:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:36:07 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:36:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:36:07 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:36:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:36:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:36:08 GMT
USER haproxy
# Wed, 05 Nov 2025 22:36:08 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:36:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f615aa1b0577ba10dcc1fcf3aad85b630efea812bc7851a8a6387749186a414`  
		Last Modified: Wed, 05 Nov 2025 22:36:48 GMT  
		Size: 1.6 MB (1639409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48153f0a1e542c115cac11f194a7fdb0d35031ef44640608132e94e0a3f08e65`  
		Last Modified: Wed, 05 Nov 2025 22:36:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeda508485b2ba4ea71535bf7e81674d459e2644d004c886ea2b7b4cdc7669b5`  
		Last Modified: Wed, 05 Nov 2025 22:36:49 GMT  
		Size: 11.7 MB (11674415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69eb2149999cc215be44aff47aa0168367a2bbb063b046931ca065c904f5ed8`  
		Last Modified: Wed, 05 Nov 2025 22:36:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:19898de4b70e9b69529d20a21f05fb942478db3eedd5d9f497e62523fe8e7620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7648e0a3aad450ec39b9269329e61f301731ecde0a4753dd2faa83fcd4ee300`

```dockerfile
```

-	Layers:
	-	`sha256:96e3163c48c9808516dbe1b5da46973fba94abe73656fe204b97771b6d5a9523`  
		Last Modified: Wed, 05 Nov 2025 22:57:16 GMT  
		Size: 2.1 MB (2117866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d3c6415fe809c33a82c46f1460b06aa5a1c6dadfa3f512469fd882bc14d5f4`  
		Last Modified: Wed, 05 Nov 2025 22:57:17 GMT  
		Size: 22.3 KB (22277 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:88ab9d401d32791fec0a8329a9bfdc5f90d565d3639136a3ea9327a39eac4c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40494045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c36cdd87cb9b6d44a1082fafb836f7e2d588c7b19804e8619e9aa4214a0e6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 22:35:39 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 22:35:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 23:50:02 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 23:50:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 23:50:02 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 23:50:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 23:50:02 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 23:50:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 23:50:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 23:50:02 GMT
USER haproxy
# Wed, 05 Nov 2025 23:50:02 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 23:50:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2042ca14ad87d8c021e8286d1667682e0de98485deadb67991e7993ec90d3749`  
		Last Modified: Wed, 05 Nov 2025 22:59:28 GMT  
		Size: 1.5 MB (1535273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c360eabe566eb9acb38e529bc5260582b5a429818450426d32180a163ed1ae`  
		Last Modified: Wed, 05 Nov 2025 22:59:27 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc2c9cab269120de4221e5b691eb71609609431bf890cf6c065f7635677ab72`  
		Last Modified: Wed, 05 Nov 2025 23:51:11 GMT  
		Size: 10.7 MB (10681345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e96b443e9fb1e2ced08255ba0f757ce3f564c5eb9d065b015ab02bfafe5a63`  
		Last Modified: Wed, 05 Nov 2025 23:51:10 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0463b7a58dcc559bdc729c0bb09c3090d17db239f732b3105f26c766207b47ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84acd09dd8d10a8b85deb9a962c1fc55a22cbe44cc99165aca0aa23e53777a23`

```dockerfile
```

-	Layers:
	-	`sha256:95f905d2c363780d5d30f6680922c728c2bea79f5507c429649bce2eaac5a97e`  
		Last Modified: Thu, 06 Nov 2025 02:01:48 GMT  
		Size: 2.1 MB (2108257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf89b72cce47e18cbf1cb363c2868e3b66abf7c7b1c26e04840d1f88ba19ecc`  
		Last Modified: Thu, 06 Nov 2025 02:01:49 GMT  
		Size: 22.3 KB (22277 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:8433c32f0029f348d99c33f6ef2d87ef2f1a4d5f4ff8f95ecb63b3013aac3dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42761494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4f9ece9f087db9a2b5c6b0b7cf7556680fd24e5e768dc2087175d0015f9ea9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 22:37:47 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 22:37:48 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:38:38 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:38:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:38:38 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:38:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:38:38 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:38:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:38:38 GMT
USER haproxy
# Wed, 05 Nov 2025 22:38:39 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:38:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ba0a4343a98058eb49f4fcee21d1af126057bbdad120badea5c1524c637f1d`  
		Last Modified: Wed, 05 Nov 2025 22:38:58 GMT  
		Size: 1.6 MB (1599824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609144e1e61cb7ee0bb68aee5d28f6f2dcf395039d5f2f2482a4f4d6a49081a`  
		Last Modified: Wed, 05 Nov 2025 22:38:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f3f4c1f97ed42c5eeb9a04dcc20169e10c34eb35efb8b4985838098dd397f0`  
		Last Modified: Wed, 05 Nov 2025 22:39:00 GMT  
		Size: 11.3 MB (11322637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a83ed79e3aebb641b4cb4f84667ce5126cceddd850d1d2e7519bc6fddf2123f`  
		Last Modified: Wed, 05 Nov 2025 22:38:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:be5263c8b2197b8f73e4c67706d272dd6f1f00f32195b46dde5fc04c319e373c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05b98007566aac3fa2804d479b15ca2c1731ea109ff5975937a0ae06e9d6b74`

```dockerfile
```

-	Layers:
	-	`sha256:f666bd1c5460c7c61499b93c2a3ad13d22da9b51b95c9582b97f9372536893d8`  
		Last Modified: Wed, 05 Nov 2025 22:57:25 GMT  
		Size: 2.1 MB (2115752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5336716aa7461a20198d263857d6d0a48c9275827c29355c9bf85f7211fdd02`  
		Last Modified: Wed, 05 Nov 2025 22:57:26 GMT  
		Size: 22.2 KB (22204 bytes)  
		MIME: application/vnd.in-toto+json
