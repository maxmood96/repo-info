## `haproxy:lts-alpine3.22`

```console
$ docker pull haproxy@sha256:86a23059cd1422671f6db178dfc37ea247505c6face3b55a60294b60048ecbd3
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

### `haproxy:lts-alpine3.22` - linux; amd64

```console
$ docker pull haproxy@sha256:77321509a26dff73f71cf9380ac5bf2bea951fcb9867a622d8439cab1eab0f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15083629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ab604ab3ca8dd510f21d47aa528e0d1b5f05f9ba20d12b121c815609fd85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f43c444b745a59149adf2644ac838bfa169f1d4a7453cf8bdab6c8ee73b9f2`  
		Last Modified: Wed, 02 Jul 2025 18:24:19 GMT  
		Size: 294.9 KB (294930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d9d39d3b5abcd6fbcbdf9d4603f2e6fe96dad26f5d3c4d45a43ca7cffe99e`  
		Last Modified: Wed, 02 Jul 2025 18:24:19 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3303a08fc480b720d1f121a65f8c96ef137ac5e1cfdced75671403ffe92c8b9`  
		Last Modified: Wed, 02 Jul 2025 18:24:21 GMT  
		Size: 11.0 MB (10990414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c5b548ef583be5fb13945ad69237a70ad544872ae5943406b35b51b067e9f4`  
		Last Modified: Wed, 02 Jul 2025 18:24:19 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:c04febe72b5ae7558685df5175312f1ee91e6969c2624631cae9e59d0caa9ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 KB (210395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b28e47d0b82513b1018e27d4682c56c027f6f971f69d53e54da7133c4a8600`

```dockerfile
```

-	Layers:
	-	`sha256:d952a20c8bf9f36cf098952007cf4a76f0002d614985ace078d1cca61264f3da`  
		Last Modified: Wed, 02 Jul 2025 18:57:07 GMT  
		Size: 189.5 KB (189510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2240e9bf0fe0880797523252e027b522645b89be4d533831ae524e7c1565a924`  
		Last Modified: Wed, 02 Jul 2025 18:57:08 GMT  
		Size: 20.9 KB (20885 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:80906aff067fc0bb0f1d8ced9c609fb0b8fad96b8b117980158c1b8588128fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14894215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fa503d7564141a02472661165261aec6a042a1360ed393c0bf26e928d91da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe2e9ae34585b30de5b57f28b0da070ee0c70df23931f62cbbc087ccf8326b`  
		Last Modified: Wed, 04 Jun 2025 08:18:28 GMT  
		Size: 296.3 KB (296282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e4786477a780f57df23e8664bb3abcf996f51940a6ce4a4f72fcf498ea22b0`  
		Last Modified: Wed, 04 Jun 2025 08:18:24 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce92f6b5380df4e319f1ac8e42eab07ae488a2bfeb02e00813321e535e155fe`  
		Last Modified: Wed, 02 Jul 2025 18:23:20 GMT  
		Size: 11.1 MB (11095565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a43935a4d245e48fc00a02877bcc0b73bde7e981871fb56317fad768ba9d49`  
		Last Modified: Wed, 02 Jul 2025 18:23:19 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:addea1b40ab01c6c82817eb3b1360e7b9edaeb4df4bf1561b5bbf3884a513d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1517a25d07e6e35bd9ab789a663f49eb43b428c5a3e01ee403e68ae53eef1109`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9eeab7bb5960632eb76a0a521c39b7a82f1dc7a16a113d7c20b7212212325`  
		Last Modified: Wed, 02 Jul 2025 18:57:11 GMT  
		Size: 20.8 KB (20806 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5264500067871913599fabfb749caf0854dfc82d987b3340cae208ad61d1979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14437696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8175d7af7b0d9d5c442c7582e2487f518eddeaf126944d037d982f1a154578f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e76ccc0cfb0654d9d6add12fdddab0aee8e41b2f43fbf60c6a2d8a90b6206`  
		Last Modified: Wed, 04 Jun 2025 08:18:45 GMT  
		Size: 295.2 KB (295238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b150886d9e7d415db6d20c17dd37f4bbe5946ed57947452046ca5c28fd9b3cf0`  
		Last Modified: Wed, 04 Jun 2025 08:18:45 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de0019508550419dd4b0d3b49811f052d3c5e5ceadfddbfb62e8005d7068ed`  
		Last Modified: Wed, 02 Jul 2025 18:33:25 GMT  
		Size: 10.9 MB (10921836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ce06f9b7b7c35bd255c384c7e3f8569cd25e1475f9e4acdcf82be3fbb121f5`  
		Last Modified: Wed, 02 Jul 2025 18:33:23 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:8793e128e0f12fff2bc40bd9f65db2a953a94aca3b15f365f1ed9f3f98efff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 KB (210599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8d1b853736f4409508ff1dc0fd3a072da641a03f1c7490006f2ba75ea42e3a`

```dockerfile
```

-	Layers:
	-	`sha256:b1a704f76dd736454fa0edb0d9cc6af9ac86e2b7b184c8937f7b04b05b0f543e`  
		Last Modified: Wed, 02 Jul 2025 18:57:15 GMT  
		Size: 189.6 KB (189578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b95a8f94ab94cd69549290d9b655f8c82d587e4bde127bf4e77030760a87d5f`  
		Last Modified: Wed, 02 Jul 2025 18:57:16 GMT  
		Size: 21.0 KB (21021 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:118de5460269b108bb4e368150a9f7955a465a71dae3488a2e808318a7357914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15370456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f3152a79f9a6a69e46302ee4a1c7a2f34025e221e158dc77bbf2f15081ae18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af3b366839a82db22e060f113a4f62e6812bc7e028256025cde8d1e0051695d`  
		Last Modified: Wed, 02 Jul 2025 18:24:59 GMT  
		Size: 297.9 KB (297893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264db9a17e978c05ab7b23f2c5c05bba806b60ef36bcf6928f4dd2f7d4b4e8a4`  
		Last Modified: Wed, 02 Jul 2025 18:24:59 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef370c68340dc80d18ec9a48b2848014d835712be293aa492f55b8a60d7e5d`  
		Last Modified: Wed, 02 Jul 2025 18:25:00 GMT  
		Size: 10.9 MB (10935181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c411e79dddab88b8fd0d7697219bd05d6e3af94a6956f9404e377202550c9fd2`  
		Last Modified: Wed, 02 Jul 2025 18:24:59 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:bd1c045b11710bd141912905a691e8eee841dbc8caa12915b30b887d69da9caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 KB (210683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d8457c6dde1b2afccf02afe401fa0e1918c0fa57dedba63cce96006004a47e`

```dockerfile
```

-	Layers:
	-	`sha256:d6127cc92cf958f958aef13c7097f92cfa4a28bed9ec73c905adaa3711104a30`  
		Last Modified: Wed, 02 Jul 2025 18:57:19 GMT  
		Size: 189.6 KB (189614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f38fd5c2ca8e3718e8d64bb85f54f5e7658007b35cc95274b69648f56914d1`  
		Last Modified: Wed, 02 Jul 2025 18:57:20 GMT  
		Size: 21.1 KB (21069 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; 386

```console
$ docker pull haproxy@sha256:38a78843236b470339223a88e49ba7f68974ed971b64e0169526a6190bf3df85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14638742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7f9e0033d4678a7ca6cb6e0b46fadd618421f5ded43760536b48c3b00ffe15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b250e84676bd571caf2af9e66e11bd7fa9efd30790e973135f881e5293ea376`  
		Last Modified: Wed, 02 Jul 2025 18:24:31 GMT  
		Size: 295.6 KB (295618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636e003ef74d718ff3e4c0368dd66a786b8618369103cd031a641d4cd3ae185`  
		Last Modified: Wed, 02 Jul 2025 18:24:31 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bc071d6bf273d59c9c7e4c4715576927173117bd44a17b5c1ead6e284a97a1`  
		Last Modified: Wed, 02 Jul 2025 18:24:32 GMT  
		Size: 10.7 MB (10725655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781f709b7e9915dd024bdfefa7a36e04a312243aff3bf0a69d9069aad4b6358`  
		Last Modified: Wed, 02 Jul 2025 18:24:31 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:40779386f1bb774b46bfa1feac02e8101a3626c70210893ce0340cb7c2f8168e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 KB (210296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0091f5bb7bbf1cfb03205171d87ca58a6be6a68cafbb6ab55394face70978f6`

```dockerfile
```

-	Layers:
	-	`sha256:ee23941dd65c4e98e4a498f1b2d3d08900c449f781a1e4a703fa326657a3aa49`  
		Last Modified: Wed, 02 Jul 2025 18:57:24 GMT  
		Size: 189.5 KB (189465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3911decb89b6715356141e586f56bfa82fa1dbbae640a0df37994f0495891c54`  
		Last Modified: Wed, 02 Jul 2025 18:57:25 GMT  
		Size: 20.8 KB (20831 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2d57eb7b1d49053d181974ca573083a13daf23ee6846150f48732d453bebe2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15649344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5069fbf053c2a7b7cd29b24137842d7cfdfc6f4bea83bc03b28fce8855f0d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93fba4aede29632f597a7ecb4a5b6591a1b0b068d963c96a47e54369d702da1`  
		Last Modified: Wed, 02 Jul 2025 18:25:47 GMT  
		Size: 298.3 KB (298328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7125e52130c253b2ba3b0e567660a774577bd0cb6718192ef3b825d095ae15d4`  
		Last Modified: Wed, 02 Jul 2025 18:25:46 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e52433b836277d4a460544a7aec4d48c97b76b3d113e34ec9e9d319dccf40`  
		Last Modified: Wed, 02 Jul 2025 18:25:49 GMT  
		Size: 11.6 MB (11619383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13dc043d577b98960c5cec7e05a4552af5ee7186f9f5f393c86aa1a043cea80`  
		Last Modified: Wed, 02 Jul 2025 18:25:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:81ed2437f4416b57119bcd7eaf481ddaa62f041c8cb40eedde0e2ed888e11f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 KB (208576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc159b4c6e2922ae904a27ee175da997f90900d7857324855263b13be65368eb`

```dockerfile
```

-	Layers:
	-	`sha256:5ddaf237b307d3a98b577e4baefbe2f742da637a7943f2dd0dc7ec551b50d2a0`  
		Last Modified: Wed, 02 Jul 2025 18:57:28 GMT  
		Size: 187.6 KB (187617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece58b5624d705a748c006a6d26c75342aee6bdd90370f605101ce2a85c56ab0`  
		Last Modified: Wed, 02 Jul 2025 18:57:29 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; riscv64

```console
$ docker pull haproxy@sha256:87b80bc18b9fd8742985faf3e3546b481cfd31cac806f1c79f118c5233b942b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14499435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080cb79479fe6dd658670430ff0a9241bb39110038665f0ef643c2feaea597ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce0dde45abdad321a39c77b330eb310e01cd6163224eb49bb346d7bda18768`  
		Last Modified: Wed, 04 Jun 2025 08:20:08 GMT  
		Size: 295.4 KB (295397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5589bcc1c1ea4586b46891af00bc91ec3b315f3c2a0890e474d7cfc6bd74f095`  
		Last Modified: Wed, 04 Jun 2025 08:20:04 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c534e9dcd6f27480d4ca2b897ba42b0af1d01888c1d833613b5fbe6904b2192`  
		Last Modified: Wed, 02 Jul 2025 18:36:01 GMT  
		Size: 10.7 MB (10688780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae55927a30c28ff53cc00a23f88f1c356066c2e2ee88302a412e64b4647bfb2`  
		Last Modified: Wed, 02 Jul 2025 18:35:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:35a43a1730c808ec1f29454e3aebbbf12e5aeac1cf5d68814cf6d50f463ab297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 KB (208571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc35b2d7a09cfcbc05487f987e9bf446ec0883a43ac63ab78821356319ea7d7`

```dockerfile
```

-	Layers:
	-	`sha256:6d11b8b28d563665753f86c113233ed3836fddd8d7c813e943184e0c66b76bec`  
		Last Modified: Wed, 02 Jul 2025 18:57:32 GMT  
		Size: 187.6 KB (187613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c18ecb951ab2ec5e682ace29862f4b81fc65d7f5e3e6535675ecd5b0f904386`  
		Last Modified: Wed, 02 Jul 2025 18:57:33 GMT  
		Size: 21.0 KB (20958 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; s390x

```console
$ docker pull haproxy@sha256:dc70c7f23815822429cbbde932ec97ac357db26ee7562fae41d9a2b0518b1951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15302873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66de7868accae324e265e88e4328b9300382232747eadaa1d262e102eebde703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_VERSION=3.2.2
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.2.tar.gz
# Wed, 02 Jul 2025 11:13:32 GMT
ENV HAPROXY_SHA256=be64ed565c320e670bb909c5834f90303c3ec0c97af5befa45994961aaa6c6ec
# Wed, 02 Jul 2025 11:13:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 02 Jul 2025 11:13:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 02 Jul 2025 11:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Jul 2025 11:13:32 GMT
USER haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 02 Jul 2025 11:13:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252ee3cfa4cedaae95c391dc065924268b148899eb30e7874f6d538af0e4b083`  
		Last Modified: Wed, 02 Jul 2025 18:25:58 GMT  
		Size: 296.2 KB (296228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63c69f50a0a3e81598b5da9194eb321e06037e858b04c26e61df635cc4fbfc5`  
		Last Modified: Wed, 02 Jul 2025 18:25:58 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821154ac7e29d84180c014d44f5172c278026557b876740373374e7744c52cbc`  
		Last Modified: Wed, 02 Jul 2025 18:25:59 GMT  
		Size: 11.4 MB (11357678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac809e6155218cdf87668ffe1ab0c424ff199bc606768e490b4347a853fe7481`  
		Last Modified: Wed, 02 Jul 2025 18:25:58 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:7de989a586dfeedb448323a3cc26fd3af6259626e3b5f8398a1a251afb2fa18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 KB (208446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6a585d65fc67c10e979cd4f72afc8093db75a6c81d4422f0f3f323ceecbca`

```dockerfile
```

-	Layers:
	-	`sha256:b424475a8fa847ec7eebd50630bc0b204660f17367bdb23237127de25f858daf`  
		Last Modified: Wed, 02 Jul 2025 18:57:37 GMT  
		Size: 187.6 KB (187559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd635352fda70e07d46f1a1bf3d43c1dc54c8d28483b967d458230fbe06cdca1`  
		Last Modified: Wed, 02 Jul 2025 18:57:37 GMT  
		Size: 20.9 KB (20887 bytes)  
		MIME: application/vnd.in-toto+json
