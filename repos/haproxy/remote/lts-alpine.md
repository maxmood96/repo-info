## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:fa8c605b74e7db984ef9297d6412c1705fd9961c46c955e5d607a7c53aea3584
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
$ docker pull haproxy@sha256:9b9deec31bf902b369acb9c459326d2d97f0bfe033cb315079d43a049344f01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17884208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a715e9508bf2535e0d3baa64c2a163e72a7aee5fb2e65ec7be77f8870a2a3672`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 02:15:57 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 Jan 2026 02:16:38 GMT
ENV HAPROXY_VERSION=3.2.10
# Wed, 28 Jan 2026 02:16:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Wed, 28 Jan 2026 02:16:38 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Wed, 28 Jan 2026 02:16:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 Jan 2026 02:16:38 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 Jan 2026 02:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:16:38 GMT
USER haproxy
# Wed, 28 Jan 2026 02:16:38 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 Jan 2026 02:16:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f2510cae69e93fd06ef5143cdbe1d7c3c0d5974e977b785d099116cafae0e`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 829.6 KB (829597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f26c19352541d4490819d3125855f279e3216156f0b9ed15cd7cbf1b7b536`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7733d2f53e7a424f29952cc4e2f5d896c6d72cda71a2dd36da4eb9d617b65d8`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 13.2 MB (13191354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71687df17dc440364a482a04be58787763c0c6e6c35f4b621b1ea1e44194db5`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b309fd4b25157c7e7bbbc7e14b10415533089b4442e66aad5797cdee971f298a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 KB (248523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b691d8e11b07cac84115708ce17b8bc2b37b9bf56387ba134c972d7199be22`

```dockerfile
```

-	Layers:
	-	`sha256:2a4c2f44b2b6e6c901a471f3a8c02245b09f88353b89e988693d29e3d19a3f76`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 227.3 KB (227328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d902af3ab59afbfed90b64de79fd5415983275a015ee3fcbcd6fbfa97b03b65`  
		Last Modified: Wed, 28 Jan 2026 02:16:44 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:f43ce21968b4f8c6be1449f6b7e11bd4171e5ba523c03b6a39f80de7d600577e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17749451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df9e86073d145923f5caed6b21e324d459976ec3e1463cf68706c9517875429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:02:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:02:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:03:10 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:03:10 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:03:10 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:03:10 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:03:11 GMT
USER haproxy
# Fri, 09 Jan 2026 18:03:11 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:03:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4930c0f44abd4a01a2ea805025848b2eaf3d9ef929308c0f94f7a286aa3e0a43`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 821.8 KB (821846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1ca1d93abfeee2105cca0af9496feb8eb818a7659434d8d501ef9e1b006107`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce73c89cc328fffaf77b9c43b415a149443f3a874e69e4a406b4e5f03c7b98cf`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 13.4 MB (13357736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8baa79e6a210e797e8baf2e407d1159f190df48d0d96399622a4b79c7817da`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ef7b043db1f4ead56736ee48b1c12bbf623cd7745e1360ca886c7421c806f6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b879f38b4b7d9a05b2410e41bc12ba2d90b97e24f778ffd4f7cfa07b0b2ccd`

```dockerfile
```

-	Layers:
	-	`sha256:94d2879f6b27dacce67d5456249b76777f71108a1e0fc945502241d170790098`  
		Last Modified: Fri, 09 Jan 2026 18:03:16 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:48f9da800da992ba97599c1f98ce71edc0013d9340d313780a02696741164b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17236316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c443e0253f5e5e3fd4b0fdbfbbab44e12fb0235e33a3dfc3de46417c5a2424bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:20:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 02:20:10 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 Jan 2026 02:21:00 GMT
ENV HAPROXY_VERSION=3.2.10
# Wed, 28 Jan 2026 02:21:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Wed, 28 Jan 2026 02:21:00 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Wed, 28 Jan 2026 02:21:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 Jan 2026 02:21:00 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 Jan 2026 02:21:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:21:00 GMT
USER haproxy
# Wed, 28 Jan 2026 02:21:00 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 Jan 2026 02:21:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d705655090423cb4c33cc56d61efc4857d77a0e008af4dd519b550d6e3fac059`  
		Last Modified: Wed, 28 Jan 2026 02:21:06 GMT  
		Size: 777.7 KB (777733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ff3b60ed7440d05524511f5253863fc94abe3f1f11d31073c3bc4c160c49e7`  
		Last Modified: Wed, 28 Jan 2026 02:21:06 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bfb3bbe3192e6b769dda0ffe9d6ff11ae791e31f070212845ca281bb822f1a`  
		Last Modified: Wed, 28 Jan 2026 02:21:07 GMT  
		Size: 13.2 MB (13175424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fea62cdcac7fee4a96aa39442f2ff825dec0972a785f07d0629ec2d885eaba`  
		Last Modified: Wed, 28 Jan 2026 02:21:06 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0da736ce47c85b221c7569dd2d99c4ec8d2a5bca56ba65484f148ea0cb43ee12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (248047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186a8293cf4eb15a99d4fd1dbd05e5edea5eea11b2970aa68c6257046961c582`

```dockerfile
```

-	Layers:
	-	`sha256:64d6132ae128ee19d0901e90fa8c4c1030faf4c94b0aac1a4625a8f4b9087c8f`  
		Last Modified: Wed, 28 Jan 2026 02:21:06 GMT  
		Size: 226.7 KB (226730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe5d241b62c66785f2957373c5e6b7286d8b7f606316580d4d3fbd352211b27`  
		Last Modified: Wed, 28 Jan 2026 02:21:06 GMT  
		Size: 21.3 KB (21317 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:466271e6ce9a8500f5b808d1e8a43e29caba3cb212309e659c2089aa95591b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18040418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d95007491e61cacdd26218210f26dcf7051eb1ada511f2fe5770773bea41772`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 18:04:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 09 Jan 2026 18:04:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:07 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:05:07 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:05:07 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:05:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:07 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:07 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:07 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:07 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d0245d27a0cc0b2f9beee1bf984f8fd7a27b29167c873ba18e5f90ad842ac`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 842.3 KB (842337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b3972e39449e5ff3bac83f7a41cd3edabdfff10451d960c5c39ec99187a48`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9e118accb034735586b501142255adea36c10a5bf36af9ee971bfcbf28ffe`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 13.0 MB (13000903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aad01a15706de15e9ff42fc297144c9b2d2f01c18a0fe9f0b04f53adcff5ef`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b6fcd173af45d76163f506821e6bc9d250f67830629a7de9827e9aa2ec408328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 KB (248111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c7b7781c9d5d1fd08e073e4b029f739f6207fd3de8e627801550487185f5a3`

```dockerfile
```

-	Layers:
	-	`sha256:87703172cd4728be3ffe88fba6737163e71e3430aa6fe40b6460f215459085b7`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 226.8 KB (226758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7fbb8ca9fb9d3031e8feddf272f5029eb1788fb1a205f9dd279146f47d8d81`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 21.4 KB (21353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:8ac1c7cdf94e595525bf846d97db64b4b39016f8ed65b56356866ba8d3b0294f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17421891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222c897fd7813b521250d8b26feb0f7d2830335173d216dc2609b033524771e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 Jan 2026 02:16:22 GMT
ENV HAPROXY_VERSION=3.2.10
# Wed, 28 Jan 2026 02:16:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Wed, 28 Jan 2026 02:16:22 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Wed, 28 Jan 2026 02:16:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 Jan 2026 02:16:22 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 Jan 2026 02:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:16:22 GMT
USER haproxy
# Wed, 28 Jan 2026 02:16:22 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 Jan 2026 02:16:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1474425876b98f7a4c528976a12d0444d1c5debe755854702c199ea0c0ffd1f9`  
		Last Modified: Wed, 28 Jan 2026 02:16:18 GMT  
		Size: 835.9 KB (835918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8881c73bf2c94795753e8585c164a697bd495df6bcfe46a907af5ccc14f7f22f`  
		Last Modified: Wed, 28 Jan 2026 02:16:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961ff60dfcceb42ed1a8af5026100c27746e174467f73615adc2744045caa23`  
		Last Modified: Wed, 28 Jan 2026 02:16:29 GMT  
		Size: 12.9 MB (12897535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e74784874ac1ac3e9d8cd3cbae3dbb092dc68987cbedced5318c651b2287a`  
		Last Modified: Wed, 28 Jan 2026 02:16:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:152bc84a4caa2d08900c35578c5b031eaea867066f53f891a68c38eb46a61c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 KB (248442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b7ba47674abf045093c904d76958d700f03847880c98c9f2df7e0f7361ffa0`

```dockerfile
```

-	Layers:
	-	`sha256:512d195de14d890ebd2d525c752bc70ccee1479c40a445eb37f446ab0c3e3cfa`  
		Last Modified: Wed, 28 Jan 2026 02:16:28 GMT  
		Size: 227.3 KB (227293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21b9f46c303420a9a1df5730cf6f972e70dd2ebca11b4894675c4bc1923a211`  
		Last Modified: Wed, 28 Jan 2026 02:16:28 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0ede31fbbb8ddc331f846c032fb03fc429acf28483cbe33e94e07e8ce9b2e158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18630921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a4e3ebfe6a1b2d594bf049c58657bfec4384883c2d07ee399ddc9e71665860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:27:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:46 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:05:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:05:46 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:05:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:47 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:49 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88a0fdc4bb301c69fecfecf50058cde63750c19fa0b3a70fa341b6f2fcf528f`  
		Last Modified: Thu, 18 Dec 2025 00:28:27 GMT  
		Size: 865.8 KB (865810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00141f74db030864fe82dfb8884aeee311a70a3e2d18b678d14d71fcb989fdad`  
		Last Modified: Thu, 18 Dec 2025 00:28:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ffce592aee262f73bfca77c690082a0f099abcb2eae31ff7a76cdbd8df3c6a`  
		Last Modified: Fri, 09 Jan 2026 18:06:06 GMT  
		Size: 13.9 MB (13935915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b277db33511f0e2b54bfebb946d6a705d37fe1f349e2599beb4af83fde8007`  
		Last Modified: Fri, 09 Jan 2026 18:06:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:837202f8c56819055dccc1f9246be343e667a71153eccc9747124fa608ff61d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79458852651f5bb7f0151406cd4ffab2dbb9c6f054dd185c8e4a3825cbd8969a`

```dockerfile
```

-	Layers:
	-	`sha256:9a0a93cd55760b3df04a92358f1d4b1ff6f579216edbf6fcc7ccc5b418be7ecb`  
		Last Modified: Fri, 09 Jan 2026 18:06:06 GMT  
		Size: 226.7 KB (226723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8d8cb6a6c0a6ad1396007c8d77611242427f6cc83b8ed40581fd0babdfbab3`  
		Last Modified: Fri, 09 Jan 2026 18:06:06 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:42d927939cfcb04da99613f997d709db50eb1b47953a8993430f690e4224b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18631065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8c3b4a21ea19e798e2e7abdac100969c2f0f239613a28f2b5d406fdab7a81c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 05:00:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 05:00:20 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 19:41:17 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 19:41:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 19:41:17 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 19:41:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 19:41:17 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 19:41:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:41:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:41:17 GMT
USER haproxy
# Fri, 09 Jan 2026 19:41:17 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 19:41:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac202a4ea053c559abb0839547921026b5c60ef3268d982da82c523fc6ec02b5`  
		Last Modified: Thu, 18 Dec 2025 05:14:54 GMT  
		Size: 849.9 KB (849928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2942b29757a2f3be1a51fbe0d838f5da7e1811a07e28b7e01723666deab1f454`  
		Last Modified: Thu, 18 Dec 2025 05:14:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78626dcd137247653aab536067582c3e9f995672fc5e53d7621c2c2164bf6fe5`  
		Last Modified: Fri, 09 Jan 2026 19:42:00 GMT  
		Size: 14.2 MB (14195751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2adfe6840ebae71d17b3d28159fd29ffea7d44e13a370a1074879d18f60fd3`  
		Last Modified: Fri, 09 Jan 2026 19:41:57 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:4de6e551fbd4dd1f0bb6ab4b8d2d82a17a338086e12536baea270c92014aa4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 KB (247974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a45e3a9903c0729ce6660b120289c9bba1577e3efc453fdba6346f3f14184a5`

```dockerfile
```

-	Layers:
	-	`sha256:3cf879721fcbb9516029771861c197474bcc1d0666a8d591862875efe5e62b0f`  
		Last Modified: Fri, 09 Jan 2026 19:41:57 GMT  
		Size: 226.7 KB (226719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87407f35ddd009bedfc65783492d2ad6c3877ad21dea5b3c1baecb5599b9d20`  
		Last Modified: Fri, 09 Jan 2026 19:41:57 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:0ae95e6afdae4b8d96683ec6f75705a26e86005f14b3b558e7a40938b241eabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18135003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26429cea835290f64fd1e3fcb89523888156249d54e0bef4fa2014fd77ea309b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Thu, 18 Dec 2025 00:26:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:04:50 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:04:50 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:04:50 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:04:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:50 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:50 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:50 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:50 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb4c31af08adac97c43e9de41558d8e4f045415ddcc149f4c0c086792d3713`  
		Last Modified: Thu, 18 Dec 2025 00:27:26 GMT  
		Size: 891.5 KB (891548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f0a83fd7ffdb53f0a260c4043ad39b2781b388b81d8b97ddf6b144b89af86`  
		Last Modified: Thu, 18 Dec 2025 00:27:26 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7830145cc13181ddc4992e5c1f21caeb5968c15b53320dd43a0c91b9fc92d377`  
		Last Modified: Fri, 09 Jan 2026 18:05:00 GMT  
		Size: 13.5 MB (13517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75617199b1c6de8b3c82c957be39362377d7eb11848fff126ce3f56e76e4f3`  
		Last Modified: Fri, 09 Jan 2026 18:05:00 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:2302806f91561693f56d8868f1e8d074e82f0e085b1a758ca6d48ba3a9870cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 KB (247872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202d417122b30e740ba3f316071746de9a645c212c3974092b92f61e0dc92811`

```dockerfile
```

-	Layers:
	-	`sha256:f90fdf9d39f1d138d609f9e8733fc9af5c1b852f04dfa4b2aa1d58a409073eb2`  
		Last Modified: Fri, 09 Jan 2026 18:05:00 GMT  
		Size: 226.7 KB (226677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6cccc87ed821f57fef5ddd54150c328cc43eaaa4f0bc004294bda54878e9a36`  
		Last Modified: Fri, 09 Jan 2026 18:05:00 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json
