## `haproxy:lts-alpine3.22`

```console
$ docker pull haproxy@sha256:ad9092d87b53d506e938c2d4add1214d80801e0b529d65dd86efbd2368304491
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
$ docker pull haproxy@sha256:1cbc82126de93c9548a7fc31141c361961ec93a8badf77c8c3e8e211d007790d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15104621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5375ab491f95263ab4fa61f6341671b44fe098dedad9e2733251435f357f253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b92336b8237063532fbbd11c6790107c0674504b981cb435151cb5c0acce6`  
		Last Modified: Wed, 13 Aug 2025 21:17:37 GMT  
		Size: 282.4 KB (282445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cee334a64b05f273c8a73099fed09e45496f8a6ae7aa262aa75cb87edc28e7`  
		Last Modified: Wed, 13 Aug 2025 21:17:37 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536eff87c11a3af92c89dcc27214c00484e04fd5721fbb85146ef4241bf94161`  
		Last Modified: Wed, 13 Aug 2025 21:17:41 GMT  
		Size: 11.0 MB (11021051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2aa9ab96aeae67fa47482bb58c437ee26440d79107ba3552032ed1de0d028f`  
		Last Modified: Wed, 13 Aug 2025 21:17:38 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:2b9eafe6659c59dc78d3523cbbcdabe4b79e6ccd81eced739a62bf5d4050868b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 KB (205854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e183706f1aa7b5e650573b9e53f37af05d9be8f6531a49e471e1f091482f8b`

```dockerfile
```

-	Layers:
	-	`sha256:410d251ede9b70cffdbc96217333262d4a139cdf93a8b6c462f6d15f1cec30f0`  
		Last Modified: Thu, 14 Aug 2025 00:56:34 GMT  
		Size: 185.0 KB (184968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e2a1336fdb028d73e7b69c38cedad5856b47bfb82da87dd5f89130037d0227`  
		Last Modified: Thu, 14 Aug 2025 00:56:35 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:cc3e1660788674da9f17cdde89370200f34216c6a780fbfd6155335c85e1db20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17144041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11cc363dd172136b6b012fcb29ebc87ff622e3e02d02c88d09887737d5264b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4debe2bbfe62895770300bb3d0e66618e6e5c3d866e6e821391941031d8df9a0`  
		Last Modified: Tue, 23 Sep 2025 18:04:59 GMT  
		Size: 283.3 KB (283321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a403d4844a0b0bb00cbff19c61558fc9a2c1afd9e2615c648678941e9e0ac8`  
		Last Modified: Tue, 23 Sep 2025 18:04:59 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629e2096d31920fcfe27b8631abf92bcf64d210c9ca679a90981c867354d72f`  
		Last Modified: Tue, 23 Sep 2025 18:05:01 GMT  
		Size: 13.4 MB (13358375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcedcd6cdafab6fc0745244d3a2a792d830fd3a0814429829fbc4e754815c2e2`  
		Last Modified: Tue, 23 Sep 2025 18:05:00 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:ef624d9ecbd88d3b8743f3b246360402d871e08ba5bff1b5843d25d994ee92d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d203b0f044f4451ee6d7f2746d074fdad1f238959de9b1ef7a45364ff455bdc3`

```dockerfile
```

-	Layers:
	-	`sha256:0a477e1df089016db495238556a083efae296e0148492ee7d62fe4fde26094a3`  
		Last Modified: Tue, 23 Sep 2025 18:56:35 GMT  
		Size: 20.8 KB (20810 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6a07c121add492ca643e484e44d8d6bf745ffe1a8b77c5535749428d089bb551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16526337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a28db8948a566dd0cd5e8b49e390da8988689908904d8b84d1734262291098`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ed5200bdffbc5bd7ef5eabc9bf558fd09aed5131b9c392dfd4e41264c15398`  
		Last Modified: Tue, 23 Sep 2025 18:07:40 GMT  
		Size: 282.5 KB (282505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d49f2b03bf3591b2da36930507263b23d317cbe72e48046bf968866db9eca`  
		Last Modified: Tue, 23 Sep 2025 18:07:39 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87facd0004c34139596a7d03b76f7e0b013666dce942785a9e2fe2eaf7c252a`  
		Last Modified: Tue, 23 Sep 2025 18:07:45 GMT  
		Size: 13.0 MB (13023359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdff7b8a29c799f4e2a5eb8700ad2c60990306e94a44c6db5fa035bdb33e4a3`  
		Last Modified: Tue, 23 Sep 2025 18:07:40 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:7e1a574ed11057aed6021faa807e0dc0844a119111a0e0c9c46229adae9437f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 KB (206061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9375717159e9f6ac69e6113aac787e3f8958453f8a213dbc0c101281be9c8e`

```dockerfile
```

-	Layers:
	-	`sha256:b03feb85e89959f45e46fa8f0e14a5a5171a60160ed2230a3aa3639566288c6f`  
		Last Modified: Tue, 23 Sep 2025 18:56:38 GMT  
		Size: 185.0 KB (185036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a79979c7a250faba9956628249106476411fb1a33ef6fb8c409e641bebf0271`  
		Last Modified: Tue, 23 Sep 2025 18:56:39 GMT  
		Size: 21.0 KB (21025 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:dc5d3f50e4e517a47b45e59aae28755d956827db51f8d209c51e9cabe2873676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18277077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d01305a2bf551d460e9280234331ac3b14d6cae8b1478f4763c26be5cf06a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce22cfc15249239295b12180fcacf3df92c2534995236434ab14ac544651ed69`  
		Last Modified: Tue, 23 Sep 2025 18:08:15 GMT  
		Size: 284.7 KB (284700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70983361f278160afd23a842b8c23a6b51f03edaf0b559643c931e26dcff1299`  
		Last Modified: Tue, 23 Sep 2025 18:08:13 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9972d6887a56e9ce0b59aea0649c777f69d823152bbdc641de548d90968072f5`  
		Last Modified: Tue, 23 Sep 2025 18:08:16 GMT  
		Size: 13.9 MB (13860187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982fe229e4a9a1cbafb978eb54eba614c931601af9478f92f2e2cfdcbfd93a92`  
		Last Modified: Tue, 23 Sep 2025 18:08:14 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:c4b7a3a959b0512ebbe1974ec03b17531e5db503ab35bf9448d65b9cdf06e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 KB (206141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bf0ef6f1d05c60ba432257ff3cff203f9a623b4c1a5732e1993297895f1826`

```dockerfile
```

-	Layers:
	-	`sha256:d50ffe48d87a7aef3bd9cad8f29c23a30aca6bc16b5663b2c7f217acc6d8700a`  
		Last Modified: Tue, 23 Sep 2025 18:56:43 GMT  
		Size: 185.1 KB (185072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7532673cf441325c3fee50ad5492f71fa54ff19bb2df3ed6e39f3ad7de54d84d`  
		Last Modified: Tue, 23 Sep 2025 18:56:43 GMT  
		Size: 21.1 KB (21069 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; 386

```console
$ docker pull haproxy@sha256:41a423057ea74a290021f9c9d492e7788c91772f86023b2b136c63cc8570a5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14651832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89cbd430204f48a4601933e7d55b44f50859e8df14d499156495d6c163c306e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4368823f3a8c77d0c4cf0f74098da17663c06aa067905c8c97ee4ab7d0818a`  
		Last Modified: Wed, 13 Aug 2025 21:17:32 GMT  
		Size: 282.9 KB (282926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879a4cbff3e7a2796f48703a34a03538e09823a5a77ccad072a1d2bcddbadfd8`  
		Last Modified: Wed, 13 Aug 2025 21:17:32 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee194224c2db474de235e6a181c30588e75937a222d88ab826408f2b7b2644`  
		Last Modified: Wed, 13 Aug 2025 21:17:33 GMT  
		Size: 10.8 MB (10752464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13027646c24c24140138e6d57c2b52625d4f41fe6001f6768be4f4337a2c3179`  
		Last Modified: Wed, 13 Aug 2025 21:17:32 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:bd6b449c985d43d11d88e90d1386319f2376999e6acc73787e035118b0d3e1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 KB (205754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942a9d8c300e78858ac56385346e62a0b6aeca750c3132df09fd2ec2cf73f7aa`

```dockerfile
```

-	Layers:
	-	`sha256:dcb5dd903c36a8c756b5e1d275a161c328a1c12a61c03af543464b47893541e3`  
		Last Modified: Thu, 14 Aug 2025 00:56:48 GMT  
		Size: 184.9 KB (184923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c7fc548ab6b777ca7cb6de5e232b3606afc8bf519b50c79b83c9f5db67e25f`  
		Last Modified: Thu, 14 Aug 2025 00:56:49 GMT  
		Size: 20.8 KB (20831 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c2ade33cfda22a524bc1c5e102c00ef0a0b8a0468c47dfff24cb3f1cd41e5cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15655695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9517d76f1f483f93d85341855d9958dd8176f9eb6a202ee328e2a940c7de94d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198609f1c9e1057cf961a3bf3e60a68ca3f2d603b5f6904f13a6b82ed4d04f54`  
		Last Modified: Mon, 28 Jul 2025 20:36:23 GMT  
		Size: 285.1 KB (285112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3773df3be668e325bd4ddc5ee1408e7a4e8e5d286788c48ca827a5c3e8ff47c7`  
		Last Modified: Mon, 28 Jul 2025 20:36:23 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bcfaa3bd41d48fd45ab5ce4cc3e26713cacda51ca7661819745e00698363d0`  
		Last Modified: Thu, 14 Aug 2025 02:28:48 GMT  
		Size: 11.6 MB (11642028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec1cbb19fec62a273a6390b63b5ac48ac098bafa9a8529e3ab5aea30c1665cb`  
		Last Modified: Thu, 14 Aug 2025 02:28:47 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:db751495f76b08e6edaffd9839ad11d375203189bb104c6101d41ad69420b3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 KB (204034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39c7027563b17e84860774365321ea40e28ef5d0f4cb8f82d563dd802aa90e6`

```dockerfile
```

-	Layers:
	-	`sha256:1d9df802fac9e4b342b5bb6dcad4d527e1449770cb3d78c4f9324e675705bfdc`  
		Last Modified: Thu, 14 Aug 2025 03:56:41 GMT  
		Size: 183.1 KB (183075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d76420ecfc406839e9f10e64bd0489ea12abe5baabca0b88ded823ddf17148`  
		Last Modified: Thu, 14 Aug 2025 03:56:42 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; riscv64

```console
$ docker pull haproxy@sha256:cf4c9a6896d05294da67446051ddde34439a5e17a2424e3f9696d45bb2470276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14509880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b9e48b7a95271da1a429651083b68f90aa8e11fcf91bdc6f8d0de01a1bd12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f539fdb6ecca3bb86772adb6681f27870137dd17fd868b7956cf9099de5d62`  
		Last Modified: Mon, 28 Jul 2025 21:48:25 GMT  
		Size: 282.8 KB (282786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a022e1c3cde2a4a36288ccaa6c7eb514886b1e2ec18f0d548f1d1b6afe3ec53`  
		Last Modified: Mon, 28 Jul 2025 21:48:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f49a5ff820c816069df309b289d8e2df9984dc34e7567dd5d180919760895a`  
		Last Modified: Fri, 15 Aug 2025 09:09:30 GMT  
		Size: 10.7 MB (10712847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88792fc0a93eb502c09b88d63220edf74ff0b5c2a2edc4f3f002304393721265`  
		Last Modified: Fri, 15 Aug 2025 09:09:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:87e07f9477e17b2ed4c58cdf5e21fa645a67c95fc546da9e55a4841689565db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 KB (204030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a800813165acd77813e7934dc8e67d84411ecac29dd8d203e711316a5ff068b`

```dockerfile
```

-	Layers:
	-	`sha256:383db0aaf6ba2a8d0d56137db0e4e08542189b0f55990aafeb03a4e45c0b59a7`  
		Last Modified: Fri, 15 Aug 2025 12:56:30 GMT  
		Size: 183.1 KB (183071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ee3e8a7f80f29580459d7268aafd752f59e8c99ef732dcefeeebddc61b0bd3`  
		Last Modified: Fri, 15 Aug 2025 12:56:31 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; s390x

```console
$ docker pull haproxy@sha256:e47d83012f07c3a4846d234665898d06cb25ed5fe8df1696f182b9510829aec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15314991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13038ad89b98656eb3ccfce5b0193b346808e8b207151349ee696ed35ccb2cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9fbf119f66e390d7f97f244c420c7dc9095146514aa479c52d068f7cea048b`  
		Last Modified: Mon, 28 Jul 2025 20:37:34 GMT  
		Size: 283.5 KB (283469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9652edab46aee98a65877331f0bbb2a343ca530f2fbcbf9f5fbcc34af2cc7998`  
		Last Modified: Mon, 28 Jul 2025 20:37:33 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0e756554dd8831ce60b6fb495541ce1671a0133e48fa6e70870c6861c8e15c`  
		Last Modified: Thu, 14 Aug 2025 02:53:45 GMT  
		Size: 11.4 MB (11385113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49cf9d1c9e7576bde7a5c531f7c437f2e5ef2a052ae61534c12c5497cdbf4da`  
		Last Modified: Thu, 14 Aug 2025 02:53:44 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:d13ee9aa6e5017dd40f4634ec4585a47ddc40085f0aca46f5c498d7f9e00b7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 KB (203901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd52785b3039684e069a79ea806164d1c287fa467e3e5d5c8cb0dde865432be`

```dockerfile
```

-	Layers:
	-	`sha256:25127c45659f239b6e4839c1cd37bc63acba176f61bd0fd78a0e336ed84d93fb`  
		Last Modified: Thu, 14 Aug 2025 03:56:47 GMT  
		Size: 183.0 KB (183017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9324906ed028200d145510c0fe8a080ea86f78f211d965d16a1f8c803fb62ef`  
		Last Modified: Thu, 14 Aug 2025 03:56:47 GMT  
		Size: 20.9 KB (20884 bytes)  
		MIME: application/vnd.in-toto+json
