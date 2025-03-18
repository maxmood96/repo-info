## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:b9c478426f5b62164d4552c595a546f42aba4fabab5edd2a74cde084362906ea
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
$ docker pull haproxy@sha256:ab1e6457b94b2cb09d287aff2fd7199e0964ae333fe1c4d93adaaf0a4e06b400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41721984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbacdc4037c50dc81ad518b420417efb74e70b23a827cabc05db7e59c611360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0049f1195b0577f6707bd5efa4895831db8d76c0e0aff66890fde0b1004a1`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 3.5 MB (3499359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11136e79dbfa2ea9985a6aac4878a50e805b0cafc38e8e6f84ea551bd90a7a86`  
		Last Modified: Mon, 17 Mar 2025 23:13:11 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d07d7aa5811c5335aed9d3bdae59c01938a5aaf9aa7503797f15cd0027949`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 10.0 MB (10016123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a0e5f066f7bbf1761dbd289b50e14917d0c97f74cd5ca2189ee4517cfa8a26`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc336803932e86bf5869a7d86ec3e9ac9fba43485bab9ec46a40ad60817290d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545e37b309057fef6c221d641ccbd41bf4cc9bf2e46f4885862483a4ec5a10f5`

```dockerfile
```

-	Layers:
	-	`sha256:0250df2f27e4575df1ada0b840abb4a6022c91dc499780933eb9b5d177327345`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 2.4 MB (2369071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee3c21f60f3bfb648ae893a7894cada33be0415b69068ecdcfd458be5a7c46`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:4a5fd691b8b74cdef78c9179a84b6bf3067867480023bd48f065cb3378a0f38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38819232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964249dba15a0e3fc1245695c4b15088d705f3e6bfab5b30092042895c2c92a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a06bf00a22e98835898fabeb6f4b4e688d5e3dd40a63cf933c7a8f01f50907`  
		Last Modified: Mon, 17 Mar 2025 23:15:23 GMT  
		Size: 3.1 MB (3073487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e989cc552c37f191008030afdd4b3a51980fe51d0d335aac5432300cdffb3`  
		Last Modified: Tue, 18 Mar 2025 02:24:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee39fa3e56964bc222d59625bf9e184b8da06e1bb7d8c6dc846e37b17592807`  
		Last Modified: Tue, 18 Mar 2025 02:25:39 GMT  
		Size: 10.0 MB (10008253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f264488c531641bd9d9357e881e931fe55b9ede3787d904c5d876715bdf9ebef`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:5145cdf1d733d13fc81efe75a871a3f0bb3d942196d00ae323dbbdbae7113e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a69f9f0a7fe599e86aa552ac2e21bf9a0717d40d35af89e32e657ef843ff4b8`

```dockerfile
```

-	Layers:
	-	`sha256:71555d98bb73d9b00c86e812bb27d2dffc4b5c062f06d864a5b83d0858832de7`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 2.4 MB (2372585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853d70f04c76bea32a455f3826436ba5d67ba69b6f967bb4c78f9600c510a0c0`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d03a293a5d690e571b116efd6d67ad5adea8e87a7958711303e5959e9f33ae69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36637221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c1a231c399eb6ed9df6a62a62b60188f10b248175c3914bc28926cbbfb926d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de84afec6d4f313e7bf277c66cdcd6136876e4c4965613cc67e1980d1444fb`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 2.9 MB (2907809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3765238d144b9228c5e898a9ec77dcc08b04f997fa12e4fc93987498a9d089f1`  
		Last Modified: Tue, 18 Mar 2025 07:08:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096995b20684bdc81bf0ebc6a44753b78dfa3779312d549a3c0b4a34fb6cb195`  
		Last Modified: Tue, 18 Mar 2025 07:14:48 GMT  
		Size: 9.8 MB (9812682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a88ff757f7d9291f0388c0bd8ca21b15c5d433a3fd5c61518ec29d686424c7`  
		Last Modified: Tue, 18 Mar 2025 07:14:48 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1fe878bdcb2c40acca42b79e238ff5e18fbb18184f980745e54a1a32319618a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14ffc4f611d1371272f47d1702a042f9c5146cb95ded7fcc4bfe1dc55f36d4`

```dockerfile
```

-	Layers:
	-	`sha256:60e45df5d91f1c87b0d17ab6d3f118a9f2e7f8088fcd0a55ab8eda1ad85437b0`  
		Last Modified: Tue, 18 Mar 2025 07:14:48 GMT  
		Size: 2.4 MB (2371314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3f499035b1f6b8e05fa0ce6f1da54af98071e1733660dc026f9e89a259914f`  
		Last Modified: Tue, 18 Mar 2025 07:14:47 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:8e86ebbe525d68f8cd92afaba90a8a910883395c7ea53a9a90ac0ce4c6a1fdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41355798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37894457d36c2cd3478415c80497399f01a73b98a76f773bf1debe7b2597f8f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1f5b37bd6494f4c979734eddbf38ec3c9d650a090b347a2d957a8954d0749`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 3.3 MB (3322905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fda645ddd2b5a49119537bcb0432102fb1e852edf58b5e103ffafaf3d2b76f2`  
		Last Modified: Tue, 18 Mar 2025 08:10:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a6c88a6fd1361c656584b51c120d71aef54e79ee4968c71952a6447ace4313`  
		Last Modified: Tue, 18 Mar 2025 08:15:30 GMT  
		Size: 10.0 MB (9987218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4782360c5635a715f3eb5e06ee0c6521ad161c9be392cdc50f08af8360e30ef`  
		Last Modified: Tue, 18 Mar 2025 08:15:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:cfa1b55f53cfa934859861c0e64b952cabdd39375a9393d19c93ac1ad9cc3930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c9c03504ee9f2a312ce74cf2f5dc6a446409a7fcff9cd84234cef72cd7ac67`

```dockerfile
```

-	Layers:
	-	`sha256:830c385042371a3e0517620cea8e60b384c41a614762f0ee304d1944c3152146`  
		Last Modified: Tue, 18 Mar 2025 08:15:29 GMT  
		Size: 2.4 MB (2369354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d492266059947529306519c719a3b9d9d1a9d9081638ce4c54af8fe91f7d078f`  
		Last Modified: Tue, 18 Mar 2025 08:15:29 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:020a23c6edd60f421de4b36fe32caa21fceaf6d98d10c31115730aea04e66a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42443075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ec514e3a4a7f1a6761e08bfcab4dcfd6db6cc61bf95d15e19a0006adda57e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cadead52749063b96e13dd2a889ff0d752c169ebf517085465bcd00763460f7`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 3.5 MB (3503408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b27197f6d64b5ed020420080dab2741a3218e77347640f955bbdd82f06e91d`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd36bd5f66c14c5c25ee40e08e22e1c24c275fd91be421a719a3f5e8ff3aac0b`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 9.7 MB (9748499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a782d14963a13621987c53de7f6fc0119589d647c26a6badaa8be4771e086b`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:343936e5ace5e020f90d651d4b6f787b6c307fc31f6b00417e10a758da401798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152986681ddffa2a195c7b6a631cf344345d2aa3d01d0022d984a5d0104b5b74`

```dockerfile
```

-	Layers:
	-	`sha256:17687d261b14c10690c735efaa4a8be82416b4c840e192642364dbd0d904135b`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 2.4 MB (2366199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d76b3d3101112bff878b789130b7598bacc17d507674d3d071c7cc114bd44d7`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 21.7 KB (21723 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:e2553890a6593771a39d1c4d562d84b8b5a91433d9dc0f9530c2199fa1730b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41509321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4b60d948de552e03fb9b27aa7651c06e343e0575b138e9fc5e3c0e783bd12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c82bfc1c2f5e4b0dc4b532714b8582fae92d04a9d4c6e432252fb2e247fc44`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 2.9 MB (2895386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d134d9bfb627f1719193c98a83137b618b72692f2b807ec8b91ad1507959f317`  
		Last Modified: Tue, 25 Feb 2025 02:24:08 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f168b861087b1b2a2c03f310fbd49ac0e75a6a89936860f6a0f2863778567860`  
		Last Modified: Tue, 25 Feb 2025 02:29:04 GMT  
		Size: 10.1 MB (10118607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f4ebb43b12fbbc6d5643e518fbd11072ac9a954d204ba438fecbf4965109d`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ebea310c156e07c3d68c33246d876a42c2ec2cd4ad233c7b301b66bfa0a181e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1fcdb5b0571500c693cc3c525d581930214dfc2abc86fd5b8c1a74f666569`

```dockerfile
```

-	Layers:
	-	`sha256:8546480388ca37acd62249f8a4515d23d7586c0b96b4f9822731e206ce73d58f`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ef6c81772fc36b5cce997a015c720a32630eb6aebf3fc816640b2f2ec6e259f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46257712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1219f7c91b5d0bf4f9707cc84267316cc1fc431891ca500082d7590e9c4693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297f17f6db06f7ccb8ce850d74e9476f76be07c3d767a47f85269129c1aa3413`  
		Last Modified: Tue, 18 Mar 2025 00:05:31 GMT  
		Size: 3.7 MB (3703023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362219842806f48e93cf4a662cc0a59d3d9b5f9daf98f8205062caca3e15349d`  
		Last Modified: Tue, 18 Mar 2025 04:47:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae2d0e972212cafad7d7cdb10d2e21f0fd9a87f02f037a6898eee15e80efb5`  
		Last Modified: Tue, 18 Mar 2025 04:53:48 GMT  
		Size: 10.5 MB (10505235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a0544b29d6e347de65eef0514ecdcb3626b114abad6f0b36ec1db467c7bf17`  
		Last Modified: Tue, 18 Mar 2025 04:53:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:19e8e8c175e0ee0011308bd7bf0020dcf3860c0314490d82d2100f721b48377d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1a1251b98e35421c804409c5363742c501b77d5162578e61eb1c02b3587dd8`

```dockerfile
```

-	Layers:
	-	`sha256:0fc36b6809a027a986d79f47eb396c18c24e02c6a40322f47f8e442220b3797b`  
		Last Modified: Tue, 18 Mar 2025 04:53:47 GMT  
		Size: 2.4 MB (2373385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125ee9a192b3de9cc3d9b6067c7011eed64a8f78500acacdb44cfaab78a3bc8c`  
		Last Modified: Tue, 18 Mar 2025 04:53:47 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:8d12668101040f7ea944bc20c024b0551684f5ff051e9d349808e806cb180c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39918191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789ae4a0e2c2ad6fb7cd650040106c48aaaaadb06319da2d78058319f34d6993`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ac3c278183a5f89567d212db7d1cf86cdf072aa72fbb0786fd4105c665de4a`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 3.2 MB (3163408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43ce713239db99624dab96db5ea2c8992f8b744a35530773019f8a009022034`  
		Last Modified: Tue, 18 Mar 2025 04:34:19 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dca3f056fab44b46c21179dce7b0f3d420afa145bf66b6013076ac6b3e8548`  
		Last Modified: Tue, 18 Mar 2025 04:35:24 GMT  
		Size: 9.9 MB (9892086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4682507e067b96dee41fcd009153f6c10bc8413d90ce4048a52bfd165bd4d702`  
		Last Modified: Tue, 18 Mar 2025 04:35:24 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:80c680547728be942e30429092e7540def32bd7111ab9f189a1509a47ebbb6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541c8f1d9752c56d25ff026a076e558e579462aa2765a176a3e68ddb63bece84`

```dockerfile
```

-	Layers:
	-	`sha256:b5a186d4d69df9b84f407ad051c18d55f12c22df0f675165aac8ef1c087b4cb1`  
		Last Modified: Tue, 18 Mar 2025 04:35:24 GMT  
		Size: 2.4 MB (2368793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116fc77afcd7cee1c716aa3ce76222b9a51485c07c7b7cfacacc395654b3053b`  
		Last Modified: Tue, 18 Mar 2025 04:35:24 GMT  
		Size: 21.8 KB (21769 bytes)  
		MIME: application/vnd.in-toto+json
