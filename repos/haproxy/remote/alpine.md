## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:f0419fc06ad76571a4ede85095e298d121cedd3a48add045d0b4a3c56df7366c
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

### `haproxy:alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:b8e6f49594621ec11f25979c789c50e91c14fe8e9ebab480d913c7ab859e9713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19122604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab704795476155555ed13991bd5fca97ca4597b3ecd9faef1c88944b634753b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:36:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:36:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:32 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:37:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:37:32 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:37:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:32 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:32 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:32 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad25742bf5f71a1aa9b2644fdc9d8199d4394c5f1ecdb49ae0828a95ba205a0d`  
		Last Modified: Thu, 19 Feb 2026 19:37:39 GMT  
		Size: 829.7 KB (829651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373ca49be21b7c6b01337685e3382601688fb7bc5c8ecc681a116fc03316c93c`  
		Last Modified: Thu, 19 Feb 2026 19:37:39 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c38d3bea860e471eba2f5b63c4f1197f00d1e0e5c78a634abb747410bf3f85`  
		Last Modified: Thu, 19 Feb 2026 19:37:40 GMT  
		Size: 14.4 MB (14429694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aa20367fcf1a5313f36353c661b31069362f234f9ab2386f415491a25e400d`  
		Last Modified: Thu, 19 Feb 2026 19:37:39 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:89737a4b25e846c1b5b2867d931a7f9fcd9530ed0d2f466f17530ec1b0f672bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a08ecad123ef3da06e98260dcdce08a2212e5a29f4f41cfca8253450b3e496`

```dockerfile
```

-	Layers:
	-	`sha256:da10e50d048eaa36a198e20fc3ab237061c2f0d2b5d046776e56ee98d9e457cd`  
		Last Modified: Thu, 19 Feb 2026 19:37:39 GMT  
		Size: 227.3 KB (227306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dad332b9a7d928ab3903002e3ef9c58f961501e8420a2f2be63a6aca8786aad`  
		Last Modified: Thu, 19 Feb 2026 19:37:39 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:aadcd65e169c7dc8ed318bf44ab4d8aab2b257c9bb72810f0dad7d028b5f3a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19052410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e77fec5b3d360dbc50631644844f8afccf7e532a8973a1a362361a194d7e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:36:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:36:48 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:35 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:37:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:37:35 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:37:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:35 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:35 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:35 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e24b776a3b4860c70cebb76585a380b9ccb6abbf5d3c0441ed2ac789cb2917`  
		Last Modified: Thu, 19 Feb 2026 19:37:41 GMT  
		Size: 821.9 KB (821857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac2e008c1665c70341eb399e2a3355b8e02a4c2f083c055b1b5bc1b0f9df6dd`  
		Last Modified: Thu, 19 Feb 2026 19:37:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64de8afa2d16d9ff0102822177bc4ca8ad425d398cd92dadf54a5d25934480d3`  
		Last Modified: Thu, 19 Feb 2026 19:37:41 GMT  
		Size: 14.7 MB (14659296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc07403c6fbffcc6fe457db5f36a98c804a13dad9f67f04f1a1284bec046913`  
		Last Modified: Thu, 19 Feb 2026 19:37:40 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2137b8136ba1cac56a716064262c80f7e9e30f67abd8f0f6364b8ba855b20b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b518c4c0df20f0a19cc56d970a0ac0e034da4ac6f6c4fc15ca9d3fba5e02b7b5`

```dockerfile
```

-	Layers:
	-	`sha256:542a9a95c894f9a7ae40ce34513308cec0fd360d634a43a8f0ef94c67b48f682`  
		Last Modified: Thu, 19 Feb 2026 19:37:40 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:3afe3419fbc244bbf1bcef056d6ef4834978f799588ea2b59601b36821d729f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18563258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e171f7587c8e23b4c69a782ba9bff3faa915bd542eb7ff8ba54d6e42fe6d9323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:37:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:37:55 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:38:39 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:38:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:38:39 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:38:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:38:39 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:38:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:39 GMT
USER haproxy
# Thu, 19 Feb 2026 19:38:39 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:38:39 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6758240fb16effbca6593d4422fc21b1a3172f57b3838f6a97fe3e8394d597ca`  
		Last Modified: Thu, 19 Feb 2026 19:38:47 GMT  
		Size: 777.7 KB (777730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e191294e6dbe5138c4f4713856768d962a7983be7ea60dfc6f44b213f7abcd1`  
		Last Modified: Thu, 19 Feb 2026 19:38:46 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a6f180429591e4831c6a280924c77ddb23fa98d6f68d6b58e667c06a9c7b4`  
		Last Modified: Thu, 19 Feb 2026 19:38:47 GMT  
		Size: 14.5 MB (14502369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545891c7b6643af3ce5c493c4be74abd71503107b7560428501cc6ce6cb7cc`  
		Last Modified: Thu, 19 Feb 2026 19:38:46 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c39439c0381212f3cf6fe71f87aebc482448105a0e5ac13cc1ae0c0f957b52fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd781e4e25ac41c5d801ad0657329729d77dcbf6f6438d5ad897a52e3eb0dcc4`

```dockerfile
```

-	Layers:
	-	`sha256:7af7e7c9fcf0b7f80f16994cc36c22c5d689db772fd8f12aece4b01d80702742`  
		Last Modified: Thu, 19 Feb 2026 19:38:46 GMT  
		Size: 226.7 KB (226708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e058e87e4ea4bc568f8caef17e4c82c613f529303dda349d21f5249a7919ba7`  
		Last Modified: Thu, 19 Feb 2026 19:38:46 GMT  
		Size: 21.3 KB (21290 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:978aeb6e2c91e25b681a7bc0cb698010ecbbfe63c75c9ce9c4a85ade57d7b0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19229938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2196ae1596e294ffbc50f6a6e98e5c46f52e792480df609fad257b19c9b3cceb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:36:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:36:35 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:16 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:37:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:37:16 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:37:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:16 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:16 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:16 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:16 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cb2334758ae0224d366eb6bd91a877cac64e29592eec442c8407014ff9bc67`  
		Last Modified: Thu, 19 Feb 2026 19:37:23 GMT  
		Size: 842.4 KB (842400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b068e5475d2fa8b8ec77d305c01ed61bf748bdaf0812af73af1547355c9e7bb0`  
		Last Modified: Thu, 19 Feb 2026 19:37:23 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1046b0304a5bd056991a36737c51c9507251f85e470d10a902a6e610eb45084c`  
		Last Modified: Thu, 19 Feb 2026 19:37:24 GMT  
		Size: 14.2 MB (14189010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9aa63e7920318d07d2e4fa8765fa37f01fe18fcc11a936d2509bc3d73813f4`  
		Last Modified: Thu, 19 Feb 2026 19:37:23 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:bd4e586b0f7200f60418026c5ef7734a738e17cc0608422a4f43c43fe8812533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2c34f19734a3c1a32f49643533bc7101b45110ee3689c25acf5543a3269d8f`

```dockerfile
```

-	Layers:
	-	`sha256:9f39d006e095a2e18ed78d540d33aa06a6e1881561680982d85502b927515e0b`  
		Last Modified: Thu, 19 Feb 2026 19:37:23 GMT  
		Size: 226.7 KB (226736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d899101dfab728a37a67e0033c12c4cadacd156d7996d6da18eb8d8f30f007`  
		Last Modified: Thu, 19 Feb 2026 19:37:23 GMT  
		Size: 21.3 KB (21327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:2d6046aed70d5352aed0e12658a90bc066ded8804c386c227b927c9702bdcfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18745396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff6886005a46b7f21b4f979f1c4c6d38d18c86b251e9df3e48a39f88330cdac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:37:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:37:09 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:37:56 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:37:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:37:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:37:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:37:56 GMT
USER haproxy
# Thu, 19 Feb 2026 19:37:56 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:37:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325281d9c65191a3a9c57c3b4f5b025522a547b765fd6726e7dd223372c5565f`  
		Last Modified: Thu, 19 Feb 2026 19:38:03 GMT  
		Size: 835.9 KB (835930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22230449834aaa9107f810e6e6e19cf4a6ecaca0a887641a87b8394b8a1694f`  
		Last Modified: Thu, 19 Feb 2026 19:38:03 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436011e97ea63b9453aba6f06348f18f7205b09e340e6bb66cac5e684948741c`  
		Last Modified: Thu, 19 Feb 2026 19:38:04 GMT  
		Size: 14.2 MB (14221033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ffa752ca5789319faff3468734995dd8e44ef6306645d0808b4c8bb733dc4c`  
		Last Modified: Thu, 19 Feb 2026 19:38:03 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fb48b7b7947902ad43730bc14216d1a6e8862bf29e30d0a72878f20814ddf0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec47688ff939575632154a4ad5971951c3baa3ec0356198c32da3158e588609`

```dockerfile
```

-	Layers:
	-	`sha256:fb26f89ec8ba6921c7e5f5993e25968aa5a1f4b0dca9aa5a0b9a332e81d89380`  
		Last Modified: Thu, 19 Feb 2026 19:38:03 GMT  
		Size: 227.3 KB (227271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2b9164f3e15a325b8ec6c292d2fdf6265a68bc639504c6d2b2c0760234782a`  
		Last Modified: Thu, 19 Feb 2026 19:38:03 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:01e778730c8871c8dd1d886bf4f3e7ac03611bcf8ad9c237463038cb8756034d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19906927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2a92a65b4adb183c709f384889e4dd2cf4d6cd13f35fd24c02d9d76a5010a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 01:02:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 05 Feb 2026 01:02:02 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:38:27 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:38:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:38:27 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:38:27 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:38:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:38:28 GMT
USER haproxy
# Thu, 19 Feb 2026 19:38:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:38:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1a3c9b23f916e4c28eda91c4716cbb12c72a87db35b7b5da01ab33b1261358`  
		Last Modified: Thu, 05 Feb 2026 01:03:16 GMT  
		Size: 865.8 KB (865829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918fbf427d1b030757c848f48e4b6122f1cc20612b0cdb6f69615da40bfff160`  
		Last Modified: Thu, 05 Feb 2026 01:03:15 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2982043b00bf5805b2b2eac58fbe8c0867bed7ca9d87db5c89cb2bcfa10e2310`  
		Last Modified: Thu, 19 Feb 2026 19:38:44 GMT  
		Size: 15.2 MB (15210010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42095ef02e7422e842cf0f020bfd892acb00c9e78b86975d256059ee07097dd5`  
		Last Modified: Thu, 19 Feb 2026 19:38:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc867ed758390a2319c6d7bafa67945f7e72755c6ddd138b8c22c611ee787241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b92c8944f236a52a11db2a2991be3ff9073193befa6a68bfa7efd3566e5d663`

```dockerfile
```

-	Layers:
	-	`sha256:74b162b046dadf1de65e588ba64d17329b8f9c7ff6608548e1561adf3e52cee0`  
		Last Modified: Thu, 19 Feb 2026 19:38:43 GMT  
		Size: 226.7 KB (226701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4d8242389999e2e79bcb0b70495aa84ac1fcfb9012c6accc1c1b663d64295d`  
		Last Modified: Thu, 19 Feb 2026 19:38:43 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:179760e9e6824ad6705fe536769fb23d3bc9ee1fab4f4ca07b4adcc02efc2901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20018799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058463fa42e1ffd3284fa54a65abd6ede2544e3ed5142be16de61347ec6f5a8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:30:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 06:30:03 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 20:43:17 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 20:43:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 20:43:17 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 20:43:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 20:43:17 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 20:43:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 20:43:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 20:43:17 GMT
USER haproxy
# Thu, 19 Feb 2026 20:43:17 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 20:43:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c9470919a79f39f2a2a1db9bf476647c20b35b6e97f36111db731eafdd6c58`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 849.9 KB (849900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495b0565d23aaed2a0be6162e94f23c2de4ca298bc65512773f4fba68e98bf5d`  
		Last Modified: Wed, 28 Jan 2026 06:46:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62264c0f58b9d71e32fb29528a769d2365a512f93ea5e67dd855e4c45fb6f029`  
		Last Modified: Thu, 19 Feb 2026 20:44:08 GMT  
		Size: 15.6 MB (15582169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ac72be1a32b54f635f6b83861b52a25d698cac378d2bf058de3d075634326`  
		Last Modified: Thu, 19 Feb 2026 20:44:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f5116bb4c6bc5fabd7e56a397d578893c206c08590d66e97ab72f30358c2fc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4e14a551a944e3dc6adb0335e6cc8d734c02aa07c1a80aba83909e9d3d0af7`

```dockerfile
```

-	Layers:
	-	`sha256:198e3407859a6181f06b0a92be91c46d91f3aeeff28d9c004c0878dc91a75a7a`  
		Last Modified: Thu, 19 Feb 2026 20:44:06 GMT  
		Size: 226.7 KB (226697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b995b9c9e961fc177ae63947d6fe7c80fabed21689bda333cf6b69ba4666f5f5`  
		Last Modified: Thu, 19 Feb 2026 20:44:06 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:6c23860848115e4729a147fd61a793cfdc93dea38ff00b090edb7d1cdb65f688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19445583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da080094e0c882056205385d11b9cc769f48815c2cdf645c2c5d9aed8cce829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 19 Feb 2026 19:35:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 19 Feb 2026 19:35:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Feb 2026 19:36:49 GMT
ENV HAPROXY_VERSION=3.3.4
# Thu, 19 Feb 2026 19:36:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.4.tar.gz
# Thu, 19 Feb 2026 19:36:49 GMT
ENV HAPROXY_SHA256=5063eccd818a0bb131a7529ca9824da952697fbf777de0c8376ad610a66173ac
# Thu, 19 Feb 2026 19:36:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Thu, 19 Feb 2026 19:36:49 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Feb 2026 19:36:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 19:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 19:36:50 GMT
USER haproxy
# Thu, 19 Feb 2026 19:36:50 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Feb 2026 19:36:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6adfa245b40833bb947623236264af9d46b4343c413ce3b2485998bba84c1e`  
		Last Modified: Thu, 19 Feb 2026 19:37:11 GMT  
		Size: 891.5 KB (891550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2bc175dcdd3884f55546e1384fc082d3be8d2c459d0ebb0cd61c501125649`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f2ed72a3c1c25f19b371b67634b0ba0615196552ed5ed907d62774fa06120`  
		Last Modified: Thu, 19 Feb 2026 19:37:11 GMT  
		Size: 14.8 MB (14827252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4f5cf030af07f1dba199ff2061631f13128556f005283eba7cd965d914c175`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:6bb6379e45824e4a3b9dfddb8ac251a37c488ade3cccfb8237b368f375d56d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 KB (247823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1a9c9582e69ebd742c2549cebee6b7707e933dc9c82eae38bfaebf9259176`

```dockerfile
```

-	Layers:
	-	`sha256:0a3039a835f5d025f782e061e7f799e71f0bae88dcbefbe89b3c49ee64e85c97`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 226.7 KB (226655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b996827c653c2694905cc4592f40486c25a52bb9bde43587fa379977961c8800`  
		Last Modified: Thu, 19 Feb 2026 19:37:10 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json
