## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:93ad638f0dc5ad6c0c2a8115cef152cde43cb1f9f43dd881224d41fea3dd17c1
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
$ docker pull haproxy@sha256:fa85e1539b943d6c5b2a076ef287f6d74d5459d1ce2b7b4b677cedd87fdc77cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14928215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8759aa829c1dcadcfd96045f772a0ffb17dd0b7b01965d30d0472ceaade68e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ca8e4870c8f9eb815092ef3ec03ca13ff745195f016759eef9bdeba9a8bde`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 294.9 KB (294916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2e98e2ca43750daa012a2895316fdcdde6335776a41edbc704ba898d645c7`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2450298bdfb8e091f3f1f964b5094a23b61b485dbae6f86c243461579e54731e`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 11.0 MB (10989608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2ffe7adf5a04444803315eb95719c867b376c71ccd1e6cc01e0d0d9de2f3c`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:16ebff3945063d17ae94abec9f45f256db96a01e6258f65133d7d873bc6f2f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 KB (209807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0ddff18e4a44492882b62075cd25c1bf2296620f0f6bcc614daae5db88239e`

```dockerfile
```

-	Layers:
	-	`sha256:afd3e303e3f7ff5f1a1a303ade8828c105a1f3d198ecf551814ac340c2842539`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 188.7 KB (188733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302de5687b994a382ea1e8f82e667a3aed18d20f15c2cc93eed8cc11b817fa4f`  
		Last Modified: Wed, 28 May 2025 17:25:21 GMT  
		Size: 21.1 KB (21074 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:026f05219cd5e99a33e9f042ffd37c0a83cf1cd5e989b16b5befeae9cd4fdb96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14755537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fd3db26a0eb5cbd48bf5558c8975026d567d2e22f306508df96e34655fddaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1687a14ad260fb4fc6db1f0c86d25e09804f3d50a74985686018c2f56f7dd8e7`  
		Last Modified: Fri, 14 Feb 2025 19:48:24 GMT  
		Size: 296.2 KB (296243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16df665dca9b0f015404e24fbb55fbf1e84f5db281481cb4a0039b142b0104f1`  
		Last Modified: Fri, 14 Feb 2025 19:48:24 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b2ddaf99c5256928c4c8cfed0799abe93d27ea1f45bc9c57c219e42da980a3`  
		Last Modified: Wed, 28 May 2025 17:36:32 GMT  
		Size: 11.1 MB (11093120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e017e16c353682140d1c313a7562c285eaaeb779d4e0fe0846faea6f9ce9006`  
		Last Modified: Wed, 28 May 2025 17:36:32 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:af61cb05b74811dac3c2d1c1c50cfa2afa3eab66dcd388909166ef6af1cfa2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4176c937d65dcc15922ac75fecb523f294dfa7360948e7f90f5840e083bf428f`

```dockerfile
```

-	Layers:
	-	`sha256:5ccfbc6ac3d6e2dfd9261a5392498f11e677f4c27455a3e6a35edcae3740d4d0`  
		Last Modified: Wed, 28 May 2025 17:36:32 GMT  
		Size: 21.0 KB (20993 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:faa94a4ab889ee9ec7c31bb6cdc5c784ae5a8e147e080eee537e5fa9c2df809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14312680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2692744ccba8872bb33de4791480fad1fcb4a9a33e5014d7aabf6eac62c95a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510a4ca166402494f4446a67668b9451a59e7fc3a52d6f75a82f0f5e8765808f`  
		Last Modified: Fri, 14 Feb 2025 19:31:33 GMT  
		Size: 295.2 KB (295186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997b631db78d26a36cacdaec7a75f0bc011ca691253882b64e0cae631d3e84d7`  
		Last Modified: Fri, 14 Feb 2025 19:31:33 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8389820ca2ed99ac989ee98cd2eb13608510448a56fc5b01f0c8c9c330f40`  
		Last Modified: Wed, 28 May 2025 17:29:38 GMT  
		Size: 10.9 MB (10917935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ee321ef492e9fe18de45774dd50da6c06cbfd93961a35753509970fce8139`  
		Last Modified: Wed, 28 May 2025 17:29:38 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d24aac9de107bf0b579cb8bd9cd4a7a209254d74c28de0c96338e5068a2376f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 KB (210008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f90364c8a1ac0fcc07717a79c0e047ec7a0d237e8e41088638ce2c16ab6361`

```dockerfile
```

-	Layers:
	-	`sha256:7c727b52b14f2341eb27443eadc025b34a0b625179a9e33a4cff69d02092d2bd`  
		Last Modified: Wed, 28 May 2025 17:29:37 GMT  
		Size: 188.8 KB (188801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96a5f87b8a2b1dca066a7dc13e19ac95a5a0cbd6b40f84176d27969ecbde3a4f`  
		Last Modified: Wed, 28 May 2025 17:29:37 GMT  
		Size: 21.2 KB (21207 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:87fedb1efc7c95c3a09de8d5c05662e2136b9d68a3249f622d43f8852a7e713f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15224612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ccd49d404958cb5a1f717d0ca020e3a36ce58ed421ee9ee30154e9ebd5151a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e406e68f8d4926d5fc6c4ecf387d92e3d995813f31e47e1b1c8be987a24e6a6`  
		Last Modified: Wed, 28 May 2025 17:25:29 GMT  
		Size: 297.9 KB (297877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a9164ea002e2a4cc183a9018e7e8b11c365cef9fcc42522637024d416cd085`  
		Last Modified: Wed, 28 May 2025 17:25:28 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7949348cf0d4ebc5d0e05336d6f97f3a23c8e4a29f7020ee0da5a8e9a875b067`  
		Last Modified: Wed, 28 May 2025 17:27:05 GMT  
		Size: 10.9 MB (10932259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63eee67964962263ac74d3c4df047c58bf1258f7d50d9c90c30a78cc02b3bfde`  
		Last Modified: Wed, 28 May 2025 17:27:05 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3dc4b625dd699314fd3e7add13f6d7da2e1d8ff0cb00ea515528bcbcad84fb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 KB (210092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa400b709fc19b0c22c9b67cef539909d9bbae56d25fbc33df17ba6fb7a3543`

```dockerfile
```

-	Layers:
	-	`sha256:74c143fca3b2b861c1d1f927d526b3ea1946868ec7faa83232c9bac880207572`  
		Last Modified: Wed, 28 May 2025 17:27:05 GMT  
		Size: 188.8 KB (188837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068686631ec73fe5324050c16aeb30259a2afc219863bc2aea5562b35d4d7b6a`  
		Last Modified: Wed, 28 May 2025 17:27:05 GMT  
		Size: 21.3 KB (21255 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:6b1581f5426e16d6cee613377361a84b187d299fa238062cda5acad6e55abc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14482915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2f41c6983b15ad63039b1710540caa957c9d36dc79dab8d3fda9b1dcfb318c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11dd13533bce934cf7abef42c562a9c11b40922361910702b4d084e659204d`  
		Last Modified: Wed, 28 May 2025 17:25:31 GMT  
		Size: 295.6 KB (295599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7075be5b51e62a168d5db98631b6b779c92bab6d91a5241e65f16fd304fe3f6d`  
		Last Modified: Wed, 28 May 2025 17:25:30 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca1b3de32b86e3c569f44410673ef1e204018fbcd055c7b5303eba66f21d2c0`  
		Last Modified: Wed, 28 May 2025 17:25:31 GMT  
		Size: 10.7 MB (10722250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5f016fe17ea3bcea05b41a4cc04b843d47f0e3baa265c3de3ef1d124fa18`  
		Last Modified: Wed, 28 May 2025 17:25:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:9da031b5fa45922cffcadc331a279753e6ef4aaed1400c66f10794326e46c80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 KB (209706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55276c4f1af8ce42dea36d1d78689f38926c73e8204fe23b0c6e1742f175bcb`

```dockerfile
```

-	Layers:
	-	`sha256:5df44d08755bf40437955c527abdee281013f6625f0e45d0486ae08552b89586`  
		Last Modified: Wed, 28 May 2025 17:25:30 GMT  
		Size: 188.7 KB (188688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ab5b7bb3982e6189c4e1e343096c46f009a52bb1ecf3ed5e9853efeca6df60`  
		Last Modified: Wed, 28 May 2025 17:25:30 GMT  
		Size: 21.0 KB (21018 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2b625140a852a31622469f0d737a0b597ed18ae60c6f64bc2fbfa1217321883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5086cc0be4d60dbd95e28c94326371055c93c000bc2146177a74cf9f476873c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c30a62047fc2b8443ff64d3b441f83d51d0b9c09a284031b622c5091c4bc0e`  
		Last Modified: Fri, 11 Apr 2025 18:46:43 GMT  
		Size: 298.3 KB (298275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fdd75ae6d5c366d14f5d78c37e4519e7806aa1bd354a37c6eca62f90cd5d97`  
		Last Modified: Fri, 11 Apr 2025 18:46:43 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adf5b8b428dc617346e16b6946eb2af1ebcf72d5e28b5006683961694b944a`  
		Last Modified: Wed, 28 May 2025 17:27:11 GMT  
		Size: 11.6 MB (11614065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4643828fcc2fe84f08b038ab69eae638d99b2ff126341195f49f421f97696cad`  
		Last Modified: Wed, 28 May 2025 17:27:10 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:f1de3815206c9317f36b3619fa1ad3c855f0e728880253b67074744a815f1efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 KB (207986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517cf63d3d2c978d281f59a621c35915dac78b63e48907b6a2e615072b035a82`

```dockerfile
```

-	Layers:
	-	`sha256:4fb696d2868ee12352b5bba32a7d605c2dd64b9fbeea2367358dc81405056a09`  
		Last Modified: Wed, 28 May 2025 17:27:10 GMT  
		Size: 186.8 KB (186840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c6b3e35b7168517d8a0c4fcfb232dfd1e712990acbe328500510df787cf7f3`  
		Last Modified: Wed, 28 May 2025 17:27:10 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:0dcceb11ba68cbb1f43a1a005a2069cba028cc1e89dc48f1bdefebaff1898f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14335817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4f9e8e6763b45af4f10e526a804b87f188e2f29a1e7d9634b6f6bea5c45678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22171ce9b4c4f3b6879cfc2f72d965a79cdb9074a5b06c77c217e1981dae2e2d`  
		Last Modified: Fri, 14 Feb 2025 20:54:59 GMT  
		Size: 295.4 KB (295351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65efa07118c7ad2eae25639ed9a9d25b87ce01b795b0b74cc8fda0267ef465f4`  
		Last Modified: Fri, 14 Feb 2025 20:54:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522668e45daff498e5dfea5c7ece6e1819e21d28a09abcb76770a32a74b79576`  
		Last Modified: Wed, 28 May 2025 17:50:00 GMT  
		Size: 10.7 MB (10687585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84d349b3868b0f96a6c12011036c0bc2107dfe7bd5acf7de87dd5f511de2e7`  
		Last Modified: Wed, 28 May 2025 17:49:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:4b01f36b5fc44a48ebe721e13df8eccf3e9c90f8a374fd66e848f7543c3a4121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 KB (207982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61099df20566de808e0d1d5439a6128a499715a9b4824f69f1c7873e366e7a81`

```dockerfile
```

-	Layers:
	-	`sha256:64fd82b6a2992b86bd0bbbfe32f81121c09e7367aba1f22936afb45bd4bc416b`  
		Last Modified: Wed, 28 May 2025 17:49:58 GMT  
		Size: 186.8 KB (186836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852e60fd8365627dad6131cf553ca636271a66bc9e4f84019b43e2cf211fdb64`  
		Last Modified: Wed, 28 May 2025 17:49:58 GMT  
		Size: 21.1 KB (21146 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:f41a47a2c2c84f5dfa54200cda19bd44b68626fe3a4e0ac0960a64269b52e197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15120089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4768029d75ab4082ae2091681bd4a70b1998d540c840e2d222e39bf5a18b29b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_VERSION=3.2.0
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Wed, 28 May 2025 17:01:37 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Wed, 28 May 2025 17:01:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 28 May 2025 17:01:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 28 May 2025 17:01:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 May 2025 17:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 May 2025 17:01:37 GMT
USER haproxy
# Wed, 28 May 2025 17:01:37 GMT
WORKDIR /var/lib/haproxy
# Wed, 28 May 2025 17:01:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5045c7951f8c67bc5636438827f0a120b4cad052fb9236b9f7050c9481bc39ad`  
		Last Modified: Fri, 11 Apr 2025 19:07:51 GMT  
		Size: 296.2 KB (296186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b649b43b017876233130d5eff5a0a44268a197d1a56fb67210404df1baed5d8b`  
		Last Modified: Fri, 11 Apr 2025 19:07:51 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e56b388189e1d55459a4b5c927ea2722205a57399d4e0c583cb137a5238c17d`  
		Last Modified: Wed, 28 May 2025 17:29:01 GMT  
		Size: 11.4 MB (11354889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3947eb1efc508490b5387c4c5cf2ff6d8bea85007320d836312369d23335839f`  
		Last Modified: Wed, 28 May 2025 17:29:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:79095895f8956a9c7753df6fa9f694ea5206737f4b4f37e3cf79f94d87286acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 KB (207856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b23f0c84eb6eb6eea42b64adf5d173d3773d5bb87035b2469b3bfb60fb3a19`

```dockerfile
```

-	Layers:
	-	`sha256:0dcfc4660d715c3e7a8b39bfa936dc642309503ffc23db912f1f864f8479e409`  
		Last Modified: Wed, 28 May 2025 17:29:01 GMT  
		Size: 186.8 KB (186782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3d949b35593b6ee8b7514bc4da7515e35573a0f1a8caa2dba46cc18a3c9abb`  
		Last Modified: Wed, 28 May 2025 17:29:01 GMT  
		Size: 21.1 KB (21074 bytes)  
		MIME: application/vnd.in-toto+json
