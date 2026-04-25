## `haproxy:alpine3.23`

```console
$ docker pull haproxy@sha256:2afa53c856e4e9fcc7dfb35b807fcb189896d7e62b38d363f9bedea92bce7f9a
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

### `haproxy:alpine3.23` - linux; amd64

```console
$ docker pull haproxy@sha256:07b8c32b0eece8b79bcabf1c939068cd1b460b6b1a69834c154c76d9eca7114b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19301268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d16c2477c87d1a89cecd064558bd14b825e19f7f7131fd44d6192e5b3cf6c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 18:12:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 18:12:47 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:13:29 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:13:29 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:13:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:13:29 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:13:29 GMT
USER haproxy
# Fri, 24 Apr 2026 18:13:29 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a01b0d8aea1e5903fabf67bade6170b92a3af1844f4f4589a443ec0df7769d7`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 824.7 KB (824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31937d7dff12127e8fad44f9b8d76735048d3990538b42f9d436986336b455a8`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8be617eb5d77baf0590f03cee55b08cad1a7c7aa794ddbb0d01a0d13dc7b77`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 14.6 MB (14610924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343e315f5e7fbbfafa5c1209824a0e67543d68d36140ffc87c6c6755c7f3e3df`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:8e8b5bd9ee8ab96436523a8ec91d47dabeff517fdad3b7e663c0aba228a97d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 KB (246519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2101dacc6cd1d7bd38b8fdfdb9d0c896e31f57a69f04b3323833ce2622646598`

```dockerfile
```

