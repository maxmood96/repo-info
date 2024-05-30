## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:53828f21052cb0cf56a3c86d1419af44cf556151f5d762d32980e35ee02b2dcf
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
$ docker pull haproxy@sha256:cb6000cb4917682452a5d7b3d6f5e8a0254ae5b39e55a1daa4ed5f123347c5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13117227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2cb60a390a2b8b322deb6361e4db1ce11ee04e4481d8ffa1d409fa25d888b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471cb4e46ac14fe3e881f0227e8b2a033037619c4ccbf576cb11e49147bf4024`  
		Last Modified: Wed, 29 May 2024 23:01:51 GMT  
		Size: 292.4 KB (292419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2f2507d995842b708e94051f241df085cf7f98b2ee8c019cd9dd27a300a28`  
		Last Modified: Wed, 29 May 2024 23:01:52 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e021905bce6b2f3e612197cb147cc62ef89324f1febcf03b698ff9b6591ca1b`  
		Last Modified: Wed, 29 May 2024 23:01:52 GMT  
		Size: 9.2 MB (9201260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7cba50abec2e5ba1727bd8a542963ea2be887d582755b18057b2b3d9a1476`  
		Last Modified: Wed, 29 May 2024 23:01:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:c9a8e6e9c80b5fae6cd471152e24afc3b21471defc9a40acd2e517f265302b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75e86711e4a0b2e4b5fc313a1a44a3ea57179e83b2f48c4b1c3e38e1525886e`

```dockerfile
```

-	Layers:
	-	`sha256:dba9732be0bde30b9b0c555d16b3e9ed49b90d3ea4c24f8fc2cafe1ab82cfce7`  
		Last Modified: Wed, 29 May 2024 23:01:51 GMT  
		Size: 176.6 KB (176618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475dad880677c022284a096ab587cbd5c618069e41423748cf0d4e627a7c9f8a`  
		Last Modified: Wed, 29 May 2024 23:01:51 GMT  
		Size: 20.8 KB (20801 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:48044493a15c8be91fe8f9ede14f653c9bab2e0efc9e7327a7442e6a7df21dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12871740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e354c79b61a7281c8559ba863635820d125a528d87e8bf1c629a67cf3f076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749987d659c1c3d7d8e988f0e114b715fdef359ad6da37268f889f854820a62e`  
		Last Modified: Thu, 30 May 2024 00:18:16 GMT  
		Size: 293.6 KB (293611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfdea1d724bb22ca870eaea8149eea4c481fbc65c5ca7ab6009528f397c41e9`  
		Last Modified: Thu, 30 May 2024 00:18:16 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6380edc3b4aeb20991b76ecb2cd259b9789e8694c09242879a7a767add2cff9b`  
		Last Modified: Thu, 30 May 2024 00:19:05 GMT  
		Size: 9.2 MB (9211621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369ecafa2afc9e5daa8c7fb1bbb47ca89aab9022c1f8a529df26e13ed475f6d5`  
		Last Modified: Thu, 30 May 2024 00:19:05 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0d8397cf03abe6231bc179c2a461debeea5c90181f71b11af7315d9bead1ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39adedf267d0aaf1b6b2bc6a9b9e6668cfb906f000f493d787d061c7f6b70463`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f3c4c6925a7899453af9b60bf81524c2bc68845aad1fcd5744af4666a3956`  
		Last Modified: Thu, 30 May 2024 00:19:04 GMT  
		Size: 20.7 KB (20709 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:271471ab7bc6a3a86abf003992fd5eed02cc2e1b9f775be864fe285df3e6f14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11884806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e4436f7fd9da54d9a6a399ee9159b2bac0a184e316e33671eee680f5891b55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_VERSION=2.9.7
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 22 May 2024 23:39:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 May 2024 23:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:39:55 GMT
USER haproxy
# Wed, 22 May 2024 23:39:55 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 May 2024 23:39:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1859e46a631b6d5f4a42efbdea792f5b286c78c4edac1f6dd8b610455a2b96`  
		Last Modified: Tue, 28 May 2024 23:25:41 GMT  
		Size: 292.5 KB (292463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b83b8d27e3ea28af2defafafe62c601b0a85eb73315519b6c6845183c280e`  
		Last Modified: Tue, 28 May 2024 23:25:41 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47055e509da43b182fb2595a59b11bca398ab14037c06d95cadbb22aee875a5d`  
		Last Modified: Tue, 28 May 2024 23:25:41 GMT  
		Size: 8.5 MB (8496857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12e33914830e52bbcd8207c39d5e5d6e8a710376df8b76dde308a4783741a4a`  
		Last Modified: Tue, 28 May 2024 23:25:41 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d49499bf93ea72515cd2ed4f00930b4be752d62b75ec480b207bb80c58da1186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 KB (196335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e933f58f2f79a4f35190152808d6d768ff259d0074aebbc526d652bccefaf1`

```dockerfile
```

-	Layers:
	-	`sha256:893a3283b8fe874d38c2754fe61f6de5c1ac9da78c220589fff80631b58c8a9a`  
		Last Modified: Tue, 28 May 2024 23:25:41 GMT  
		Size: 176.0 KB (176046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c3c2e99bc37bff54c5aee4d1fa00c60573576452ecee96662a67cf8b843967b`  
		Last Modified: Tue, 28 May 2024 23:25:40 GMT  
		Size: 20.3 KB (20289 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:05af2c46a1136756bff84c32b2194c8a0c8b2f91903768b06b618c089f0f59a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13004909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bd9c7794210ccb577910d6bb86d9574b506a397af733a724be8d9abbe1b8d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_VERSION=2.9.7
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 22 May 2024 23:39:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 May 2024 23:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:39:55 GMT
USER haproxy
# Wed, 22 May 2024 23:39:55 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 May 2024 23:39:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bf932126f6659213bc8687d78a936c87aee5b89895f235df5a41ac6fc412e8`  
		Last Modified: Fri, 24 May 2024 02:05:04 GMT  
		Size: 295.4 KB (295432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd62677503492e4ac1cee1266beed9579db31fba8a170664e503b61e99467d`  
		Last Modified: Fri, 24 May 2024 02:05:04 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392ad30410e68d35605456ebe52753b5ab9c482f31c1ed0256eb63ccc66c83b`  
		Last Modified: Fri, 24 May 2024 02:32:22 GMT  
		Size: 8.6 MB (8621246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02e212d77912363fbf74237ab1050ab708310d5ef89f26141f2b41fc4c27dc6`  
		Last Modified: Fri, 24 May 2024 02:32:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:7d85b5379c04323bae7d9057c9656068186685cc477e5cdee8443b6d23e66920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 KB (196200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6146b9d577b089d73d7c6341531413f6d21d34c610c813a5ef9f11f6cde88afd`

```dockerfile
```

-	Layers:
	-	`sha256:c8674e9ab893da25b90a97693a502d3990974cdf89b09f5fd4026d32b2314557`  
		Last Modified: Fri, 24 May 2024 02:32:22 GMT  
		Size: 176.0 KB (176009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09da43c5ddc636cf56c28b46d9b263b241e09b27510cc0b0b586e6f766ec3fe2`  
		Last Modified: Fri, 24 May 2024 02:32:21 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:0f0a4fa1b784b167dfe487a1aa7976e3dc2488cec3a6d58cee073f15912ab40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12758158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ed612583e71e46d23bb7db1e9dab56fec3ddd25b4b702b0b31a6f65e89dc93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02117855f7feabaf5562b24ef1980cb6b661bd723e7fc25e8048c928b96c5b3d`  
		Last Modified: Wed, 29 May 2024 23:02:23 GMT  
		Size: 292.9 KB (292876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8683928900f5965225d1b6db584b73edb3ba58ead3b9f8b0a1cfb9994d106a0`  
		Last Modified: Wed, 29 May 2024 23:02:23 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71c5ba9aa3c21cb1b6d1f0ddb3d7419e35780899da7c8b6d5849c927f0509cd`  
		Last Modified: Wed, 29 May 2024 23:02:24 GMT  
		Size: 9.0 MB (8996650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a80f696536776caec47384940893ffc317853847f78aff34ab9623528959b`  
		Last Modified: Wed, 29 May 2024 23:02:25 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:929e9e002df13aee5dad46ae98f0db364d280d0608892dce775f4be2c13ed04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a11cf9c6101b6c0287c5f05808c9f2868b2100d466326dfe7d09937a6d0d6a`

```dockerfile
```

-	Layers:
	-	`sha256:c387f480400d0b37be7362563179430fdc6457223034ad1707aa78e7c9652288`  
		Last Modified: Wed, 29 May 2024 23:02:23 GMT  
		Size: 176.6 KB (176573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:821586acead46cd4443fe99126dba47e184b27bce72f448e28f537db683f75bf`  
		Last Modified: Wed, 29 May 2024 23:02:23 GMT  
		Size: 20.7 KB (20748 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0d7be2fc875811ecea7edef7030a739211b221d094c8667468c36881e775190a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13593761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8dfa8b7e65d928a78cc02d545adfc00b4dec3e7add4d2d83155e6986567455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205b34e4839457aa1220a821e34f600a43aea330bcd67ff9e43f1d52116f9fc`  
		Last Modified: Tue, 28 May 2024 23:02:56 GMT  
		Size: 295.9 KB (295874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4193c5bc86ef2cb6bc462858d92bdbe325ffa99705483773961925419201550`  
		Last Modified: Tue, 28 May 2024 23:02:56 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f05aca8def00f834177332aa0bacf4192db63dfeb0ed452b4424764aa31a52e`  
		Last Modified: Thu, 30 May 2024 02:54:15 GMT  
		Size: 9.7 MB (9726587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f35eb58028c93dc711b2c49ed9f78612f099c4650c8f924e6d66a563329f5`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:260e45710959b711c30620523253b75b6044baf44073a8bd3d2f843f541987b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 KB (195589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e000fd25c5ec05a8e4af2540e08fff913d0eab7d2455351d8a16f8a0ab300749`

```dockerfile
```

-	Layers:
	-	`sha256:eeaa2a04552ccde040780fc34b7d5d1e02556b4878fae6cbf09c5759702a4364`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 174.7 KB (174722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639d3fe504b7f10b467f6853b629d007d0aef028ad1c9dfc412dc5ff9b8f1b7`  
		Last Modified: Thu, 30 May 2024 02:54:14 GMT  
		Size: 20.9 KB (20867 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:5ec6a7fea5d282dd5a13e13f5804b42e4f2ad492f39facb56ef2cdfab57c13d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aa5283cbc936f03330d1a29e8e41337892bdc6a192b3c1ef39151c94588f59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_VERSION=2.9.7
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Wed, 22 May 2024 23:39:55 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Wed, 22 May 2024 23:39:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 22 May 2024 23:39:55 GMT
STOPSIGNAL SIGUSR1
# Wed, 22 May 2024 23:39:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 23:39:55 GMT
USER haproxy
# Wed, 22 May 2024 23:39:55 GMT
WORKDIR /var/lib/haproxy
# Wed, 22 May 2024 23:39:55 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e9d0aacad29adbcc630c6e2a62753401bf009ab62d63a3a874de9468105343`  
		Last Modified: Wed, 29 May 2024 20:53:58 GMT  
		Size: 293.2 KB (293166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d9fc3e31dac40a32b21a715c2b578b1b4802992c0a2f0db0eb48cd3b783a73`  
		Last Modified: Wed, 29 May 2024 20:53:57 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d54f7fdb05bdb886a57992fef2378961178b1f982dadf24a8960c4dc95ec5fc`  
		Last Modified: Wed, 29 May 2024 20:53:59 GMT  
		Size: 8.3 MB (8311431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152b1708fe4ec1470ddbbda8e3131d5d9e0ba342600f77215c6f994855ca7b7a`  
		Last Modified: Wed, 29 May 2024 20:53:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:29283d79d54da7934aa3c8266918c5005b265e7f4ac376c1c473023cc1ce1f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 KB (194313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f359bba6adf800b751ddb8a09d9275d38370a35368133d2d52ac9314e7f22`

```dockerfile
```

-	Layers:
	-	`sha256:cd87b317ee49274d630cf24b10e36f34572fb0c2cf4c3d13466121a2ed774f38`  
		Last Modified: Wed, 29 May 2024 20:53:58 GMT  
		Size: 174.1 KB (174082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da38ce6f71bd6102a78f437b13309246351951057de760bb185b08fee7028198`  
		Last Modified: Wed, 29 May 2024 20:53:57 GMT  
		Size: 20.2 KB (20231 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:28935ab095893382f4edf37183b601e148fe86d02e2ad0fad2c3759acf010be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13190995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb506f03339adbf47a6968d9914e5ff16056b49cd3bacdf5f6c10e20dce76e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_VERSION=3.0.0
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.0.tar.gz
# Wed, 29 May 2024 17:13:26 GMT
ENV HAPROXY_SHA256=5aad97416216d2cd9dd212eb674839c40cd387f60fbc4b13d7ea3f1e5664a814
# Wed, 29 May 2024 17:13:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 29 May 2024 17:13:26 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 May 2024 17:13:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:13:26 GMT
USER haproxy
# Wed, 29 May 2024 17:13:26 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 May 2024 17:13:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63619438766320b6ae7f786296090adefcb6654d3a9eb884cc140bbcb843b720`  
		Last Modified: Thu, 30 May 2024 01:30:45 GMT  
		Size: 293.4 KB (293404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f61d03d2873b4c3f8bb10b3ad9ff8d74e8315271fd7282a387ea13049cd99c2`  
		Last Modified: Thu, 30 May 2024 01:30:45 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce7cd40a12f7160834e679183653f9d94a3cf9196c9553556b880b556b200d`  
		Last Modified: Thu, 30 May 2024 01:33:01 GMT  
		Size: 9.4 MB (9435800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4054e8fb863e5bc01a1006b684e68034cc9127f6729463a46fddbb86d14a7`  
		Last Modified: Thu, 30 May 2024 01:33:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b236104dac5c0b965355cf26145e2b44ada732aebad6384a611edfa0bc9335a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 KB (195465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74fd550266f286e5aec8446819bb00c9485784e8dff03159f57361724c3692d`

```dockerfile
```

-	Layers:
	-	`sha256:ee841ab5c2c997cc03e41e1f86b95e32aa9160ec9aea5a953646750062232a43`  
		Last Modified: Thu, 30 May 2024 01:33:01 GMT  
		Size: 174.7 KB (174664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd3bf47e5892356a2b649afcdaffeec434ba9f08014de78a859844cdd146215`  
		Last Modified: Thu, 30 May 2024 01:33:01 GMT  
		Size: 20.8 KB (20801 bytes)  
		MIME: application/vnd.in-toto+json
