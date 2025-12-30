## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:8ec7ee30de8799a3a1c1935cc039404871919a03b9465eb96a5f8c22bd1bc30e
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
$ docker pull haproxy@sha256:0f71ff1e8c3947be88f006b7c1a4faa07225d4731c1c904c409b7114b5c2ccab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8554d43df83f974c02c4b6dafa8634dd16cf3e1d276d49b7334f053a1261ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:16:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:16:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ENV HAPROXY_VERSION=3.2.10
# Mon, 29 Dec 2025 23:16:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Mon, 29 Dec 2025 23:16:44 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Mon, 29 Dec 2025 23:16:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:16:44 GMT
USER haproxy
# Mon, 29 Dec 2025 23:16:44 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:16:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f09a0abab68f897efd283a8aa3ee21b0af86b6bbe74f2770605f1e0be28cee2`  
		Last Modified: Mon, 29 Dec 2025 23:16:58 GMT  
		Size: 1.6 MB (1580892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ff83dabe353487852fd2df07b766cced35b060c103ffee20c52a1130662f17`  
		Last Modified: Mon, 29 Dec 2025 23:16:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c01422a21615632db4abf1d1b1944abb462d6d9cafa683b69346c9531eb25c`  
		Last Modified: Mon, 29 Dec 2025 23:16:59 GMT  
		Size: 11.0 MB (11031451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf0a2ed3305f425d55298939344a063df6df7e2def282a568d2162792ad198`  
		Last Modified: Mon, 29 Dec 2025 23:16:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e2fc6008e858f183a133231afdbad181c2128d1cda47e76529c80a62f66a43a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ac9e67df4cc88090fce335b7a5d0a18e98c77835214fb0a45b28e3ab00be9b`

```dockerfile
```

-	Layers:
	-	`sha256:64bec750a4e17e9793a9ac7c568e339f79585c66cb7483ded52841d02927b18a`  
		Last Modified: Tue, 30 Dec 2025 01:58:53 GMT  
		Size: 2.1 MB (2113708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3146035b8c1cbe3b457c417559fca998daacf82d46181ffe0e8f9731f65d084`  
		Last Modified: Tue, 30 Dec 2025 01:58:54 GMT  
		Size: 21.6 KB (21610 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:a35e8a6e394b4eb5587c0634c3be7775953c403077cde122e72365b79544aa74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40592155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22336555c992c560a03fe4f66e227f950e39178c727c1243cca3048f06673a75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:36 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:14:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:15:26 GMT
ENV HAPROXY_VERSION=3.2.10
# Mon, 29 Dec 2025 23:15:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Mon, 29 Dec 2025 23:15:26 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Mon, 29 Dec 2025 23:15:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:15:26 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:15:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:26 GMT
USER haproxy
# Mon, 29 Dec 2025 23:15:26 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:15:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e780af02c380a86753e7e9838c7f7a2dd44bbce13aa73158cec733fabf3b905`  
		Last Modified: Mon, 29 Dec 2025 23:15:40 GMT  
		Size: 1.5 MB (1534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636452e8759c464383bc3d52a3fd8f518065043d748234feaa80a2ef52cb0d40`  
		Last Modified: Mon, 29 Dec 2025 23:15:40 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26198a75e200d7c4c9205290ae54e51dc84fba40caa8bd186853c758b14491f`  
		Last Modified: Mon, 29 Dec 2025 23:15:41 GMT  
		Size: 11.1 MB (11111593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b17cd6cb1bd172cac33d1d133fff79207daf02db1cc6b1b05c1e540f7a7bffa`  
		Last Modified: Mon, 29 Dec 2025 23:15:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2d76a3c196330d7d596d9adb9f8738d5582f6d5778a83ef5cd2dc7fd5ee1a4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534f30efac7677ce652a3c0866a0be8fb97f71cf76abfcc7c474145396f2f15f`

```dockerfile
```

-	Layers:
	-	`sha256:831a312295aa4c6954ecfe635b17fd73a4c45753b117a227e6886a2e23b20b94`  
		Last Modified: Tue, 30 Dec 2025 01:58:57 GMT  
		Size: 2.1 MB (2116688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5f23286dde9fa1f4940a1b3b6c4b35ddf514dcc2a0654f0cb04e8428505f87`  
		Last Modified: Tue, 30 Dec 2025 01:58:58 GMT  
		Size: 21.7 KB (21732 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:56a1069062b2aa8ad261d334cbd92eab90e37f5b5761abba7da9e857dde3a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38602341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f363b50541cab3e31cfcdd0b173e6fe2b0ee70cffd012a46cfee1918cfa4fc24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Thu, 18 Dec 2025 22:35:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 18 Dec 2025 22:35:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 22:36:01 GMT
ENV HAPROXY_VERSION=3.2.10
# Thu, 18 Dec 2025 22:36:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Thu, 18 Dec 2025 22:36:01 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Thu, 18 Dec 2025 22:36:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 22:36:01 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 22:36:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 22:36:01 GMT
USER haproxy
# Thu, 18 Dec 2025 22:36:01 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 22:36:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c30106e365a977090825116f91e740915b3b642ea8c05ce0a366181d821a`  
		Last Modified: Thu, 18 Dec 2025 22:36:15 GMT  
		Size: 1.5 MB (1488768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62358808f2b17a31c7babfdc4765402a4e4b12efdf3139a2a5952552c71c145`  
		Last Modified: Thu, 18 Dec 2025 22:36:15 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40539453fa4a526d683ec191febcb44fdcb8c2b06bf52e8288e5403fbc31d41d`  
		Last Modified: Thu, 18 Dec 2025 22:36:16 GMT  
		Size: 10.9 MB (10901917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9cc3f5b5e690e1b23f7531cb0daf1140dd1b1e4173fe950b9e24ddf453b72a`  
		Last Modified: Thu, 18 Dec 2025 22:36:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:aa6eb22e0890aa0a3b22cb66a9c09818f9b0215f71360b5078fa125f5aa360f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ff323c682620dcf66f54572f7cc85c30df91143bb62561f61e311003532bcd`

```dockerfile
```

-	Layers:
	-	`sha256:d04c2e754aeb631f9da7aab416ce7c5019510e1b65d41d54c6665f331bd4f4e1`  
		Last Modified: Thu, 18 Dec 2025 22:57:01 GMT  
		Size: 2.1 MB (2115131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4133d51349b5bd7d97c496b48b03dfe32ccb009ba68c0b318e7c388f41adec`  
		Last Modified: Thu, 18 Dec 2025 22:57:02 GMT  
		Size: 21.7 KB (21733 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:34f6425d9d0eee1e25ad1e86956103da79c68e744e52d412c67538375ef1fb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42669205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f1526a227453478ad41678f43099fc09fa6b0b09caf7830925acacb49c7946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:14:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:14:43 GMT
ENV HAPROXY_VERSION=3.2.10
# Mon, 29 Dec 2025 23:14:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Mon, 29 Dec 2025 23:14:43 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Mon, 29 Dec 2025 23:14:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:14:43 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:14:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:14:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:14:43 GMT
USER haproxy
# Mon, 29 Dec 2025 23:14:43 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:14:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f123d21eaaecfe3eb089934aa98dadf5c2ca644e14b4b56d053316bfb59ae1df`  
		Last Modified: Mon, 29 Dec 2025 23:14:58 GMT  
		Size: 1.6 MB (1563655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad3dc042b670383899b856aa5bd36d0a9e04265b3d2dfb9306a0da63cf5e12`  
		Last Modified: Mon, 29 Dec 2025 23:14:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b7b0d065c34d2aa2c41f55f1419f9fa96e95d81a9caef0d2eccf544805563`  
		Last Modified: Mon, 29 Dec 2025 23:14:58 GMT  
		Size: 11.0 MB (10965278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d366247ef0b575150d89ef66df59b331eaf38f38fadb9f446447b2b59b8be4`  
		Last Modified: Mon, 29 Dec 2025 23:14:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a68d5b091c8863a2a3a6d0a6691f3b290aa44ef5343f28b62fe7abf85ea05d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16197f9f896e8a72f1b59b2cd50509af54a470175d01f52dd781710b3571d1f`

```dockerfile
```

-	Layers:
	-	`sha256:2ff55cf0661d387c40706d90a133ebeb91e9d421877519f264e9ce2e1bc7c9a7`  
		Last Modified: Tue, 30 Dec 2025 01:59:05 GMT  
		Size: 2.1 MB (2113993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5eea8ae852f0c4deac6b176ba8c404997b611e2675799cafcd320e911f354f9`  
		Last Modified: Tue, 30 Dec 2025 01:59:05 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:9742e983bc1263f2a0233361c088c55ec9a5758b5800d8d1ce15cfee00af20c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43641217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0468717aeb1bb945224ee1ed73a43d79222dce462b8a85b7249df98dd0557853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Thu, 18 Dec 2025 22:21:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 18 Dec 2025 22:21:44 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_VERSION=3.2.10
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Thu, 18 Dec 2025 22:22:25 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Thu, 18 Dec 2025 22:22:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Dec 2025 22:22:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 22:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 22:22:25 GMT
USER haproxy
# Thu, 18 Dec 2025 22:22:25 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Dec 2025 22:22:25 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc574a74b73ba1971b73aaa4f4641968a284b411f108b53a5492b3ee7e7dd4a7`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 1.6 MB (1603066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610105c15b35d2ff6b946cc8599bb940c72a03da5d2febb26f9280c63e8743a`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813e44e556842af058f5b6bdd7c3772fa65d69a0c1e1bb953a8f87ec5c077043`  
		Last Modified: Thu, 18 Dec 2025 22:22:40 GMT  
		Size: 10.7 MB (10743441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe1c439d65f40eaada0bef870b9fd32d5333fd0bce1c5b6b116b710a11d1e3`  
		Last Modified: Thu, 18 Dec 2025 22:22:39 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d511fdb8ac816a6e9c26bb56b0f7d761f77ede5fcb2d4b88911da41b637fe910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5f7eee5a548f7da9b329f59ece2071a5f11c5f0631eeb83d348f88e59923fb`

```dockerfile
```

-	Layers:
	-	`sha256:23ed9a054bcf1549443225ee5fa5badc52ee3f86e5ee9ca600d1955cb76d09a2`  
		Last Modified: Thu, 18 Dec 2025 22:57:06 GMT  
		Size: 2.1 MB (2110889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c332b5b464ca4d2a96ce001a321e170a768c557dd6394e1923bdcdd9a3e762bb`  
		Last Modified: Thu, 18 Dec 2025 22:57:07 GMT  
		Size: 21.6 KB (21565 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:4454bf420a4489203af80fc19258fd3930edc74c1fbee5dda646b97d16c292b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46930617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1cea2dd50d5b5a83d6dc21eb63ede59b246e34b48096b635c8a25fd0ec642e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:16:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 00:02:19 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 19 Dec 2025 00:02:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 19 Dec 2025 00:02:19 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 19 Dec 2025 00:02:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 00:02:19 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 00:02:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 00:02:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 00:02:19 GMT
USER haproxy
# Fri, 19 Dec 2025 00:02:20 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 00:02:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185480bdc18ea021a0fc7f5119aae641bd26bbb0177eb9faf2ff183fe47f022`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.6 MB (1638932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c1fe78578524cbf853cfaafa2576e0205722868fb7fcd5b0011a9d050049d`  
		Last Modified: Tue, 09 Dec 2025 00:19:02 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87093b0c7c845231ccade39ba7d222f137842e474d60e24ef05af5b137bfc929`  
		Last Modified: Fri, 19 Dec 2025 00:02:45 GMT  
		Size: 11.7 MB (11693153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae9ec9dc6f8e1bcf66e459af7861526dbcf1ae7dcca5ed07bf35b5f8f767b41`  
		Last Modified: Fri, 19 Dec 2025 00:02:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:6521e9afb5654d926cd9bde189d32eed6c80c0dbc2bf43d6bfde846466795976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12fee9d5f6dbe3826a0d9668a600c8c7d8d19746600127fc1835a9cf75b8561`

```dockerfile
```

-	Layers:
	-	`sha256:810fef26f2e24b1d8879f01746d86cc2470efade8d110f0cbf3a6d804a1f916b`  
		Last Modified: Fri, 19 Dec 2025 01:56:34 GMT  
		Size: 2.1 MB (2117254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1593485a5b16b70b9c652d6d851a31e51b57e336a83f04ca3e464f632631a5a`  
		Last Modified: Fri, 19 Dec 2025 01:56:34 GMT  
		Size: 21.7 KB (21671 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:92c491191be073a38c27946ea1944399af91c1d0ba2c6fee9a759ce41e57f687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40504356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47e54d368d1df6d792c3c845fc2a062df2725fd91fe6ff8f2b2655866ce43b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:15:22 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:15:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 19 Dec 2025 18:14:21 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 19 Dec 2025 18:14:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 19 Dec 2025 18:14:21 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 19 Dec 2025 18:14:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 19 Dec 2025 18:14:21 GMT
STOPSIGNAL SIGUSR1
# Fri, 19 Dec 2025 18:14:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 18:14:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:14:21 GMT
USER haproxy
# Fri, 19 Dec 2025 18:14:21 GMT
WORKDIR /var/lib/haproxy
# Fri, 19 Dec 2025 18:14:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8764214954a48097c0e9e75920ec71940c64da22d529cf119465be01a382f7bf`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.5 MB (1535074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8e3b90d2e358dca114fe7f69a507e4f358fbe2966b2f6df9510975fe1daec3`  
		Last Modified: Tue, 09 Dec 2025 03:29:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac1af271397c8965273dc3547b7a953a79bb0776d765b7459dfbec963d532d3`  
		Last Modified: Fri, 19 Dec 2025 18:15:32 GMT  
		Size: 10.7 MB (10694485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30e190626726b5bfb31d2779ab08ead46b96e3459b7b566a3b485bc0647f8c`  
		Last Modified: Fri, 19 Dec 2025 18:15:30 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5ea5dbf8533896a6e5864ece7bf06746d2bb11547c6f4059c4f474335334d611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff66bcda7656170848b9af6ecf0e3da7cf680a6a11f0553f229d4e328436e1ce`

```dockerfile
```

-	Layers:
	-	`sha256:e8bf06ff6ea9a0b7000311d461a5a22728d59b3dd482cfbd2140b0b210fb4bef`  
		Last Modified: Fri, 19 Dec 2025 19:57:38 GMT  
		Size: 2.1 MB (2107645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a318a347ca42c20ffd80b77bfc978a4e77ea2cd9c62ae1531371b5e7f0743c73`  
		Last Modified: Fri, 19 Dec 2025 19:57:38 GMT  
		Size: 21.7 KB (21671 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:f5d81dd3999c8d586b97803f1a0d1b9d7d7e18d1c1e2352c9cb1c7b3e32406a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42761220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80c6d8be72baea9aae0c2d137324af304760844198371f55f956f023a554ba6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:12 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:14:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 29 Dec 2025 23:15:18 GMT
ENV HAPROXY_VERSION=3.2.10
# Mon, 29 Dec 2025 23:15:18 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Mon, 29 Dec 2025 23:15:18 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Mon, 29 Dec 2025 23:15:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Mon, 29 Dec 2025 23:15:18 GMT
STOPSIGNAL SIGUSR1
# Mon, 29 Dec 2025 23:15:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:18 GMT
USER haproxy
# Mon, 29 Dec 2025 23:15:18 GMT
WORKDIR /var/lib/haproxy
# Mon, 29 Dec 2025 23:15:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214750d64bd6cca1938456e19743ad32bb86245c69dc747aef87bb3a136ec6`  
		Last Modified: Mon, 29 Dec 2025 23:15:27 GMT  
		Size: 1.6 MB (1599454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec92cd795004ea17e7e92bec2b7106f2f95c83921949c6a00dc5752c548fe22`  
		Last Modified: Mon, 29 Dec 2025 23:15:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e64b4ae59fc37154230b20cf431235c8779c510a36bd7ce0c74441c0720ae3`  
		Last Modified: Mon, 29 Dec 2025 23:15:35 GMT  
		Size: 11.3 MB (11325709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7963d3febf5db67a5f8a2af18a9b2fe19507c905a2d0f59294ef45b8a6727e`  
		Last Modified: Mon, 29 Dec 2025 23:15:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c8f9b193d67412a863ba71a0b37ff29613591962ed3490bad68b96189e0729ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb93d1829507ef506e29bd91766c1eba5c0a8a49900392e21725151665147ac0`

```dockerfile
```

-	Layers:
	-	`sha256:3060758e7806a14b5b3cec977865d2e24610b6b999976bae48d502bce62db987`  
		Last Modified: Tue, 30 Dec 2025 01:59:18 GMT  
		Size: 2.1 MB (2115152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67c32ad03e54749716b90383ed0da8393a6c6f6cae5092e2796baef4d0250a3`  
		Last Modified: Tue, 30 Dec 2025 01:59:19 GMT  
		Size: 21.6 KB (21610 bytes)  
		MIME: application/vnd.in-toto+json
