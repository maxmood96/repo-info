## `haproxy:latest`

```console
$ docker pull haproxy@sha256:d5b528eaaac3232dd986b46e9daf1ae0787b08bde1d580c1f39abce73f446f99
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

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:0a56554f0f90c2505c408bd6edd03a1d4d1dff281e4cde9d21546d0553c92711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396358d284fdd9be8833327f335452ace2001f9bd4683881a98dd75dcbf98ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d482d6271b2e1a11c697d2bcddf407e1eab30ebf94b74347c7f33efcfd490`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 3.5 MB (3499324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b31ae772192af3a3af9498e3d6f42fa63228d659fa1205c808c3fab332a1b3`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9e40c7c46ab157f400a465c0f06612a29356b32724dd74e171d26a858ecfc9`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 10.0 MB (10015413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2152c684c1297898de2f2a61552177b6ef409d0faa920b500f3753a365bfdd8`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:18a295758c20c7eab91015091d490489590963f0c12d4403016a0a38cbfbc365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb23c09b068b4e659b9ef385b8cd9300eaef6137c13a3ea71cd85fa337e1199`

```dockerfile
```

-	Layers:
	-	`sha256:499949fd2fb150b066aa5c8a188e47e97e5b11be1ee736572250ad72fb0abab5`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 2.4 MB (2369045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccf67b5b2c10f79e22e3eaa781de3fe5e5d37d2714f277ad823f1edb665dc27`  
		Last Modified: Wed, 29 Jan 2025 23:26:59 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:2edd61c72132f4076b78806bc5b26817d701ab7a2d2c073b59b350befc84c119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38814725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ef249b3f729e4e8718aa396ec0c66646a59b895ca6b5e6f5347725ae3eb012`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
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
		Last Modified: Tue, 14 Jan 2025 02:19:09 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c07df56cc142f741158f6a6e60c3f325bf6fa5d10910c58b1b9215c6245066`  
		Last Modified: Wed, 29 Jan 2025 23:27:20 GMT  
		Size: 10.0 MB (10002981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2a8436df302acf449bc2e9cf182270ce48521532ae80606526f5b5e45ce469`  
		Last Modified: Wed, 29 Jan 2025 23:27:19 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:5b872e1d70ce8defe6fffe9b3a6480a68798a3ae761301eeb142a30a0e7c791f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a826a6f57441f92dc80560203761193547ccbc20d7a8e68d560a11426057b86`

```dockerfile
```

-	Layers:
	-	`sha256:ca2a70efa231f3cc8e025e53589af1a0d172dd0c768eb771471c9dea3642c203`  
		Last Modified: Wed, 29 Jan 2025 23:27:19 GMT  
		Size: 2.4 MB (2372559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40f7e284ddd7bd4cac4d77dccdb1531c02e33d7abbcf5b953fec92441a3c329`  
		Last Modified: Wed, 29 Jan 2025 23:27:19 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

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
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:22:42 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

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

### `haproxy:latest` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:29:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

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
		Last Modified: Tue, 14 Jan 2025 02:29:00 GMT  
		Size: 2.4 MB (2369328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca5ad022a0ff53696f8cff789934d6ff2f77f5a29446d7f59591e9960e0513a`  
		Last Modified: Tue, 14 Jan 2025 02:28:59 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:71feaf8bf1f3c481b132e5d4ed2e6910263214b0f76a73c59613f5ec956418ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42431519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120ed53518c349653b9af65f57a568209e16d47421f0c90624326d60aa3d1d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9791bd06b1782743883d0c46a0076c77d63806bcbfe102db947ef0e23c1cd961`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 3.5 MB (3503414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a07075bcaf2ce6dfdc40470a84a1b2c410b9f031aaf92ab133ee57a18872c8`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0feaa1dacb515dba5dab37fa0ffe1a69ab3b19c68009bb26c93cc3daf7c9a9`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 9.7 MB (9738867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb959d855b609d546ac34461c62996001aa0c47d45cd0d867d843fa0b178128`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:fd71729916c2032a7be25f0c677d5bd87e82c469bf68ae2cc4d1c1570a01a574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6ee7c7ac2dfc23076cf215350fb9e5db4cd0ef54e3c9204286efff81d1e61`

```dockerfile
```

-	Layers:
	-	`sha256:4b64818d0a025f8abe8936b17a90fc96a2fc65409b8aa444f356a1ad863977e0`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 2.4 MB (2366173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b4ebfcf3986ade54112ff6a5e9466a13b6929b86ae26aecb4fde3a28184f48`  
		Last Modified: Wed, 29 Jan 2025 23:27:14 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:c0f8368160538ca70b086b6f509f0f90e1749705a110cef783145964f72b4ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41496571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882c8becc622f04fe22e412690ff81e92e7a69a587e2f3530cee895818fce623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
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
	-	`sha256:9cf2a7d829dd4829c4a5a3627aab27557299f35fed6d8af8ffe5ac9708bfdafa`  
		Last Modified: Wed, 29 Jan 2025 23:31:38 GMT  
		Size: 10.1 MB (10112912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ac41e4496c28cc52c8e84c1395bdb59ce195cd4070311965759e62ad84856`  
		Last Modified: Wed, 29 Jan 2025 23:31:37 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d9adb888453e061b84870687545b7d7d916cf8a4c3d4da93603a645b4a12dc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa8ed2214cc78d032af59c0cebc4da18f17dc69abfb8d9d730cb32039ba3e8b`

```dockerfile
```

-	Layers:
	-	`sha256:171a7c7bc5d45972ccdc86ab059483d6bb159b65607e9332766b34521c2df7c2`  
		Last Modified: Wed, 29 Jan 2025 23:31:37 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:d2966f60892f43856b16fd2bb58a0afde6c717286db90ec6d962d650f0029ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46249505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88c8f591170fdec63e7a20cf889c4fb1f42d5cff785c0b47987ff27b5896c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_VERSION=3.1.3
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.3.tar.gz
# Wed, 29 Jan 2025 18:24:27 GMT
ENV HAPROXY_SHA256=6dd21f9a41f0ec7289650e299180b64f9dd225e35113fd1bddc6a3a2e79d5172
# Wed, 29 Jan 2025 18:24:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:24:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:24:27 GMT
USER haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:24:27 GMT
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
	-	`sha256:3ab19ef049110189d6410acbf925b3c6ac46ff4264affba93cf10253cdd61c77`  
		Last Modified: Fri, 24 Jan 2025 19:29:07 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d685b5dc221d900d3586d18fc9d5136bf57e252116c2639d6de2d323a90e00`  
		Last Modified: Wed, 29 Jan 2025 23:27:42 GMT  
		Size: 10.5 MB (10500109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9b0b616172272958b3247bcc677bd080e6a2a13b17d70a471d87792a6dde96`  
		Last Modified: Wed, 29 Jan 2025 23:27:42 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a91cf578b267ff9e244782472ac1b0e5f5e47d33ba1920515bda8f951eb60bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213299a1b04e2380830fdbf672ee5deaa8d5c878f7a4def034a05948eb3e4a7a`

```dockerfile
```

-	Layers:
	-	`sha256:3643c92c9734978c5f8d8281527155a9056473f2576a6a695618bae216d520ef`  
		Last Modified: Wed, 29 Jan 2025 23:27:42 GMT  
		Size: 2.4 MB (2373359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4e683f9af0329dcb180d2149282edb7da6007bc5d8b4a0764b2258d3631097`  
		Last Modified: Wed, 29 Jan 2025 23:27:41 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

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
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 9.9 MB (9883176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da80651fd9c77e74897f305d3b69ff2fb50dc85652ce9740ca0732253b79dfc`  
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

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
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 2.4 MB (2368767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7453c11aac39c89024fab5b5c9fb36f51812e8980ade1243524fb342f3a34c0`  
		Last Modified: Tue, 14 Jan 2025 02:35:08 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
