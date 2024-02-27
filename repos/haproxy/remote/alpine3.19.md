## `haproxy:alpine3.19`

```console
$ docker pull haproxy@sha256:0b8ce5ef29cb27837da279c46d673b6412beff2192ae6e804cc4b63d3498a27c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `haproxy:alpine3.19` - linux; amd64

```console
$ docker pull haproxy@sha256:7263ae88398ab7fc3789e5b739baf0300def1872410eaa33896f009917d1c72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12260904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac13f05382674d38daabf548bf252965a9eca8efbf2e2fd42259c0a0e2fc8ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c791dc20d56c97903ecdd4243d5d841e36fa37ad89982ed7cb41ec37be8585`  
		Last Modified: Mon, 26 Feb 2024 21:52:31 GMT  
		Size: 284.1 KB (284103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe631c89a7ba0e9f8732fd19c1a036a89e7dd40c8f013a6b29e61968cb35bbdc`  
		Last Modified: Mon, 26 Feb 2024 21:52:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b8b4f1975716b7a5bb3f87de533a2c27d5fe085b11bb584176b70258e23912`  
		Last Modified: Mon, 26 Feb 2024 21:52:32 GMT  
		Size: 8.6 MB (8566334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20d16a04cb77fbde387637bd66496697101dd1c063846bd85dcca1f5fb8014d`  
		Last Modified: Mon, 26 Feb 2024 21:52:31 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:25be0e25120bc517fbd2de9a4f7809c62683f11814d7a4eb61295745f0c860cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b5aa29a079f31df6301fb1c91602be2e1898368d6ccd803d5150d169b0d869`

```dockerfile
```

-	Layers:
	-	`sha256:34e465ca7d053f80022e7e30234e3f4067f56c5c6737f2f4a78280f737a486d9`  
		Last Modified: Mon, 26 Feb 2024 21:52:31 GMT  
		Size: 175.9 KB (175915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d209c0b1717ac7f565bd224b57c8dc8bfcf6de389c04abd289dd9e90d3b2b56`  
		Last Modified: Mon, 26 Feb 2024 21:52:31 GMT  
		Size: 20.3 KB (20342 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:f063d6fd6a60ad315002c941a61d8e7777a1dc97bec3ee3d4868b99f691d0fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12037649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3813263c9a27f83722533fd048367eadbad000bde16a11a272f1a9f6707fd0de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973323ae72fac29e4c102c16b5f42568aa24a9892b4a45ecf39c41319df88ab`  
		Last Modified: Mon, 26 Feb 2024 22:19:52 GMT  
		Size: 285.0 KB (284969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c51c2dbca0ec8003f60368696777f039bf208f99ab3aee6c48606cdd7c422c`  
		Last Modified: Mon, 26 Feb 2024 22:19:52 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c5d6ffaea283c8258bda9ac6faf332d0a633e0cd293faa77d2075333911b3`  
		Last Modified: Tue, 27 Feb 2024 01:20:58 GMT  
		Size: 8.6 MB (8585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b86aa05da0a6d9dc19b278277b28d5918b95dc4b02a3000aebe1c25924745d7`  
		Last Modified: Tue, 27 Feb 2024 01:20:57 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:69e39670f4ea6926dcba3cc15e7aab255c0fbc9045fc0672633553d99fc5adeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 KB (20074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b16ab837196423adfd556263a42565fb1501c551f6f4602cd817b25b822b66`

```dockerfile
```

-	Layers:
	-	`sha256:58a8ba2668305b34c6ecb1ca6bf863c73ace61274a83bb826eff78aefe7999dd`  
		Last Modified: Tue, 27 Feb 2024 01:20:57 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:937ed4ed461c65582702040464f7ae2b185b677a807c0e56d58afa827a8147fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11652134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec9585201e2fd144f795030ea49d50093b7aa34b48414d8fd5e1b33f9585ffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34457f305359ab30eac9a9890df125c672c840e6448eec07d80321c3bac0a29`  
		Last Modified: Sat, 03 Feb 2024 09:41:43 GMT  
		Size: 284.1 KB (284127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f278677e1da6524e7094dc917e821adc1a7434e6a442d28872bbf23b4304f`  
		Last Modified: Sat, 03 Feb 2024 09:41:42 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff0e0bac8650fe9cf9bec843257e2a3e532581f32c9a29da07d66b8d29781d`  
		Last Modified: Mon, 26 Feb 2024 23:47:44 GMT  
		Size: 8.4 MB (8447371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89d26f1d2da1af3849acd045f71d7e7b98fa5007a46251a564417a14f41cc1`  
		Last Modified: Mon, 26 Feb 2024 23:47:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:17e3e22e2c1ac1f73fc3acc68ebd9a2a6a0856bb747426f14c9c506a88081890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2581273b64c3612dc58d596cb3808523fb2b4c4ffbb7683a45de88512c67ff`

```dockerfile
```

-	Layers:
	-	`sha256:f62f6bba7c8a893f0e155b0f5ee8d4412090f18ca84e9c3d7d8f41c09ae21fd9`  
		Last Modified: Mon, 26 Feb 2024 23:47:43 GMT  
		Size: 176.0 KB (175967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fada2359271418a92266fffd3deec1f1c1fcad4904851cc6eab6434b72d8388d`  
		Last Modified: Mon, 26 Feb 2024 23:47:43 GMT  
		Size: 20.3 KB (20288 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:0385be62fe6bb9bc6c816722f81ea09416b29d850667f1a05937c3dbb5eeb236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12214702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9499b7b2e701134fc40f7f4a5eb75739c24526295b065769380748b96a55d2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffdba998a7d9cb80d56d3a75f4823cbc595ce14eb785a35376c8d2f7f48855d`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 286.4 KB (286386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d642c0f21728d496d6aa268bd2d344d9e3c63786f31cd6e353da1abea11b47ed`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8752c6589c0f33fd93baf802da79fe875946bf8a10a55edf744f8749963a3ea3`  
		Last Modified: Mon, 26 Feb 2024 22:05:06 GMT  
		Size: 8.6 MB (8578869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b7aad20ce83fc783929cb7ade8553111c569a571849fe3beb71fecdff5682`  
		Last Modified: Mon, 26 Feb 2024 22:05:05 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:98924fecba5393f0b0dde33946182569923a7f8204fc7043ba3655ce93b85ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dac2d0237101b84d5e8dd58cccc860659493e11451119cbc2d1f475fbe9c460`

```dockerfile
```

-	Layers:
	-	`sha256:5ba97079690b4e78bbec9538b446b35d4c634d14259bcad0efec730dc982f9a4`  
		Last Modified: Mon, 26 Feb 2024 22:05:05 GMT  
		Size: 175.9 KB (175930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5a5c598d79d4c1d0dfdd1b5dae63eb80f39af2bedddbf72daa91ae9fcb5a02`  
		Last Modified: Mon, 26 Feb 2024 22:05:05 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; 386

```console
$ docker pull haproxy@sha256:bddf3a78a6ec9d2bf42bcf3ec046af7691d436fdfd3bd5ff534c8d9f00084dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ddd4a4be24144333263f47075fe3904fa6fd8829d02072e9fa2bbe28d7b916`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb2c5f0812b45b8ce9ef0bffa53548b9f312dfc49fb1694ba1051b8ec368c3`  
		Last Modified: Mon, 26 Feb 2024 21:52:23 GMT  
		Size: 284.6 KB (284559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865782caae095f7fe1a2400420ce9f434640365b12f212164023a4e8eb17e8b9`  
		Last Modified: Mon, 26 Feb 2024 21:52:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c6f72a15579306447ed9fe6f8ab858da00b5c36059afb015fd12b58668c6cc`  
		Last Modified: Mon, 26 Feb 2024 21:52:24 GMT  
		Size: 8.4 MB (8366758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2668fb6898a4961d45dd2e86d440f7e45ce8508b4df49b2ac8e915ca02774b`  
		Last Modified: Mon, 26 Feb 2024 21:52:23 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:02a339cc899d310ec78a51fc7859c8069bf83a4677f0f1b1f81942429f799da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27561ccf127fb1d363d12b431806d68e9a933f8bf4784cc88d871d35b433940c`

```dockerfile
```

-	Layers:
	-	`sha256:bbd78fc15e7fd98425a0c91b46c0a1b24bd7dc528cc805f4e83c67aee3bdd202`  
		Last Modified: Mon, 26 Feb 2024 21:52:24 GMT  
		Size: 175.9 KB (175880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795b940112893cd3d36429e30ffb01e219665a2e03a9aebc51056774f85b89ba`  
		Last Modified: Mon, 26 Feb 2024 21:52:24 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6de6b5e7cdea203b5b790800a5bb987c653ab311445edf19f64b5b81a5774a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12714697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bc62fd3591d3f43a8b5f4af67337316df11a6478ee6b5137482e30c49e8181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_VERSION=2.9.5
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.5.tar.gz
# Fri, 16 Feb 2024 00:13:28 GMT
ENV HAPROXY_SHA256=32b785b128838f4218b8d54690c86c48794d03f817cbb627fb48769f79efd59b
# Fri, 16 Feb 2024 00:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
STOPSIGNAL SIGUSR1
# Fri, 16 Feb 2024 00:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Feb 2024 00:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 00:13:28 GMT
USER haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
WORKDIR /var/lib/haproxy
# Fri, 16 Feb 2024 00:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562ebb05af8ae069f087bcc9e91a066e4f2b4cac2721a591b77d7fcc503aa75`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 286.8 KB (286751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d6fcf4017a80ca60bfd78b795af26fae6f2291641f6c9f6f5451f0e6a5dcd`  
		Last Modified: Mon, 12 Feb 2024 22:41:20 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7624d385bd90f1eb5e9c5c280e106cf7e21e53c6c8b230f32f20655271c069`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 9.1 MB (9067863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f781ce9dda4fe76be624d8116502a24ea8fc27f698a8435993e257e0b199af`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:e745443ef728ef6cef82035b0490c21cdf287c541121119f90958d5cb94a5fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e7f4e421be4928efbf5557ee1d5db2fccb00878d089c4620eaa93540a53277`

```dockerfile
```

-	Layers:
	-	`sha256:c721ede3a2f7079e880b60111bab9e9b6b4c1113f756132621cc043ca288ab66`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 174.0 KB (174007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a56535225cb5cdf6ece0ba8a73eb9c8a6b3a45aff9e5e799ac76d8070d2a13`  
		Last Modified: Fri, 16 Feb 2024 20:12:36 GMT  
		Size: 20.2 KB (20231 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.19` - linux; s390x

```console
$ docker pull haproxy@sha256:e4c0e46b5f5d78e73c8ce7dcba3606dfc8ac7079bf4dbc1f16dfcffc199e21b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12331203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797ec3ec2144bbe96da92775a076204acf5bb06c7ea8dd482802d04afd73b35e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_VERSION=2.9.6
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.6.tar.gz
# Mon, 26 Feb 2024 18:13:28 GMT
ENV HAPROXY_SHA256=208adf47c8fa83c54978034ba5c0110b7463c47078f119bd052342171a3b9a0b
# Mon, 26 Feb 2024 18:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
STOPSIGNAL SIGUSR1
# Mon, 26 Feb 2024 18:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 26 Feb 2024 18:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 18:13:28 GMT
USER haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
WORKDIR /var/lib/haproxy
# Mon, 26 Feb 2024 18:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62165fa6c8db49ded3bb26d6fb91f158b9c77eaf2bf8de692b2da00a4f72dd48`  
		Last Modified: Tue, 13 Feb 2024 20:16:10 GMT  
		Size: 285.1 KB (285098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcf97c2ae52a60b1d36228750242f3ca9e590b00fec1eeb6212ecc1f2deba11`  
		Last Modified: Tue, 13 Feb 2024 20:16:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfe80fbbb691d50f37c0a82e2193d5061742ff9e68e105abc586b1c16037862`  
		Last Modified: Mon, 26 Feb 2024 23:04:13 GMT  
		Size: 8.8 MB (8801734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cebf25fd61e8d5960056cf4fcbec38d2ba8dc817af497c8b18f7985cd6885a`  
		Last Modified: Mon, 26 Feb 2024 23:04:14 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.19` - unknown; unknown

```console
$ docker pull haproxy@sha256:1f2a137450226c42e6150ecae03e8ae8001cb49164fb29af59b839b0570409bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 KB (194138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0fd548b4a9d2b002cefc513a4606c93e390adc6e4bbcdad48939989e8dfe8b`

```dockerfile
```

-	Layers:
	-	`sha256:380e3075384073d14437dc5e641bf2b56b11122f0f6a0b0fbc8686c5f5d8fb69`  
		Last Modified: Mon, 26 Feb 2024 23:04:13 GMT  
		Size: 174.0 KB (173961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b1af98645e029fd7555880f5e1ca78a98c6a451592669cd3afb7eb53f89b81`  
		Last Modified: Mon, 26 Feb 2024 23:04:13 GMT  
		Size: 20.2 KB (20177 bytes)  
		MIME: application/vnd.in-toto+json
