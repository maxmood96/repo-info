## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:46158355f629a5e8e9235a9c9a82b9faac2e1a8bcb036c49996f7a729af95dd9
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
$ docker pull haproxy@sha256:5fb6e69f062233768edca21062ea5818a602d92e4d608b6739f58dace6dede3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41725444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951a8c9fcd32fcbc06df1ba5942e885209f7f30b10f55182d4605ec0b32bc6f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d02d7622fb8b091c65b014e4f35d10309bd31cdab123d8e2c654fe23140787`  
		Last Modified: Tue, 14 Jan 2025 02:16:47 GMT  
		Size: 3.5 MB (3499325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d2efce4b7fdf6c4644bf1aebc294a4cd0f51a20e36ffa3ab1aae7d6687ac35`  
		Last Modified: Tue, 14 Jan 2025 02:16:47 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c18dd7094ddc86f539985b41029f0b03d15c6396bb323f660fc5db167b5bc`  
		Last Modified: Tue, 14 Jan 2025 02:16:47 GMT  
		Size: 10.0 MB (10012066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe85531da4193f48b50f6626e4827d1b32812f0059f9ee913dc14516bea0771`  
		Last Modified: Tue, 14 Jan 2025 20:33:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ab1e0d34e45d22cb8e56320c58d6b24932585ed6f24f9756cb8bbcd0e67dd980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f170f6bd8dcccb8ad94de53051ee310b793f2a5c4dd91e28ef7a2d5c2003ecf`

```dockerfile
```

-	Layers:
	-	`sha256:508e7a0bf0e524eadd724c08a452ddd91669499ec4e4c0da585719f52fcac9a2`  
		Last Modified: Wed, 15 Jan 2025 00:07:40 GMT  
		Size: 2.4 MB (2369045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec2e273a0cecc8171a089c41dc1f14760636cea0de586ddf836e629e8bd7aafd`  
		Last Modified: Wed, 15 Jan 2025 02:56:03 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:1de22d0af39ea94494e280c57adfe0e9d8205af1f85b971b74990a5047a2f6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38809369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d8e32f494b086d827813b83659d2521fd5b8ee7c27ea157dccb82d9232e640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13cab84d28620a7a08021a20ad2ffc76f921f7e124b546f8caefddd64d8d572`  
		Last Modified: Tue, 14 Jan 2025 02:19:10 GMT  
		Size: 3.1 MB (3073438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347acb2bab2b92056a6d75c784e5cffb8e14a0a97a5f293450554d7152b652e2`  
		Last Modified: Tue, 14 Jan 2025 22:25:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabc5c06a5dbd6563dbeabb7d4fddb4f598042e44e63cbaf33fdccbf32394c29`  
		Last Modified: Wed, 15 Jan 2025 00:07:40 GMT  
		Size: 10.0 MB (9997624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716e3bea59255b3c02a911f07266d22852f9cf65df7ebd798cacdc51df02910c`  
		Last Modified: Tue, 14 Jan 2025 02:20:23 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1b1fcc8b53139f6eca74d76709e6a9264c2ae840a2510fb6bc321f9f6ee4a329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770f0161b28cd8fa4d9349e95ee289d631b12b79392bb5c932d818ceefc1c3c2`

```dockerfile
```

-	Layers:
	-	`sha256:ad1c6fe0abf7dfbf3d0dfab98657e441261f552d777609d20619129a5a591376`  
		Last Modified: Tue, 14 Jan 2025 22:11:25 GMT  
		Size: 2.4 MB (2372559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635769d9e855706b65435aae8a8f7100b76d537e6904d7132c5b82a724ec0d4c`  
		Last Modified: Tue, 14 Jan 2025 22:11:24 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:de40603ef4b90be97813948747d271c948c706a38261b91cf1d032a635af27a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e478b31e702d2be8e5ad648f92f23f08175daabf1b75a21417fd1831e0f844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 22:25:06 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312571f07e47f0b85563d7245f56f68d3f119e36dbe459d1fa3d77f999f576de`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f85eb8933604f8ed1730c95015af01c32655231cdb7b1b450babf76faa0e8ce`  
		Last Modified: Tue, 14 Jan 2025 02:22:42 GMT  
		Size: 9.8 MB (9802544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9a45655168b43d17bae1e0c718b54fe577cb142ccb62b0b172249e2763bb1b`  
		Last Modified: Wed, 15 Jan 2025 00:07:41 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9260d1f011fde4276c2af04e73b6b3f8462032c0959e4d3711a9008b9d5fe5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7fb3c9836c5139d15be3948b4c16ae7ed8d1833f6894d6f80f937c283a376e`

```dockerfile
```

-	Layers:
	-	`sha256:94a2cded7e839b9f20c179f56185714b45de07c155fc3763521e1fc0d8f265e3`  
		Last Modified: Tue, 14 Jan 2025 02:22:42 GMT  
		Size: 2.4 MB (2371288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b211f66b6ff02200dc3647d4f2a2c91cf955e4e2ba08fd51fcd43a68d83a17e`  
		Last Modified: Tue, 14 Jan 2025 02:22:42 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:c333a5ab3f1fa82967587d4cfbf3e4d6e6bf99169b1702a1e462500f88277607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41341177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf38331e0387a63df21a594aac1e2becc173d43a09095140895fcb7312e5075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3616c13f0ae03b4667ff114759560d5f2bf0f9ce7a42468a64f52fea448195`  
		Last Modified: Tue, 14 Jan 2025 02:28:12 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fef0736737aa905dabedfa27a9b5fb6f13f5a6e6a5e454038f2f849bf6049b3`  
		Last Modified: Tue, 14 Jan 2025 02:29:00 GMT  
		Size: 10.0 MB (9975632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c07f10fc0225ded7055571578f0737d238b454663b72aee9b26cdeb74d3463`  
		Last Modified: Tue, 14 Jan 2025 21:17:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:07e8ccc6598fcf893de9a3a2b97a89dba9f5b2862d94f93ff3478acf8bc9715f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b63eea3fab0a2aaef40835a30c94d38d667b0696050c68b3fd147bbce6c655a`

```dockerfile
```

-	Layers:
	-	`sha256:9bc980b9b43d848436e17a259b964469dfee23b5003800fbc13aed8a62986118`  
		Last Modified: Tue, 14 Jan 2025 22:11:27 GMT  
		Size: 2.4 MB (2369328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca5ad022a0ff53696f8cff789934d6ff2f77f5a29446d7f59591e9960e0513a`  
		Last Modified: Wed, 15 Jan 2025 00:07:41 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:44fada68c098dd6417ff060d74ebfbb641f7a7dbdfa6e526c99c40d9fb941e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42428276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c04503e04ef02b4e95ec75ec911031bf89967f5ee92c927fee108a4a151fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705c674f354bfa1d3014afcd2c48ae36391c87a70273ca4bc9e0b4c4cafc76c`  
		Last Modified: Tue, 14 Jan 2025 02:16:56 GMT  
		Size: 3.5 MB (3503390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d2efce4b7fdf6c4644bf1aebc294a4cd0f51a20e36ffa3ab1aae7d6687ac35`  
		Last Modified: Tue, 14 Jan 2025 02:16:47 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703b8fdb9c94f982323cbe8a76512c5953c9176c2e88c4969c8464b6fddcb850`  
		Last Modified: Wed, 15 Jan 2025 02:56:12 GMT  
		Size: 9.7 MB (9735653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2da0a4b1dfdf0b7b1afa74b8d4c5ff5336a489e5f5709a3b66ee7c06eff42b`  
		Last Modified: Tue, 14 Jan 2025 02:16:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:a7dc78d3044f855fdb979b1b8686ea6789588bab3f81a85b1a83d17cba061e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0202714b820dea764fcf7f2b062c7b9c857129f50acaca262d8756c64fe13b4b`

```dockerfile
```

-	Layers:
	-	`sha256:eec7d0c3d62795f9c8ccf825547512c6c56327d931fc39c5de115d03b5b63854`  
		Last Modified: Tue, 14 Jan 2025 22:11:27 GMT  
		Size: 2.4 MB (2366173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b771f66fa2c1d32d58664669a00bc8f2555ccb37e746244e19ed313597e53daa`  
		Last Modified: Tue, 14 Jan 2025 02:16:56 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:923647feab1bdaf34e258fbe090294d4f18f2e3f4e0b74b16dc7a6606907850c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41491336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd0693aea8df6d42b37c66b6d7c0d47461bd641f90af6865d5a92d1fece7d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee81822f69876da1e9c9b593b95f8643321ed94fb5b99c1066f245cab214fe9`  
		Last Modified: Tue, 14 Jan 2025 02:28:04 GMT  
		Size: 2.9 MB (2895367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6baa679cb4b900d271d63935f647962d397fb609bac90d5b455c09d82315cb1`  
		Last Modified: Tue, 14 Jan 2025 02:28:03 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6ac591e5c0cfd2a64707e9dde268968b4c0b85cb5225272bbfe5191318bc7`  
		Last Modified: Tue, 14 Jan 2025 02:33:00 GMT  
		Size: 10.1 MB (10107675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032f105bac6d09f59e2f2bf89a49a29d7e7c6f4aefa1e1deb19e75c57b220970`  
		Last Modified: Tue, 14 Jan 2025 02:32:59 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:22774058e7b29a822161f56e671db0ef1fedbddf687b10ee487be12329ba5756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771f38f3196928a544b1149131ff6caefb82a6ce397e08e311e501e4029933b5`

```dockerfile
```

-	Layers:
	-	`sha256:580d1d0bc536ddf9e316eb9c36d41e279e30ce2c8e869f4eef0254d2eb7bef5e`  
		Last Modified: Tue, 14 Jan 2025 22:11:28 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6b3fa7976c5f6f6a81229fbbe4a8bb574f717cd380e8ca10b399c8bf08d7cfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46246803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3060b9625d8dd014f48b56ac0dc1ad9dc39815b0408e7408c4247490df1371b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44315ec43757aad8b172b926300df5a2604e6d1df5516e4bc1e3f10784621b36`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943f76e340a77be18c0adb70abf754cc28cc1347464522e41be2285dbffe1b41`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 10.5 MB (10497408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9405c3f0b4095a474852864803bf1a6c670d1485649c183b48e13dedf3c4bd`  
		Last Modified: Tue, 14 Jan 2025 02:44:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0aae50a4a74b2999b1fa5b5c5e0311ec0a8e02d17f4526d25f71d76794249b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714d238ca46748b421f8de097e4844cf7ec22c2fcab86e66af8a0d9de73102d0`

```dockerfile
```

-	Layers:
	-	`sha256:49593a4a4fe12f71111cf6aa1dadbe28cffa067c7a1a1fca74030a4672f548dc`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 2.4 MB (2373359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ddc65a18c7bd7e17efb7a6a65636de0d5ffef69358301219d6dbe4907956a9`  
		Last Modified: Tue, 14 Jan 2025 22:11:29 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:27ff425ef7674c91cad7cf89a70d288fabeb5226e85c00280ba1473ade84f46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39906862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a38485a8b064f61dbee15f1751014f32c6b5bd9cf8d0dbc9c9d34af0a27fed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 09 Jan 2025 00:13:35 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_VERSION=3.1.2
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.2.tar.gz
# Thu, 09 Jan 2025 00:13:35 GMT
ENV HAPROXY_SHA256=af35dc8bf3193870b72276a63920974bef1405fc41038d545b86b641aa59f400
# Thu, 09 Jan 2025 00:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 09 Jan 2025 00:13:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Jan 2025 00:13:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Jan 2025 00:13:35 GMT
USER haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 09 Jan 2025 00:13:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed175806a9965adb498bef3a953ad655c07286b45f574660a8685b6d96c01059`  
		Last Modified: Tue, 14 Jan 2025 02:33:53 GMT  
		Size: 3.2 MB (3163307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f309c1cf5d1c825591e3bfa7b759cc496b30d5c71dbc2f8f838946447cddcf2e`  
		Last Modified: Tue, 14 Jan 2025 02:33:53 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a51999088305db9293af33d164932ab905267aa862975ae494b38aee966be`  
		Last Modified: Wed, 15 Jan 2025 00:07:45 GMT  
		Size: 9.9 MB (9883176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da80651fd9c77e74897f305d3b69ff2fb50dc85652ce9740ca0732253b79dfc`  
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0d94bbb6da3d7d719c11307d122de1fa93fc7858c7a04ecee94603c44190d515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5923c5d361c3f964f9899a2fba74bb28753debbdfa55189a412d561018dd48`

```dockerfile
```

-	Layers:
	-	`sha256:86592d335f325ddb49fe6908df2f256b2a4ea0fc844800fc027bd90a1255a06c`  
		Last Modified: Tue, 14 Jan 2025 22:11:30 GMT  
		Size: 2.4 MB (2368767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7453c11aac39c89024fab5b5c9fb36f51812e8980ade1243524fb342f3a34c0`  
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
