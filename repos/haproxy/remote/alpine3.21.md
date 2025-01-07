## `haproxy:alpine3.21`

```console
$ docker pull haproxy@sha256:e0ce9df69e229c4f0f0ad4532ffc54e9b95ac3343d86d9bfb39e3900e7550880
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

### `haproxy:alpine3.21` - linux; amd64

```console
$ docker pull haproxy@sha256:226b11b70dbb664c98f279991924b86b2da9e5f8bcefd950457bceb23c06b20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14053296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1747baf7076541d581d9b2512c3242ed001a1e94d3f63744b0297805a8913950`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
	-	`sha256:2738e4809453579bf3cc91d08dc59b638f06bc1b8ce4098005f9949a77cd9ecf`  
		Last Modified: Tue, 07 Jan 2025 03:18:19 GMT  
		Size: 279.5 KB (279507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7faf05970d4ab8901227c30c6a5f8bd8203e37bdf64bcc5208fa5d265678f11`  
		Last Modified: Tue, 07 Jan 2025 03:18:19 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f0e68ede5f41ca9972ea5d33c60acf2788289e0e4d81f585a89e10ece31997`  
		Last Modified: Tue, 07 Jan 2025 03:18:20 GMT  
		Size: 10.1 MB (10136121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb9a5c733791a69f54a331508d96583c74c81b36cdff916663b9ed30fc231f`  
		Last Modified: Tue, 07 Jan 2025 03:18:19 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:484e0bee2826e2d1a5c9e986a3966940f6014b91a5ce4a8bcf957e8c7db27268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae1df02912e6f224c9f4db1ab2705f0cc8f3257ce6085a0547a0f0cbc909779`

```dockerfile
```

-	Layers:
	-	`sha256:37cecdb5126c14640a92a4b571ecaaa5e4f4133ced4d85e4b52e3eeaa0885795`  
		Last Modified: Tue, 07 Jan 2025 03:18:19 GMT  
		Size: 180.5 KB (180455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960327c4e8f1857c1c67bff7315fb527398ee623283e9b647b539260409c1bc4`  
		Last Modified: Tue, 07 Jan 2025 03:18:19 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:b1c3c5ac4f9525f40bb9105b15c8acd475d9fc76e6ad30bebe2bd55f78e9aaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13804349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eb8e4521dc0c882a2ec8e1bd25024ac474b638d6e6c34e185acd37699a421f`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
	-	`sha256:da39bd56aed103bb31599df55b6d043590bd7c7a63e26de923f4ce5a76b9ffee`  
		Last Modified: Tue, 07 Jan 2025 03:51:14 GMT  
		Size: 10.2 MB (10161526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49236d088b642efdc0999fde94ef912d36487f0d8bd08c80bcd68d32015617a9`  
		Last Modified: Tue, 07 Jan 2025 03:51:14 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:16439fbe148757605425b891aa94f983214a6ecdd3c2ac7612e289470a8343a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929e8e50b4f77d5f58391470ae0a72789ff735ad60af12ae7287641c9c352253`

```dockerfile
```

-	Layers:
	-	`sha256:a7813cbae85328754200c5ffb74fa9baa1cd5d589c47ad8a73c70f87f2e978d2`  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5a7c92048d5335a49d4b73120cf9be7d97a3439712b9c225f00b352e8b306224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13383063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09844a367100e9ad8121039cf994df759dd689a5668a1e06927729d4e1f9c536`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
		Last Modified: Tue, 07 Jan 2025 02:55:27 GMT  
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
	-	`sha256:2e01e3f24fe50dac5be93e40077d1c1aabbf5639909dd5f54bef9a26b96fdff4`  
		Last Modified: Tue, 07 Jan 2025 03:36:50 GMT  
		Size: 10.0 MB (10008864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42ab3f2aa11b9438d9cba7d02cf0055deab9de443b6ee8577151686f744ebc7`  
		Last Modified: Tue, 07 Jan 2025 03:36:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:edfd7ae21bec89c13ff2f4126337bd9e936bb1b28f885ad34f35096075443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9f27d8114374480258c03d00445309447d9c325f8e941d35cd3056a33385db`

```dockerfile
```

-	Layers:
	-	`sha256:82da30655940a0176a9c6e8fd6f73b37dee719e865c5e62a8ec76b0ad86762ae`  
		Last Modified: Tue, 07 Jan 2025 03:36:50 GMT  
		Size: 180.5 KB (180507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de5f504babe980105831de6e68f55f4f395c5516f9f9d4c20614c8a7d2580e7`  
		Last Modified: Tue, 07 Jan 2025 03:36:50 GMT  
		Size: 20.6 KB (20567 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:38fffdd328337d6006a37cbb51f581ffc88d4525c9caa281f811b49c557d4669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14358203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dacb402b96cdcea7f542627d1785887260aafeb75305bfada7b33eb012db53b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f86d5cc1e43fbd2039bd32583f1bad05de4cf043ef1728991312f7e212a7b6`  
		Last Modified: Fri, 13 Dec 2024 20:29:10 GMT  
		Size: 301.8 KB (301789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0200faccea227483173625c65e1dc565554a1d328bce77c17da267c2d0357986`  
		Last Modified: Fri, 13 Dec 2024 20:29:10 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ea7bf47dc4e4df9891d8a1a609c9dc7fa5bed2e09e343468635d676a06b2fc`  
		Last Modified: Fri, 13 Dec 2024 20:30:02 GMT  
		Size: 10.1 MB (10061773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2541c1db40a466008163806e2bf3920bf81447ffdb116cdea0d20656641cf224`  
		Last Modified: Fri, 13 Dec 2024 20:30:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:1286a223c10f5d54b8b20e0acbb1163cc212e057e755a2e48d03a5c482bb4b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 KB (208586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2838d132b25805b88ae67575adafc6587d5bc3627037d3517b8b4d22808b074`

```dockerfile
```

-	Layers:
	-	`sha256:92c97e5f3b837cbbd0534ad1f2a4f5edc29341c4a2313bfcea0ba3ff412ab1a6`  
		Last Modified: Fri, 13 Dec 2024 20:30:01 GMT  
		Size: 188.0 KB (187979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fad5e7813b3859828a2049d0be56d9e99c31d884168ae2fb53aaf0b3c992ee`  
		Last Modified: Fri, 13 Dec 2024 20:30:01 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; 386

```console
$ docker pull haproxy@sha256:0796750994e08eae988b18538fba407d7081dac7f23cf9490276a4473f3dba5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13629177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6d8892f15033da5f294ffb4990aedd8aa9462b179854ab8454af20cd124853`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ee0d8d6aae2a305b97705ac9c2b738c258a5909f43593c3a55d2963a745e96`  
		Last Modified: Tue, 07 Jan 2025 03:15:08 GMT  
		Size: 279.9 KB (279928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00aff244a2fceb986ee7fb3f4b8b19f728d3fdaf1c773a4d510190fff7ceb988`  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebaf033282b08a9276df4bae64ee7d2416e5152d389956c748ac70dc5c19d1`  
		Last Modified: Tue, 07 Jan 2025 03:15:21 GMT  
		Size: 9.9 MB (9889526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cd4984dd1363bb95b7e54f55631fb6bdb0f8194f10da01183dd7ef7dd7a93a`  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:8c0ad78d5c55168467ce0b895ede91261ef1a33f670ca23533a1eac82bf68233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 KB (200821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b2d6486546abea64b7fa33f5750dd3e7f426dbf0d362af69af641efa387a09`

```dockerfile
```

-	Layers:
	-	`sha256:25739a1c50a43e76521bd0c1049957d77a48b2f1e030f2ce929788abfdeb9714`  
		Last Modified: Tue, 07 Jan 2025 03:15:20 GMT  
		Size: 180.4 KB (180420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82fd1f04d7214906584a50d0da0698539dae887736831440b86efd1deffe662c`  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e1717be43f4ed054e13f03519c595b1a0be1d799d59a4bd0e7b1fbb189366918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14490698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9b7bcb4007b1346200bab2abe8c331bee0fc5ff3c11b75d0218797681a70db`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
		Size: 282.1 KB (282115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de7d93a7784969b90b7c7f2812a309fc376363099c98c03c22ae034b1787ce`  
		Last Modified: Tue, 07 Jan 2025 03:39:14 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a5cdedc93cec87ab40b08231e93fdc543179be151aec3b55a7aa21780efba1`  
		Last Modified: Tue, 07 Jan 2025 03:39:57 GMT  
		Size: 10.6 MB (10639390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36aac61be03b956bd3a4a49ef226e04522441ba98c18e5e56154c694ed1a4da`  
		Last Modified: Tue, 07 Jan 2025 03:39:56 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:d3603b6438cb2431c94559f88b430ca07d5e16812a77fb2b112d54be73aed644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 KB (199060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27251a75a9ebf631b5f0e2dbe550ae69d1675a53efe4cc3d3456f3699964ca1`

```dockerfile
```

-	Layers:
	-	`sha256:f3424d1f6e42983ec5637ff80e53a9add18886f02b4a5299a2c15869972f554e`  
		Last Modified: Tue, 07 Jan 2025 03:39:56 GMT  
		Size: 178.6 KB (178550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a28e3a094c8c3336b75d3d3cb6b7e594f5d6df328d9a1a73dca376c448d7e1`  
		Last Modified: Tue, 07 Jan 2025 03:39:56 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; riscv64

```console
$ docker pull haproxy@sha256:010183ad6874c36132f3708f2dbc646a155123cc008a66d0fc05c15878ebcd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13409236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d697c8deb7b8440c37368cad3605bc374539652f6fc8b5690951a40a7d70e4f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31ceeba599115c930bf00886a89fdfdace42c270afdfc6cf5034c408581f24`  
		Last Modified: Fri, 13 Dec 2024 22:24:05 GMT  
		Size: 299.6 KB (299642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcaf500a9bfbc533b8dae448d15e0b3e8e16aeeb12b412a6a51aee6eb18a0d8`  
		Last Modified: Fri, 13 Dec 2024 22:24:04 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91ff5931569146f554a58bba9937541ff94df389edd438f939459fd592bed5`  
		Size: 9.8 MB (9754113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcb728f46d43b83629038f4f434ef77d5025b6b9bcca46294ab83e9ac4097c6`  
		Last Modified: Fri, 13 Dec 2024 22:36:20 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:7ecf94f279e09d06e3a35994caf0fb1fea1101159cb8be8343bef7f5111542be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 KB (206494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b450f086de70a5b58d3c3b9d7498f42c3c70e0e62aba647aacd9271a302126`

```dockerfile
```

-	Layers:
	-	`sha256:c2abaa3ff21370273c56f185f1d3804a3e5761324614dfae7df8d3b78a2598aa`  
		Last Modified: Fri, 13 Dec 2024 22:36:20 GMT  
		Size: 186.0 KB (185987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4261ec4ad931a6dcfa2bbedebcfeabd98ccc402e93b947d431ac1b6694ccd89`  
		Last Modified: Fri, 13 Dec 2024 22:36:19 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.21` - linux; s390x

```console
$ docker pull haproxy@sha256:3734bff18ecc0f208aa4076312a5bc217cd2aa75ce55d082ef4b7115b6d185d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14116578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6412616d9911831a3f3539547f7ca13cdf7ea576cd318140712764dfbc4b17`
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
ENV HAPROXY_VERSION=3.1.1
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.1.tar.gz
# Fri, 13 Dec 2024 00:50:46 GMT
ENV HAPROXY_SHA256=8c1b5d439ba4b278e602445c57e20067adef214dc9c44c2a1cf172fad5f7d273
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
		Size: 280.5 KB (280499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242eaeb61e00e494db261861dbce275783f6e59b478b7a81de903294cfd13f05`  
		Last Modified: Tue, 07 Jan 2025 03:33:12 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b28fce8498978b7f2b59b427f461fb149fb724a70696d9e0f4e69fe87a6bc2`  
		Last Modified: Tue, 07 Jan 2025 03:34:30 GMT  
		Size: 10.4 MB (10375177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36d326e834d29578aa0e235fe8cd87dc137970d9081f060ca1e95a950242c4`  
		Last Modified: Tue, 07 Jan 2025 03:34:31 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.21` - unknown; unknown

```console
$ docker pull haproxy@sha256:3d25953e06e2bb756c600df52dfcce37405ff24966e7da5cafba68e767445953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (198953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22892d6dc00667573802b0bb6c670f5d6bcafb50dd43ae1f8e3a1a5e43a6a881`

```dockerfile
```

-	Layers:
	-	`sha256:1e75cdc175a1d1782bfe365b908c2f5590e3b89f06b297c5023114951b499197`  
		Last Modified: Tue, 07 Jan 2025 03:34:30 GMT  
		Size: 178.5 KB (178504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b355619b4fd30973da78683a6daec22af2cc385b18989ddcc90690c056002348`  
		Last Modified: Tue, 07 Jan 2025 03:34:30 GMT  
		Size: 20.4 KB (20449 bytes)  
		MIME: application/vnd.in-toto+json
