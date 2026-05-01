## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:0c32ec9e64a3bbacb2a1a28afbc3d46032d905bf74ccb745b45488ff41ee9a6b
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
$ docker pull haproxy@sha256:d61ad3eead65e4652cf8348b4a5601f1a3aa98f899fb8d77d3f39fc399352711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17938582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebdca047f2f2ba5eb68bfcf08852d09e0ac67887df948b2c86158012b4a8dc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:30:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:30:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:31:21 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:31:21 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:31:21 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:31:21 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:31:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:31:22 GMT
USER haproxy
# Fri, 01 May 2026 05:31:22 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:31:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598f465c9d012f3a5ae75c4c6502b7d704fa7cba941fd04fa5964532e543a023`  
		Last Modified: Fri, 01 May 2026 05:31:29 GMT  
		Size: 824.7 KB (824717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7415ad6568c45e57644ef3387dc987c750ec08bb88120aebd21faa66002cf9`  
		Last Modified: Fri, 01 May 2026 05:31:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d64330e26ad0108b10ea1abe05dd2c57235c108cf3f9caa3923347042b0c48`  
		Last Modified: Fri, 01 May 2026 05:31:29 GMT  
		Size: 13.2 MB (13248235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acbe638fafa3fcd1d610ff9c239c96c2c7dbbdb1a96a2883ca3db0556949812`  
		Last Modified: Fri, 01 May 2026 05:31:28 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:b6a7fe6f09ba7571d972bda882e9321bda11096fcaf671f9227fbf3fbdda503e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 KB (246568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bda8d0e982c3047c39fdf147f507e146ebcceb086e44342aaabce4dfdf1bdfb`

```dockerfile
```

-	Layers:
	-	`sha256:c2683830be1b3f0be1d0724ba7d729371a3f1f5a168028368b6aa129bb0ee544`  
		Last Modified: Fri, 01 May 2026 05:31:28 GMT  
		Size: 225.4 KB (225373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e56d88b10beb2dc172433baef197e33b36681a4a216ff79c0764c2a45350a33b`  
		Last Modified: Fri, 01 May 2026 05:31:28 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:a6e8adf9434074be37b8eaf6807267f7771a1ab9cb7407b2fea2fc551552862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17812885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e79fb74b5ecb30ebc5ad3c5836f39fbfe8a7ef169e4696c8008f1c1db9d4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:30:23 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:30:23 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:31:04 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:31:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:31:04 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:31:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:31:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:31:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:31:05 GMT
USER haproxy
# Fri, 01 May 2026 05:31:05 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:31:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4410fccbc81b8a7a94cdb2f5c085203b82af2446b20300e15da60de719028cc6`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 817.8 KB (817754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784f3072c9d9ff3c973738d94430ea81fce1f7d54742c81d0e0f483ca2813892`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940850d96af7e72f6c9254f0bd3a3698c853558b00384c92a9f0683b55b92a10`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 13.4 MB (13421828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45023b241da2c9ec7214d07bb2792f3f5a47e63e3de617efa801cd454b8fa47b`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d0d4270273a0f071192e32779cde0b9b0a7ddb52e9fc7514f396e7bfdee68f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b3e0f2fe73a110dcf42a6910ce82fa9a2df2599744e72279dae6f933eec328`

```dockerfile
```

-	Layers:
	-	`sha256:f8e2f448dde0a41aaddf93900cf5b4edd831b7418da23966fd93da24c9c270e2`  
		Last Modified: Fri, 01 May 2026 05:31:10 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:39daebe6088a135f03e7721e9474452eb7b2e4e0d8eed0ce77947f0cff5c4797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17297502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167153e0348e97834071f21db71d4f96a0bca4f6a8db4cfe4710df775c84a032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:30:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:30:54 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:31:49 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:31:49 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:31:49 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:31:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:31:49 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:31:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:31:49 GMT
USER haproxy
# Fri, 01 May 2026 05:31:49 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:31:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682231b9879c254dfeae1272dd9cc93838245016a6a68d01a0bda34262fd7d8e`  
		Last Modified: Fri, 01 May 2026 05:31:55 GMT  
		Size: 773.5 KB (773543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68076ccbbcdce7bbc9d78c2c4b1e38a58bafcfc44211c6d1f360187f34cc6a`  
		Last Modified: Fri, 01 May 2026 05:31:55 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b1d2d8dc168a30e9bc0c561368b8d6e9ba5bbe67542e5cf7d8a5fce158e826`  
		Last Modified: Fri, 01 May 2026 05:31:56 GMT  
		Size: 13.2 MB (13239400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f08d5252f1d0ff75b76f21d3460ce44b1c4f424bad2cb3271db279bd23d4ddd`  
		Last Modified: Fri, 01 May 2026 05:31:55 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:649fb8cf92ae7e6193a75db509b6f7c54a53664a5397fc4b4e45aaafbc5c82fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32290b863d5872c795772d6b38efc34853db2ed0d5dbaab9e67ec9ca088efb52`

```dockerfile
```

-	Layers:
	-	`sha256:e96d7c9f2fc07fdb119694de9dd8b7411784639f6d05347a6bea9ba84a411682`  
		Last Modified: Fri, 01 May 2026 05:31:55 GMT  
		Size: 224.8 KB (224775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9304757645a1f7978903f2ab60539581af81166b44d334bc8078bb8692e5c99d`  
		Last Modified: Fri, 01 May 2026 05:31:55 GMT  
		Size: 21.3 KB (21317 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b04b7550b2b4854c5c290d61406b46eaff5ff321cffa7afa49a417bfe79cc460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18100473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617a0ab7bf9e0efccfc4cb9b9236271ddcac9a0d8885d3c05600b977f2067b12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:29:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:29:49 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:30:26 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:30:26 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:30:26 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:30:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:30:26 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:30:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:30:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:30:26 GMT
USER haproxy
# Fri, 01 May 2026 05:30:26 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:30:26 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db647ebb71084dc0e0edcdb3bbeb3068a0601be2e0c16e4ad15a80ba8a88729d`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 838.3 KB (838288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10fa5ae5d8ff16b33f58b89000544610e7f9d4b10f24331d3c1cd78a5524b55`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a1df53041754ead6cea705ec6c7307b0bee2e87f706124fdc8e0ba0d5b987c`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 13.1 MB (13060879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3f6edb9c98ddcd9f6d65b09731415cacafc3c59f84d301eac946d821717920`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d9ace38c9aca58017401d6808f501d6e410c82dbf9aa3cec0b50b900aecc5113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 KB (246156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713859a8a6086a095200e3572bf754d4fc78a8de0c2b8baf5cd532f67f4372f`

```dockerfile
```

-	Layers:
	-	`sha256:90e7bdc96ccfcdb86fcc1b5d8058ef1d23f5ac175825bd1b87a63b73af6b53d2`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 224.8 KB (224803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c43b6f5a78fe259f593afed0dee9e61140e51b5c89d016196e618d9ccf3bd4`  
		Last Modified: Fri, 01 May 2026 05:30:33 GMT  
		Size: 21.4 KB (21353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:7cce22a06cda1cfd063cea91b7fbe6c2b21c598c54dd196045771061fd8b075c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17475543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3c089c10d370c0e66e887a6899d54f8ecba467949779f2017d14ed10cb8839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:30:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:30:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:31:29 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:31:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:31:29 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:31:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:31:29 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:31:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:31:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:31:29 GMT
USER haproxy
# Fri, 01 May 2026 05:31:29 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:31:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0b61b55712cc998a4ca2af8f85b651ec0bbd3dc06f733abb97d7f0808ae6b`  
		Last Modified: Fri, 01 May 2026 05:31:36 GMT  
		Size: 830.6 KB (830558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7415ad6568c45e57644ef3387dc987c750ec08bb88120aebd21faa66002cf9`  
		Last Modified: Fri, 01 May 2026 05:31:28 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4409cf22f399ef4a97169549335e975eb47c8bb83e1174f2577e787d422abe7f`  
		Last Modified: Fri, 01 May 2026 05:31:36 GMT  
		Size: 13.0 MB (12953102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171def160b5e84da90f23732d855548b978762f770f088f89d1c7f01c9ce57e`  
		Last Modified: Fri, 01 May 2026 05:31:36 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:76d8497782c74a9e1482a4bc74901d8ef18ccb382984087a84dec960d1982667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 KB (246487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c32ce474e3ebc7e3d497fcc703a22ef2513280957519a68652ae23ce72907f`

```dockerfile
```

-	Layers:
	-	`sha256:69c71dc45905ba74844eb777c0dca352f0304988e95b952324fd14405dbce63a`  
		Last Modified: Fri, 01 May 2026 05:31:36 GMT  
		Size: 225.3 KB (225338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6adb3a7a69892f0c7ac7047d305601aec92792e8378548fc9bfb0e3cab73f2`  
		Last Modified: Fri, 01 May 2026 05:31:36 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:3ba89bdafbba9986a492885c163731427eecf7c86c5efb50739b4a1b6b399a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18688794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd077ff30cc3d638b2c16eea451998db663f2168e07dd8e3aa1838eda6ee696`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 18:23:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 18:23:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:41:48 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:41:48 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:41:48 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:41:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:41:48 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:41:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:41:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:41:49 GMT
USER haproxy
# Fri, 01 May 2026 05:41:49 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:41:49 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032e619063148cf97af0653144ddd5b34dbae5efefada60ee5821c2dd3cb82a`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 861.8 KB (861798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d5a2ce151f275152156bed9b6c5a27da4a4b9922039d83b76fb94d3d42a926`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fc8d435c14d6f8fcff04c0d78f6521424caa0344181638faaa306a14c847c6`  
		Last Modified: Fri, 01 May 2026 05:42:02 GMT  
		Size: 14.0 MB (13994625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c838c7dd895f72e8b8eb6995e191392b7e5e99ef9c54eadf6ce6296f8cfa422f`  
		Last Modified: Fri, 01 May 2026 05:42:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc2b1557ff5fed03c98b93e116f2d90b23e07eec91b63d881368284c9dc853c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (246022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccfae4a1948335332c4d1768a54280d06e0dd9f2b86ddad420de6e9bc4b4d2c`

```dockerfile
```

-	Layers:
	-	`sha256:7507acf933554aaf647ca1a59110c0cc4595408ad8cd6ad2a6cb2b3e9a42ea33`  
		Last Modified: Fri, 01 May 2026 05:42:01 GMT  
		Size: 224.8 KB (224768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f5161c914013556b85d0c3ce804df2ac35acc50eb57561eba24b3bae079019`  
		Last Modified: Fri, 01 May 2026 05:42:01 GMT  
		Size: 21.3 KB (21254 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:cf7f5fc2d1254d9d32dca879f8057ded8a9397e8f710eb3b7b7135f042ec80b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18689031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b973b60d7e78c71a5de858eadd616b3cc27aa30ab36e4164351e2b7d1c1922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:39:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 21:39:30 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 06:36:30 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 06:36:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 06:36:30 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 06:36:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 06:36:30 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 06:36:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 06:36:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 06:36:30 GMT
USER haproxy
# Fri, 01 May 2026 06:36:30 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 06:36:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323dd7cd28f54b7b679a2920b8ffa91e2575431b8965d410473b83371f352d8`  
		Last Modified: Wed, 15 Apr 2026 21:57:45 GMT  
		Size: 845.2 KB (845235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdbaf29166e1dcccc7a014b08a8dc65241206620cce8985df5a83c6bc81e1a8`  
		Last Modified: Wed, 15 Apr 2026 21:57:45 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc37a3b367de66be531ca94c1109e8bd44bb0859d4c954f34b88c5dfc7e2a9b8`  
		Last Modified: Fri, 01 May 2026 06:37:17 GMT  
		Size: 14.3 MB (14254690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31ee2069147ea9deaed7c49fff3969e3cddddc5c14218b3658fb19dc5a6c44`  
		Last Modified: Fri, 01 May 2026 06:37:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3767a032d48ca80ceed50313bcac64de64f7a4056380003239e2dd199e2947ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (246019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31985c2dfc4b72f6852f288aef1f0faf77827dd33b8d03195e93c47f2e0fe899`

```dockerfile
```

-	Layers:
	-	`sha256:87b44e5a7a338d739d1abead7d1d456c3accdb5573e21825b19c85c738f71d42`  
		Last Modified: Fri, 01 May 2026 06:37:14 GMT  
		Size: 224.8 KB (224764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625fd1c3d0bdc60701add4050376f7b08ddec7a56e3e75f7bcd8f9982281bd75`  
		Last Modified: Fri, 01 May 2026 06:37:14 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:d7bea24c681a9b091044a3f205c564e4f913e9c804de0b7992125a9a74c44286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18192406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d53a5e64bdcc02818df156c917ff67fb4e0eb61b27cb62b0c101439b7aa3eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 05:38:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 01 May 2026 05:38:43 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 01 May 2026 05:40:04 GMT
ENV HAPROXY_VERSION=3.2.17
# Fri, 01 May 2026 05:40:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.17.tar.gz
# Fri, 01 May 2026 05:40:04 GMT
ENV HAPROXY_SHA256=023a9efb8a8d73a0c1b6335394400e7eeb4ad0643ffda73c5f93820a720a9695
# Fri, 01 May 2026 05:40:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 01 May 2026 05:40:04 GMT
STOPSIGNAL SIGUSR1
# Fri, 01 May 2026 05:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 May 2026 05:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 May 2026 05:40:04 GMT
USER haproxy
# Fri, 01 May 2026 05:40:04 GMT
WORKDIR /var/lib/haproxy
# Fri, 01 May 2026 05:40:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104bc504688d021abcc35fdfa9fa91fe7bcb43e3d466c2d72f077f32644dea38`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 887.1 KB (887141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08210afa9e447956e8ca6bffc2e5ea8b77556ff6b8275f9b9be403228b15d78`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e21c694ccc47b2b935097e01ad0f080bc89b341808694b00083c7ec2a8f1ce`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 13.6 MB (13577287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5283880555ee4480f40d290418f78a1f9e37e4151892267a2e5de125eb759180`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:66d15bc4c9b01aa9f28122808eaff9e18b43576ef565dce6a093bbc00db71005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 KB (245915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1713263c826cbb8687510888fbc4ee7f4c4dd9dba6094260fec8cf12abc7fbe`

```dockerfile
```

-	Layers:
	-	`sha256:1f7ecf5ea7b9e1a667e382f133d070b4026782768ce34e47544dd6b34e10b80f`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 224.7 KB (224722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1d336d828499a9e635f9779a7dbca0ecfc365ba9d83e4ec53e2027cda24cc6`  
		Last Modified: Fri, 01 May 2026 05:40:15 GMT  
		Size: 21.2 KB (21193 bytes)  
		MIME: application/vnd.in-toto+json
