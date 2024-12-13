## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:532db4fb7bb9e5bf5de17be9f63578a13dfbab8325cd2133839a799766079f61
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

### `haproxy:bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:82ca6ce4636b3d52c74e44bf2fdf8336e4a44d9376a5c4500d5350b024510f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41550567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50df48178aa1022895972442ad85104d50219e59d70c6ff433849c34c4e19c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20859b69632aa978d0793fd84af55908775d9b96a8f436c6fe7bf20cd46aca40`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 3.3 MB (3306400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fce2c60ec17914518111898868153471900f56ed35fafc3bc33757a2bbcdd1`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace9f771f5d8863604e7778ac58f2bf5158e1b9257b243d49be7d45add2312c`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 10.0 MB (10010946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e27a257af92b57f4d9c5661d01022004f418b2d7dbe774b657109ef811165`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:7a45f962416a31cf96f3034de5aa00234729ab35815f7a3adf3f5377aa15546e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5396598599c519a2eea62c99a9edb94fdb24dfff2ecaf7c30616e54d91da5a`

```dockerfile
```

-	Layers:
	-	`sha256:3d7baec0a937466cf5649b404d8aba50c1d6d8cf4d0bb26d7d375ac912426c0f`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 2.4 MB (2371028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98145496d1d8fe89e6584890048b342166c504dd6bd2cbaa83258f505ffebc61`  
		Last Modified: Wed, 11 Dec 2024 22:30:13 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:a907c7f0cacd2454a11858ba27e04932ae08973f6323af6a83322c1b48c8274b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38629867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7eb54f6111b3a49a527ef8e4f2ac76b1efaf22c0c54b218958d7acb51466a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794e5b382c6fb675e640fa71617521425dace28430774c78c514d681f8d82db8`  
		Last Modified: Tue, 03 Dec 2024 02:21:22 GMT  
		Size: 2.9 MB (2879508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2bbcc3466c5b5027bcdd5485f16486bb9dc51fc36df3b3167b39ce05e753f3`  
		Last Modified: Tue, 03 Dec 2024 02:21:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf5bfc4cc320869ea8f257440bed58098b8a8701599f8e5b1d1c6828bfc120b`  
		Last Modified: Wed, 11 Dec 2024 22:32:05 GMT  
		Size: 10.0 MB (9993793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360c5b79b48b0f5b077cb1370040aee45398287b94dae8c3cc8005e6ff13642a`  
		Last Modified: Wed, 11 Dec 2024 22:32:05 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:392c1fe871b17fa7470e4bd68eec3b1ffdf0091dd0d2066862a6e7d3ab0d8ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e3b5bc594fe97c4945777d438e5a6d6f89e5c7cafbf0a3d8b95502419ef80e`

```dockerfile
```

-	Layers:
	-	`sha256:f2646351d3d54630c7f57746bdbde16e52bcc62e2c9c6ac6a4b91cf9fa33011e`  
		Last Modified: Wed, 11 Dec 2024 22:32:05 GMT  
		Size: 2.4 MB (2374541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78386cb5855ddc04ff0f4123b425026561434df72364ee0be6991c4c0a25f34e`  
		Last Modified: Wed, 11 Dec 2024 22:32:05 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5f4a8550ffd09214130833479f854046731bba06d29607fe57f73189acaf0765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36448176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c27ddf2b1ab6f253516f00163d2497591a276647f8e7c94f6c887e38f45740`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad87253ef97c3a52ca116560670f0c15af4a39f564ea8023b77cead6d005e69`  
		Last Modified: Tue, 03 Dec 2024 02:21:58 GMT  
		Size: 2.7 MB (2714491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb09e299cedc4ff4a0ac2569641c8cfc4c2fe843859c1dbf6827907063ea8c`  
		Last Modified: Tue, 03 Dec 2024 02:21:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10195e2c435a8d8ade06d830b7d2396953742e6a190089c17ecfe0cd1ba120de`  
		Last Modified: Wed, 11 Dec 2024 22:32:53 GMT  
		Size: 9.8 MB (9798460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb71d41bf71963f31d05dc68e6d881c6200b7a313ba6d6e6a188b64cd806c5`  
		Last Modified: Wed, 11 Dec 2024 22:32:53 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9e56f1d3199bdd011c1f489c1314fbf7fda74a7e000db6ce250d1cad4bff0c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b44aa515048cd5624d47c4f3ebdff1450851271f1ad3f98e7b9a3cb9e5aa58`

```dockerfile
```

-	Layers:
	-	`sha256:e32c1cb06f28859476c727fb5f7d394f7078818294f78e94587e83cb55c6a709`  
		Last Modified: Wed, 11 Dec 2024 22:32:53 GMT  
		Size: 2.4 MB (2373270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5cfbfe7ce9a4b540e123dce09ddaf3087f6f14e9085de3dc05c51aa22546b55`  
		Last Modified: Wed, 11 Dec 2024 22:32:52 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3cb4d83a83e1a54db352ec668e2791855e3fe5f602c14af398580c71f0be9094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41164947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc617836e582c7aaadee8d431412c0d82ca1ca6df7167f641060d78cea9347`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e967a942dd70fac74366cfec16cc980040960abdf2198134b9e00e1690681cba`  
		Last Modified: Tue, 03 Dec 2024 02:24:53 GMT  
		Size: 3.1 MB (3129808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb087bec239a2d1e830d774fe22a70569dd7860d6c3fc124a3bc0bf8b77944`  
		Last Modified: Wed, 11 Dec 2024 22:30:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf0b06fa54404468b797b583199defecd054ca48c42400603719b3006e88cfc`  
		Last Modified: Wed, 11 Dec 2024 22:31:28 GMT  
		Size: 10.0 MB (9974693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f648b0065e537428f4383a85ef298a7bb2d4118255cacba94542c15a4244d2`  
		Last Modified: Wed, 11 Dec 2024 22:31:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:bb49a1ef0abc070e73fdfaa1f93f892857bdf658cb4d63da3ef0b2dd471ba506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb9abeede69480744c3338613c69e19c1737db975772adf6f870e23a65d53b8`

```dockerfile
```

-	Layers:
	-	`sha256:4ed123dca705cd3b909350298c38c212a9354c7bea500d75eeb3e0d5dc70ab80`  
		Last Modified: Wed, 11 Dec 2024 22:31:28 GMT  
		Size: 2.4 MB (2371310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403b50af6ff38f83dee01f29f7d59198e140e83d6c1d40980b1fa712e9c62922`  
		Last Modified: Wed, 11 Dec 2024 22:31:27 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:db3360b4ca0f75db1dbf867e6023e0aec605f5c33d15b693a427a85d4b55ed69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42251732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4d4d2a95e2b54e751cba5369bf0a78d3ce3d931d6684745dd5ddd9819e5191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111821be66b414c0e6ef28772cdd40580de350bf1347df9d4aece69fdd46e322`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 3.3 MB (3309291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5623f3c6b29eaa03cacf533a8102ba028e8757acb41a3aea7cafddd5a3c638c`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a512ec05637b45312a440a73c19588dbb1f1160eaeb5cb3afb5a457de893c`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 9.7 MB (9735311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0902c04b250bc52cf80053be83c31ebbce566db0e9835a5d7c0aea0c8399a9a0`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f93d125df48257e2f5b20092f17c5d83e9f5c5cda5fade80cecf0879e0d59a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d214239fe2a6a84b1c48399bdc7dc99b66bf6bb15276ffbca4069adeb5f47c`

```dockerfile
```

-	Layers:
	-	`sha256:3a43f0d604700dd123d312561884e62744b5613c5de5f89dc2e08b4ac9b5948b`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 2.4 MB (2368155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e1887bc78c793eedb2357c0f254c04577df93234f3742904d73b5411cfd5b3`  
		Last Modified: Wed, 11 Dec 2024 22:30:18 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:ec107f6e57e55628c3f211775e4b8146dfdcf6391734ff21d10e3ddf07a741ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41317206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d787fff2c0ebebf9a03b593db54c1a5d454893cd24d9e7322cad791ee438e84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e633c9f42a4d85d5fbde0a6c2cbcaf83e892f135ac097847ec3e294113d405`  
		Last Modified: Tue, 03 Dec 2024 02:28:25 GMT  
		Size: 2.7 MB (2702403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7993430be6b98226c3937c3c19a1bf3421be95510a1bdac83e4dcc0cc10dc49e`  
		Last Modified: Tue, 03 Dec 2024 02:28:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382457b574482f6e4cf52f1d6dd37c6bcfa857c7c6bff900ae0f30e10a0ffbe4`  
		Last Modified: Wed, 11 Dec 2024 22:38:54 GMT  
		Size: 10.1 MB (10107256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f529f4d22cbac389ce3a67ace645afee615be1994182c7c3a8921dd9bd9eb7`  
		Last Modified: Wed, 11 Dec 2024 22:38:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b7657e5a39736de59772ba1925492866f2b9eab2f4faf6aae4892b626c0d5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b0f4ce291ec9b9e6fac46d8d9a346704ef271003c0310ff35311ce80b84e15`

```dockerfile
```

-	Layers:
	-	`sha256:542641118872095b511f4d5e7d1fd50ac10b925beb88bdffbf57bf66a3c68c0b`  
		Last Modified: Wed, 11 Dec 2024 22:38:53 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1afddc52162d3ef75e1f26f0d3396e03d877bdf1a87c5fde3fe6f63a709796a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46067717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b70c5c728c67de8a8f0c6cac9cab0a5f0cc2e796f1aef8f1311b0aecf38e28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b5449b364af9fcb832ee06143046449d011599603f5cf5e62b5f49af211c7`  
		Last Modified: Tue, 03 Dec 2024 02:19:38 GMT  
		Size: 3.5 MB (3509551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88fbbc6b6a5215fa116f6b9d908ffd3b8c34faf57b65513db150fa51664ada2`  
		Last Modified: Tue, 03 Dec 2024 02:19:37 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21227f97175d9ca5c1d702ecaa940143f1de5cdfed68c26940afa763bba6cf7`  
		Last Modified: Wed, 11 Dec 2024 22:31:37 GMT  
		Size: 10.5 MB (10493263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d982482f8c5d20725d9d39d7427941ca29d3ee49eed2c553eff7d6fcda9d5060`  
		Last Modified: Wed, 11 Dec 2024 22:31:37 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:dc181e6a9e639b2d35a457377a0dc77866078438cd0fc485cec13a721910bff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de0f52691a884a2f0d4a4c997cd51f082f37ac0791ead5876c6a591abef4ea`

```dockerfile
```

-	Layers:
	-	`sha256:8f17fb9b3d54310573f348ced56ec67e364071affcbce8bd361bab024263606c`  
		Last Modified: Wed, 11 Dec 2024 22:31:37 GMT  
		Size: 2.4 MB (2375341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58592c8cc72ab5bd7f59561b347b2e7ce257164442835810a1f735fc3e369756`  
		Last Modified: Wed, 11 Dec 2024 22:31:37 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:14bbec20539b55a9472df7283d34eb6c3736026677e7d9e4774740ce6552ad08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39729954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ba8e5a09b2992d917663ec897a3e051782899288b365e792890048d6c02d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_VERSION=3.1.1
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Wed, 11 Dec 2024 18:13:35 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
# Wed, 11 Dec 2024 18:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 11 Dec 2024 18:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 18:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Dec 2024 18:13:35 GMT
USER haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 11 Dec 2024 18:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1a5712dbd5b4b44364c8fb8cf14ed098f92eee5aa0421fc82fc94264f627f`  
		Last Modified: Tue, 03 Dec 2024 02:18:33 GMT  
		Size: 3.0 MB (2969177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ddf8bc0b908cf7283e2cd0c726f2d5fbffb4ec3f0b82e296e6d077e4756e3`  
		Last Modified: Tue, 03 Dec 2024 02:18:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46dc4b3eba83d657edd8d2985183936a046009e9a59e92597d36d2a154d5bf7`  
		Last Modified: Wed, 11 Dec 2024 22:33:00 GMT  
		Size: 9.9 MB (9880166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a78c47b1f7471bc0c2c46b4626430c74d8aa16826c0ee79e737768282e46fd`  
		Last Modified: Wed, 11 Dec 2024 22:33:00 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f765eec47ba125ad8385286cc840b038f064b7c0864a2ed543a6ccd9b9748116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8da77fd86ebbc85497ca2d75a9e32aa32018298d7672acba6262c9cea1c2e30`

```dockerfile
```

-	Layers:
	-	`sha256:dd41fc483e411d871f8a2bc7bf6155bf8eaaed77b1e01b626e90a073d75a474d`  
		Last Modified: Wed, 11 Dec 2024 22:33:00 GMT  
		Size: 2.4 MB (2370751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3f245f5a0499335b9f5713204519f090f3b770b0a71724c15756af80e55b50`  
		Last Modified: Wed, 11 Dec 2024 22:33:00 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