-	Layers:
	-	`sha256:c07e9a24f60d9d1d25bb93cc30e6539e93c70ecff50c9604b9c29fc60962b778`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 225.4 KB (225351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079bbfbe0cba5bd93508820cc717cecbaac4b69f21d8ddf34de08d85108e6a38`  
		Last Modified: Fri, 24 Apr 2026 18:13:35 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:ae8855337d4519d626d0f0d86df4f3028c45350f3e057528a0abdcbf6a0dc0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19229920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de7764d359b48c4612dbae1958da178708f37f3142f2200cf06db724ab2a224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 17:57:27 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 17:57:27 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:58:12 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:58:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:58:12 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:58:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:58:12 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:58:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:58:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:58:12 GMT
USER haproxy
# Fri, 24 Apr 2026 17:58:12 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:58:12 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acec0e5daeb482e4a74c0e286fe684bcc07541266e678e80db6e074224820ae`  
		Last Modified: Fri, 24 Apr 2026 17:58:17 GMT  
		Size: 817.8 KB (817755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570addcd044f54ca616f8f0e9b631f6065ba819379ebbc8c831378e11c84ba1e`  
		Last Modified: Fri, 24 Apr 2026 17:58:17 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db3d84a7fa5a954e81acffe558d7b295a153d127cf59ccd5de4210bffaeeec`  
		Last Modified: Fri, 24 Apr 2026 17:58:18 GMT  
		Size: 14.8 MB (14838866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa187a21413284c38b9aca74856966f166483829ce5c58db30ad93aef09533`  
		Last Modified: Fri, 24 Apr 2026 17:58:17 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:41915a2644cbc4ab6a3d9e727f9f6f09035d889902fbe5a72df99a0c94737581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dbb22c87b271cda47ad69fb0f8778b5b0e299dc64e90cf3436e4eba358fa84`

```dockerfile
```

-	Layers:
	-	`sha256:b018846daf57db5a727d7a6515751caddf4957bad19b30403b546c3c6cc25a00`  
		Last Modified: Fri, 24 Apr 2026 17:58:17 GMT  
		Size: 21.1 KB (21076 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:f3e7e4e55a426e0c1e6afc6f2bc5969cf43f7c551674682f3fee6d265ba63b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18738397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595935be43ef1c84343460bf6eff6c940d4303a104eba9552c1de6679217fab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 17:56:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 17:56:57 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:57:42 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:57:42 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:57:42 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:57:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:57:42 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:57:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:57:42 GMT
USER haproxy
# Fri, 24 Apr 2026 17:57:42 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:57:42 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b90688c401c26dde9e1127c741da0f109c53417867b788ab3f59625bba39b3c`  
		Last Modified: Fri, 24 Apr 2026 17:57:49 GMT  
		Size: 773.5 KB (773526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbe47bb4077ec7fdd53e09e846d1d89690f50fff7e849120af91c1a82bfc13b`  
		Last Modified: Fri, 24 Apr 2026 17:57:49 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f689a26da73fe81138a2856af0c53983428a24a9103925be2839626b26e9391`  
		Last Modified: Fri, 24 Apr 2026 17:57:50 GMT  
		Size: 14.7 MB (14680312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36be0686b1b849d1d45b7a2c6bc3629e533430ec091d110774a9e3ee54642949`  
		Last Modified: Fri, 24 Apr 2026 17:57:49 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:f751b6671f3eb64f8ab9d0ecc3a2ee07ecda01e34a61317c9952c9e494d2ec9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (246044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe276fd17a01fb69138ae82135187353f392529f86e8741d42256e7691204ce`

```dockerfile
```

-	Layers:
	-	`sha256:e59729d2b838577ddefb02716b83d7f50fad2a72b4907da059a6d1f8d6c0db3f`  
		Last Modified: Fri, 24 Apr 2026 17:57:49 GMT  
		Size: 224.8 KB (224753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e838da028e0a8fcafef4259971437cc45421a7412f8d1b52378208bc98709a4d`  
		Last Modified: Fri, 24 Apr 2026 17:57:49 GMT  
		Size: 21.3 KB (21291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:bf605ac98ea7bdb63ffdb6940dddee78d44a64b591a9e198bc1e48e2cfa0d83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19408583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e995c46d78c7a129c9dc0d13bfe3d3569cc45bdc0c30282cc30885d9c9d4189f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 17:56:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 17:56:01 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 17:56:41 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 17:56:41 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 17:56:41 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 17:56:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 17:56:41 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 17:56:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 17:56:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 17:56:41 GMT
USER haproxy
# Fri, 24 Apr 2026 17:56:41 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 17:56:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f4e228393275916c7eec3a6fe30d49e60c829cadf4ee454bc87fc3c9f10afe`  
		Last Modified: Fri, 24 Apr 2026 17:56:48 GMT  
		Size: 838.3 KB (838273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c59542560c6cd750aa6350fd3f3fb9a728cea87278808aa6bb7dfe8b45e89f`  
		Last Modified: Fri, 24 Apr 2026 17:56:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1aab5eba1bf2012adcc057ad9131e5e7940def63a4651b846219d348dbcda9`  
		Last Modified: Fri, 24 Apr 2026 17:56:48 GMT  
		Size: 14.4 MB (14369005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f511ff4de29cd06d589890113539e9c19e44732de4cee1b70a6917710efd4d5`  
		Last Modified: Fri, 24 Apr 2026 17:56:48 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:d0ef4a967786fae8e288549a3d40a9018194351742469ecde21422bba8596ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0234a887c32580697781aefe06798401d2575b7002bc556ec23aac9677c28927`

```dockerfile
```

-	Layers:
	-	`sha256:385039ca75f6c4102f79ea5f24077fca13dc25d63bd5bcf786df86909722a287`  
		Last Modified: Fri, 24 Apr 2026 17:56:47 GMT  
		Size: 224.8 KB (224781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c90d45f618b0fa8b79a61798182be02589cbf11ad3bce3edef544da2c1a7fb9`  
		Last Modified: Fri, 24 Apr 2026 17:56:48 GMT  
		Size: 21.3 KB (21327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; 386

```console
$ docker pull haproxy@sha256:e428eafe6840b1685b9fcf747137c34a7ae2fee08c673b161a56d9ac51d11db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18922829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49a3354e5ffcb5da427e71c476cd3d035638de42434357865b12ab8ed9bc040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 20:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 20:20:01 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 20:20:46 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 20:20:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 20:20:46 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 20:20:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 20:20:46 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 20:20:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 20:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 20:20:46 GMT
USER haproxy
# Fri, 24 Apr 2026 20:20:46 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 20:20:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a1f43a0a2a7caf220e9ad7107848c15d8289e77f67ed79cd200188956149ea`  
		Last Modified: Fri, 24 Apr 2026 20:20:53 GMT  
		Size: 830.5 KB (830550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d650c1a58a1f8bd53d954b593084e4d3f3b9b1cda8f34f05c54d19825881369c`  
		Last Modified: Fri, 24 Apr 2026 20:20:52 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699eb3a270db75b2eb0ef04d5c336975ee8ad9f7ea10066075ff38b7de6aab3e`  
		Last Modified: Fri, 24 Apr 2026 20:20:53 GMT  
		Size: 14.4 MB (14400398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f8b624fbafae0415a019331cedc60e1a72edba62b9671591b48d267d54b41`  
		Last Modified: Fri, 24 Apr 2026 20:20:53 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:592751ccdf9a735f08cee2c7258611394993da8c485b18e49f6d8fcd158f3f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 KB (246439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc389e94c34bee3db379a9102ac0346e93718e7a701367f5798cde4a141f7099`

```dockerfile
```

-	Layers:
	-	`sha256:63c54275d74cf8f1ddd84f5355d221639bbdce5b23a3041573108568b25c2f98`  
		Last Modified: Fri, 24 Apr 2026 20:20:53 GMT  
		Size: 225.3 KB (225316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f304ebbf22ddd04837b1ba0e797a309857018224ef653bde05d72acc1201d5`  
		Last Modified: Fri, 24 Apr 2026 20:20:52 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; ppc64le

```console
$ docker pull haproxy@sha256:70da3ca9663a9407faaa3d2cb02819a781f852804e50cd3f565cb21ea2813678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20096250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1caa1cb231da2f7f7555037970f105b3ffd5b6433973a8789e886055d658a284`
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
# Fri, 24 Apr 2026 18:24:00 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:24:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:24:00 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:24:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:24:00 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:24:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:24:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:24:01 GMT
USER haproxy
# Fri, 24 Apr 2026 18:24:02 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:24:02 GMT
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
	-	`sha256:b8c9e97ff7364878ca68ad07572f7023ff82be8880b157b5d871cda5f13e4d7c`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 15.4 MB (15402081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116689da09c62cf77e7d72d326211a4fb7c3ef165a5e18cf43a0cdbe3950bdb`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:24cd01ca17fece99a467375bebf39e6c1e9b2070969f7d6857c7b5a991589d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (245975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba4469c4527cc70dbde78a7381a9fb46ec9c306d4f8554ab3ba47c250e6bd48`

```dockerfile
```

-	Layers:
	-	`sha256:28cb26cc6f6fdc832382b680cced43cc364366cc394927560892581b22c71b05`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 224.7 KB (224746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d8fb7cb8d396271af43d79b757e0ffb56f542f2888924c2bc9059db0d8d91b`  
		Last Modified: Fri, 24 Apr 2026 18:24:17 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; riscv64

```console
$ docker pull haproxy@sha256:7455f7af8d2f2da056fd2417d588a6acb26050e3470bf723022820499b3378b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20203368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaae7408119e86d198c154823fc6ed3a31075dad106536a20f57f4409fcaa81`
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
# Fri, 24 Apr 2026 20:36:24 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 20:36:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 20:36:24 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 20:36:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 20:36:24 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 20:36:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 20:36:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 20:36:25 GMT
USER haproxy
# Fri, 24 Apr 2026 20:36:25 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 20:36:25 GMT
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
	-	`sha256:a7584bbfc97b1376baa535a8f742c7989a218501f734e97fa38742faffcfc6f6`  
		Last Modified: Fri, 24 Apr 2026 20:37:15 GMT  
		Size: 15.8 MB (15769027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66f78225b12abf736d98a7ce8b8c2c52dce3f882098c23a88c5ce19d713e113`  
		Last Modified: Fri, 24 Apr 2026 20:37:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:dbf3a26d67aacf04884722a0e2ec4063c7a8c6a135f639a7966c15fb1c8d8302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (245970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c698aeb21c427f449d107449484ce33d7cf3709c0167350fc401240a21a5e48`

```dockerfile
```

-	Layers:
	-	`sha256:cd789ffb00da245f13dae5e633dc137c8f4baac681e3c78a87349773283072f6`  
		Last Modified: Fri, 24 Apr 2026 20:37:13 GMT  
		Size: 224.7 KB (224742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1735fe17eafab1609c39572476c3e08ff9efe38e501484acddaaa227c10819db`  
		Last Modified: Fri, 24 Apr 2026 20:37:13 GMT  
		Size: 21.2 KB (21228 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; s390x

```console
$ docker pull haproxy@sha256:2cee8746b63dfdb0cdd412c8c9da9a4073929c0cb954359ce59dac425a965dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19629607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5b34e4d5515cef5837f8544e24aa4c3fe02b3a856681bfb289e4052893b7e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2026 18:02:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Fri, 24 Apr 2026 18:02:59 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 24 Apr 2026 18:05:32 GMT
ENV HAPROXY_VERSION=3.3.7
# Fri, 24 Apr 2026 18:05:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.7.tar.gz
# Fri, 24 Apr 2026 18:05:32 GMT
ENV HAPROXY_SHA256=c243e17281f79fa81a321e0b846ce67897315570de1b8ccff6ca6b7a312683fc
# Fri, 24 Apr 2026 18:05:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Fri, 24 Apr 2026 18:05:32 GMT
STOPSIGNAL SIGUSR1
# Fri, 24 Apr 2026 18:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 24 Apr 2026 18:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2026 18:05:36 GMT
USER haproxy
# Fri, 24 Apr 2026 18:05:40 GMT
WORKDIR /var/lib/haproxy
# Fri, 24 Apr 2026 18:05:40 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ef09f10d4d044d81a7e1e3fca12d9af162c5a49340db6c4c441cf7ae513cb4`  
		Last Modified: Fri, 24 Apr 2026 18:06:40 GMT  
		Size: 887.1 KB (887148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b195b5aea35d76b117b50ff278924460a7bcac7c3e4d5604d6271d17c6c045f`  
		Last Modified: Fri, 24 Apr 2026 18:06:37 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66251c033ce4046cd48d096355bf52a35e1cff7e51b4084f3f6daf843b809485`  
		Last Modified: Fri, 24 Apr 2026 18:06:46 GMT  
		Size: 15.0 MB (15014482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fb9deb917e15e2ad501b3995280b97dee05fe928835703c38ffa4c695c14d6`  
		Last Modified: Fri, 24 Apr 2026 18:06:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:feb574a8b1a8c9ff0c1aa90d325db90887ebc48bbec216dd37d162e8786a1484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 KB (245869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065ccf9bd489b1e0eb6ce7428b0d9d4af986d1e4ea6c1b15b89555b0e9eb7243`

```dockerfile
```

-	Layers:
	-	`sha256:516e9d399d40727f0975a80b4d53c984d48481e50c82688ed22286f854ea15b8`  
		Last Modified: Fri, 24 Apr 2026 18:06:39 GMT  
		Size: 224.7 KB (224700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9851b3297a2e2217fb3616ffcf3b2ff6fe6921840f975a16af58e46e2b30ad`  
		Last Modified: Fri, 24 Apr 2026 18:06:37 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json
