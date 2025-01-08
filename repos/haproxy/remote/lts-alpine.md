## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:71fb8d2242624e4d5b29c54effb3602524aa754092047fd5a497b68499aae3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:f51a1a67f29c29c2198ebbc37bf7b7d53314e09fc134654af25b75155a18a9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13312641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddecf93e19c7dfaebb324fc38ca11638744a68d72a149b26eed14a3d2b585c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca122c3d6394cf84926e6c13b18a475611ea6f70455d4c889468cf537298c5d`  
		Last Modified: Tue, 07 Jan 2025 03:18:34 GMT  
		Size: 279.5 KB (279508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb2c734ddc4b90ed8a2a6bc01285229e09e06419e2a6aadcfbcf049e5a3636b`  
		Last Modified: Tue, 07 Jan 2025 03:18:34 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec90764271f44c52d226ac694d5ccc7df482bfd0f172b006502fd3af90791ba1`  
		Last Modified: Tue, 07 Jan 2025 03:18:35 GMT  
		Size: 9.4 MB (9395461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bf630c7465f04b012eb1b1c6c1def5057ef12b4aebe1250efb642a29b3e7c`  
		Last Modified: Tue, 07 Jan 2025 03:18:34 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ca5fbaf554404495f21188791aee0856f686b6831427c563f50130853207dd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f403378dd9a5d68d59da8ef04fd098775b633e831bccd36a4c1b02e5b07db5`

```dockerfile
```

-	Layers:
	-	`sha256:12b3ec6a187852ce350d9ab7a521d8475d43a4da837413bd0ee7c32af671a81a`  
		Last Modified: Tue, 07 Jan 2025 03:18:34 GMT  
		Size: 180.5 KB (180471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d73bdde1fffa61be33f8268164cb40b5f234885d1865bf9aa58bb020875c96c`  
		Last Modified: Tue, 07 Jan 2025 03:18:34 GMT  
		Size: 20.5 KB (20463 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:d71f509196f454440fdb091d9ce2531614cc578c4847a4eae40f486f1e945732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13023953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da2ea2b974c5da9feab66fd3ab3b4bbfe64c87e00fb70c7cd57af1a30fa7e40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4b356d63c335a17af655b5f257ab3701f0f5ebbdcef0861a45972d7056edc0`  
		Last Modified: Tue, 07 Jan 2025 03:50:08 GMT  
		Size: 280.3 KB (280336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae0af52d67ea93b31b88ebc3c88aa4c7929f19d7841c1ac065781117fac5aa`  
		Last Modified: Tue, 07 Jan 2025 03:50:08 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b961c186b2bef0a18f227d170418b5a87408f8189a761492343c200e68bc0e`  
		Last Modified: Tue, 07 Jan 2025 03:52:17 GMT  
		Size: 9.4 MB (9381129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf29a1ffce770bb1a7db5952d5a6126d22a67bf493830f1288512de9e2aeedc8`  
		Last Modified: Tue, 07 Jan 2025 03:52:16 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:1a1df51f9dd824dfedad35cf32dbf5d4835a8d12d0060f18e06ee3215c9e7a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16041018e3d667d23b33809dfd572950ff491a3bac0519c90001609145215e2b`

```dockerfile
```

-	Layers:
	-	`sha256:f277c74bc4e1ba27f734d0afd3a24139e749203121efd1fa82d01d3599fe5500`  
		Last Modified: Tue, 07 Jan 2025 03:52:16 GMT  
		Size: 20.4 KB (20366 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:9bb299b15bf8fbf66da3a110782edee404b8be27aaa5276401762e3378b1ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12613750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2221a823b6e852fddcc78babe05a30b1ddb2e85083053d23500ff691f02477f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb00f4e7c0f2d2675873f0c23be52045a4726379be021e88997234f8e8d113e`  
		Last Modified: Tue, 07 Jan 2025 03:35:59 GMT  
		Size: 279.5 KB (279507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb245d8362e89c100e34a156e8b9ed835b8199f32d828ee053e3d1f492e9954`  
		Last Modified: Tue, 07 Jan 2025 03:35:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc8c1cb452293d2cb9d92f90fbb6f922596a4f7ef7e9bfebd58cf2dc747af55`  
		Size: 9.2 MB (9239556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c68a85c12827314a75d555dbcb28e6019380c310aa5133188642f38efebc2f4`  
		Last Modified: Tue, 07 Jan 2025 03:37:41 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:cbd5aeedf9d8710dee5f1677b3d2f6e9cd56fcf497eed86af0f0157c92854e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6ea93bd378e1845f239250aea96111ccc75090a0f68f13542ea283b69a8065`

```dockerfile
```

-	Layers:
	-	`sha256:a0fac0acf8d1da1f98ea9dd2e4705f3b02114b0e855b975590f6e24b2cbd61b8`  
		Last Modified: Tue, 07 Jan 2025 03:37:41 GMT  
		Size: 180.5 KB (180523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d547d405c5cca92ebd44d2ce53152ae99fa722fff7db47e5b50a72b08283c2a`  
		Size: 20.6 KB (20580 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:671ddc5198108800b8a94831ac36b64e974f1fc93a2cdabb7581c7bc99980951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13618839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe0bfbca8d533c1827cb7a475907977ff50b3b54cae811c2362cb473cef9897`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1da83d816d4824f9133356b2f8faa828d3dc299f06f8bf153b0934b5dc06a2d`  
		Size: 281.7 KB (281704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cad2940be1ad412f0a3c68ce77d397954b01129f1f91b747356f8df82d79d2b`  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678cf6a16c8c2d39ee1d7ae2182722ce636299a99f4ec8a4bf12eec70d74e0a5`  
		Last Modified: Tue, 07 Jan 2025 04:12:40 GMT  
		Size: 9.4 MB (9352684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022c9aa72c8194cc9e972c2e89ac346dfc25cb411bc88c38367fd920a1a1fc85`  
		Last Modified: Tue, 07 Jan 2025 04:12:39 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3652744bf761d7edcf926daf9b1c1ef31775b340c969e65d778fd0c9fbff6788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 KB (201171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3d50969d5bb0f39f624e7a037a45ccb9c850633f07abc5526ad69df75be7ff`

```dockerfile
```

-	Layers:
	-	`sha256:d8269209f31016c767ad552b44032241f300a467d5d52381455f887be238e819`  
		Last Modified: Tue, 07 Jan 2025 04:12:39 GMT  
		Size: 180.6 KB (180551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043095292e6a587e2edcec145744dcdf076241e68c3ffb882f031b2b87c3f5a4`  
		Last Modified: Tue, 07 Jan 2025 04:12:39 GMT  
		Size: 20.6 KB (20620 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:59886ee52c2279ff801cbfbac783677ceef83892fa76cbb4438e47a45239b2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12902817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761f6a82e5ac8e2f9deeb0068f1950b55f32e03ffb88655e9a4b292e09a5393d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c22f978a77e13a6a686075aa2c16fb1ca90c38034e6b2a8d36540570912762`  
		Last Modified: Tue, 07 Jan 2025 03:15:01 GMT  
		Size: 279.9 KB (279933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9ddec47a301197d02f7c07cf36bcdd42f5dbc05eb8afe396d449b1b0af8f70`  
		Last Modified: Tue, 07 Jan 2025 03:15:01 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2303be1563e3c7bb2de3e513d228e63d4ef193a985ffefc23b5043a79b31bf16`  
		Last Modified: Tue, 07 Jan 2025 03:15:14 GMT  
		Size: 9.2 MB (9163167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc7b18784c77a88728a309201b4fe10c2c50ccaf00ccbfb41bb5c2dbc257afe`  
		Last Modified: Tue, 07 Jan 2025 03:15:13 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:870c9a2080c948632e780c3451d0741a63f14b2c279765c7ebde904d3a3cd0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bc0ba378f0fc2fb0b6d94246421af8b01725787846f1213429301f83a549ea`

```dockerfile
```

-	Layers:
	-	`sha256:deec05680f79d9616eadfa32846f1851760d9a91cca5d051bd63a5c1c2a31fa5`  
		Last Modified: Tue, 07 Jan 2025 03:15:14 GMT  
		Size: 180.4 KB (180436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2faa569ed9da5832174926d187b8f672b8c1f7c12185895756a4b1bd6587cf4`  
		Last Modified: Tue, 07 Jan 2025 03:15:13 GMT  
		Size: 20.4 KB (20417 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c381b3e19914788f2d8e61b9e971158534d062bcd286d601f15942edb258fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13753414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c26303ce93fabd41bc6db76370e59f5699e4793021197010c0660718682d6f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2763e59391230b20b539499288567b1d96ad58731916bfca6bbb499d5e4ab56`  
		Last Modified: Tue, 07 Jan 2025 03:39:14 GMT  
		Size: 282.1 KB (282115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de7d93a7784969b90b7c7f2812a309fc376363099c98c03c22ae034b1787ce`  
		Last Modified: Tue, 07 Jan 2025 03:39:14 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e3755ae986d91808ff1dcac772bd23dea850e3c10ac59a1eded534c005cc46`  
		Last Modified: Tue, 07 Jan 2025 03:40:54 GMT  
		Size: 9.9 MB (9902105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6316ff5600e16cfb5b47482265e5b80370d16231d6947c97cc19f9747fb7b2`  
		Last Modified: Tue, 07 Jan 2025 03:40:53 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:5fd546f541a60a3928980a04f1677aab19fe011b9444eaad74d90ebba0762793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a53a1dd7826af5121345c4b3f9d68d2f8909f658ce6397bab3edfd8e0c6e430`

```dockerfile
```

-	Layers:
	-	`sha256:585e21a03d134e51979696efa56e0563184cb38e32b1d869796b2b02bf91ad39`  
		Last Modified: Tue, 07 Jan 2025 03:40:53 GMT  
		Size: 178.6 KB (178566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e450c2584c13f0f30a114d4779bd76d3959a0d6b2a2cd07f2ed63f5b2ed9acd`  
		Last Modified: Tue, 07 Jan 2025 03:40:52 GMT  
		Size: 20.5 KB (20523 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:6b2721531757b07e2fe546095d53f872c29f85b664c9ceb2a1ec1d1aaf7b52ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12690196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950b4522a2cba977a3415ef4fc0ae508935b52ea1141c98a1bcbb11aa4270c36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf06d862f52fa490092d7fbbb0c7b49c7dc1ec1e36a27e74419c8f1262970a6`  
		Last Modified: Tue, 07 Jan 2025 05:14:29 GMT  
		Size: 279.8 KB (279842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b157c11bea1859e327f1547c12c5fc5c112d74ebc46ae5f06f771f0e8c0410b8`  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c96c8ec81d5739413899cec69ea6e229d9f07af04bb8ad75a7a34388375bd81`  
		Last Modified: Tue, 07 Jan 2025 05:37:53 GMT  
		Size: 9.1 MB (9063759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb3af3e2137c77ff61d043a481491047e0202e3ad8fb90870a9d22966ba102`  
		Last Modified: Tue, 07 Jan 2025 05:37:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f36911b00fad7713dcdc610f60953f113e0f1ccc3fce13ba48ed56baeaa42f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00deac900e4c7af56b54178ba1242de3e55671b5983daa44785356578f509bae`

```dockerfile
```

-	Layers:
	-	`sha256:533ab12232acef44ddf84f4592e39601800de8a759baec2a116c6b0f649d0a4b`  
		Last Modified: Tue, 07 Jan 2025 05:37:52 GMT  
		Size: 178.6 KB (178562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2701ce8aa17d536c52e0f5f175e8574ff9dbddadd7363b8f9d4b147f634b75ed`  
		Last Modified: Tue, 07 Jan 2025 05:37:51 GMT  
		Size: 20.5 KB (20523 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:bb5db7c902064ac417b3aea317566894302eed0d7f91708ab1e47bde331b7f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13322539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eaa5b86e50c4d649870a6968dbc26916852cd903df7c63af8b9067a70f4d10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 13 Dec 2024 00:50:46 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.0.7
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 13 Dec 2024 00:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
USER haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 13 Dec 2024 00:50:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af9605c9e060e17ae6407ba04b05e8b6a2623628a32885b238f7d85114c0f1`  
		Last Modified: Tue, 07 Jan 2025 03:33:12 GMT  
		Size: 280.5 KB (280499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242eaeb61e00e494db261861dbce275783f6e59b478b7a81de903294cfd13f05`  
		Last Modified: Tue, 07 Jan 2025 03:33:12 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e203a0bf1382c01bf2ba884bef42bb62911489e68e73a6ea14a5a5533e54b9b`  
		Last Modified: Tue, 07 Jan 2025 22:36:21 GMT  
		Size: 9.6 MB (9581143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dfc1ee19070cb98d3c7a0e7fe5bf95a317ac0712eeebb03741fe8ea12ac288`  
		Last Modified: Tue, 07 Jan 2025 03:35:44 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:533ed61c9de06bae2a72c347075732bd1871877d77483f8e69a92c4d844a31a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (198983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad7eb36a4e515ffc863caac71572159007d1b6885919d07a947bd4a022517d2`

```dockerfile
```

-	Layers:
	-	`sha256:521264e351b3fd313ea1da862caa6852fa2484802ec177c623bfdff8edfe7ba1`  
		Last Modified: Tue, 07 Jan 2025 03:35:44 GMT  
		Size: 178.5 KB (178520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6592df05e7011bf20c4d024350d7bdc1ec4ed948799bcf45da17a0f484097d`  
		Last Modified: Tue, 07 Jan 2025 03:35:44 GMT  
		Size: 20.5 KB (20463 bytes)  
		MIME: application/vnd.in-toto+json
