## `haproxy:latest`

```console
$ docker pull haproxy@sha256:04bc28c91d0a4a14de38c14abab63c6afdd5e647e1227f00729b26511c7d7726
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
$ docker pull haproxy@sha256:d708a34b51af22999c3449a799a9b5dfef348acf43d34b8ffad451127f1f0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45901492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7363bbfd8278f2bbcd14a21b9c81cbcf2946ac22e6cc81a24229cb2f46eb4c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:58:42 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:59:23 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:59:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:59:23 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:59:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:59:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:59:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:59:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:59:23 GMT
USER haproxy
# Tue, 19 May 2026 22:59:23 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:59:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd19dcd5f2a11635836f61cb0a1aeb84c74e419525f3632239f25915b85a8a`  
		Last Modified: Tue, 19 May 2026 22:59:30 GMT  
		Size: 1.6 MB (1581315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e6d902e906b5df6e508e9d421c2018731687ef9bc48ca4f30fff886d2c4cd`  
		Last Modified: Tue, 19 May 2026 22:59:30 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110402a6e26e347221865f477d9c12e218ebca88bdbe00ed14103b14cbeeb9f`  
		Last Modified: Tue, 19 May 2026 22:59:31 GMT  
		Size: 14.5 MB (14538611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5055908a3a025aaf80670058abbe08722547c198932db9f12539a783771a1d93`  
		Last Modified: Tue, 19 May 2026 22:59:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6b1339d58b82de149dd379b8c42714c8855623f607c8f49781be4fe8f48373e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585749e087f6f08a1e8a5e08b8cbe612092df29b39f3b2b84eddd78d8bf7cfae`

```dockerfile
```

-	Layers:
	-	`sha256:d1873c41930330713d6dc232099f31ee640643517332df156bd9ee5da2467321`  
		Last Modified: Tue, 19 May 2026 22:59:30 GMT  
		Size: 2.1 MB (2113846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154cfb13f8e0aaba649b1d3496946923d1ca4aac3ea2b265a7e6e7c375f9337`  
		Last Modified: Tue, 19 May 2026 22:59:30 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:70979193780ea5be4d8830134aaf57da7a7f547301fdff0da630329f7de39e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44228111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d9e15dc7afd38786a6eb739cfc3ad3199cc2db42c44a30dab17532050e3ca2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:17 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:58:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:58:17 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:58:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:17 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:17 GMT
USER haproxy
# Tue, 19 May 2026 22:58:17 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a545ebcc4356d010b8da52afaa199fd980ab2601862c6924e8c26e205b5647`  
		Last Modified: Tue, 19 May 2026 22:58:25 GMT  
		Size: 1.5 MB (1535909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c95fa7e29cac2b95d1386bdd2f46771de0c1f0c94a87d30a37bd8d49e6215d`  
		Last Modified: Tue, 19 May 2026 22:58:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc79ab83031d077257e92674b878023063bbc2f17f24e2f0ae454380818a78`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 14.7 MB (14736693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7182e0aea1b82db801b29fd829226fc1a82949212eae5afa2ace2061d05ac03b`  
		Last Modified: Tue, 19 May 2026 22:58:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:2f00ac9448026bfc95f2efa34af157f861199bdae6f424953234b2c0fe23a015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b08ba7cdeb2be01c7f2754a18a3f73035b23d2e6588f102722e675316f69f28`

```dockerfile
```

-	Layers:
	-	`sha256:7e6b96c40136a891c3d06cb83a92fc370cf5f887499dce4cb3a8aaa8a124c65e`  
		Last Modified: Tue, 19 May 2026 22:58:25 GMT  
		Size: 2.1 MB (2116826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad48944777e581656734e57c079dace2d0a2a09d88b4f5264475d13cce6e899`  
		Last Modified: Tue, 19 May 2026 22:58:25 GMT  
		Size: 22.5 KB (22470 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:28b8b7e649767c97e47135fe07923a303f1ed461d55912e44e8239abeca393a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42227093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fac5b7ba7e9a9ff5aa9e615a95dcfbd481661fccfa09944773c49fb9c1c10e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:59 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:51 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:58:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:58:51 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:58:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:51 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:51 GMT
USER haproxy
# Tue, 19 May 2026 22:58:51 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cee2ef5a3d4438593a8a7922577e2281d99b2dfeab78bac6c0084363ae0bb7`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.5 MB (1489610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0859991d137833624eca0ccf515b87f144209c90f719503532d2957416a9efda`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83296c61ac714ded693f404e1850cbda3f676752b2622ac90f1b8e01d027bc29`  
		Last Modified: Tue, 19 May 2026 22:58:59 GMT  
		Size: 14.5 MB (14530010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf86b58674b4bbf0dd80aa5a0f94584f3838a7b508cb249032becda545f2673`  
		Last Modified: Tue, 19 May 2026 22:58:59 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:18e5ab68cc654a787402609820dc61535046ea00f692a855ca800866696239c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1958a9ba3c923a4de8d27e29e851a8436c1dc6f7060d826de1c322706bc6cdac`

```dockerfile
```

-	Layers:
	-	`sha256:20501265edbeb201673b26d8b213b4959f975f1ce5084ded42b70544ff98f39e`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 2.1 MB (2115269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcecb41f689733d83f3fd7287065256e5fa38a33a333935f2989972d65880f2d`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 22.5 KB (22470 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:7447ac9ab82e980537cfa23a4e21673e97ae86de49f6930d9360a1450d9a4f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46118145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efff287ea2c0ea56fb0db1f017feccd40f3b62157adad7a10de2b1c4f11faa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:08 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:56:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:56:51 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:56:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:56:51 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:56:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:56:51 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:51 GMT
USER haproxy
# Tue, 19 May 2026 22:56:51 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:56:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81212c15d9aefde2b5f01a1a7337cb0b6ecbf56b63bc53ef032cfeca189add`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 1.6 MB (1563980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5735da86effc9c9b3dbc4c587d657a976ed7d19c5db521d419b5d2cb1807f4c`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec73e6fcca07279f990d9ff20e086b6e314921fa6e912a35a882608365503e`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 14.4 MB (14410607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606204b70fbd4b2ffc84fd5848b8c053c66b2d9b54550b63dd4a68e8520e280a`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e3c7d3abbbd91fcbd37dd5abe6bce69849a45b4881b93d9b7504b0b0e9e638f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d65229eeae25d95c027ed6f0c43db573800fdb7730f8c96764019849cacfa6`

```dockerfile
```

-	Layers:
	-	`sha256:c8f3eae1afc6fe84405671bca5287b48014c8cfae47b840dbbf2cbdcf3856bc4`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 2.1 MB (2114123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff32b4a688afacaa33d22ad4a0ea58a06dce3f9b5ce4ab7ab7750aa443baf18`  
		Last Modified: Tue, 19 May 2026 22:56:59 GMT  
		Size: 22.5 KB (22506 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:df90cf8cfee1e1483a470bd00ff9bb97846fb226aeb16efe6113ab7052356a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47221017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec3070f58215ae7935eff9ddc20804e5ea883bc56f01c13ec1131123d854f8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:24 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:19 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:58:19 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:58:19 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:58:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:19 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:19 GMT
USER haproxy
# Tue, 19 May 2026 22:58:19 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:19 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eb8903e95945245a7bcc9de75c6033c0f1ead6e6e010156147280878c46f0f`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 1.6 MB (1603864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be722ff74894a9d94094606408ed2cab30cf2a6a66ead80fed976ae3ec244ad9`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ee3dd48222f2c21b8fe7df92bd8da4c7d5b8423de18f813efb8bd756d6f54`  
		Last Modified: Tue, 19 May 2026 22:58:27 GMT  
		Size: 14.3 MB (14320178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312aac8809c9376db37c1102d9a1ec098f53cd7bfcb9dea9d9bb03b1e8cda1c1`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d713210670d52a77ac6fd88c52abb1806568b79019fbaba023797fd04c21e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf77ef7a6e29982eb3f849bf623d887116f5b50f6baa38dc1683830e0450fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9786150d23c05a1ae6cf79facb287494356df10ad423ebf1735f3df322031e2b`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 2.1 MB (2111027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e541d1c5c71113653add7962bc87f12062029b4477666728422ad3d4af96c15f`  
		Last Modified: Tue, 19 May 2026 22:58:26 GMT  
		Size: 22.3 KB (22302 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c9687808fff6336355a59265ad7397e3c19da6d5045d5f9e3442a38389b33a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50506077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee94de24943156889921918cd975932d98e13a2c50ab3c19c5c9bdbcb1f9a75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:35 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:58 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:58:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:58:58 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:58:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:58 GMT
USER haproxy
# Tue, 19 May 2026 22:58:59 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:59 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2682f083b1ebf5bd4e4423d2b37efeb458f008ac7b2800f061f4abeb082ca07`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.6 MB (1639553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada36dad28b45f88ff713f4189bbe40d949a14533ac18d07a0dff0cd73c3dc50`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6504400ef35bafe6fa0658206965da895fd4299f0b31b255148a71dd4b605e8a`  
		Last Modified: Tue, 19 May 2026 22:59:20 GMT  
		Size: 15.3 MB (15264432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f741d116b1cb94978525a256ec6c015609accfff86d3ce8ac94097779e81ad71`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d34cef2c503c027abd58464abd52c58cf06114d1c37a3dcc7f742027c7ad4d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eef52cf451c80f24fb5e10b8a508a5c9de2b09789fa65d467ae915383dff878`

```dockerfile
```

-	Layers:
	-	`sha256:3d3b871d84ab1332c39239b86045b3e99a6d87639619086087594408870adc5c`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 2.1 MB (2117392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a525889dcee40f0c4da2c4c3efc2d755c0792701ca50f9337d8fb081913402a`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 22.4 KB (22408 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:6b626ea857ded99b593eacce77279a7003caa659bd4c4bc712cce4e98950482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43809248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28188795ea5ec9d022ab0cf5a54f30d990ea6214b6e3e1f39463cc5bc6c10d64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:55:30 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:55:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 20 May 2026 02:14:44 GMT
ENV HAPROXY_VERSION=3.3.10
# Wed, 20 May 2026 02:14:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Wed, 20 May 2026 02:14:44 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Wed, 20 May 2026 02:14:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 20 May 2026 02:14:44 GMT
STOPSIGNAL SIGUSR1
# Wed, 20 May 2026 02:14:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 02:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 02:14:44 GMT
USER haproxy
# Wed, 20 May 2026 02:14:44 GMT
WORKDIR /var/lib/haproxy
# Wed, 20 May 2026 02:14:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43ed4caffc37a4b22e17493e24339a19567e70a308fcaab3e7c52a7bc2def06`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 1.5 MB (1535661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5c3212984eab49401eba678332008a47c0de2e4433ba8519dc27c46dfe9e1`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f8f73663bcefcce3ef22b3d4aef5c009c7d1e0fa66a2cbedb7725641841822`  
		Last Modified: Wed, 20 May 2026 02:15:53 GMT  
		Size: 14.0 MB (13994348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe86753ab1f5d159522899990bcf428111fa57a9575ffd87c99745683d0524bf`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:ef36e48416da784ee3dc4107d91fa25ff4a1392ee7625ce16b4d0b0a91658bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb78156e4343cee0a15d2e0e6785d9c0c97520a6c5e1b8dcc4365f3deec87c91`

```dockerfile
```

-	Layers:
	-	`sha256:aca5bc73a7e09d6e2a1bd90d6f340804a98fa61a37b8cb3b7c855eb4c10d1371`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 2.1 MB (2107783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bd2ab9ecfdcd127da6f32f1182ce97a965b66a753708f6f618651a94bccbf`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 22.4 KB (22408 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:c26886f27d2a98a6fac7fec84a5849cd36169573fff860197290956e7864257e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46366337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975786c92b7a23b50d37ab309082df539ba39c8e5df8b70071e9d80940d07a7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 19 May 2026 22:58:32 GMT
ENV HAPROXY_VERSION=3.3.10
# Tue, 19 May 2026 22:58:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.10.tar.gz
# Tue, 19 May 2026 22:58:32 GMT
ENV HAPROXY_SHA256=6aa919a13f3a575416ef0ae45da0ecb35f1a8d004641dd684fe9b53e646891f2
# Tue, 19 May 2026 22:58:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 19 May 2026 22:58:32 GMT
STOPSIGNAL SIGUSR1
# Tue, 19 May 2026 22:58:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:32 GMT
USER haproxy
# Tue, 19 May 2026 22:58:32 GMT
WORKDIR /var/lib/haproxy
# Tue, 19 May 2026 22:58:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6327ef2c9b917cac7a18188f086850829a86d43551e94112372abfb4a8aa586f`  
		Last Modified: Tue, 19 May 2026 22:58:45 GMT  
		Size: 1.6 MB (1600086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b86fb30089a1560989229f083c3137e05040921da5212ef417751d109f48ce9`  
		Last Modified: Tue, 19 May 2026 22:58:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b936ffd5023d7843672a22359e8794325b3c4e4d6e07dee02047b6e8c0186b`  
		Last Modified: Tue, 19 May 2026 22:58:45 GMT  
		Size: 14.9 MB (14918687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed08cf1d83b9177f34371628b4f12f3ca24a679e213f43551be89471d3060d`  
		Last Modified: Tue, 19 May 2026 22:58:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:586b6cd8c290f7a599cef3315c45cc795e2ada8fbbb2ef771302a49eb7b4ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92231d0e3b24e557052101beecf53660bd777ea917cf37b7cb779d6cf1d90ab0`

```dockerfile
```

-	Layers:
	-	`sha256:c719ba9be6fb69783cf4268c1f9a28bfaadabddc942cb8ab9a009cf697d921e9`  
		Last Modified: Tue, 19 May 2026 22:58:44 GMT  
		Size: 2.1 MB (2115290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f1299b3ba55afbf642a3a84a7850425b3036156592c903b77da116a8a713ef`  
		Last Modified: Tue, 19 May 2026 22:58:44 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json
