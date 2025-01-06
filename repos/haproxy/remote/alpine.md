## `haproxy:alpine`

```console
$ docker pull haproxy@sha256:2adc8518931611c911633d85881776566c6d5e03658a6f13fa772abdf616ae33
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
$ docker pull haproxy@sha256:afade49bd0140f87bb5096775b284511b1d3dcb2473bb0a349804bf847af6f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14081556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84653769c986a18b33860f65d3d456d7f7cad42b45a74659300b6959a8b6a032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572216df6b00d8e2d08f73dde22b806bbaf22dcfc8907cae5eabd699f0a0c05`  
		Last Modified: Fri, 13 Dec 2024 20:28:52 GMT  
		Size: 299.3 KB (299293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0d6d7786aa7c9342d320d180b23fb82d2f388fd5b100008d7082ea4bdadf1e`  
		Last Modified: Fri, 13 Dec 2024 20:28:52 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894c6c074f82227a64bcff5a335db59e9160b3dbd1fb47576eb8c6ab47af1b8`  
		Last Modified: Fri, 13 Dec 2024 20:28:53 GMT  
		Size: 10.1 MB (10136363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996e3fe68c8273279e26b6533c7bc7fce4a36a418824899fe810a9293510ac67`  
		Last Modified: Fri, 13 Dec 2024 20:28:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:0e7f33710026100ae9a865c5da4252589a41a0c12ebe9df9a9201eb2420ff8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 KB (208349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bf24938af8f6fe5e1f4c138f61509a30ec57843d4b63051de9978dfe77d9bb`

```dockerfile
```

-	Layers:
	-	`sha256:097077e6ba254100103e03339323b2b143752f4281a155ba7b42f4b202d37315`  
		Last Modified: Fri, 13 Dec 2024 20:28:52 GMT  
		Size: 187.9 KB (187899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab79a59c24898b50e69965d9312deabccf52659e3b686db65e3847f7e2f6c25a`  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:a7467d723a39279cf64539b3ce3bbb705c3123453663af079953fdf95295d1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e866238b5044a42d67386a4130aac87fdcc58e0603dd58c87f056304d0e4b1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd44aaa48485b34fdab4f109e9b7512483d23834d34d8a626f20c760ca5edcde`  
		Last Modified: Fri, 13 Dec 2024 20:28:28 GMT  
		Size: 300.4 KB (300385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15781b07f906913c6e8fd8cd015deff5ba2938111db23d71cf048ae9220b649`  
		Last Modified: Fri, 13 Dec 2024 20:28:28 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9328604bd6553d5fb7883a5cae52523293aacb87c8a43b46bc20b1989cff86d9`  
		Last Modified: Fri, 13 Dec 2024 20:29:31 GMT  
		Size: 10.2 MB (10161298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa732bdb88da893a1a99d21c2723aeef6ea4a5da862f5df9762a8e7671c0dfdf`  
		Last Modified: Fri, 13 Dec 2024 20:29:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:310feb512e2402db5d82d6b5c42a5c8283903243e7a078b01a66f90b1bc7bc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9cfa1018c039450d68993a02c6e67c108cb684dd3448a14433c4cff8e4d561`

```dockerfile
```

-	Layers:
	-	`sha256:c8701f5cf9156559d5008306c270a740ae78c7e9ab698827aa3427b972f3a767`  
		Last Modified: Fri, 13 Dec 2024 20:29:30 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0a9f82964e37324378977af99723cb6ee8a93328c754bc077727d17d64ad4e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13409523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2515e161b4b9e5cdd67f89de010921fc3800178da2bcd838e9023240216eda45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845915b26f71f4e1256d6563721ae973b56b00bfc20516b7e2a8d2be5df41318`  
		Last Modified: Fri, 13 Dec 2024 20:28:18 GMT  
		Size: 299.4 KB (299404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f517d87d15c61d5ee6088c94b526de71e4c54dbb8fe7bcdc1443b4120a7378e`  
		Last Modified: Fri, 13 Dec 2024 20:28:18 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0064aaa1920a051f0449609424dc00bba913aa87b63febdda371fb46374cd7`  
		Last Modified: Fri, 13 Dec 2024 20:29:24 GMT  
		Size: 10.0 MB (10008630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad76816b9b7f339beb3a58b985ad10822b299fb5eb19f6131741ce880b421`  
		Last Modified: Fri, 13 Dec 2024 20:29:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:84947c8c1737c953235feefc602057aba528de3a80b1b1b7a166cd1282cca31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 KB (208519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7770962c7125149de97a44c4b6e07f44bce20bcc670c90000635a486b4d47f93`

```dockerfile
```

-	Layers:
	-	`sha256:1f616e826434a87fc524034d8572ee487953d8a7a4ce7713d0ef717e0a32e00d`  
		Last Modified: Fri, 13 Dec 2024 20:29:23 GMT  
		Size: 188.0 KB (187951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5998cb0769441436e2a6bf0fb4f3a3369c6cbcb2f1efeaeae36731f06ae05d50`  
		Last Modified: Fri, 13 Dec 2024 20:29:23 GMT  
		Size: 20.6 KB (20568 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; arm64 variant v8

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

### `haproxy:alpine` - unknown; unknown

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
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; 386

```console
$ docker pull haproxy@sha256:5c77043aa36f4b2feecaaf1c22aba20e418044603c2f4ac2a3dc5b001e3aa5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13656977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1a7c8db4917082b47e1c2428ca4dead2134ca8e50581e71482e9ef8b2e7bb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe157daac5c8df6a2187e73f21e9961d99bbdc8d3d322878080bb6bc01d3e03`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 299.8 KB (299789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea620304e15e75ba914268dc426409dd0d136ec16a5f29627e4cbd29582c187`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8549130a2ae7797c39c805e8a1a0c95757b587b3610c4ad458a1ea3cec97ce`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 9.9 MB (9889658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7dd0f2290effef4f33d7f5a159093c9b8130f3984f2c25df0165ac9618778`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:7dd336a18163ed555ede275b7f475b8f77b0fd3000969942c641cf8c020f3e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 KB (208265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bd2b959284399599812519bc4b87e7ce9cb1aba77691fba23d965f40a6ee80`

```dockerfile
```

-	Layers:
	-	`sha256:110b5c1aab0b1b459ac22dd903e4813e137b4005f522e3aaea6ce9db951f0ca9`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 187.9 KB (187864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b8058bbdd1936245aec9fc8d389f28b60d3038d9232561ab319c452e316e75`  
		Last Modified: Fri, 13 Dec 2024 20:28:42 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:8d1adcfc636e782b4e62a28adcaba047296409b65aabb06320983e6eb9d657d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14519723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a86535f43e5eca8b783c7cef43caa001ff4adc19be491a36c59ceb7f9be5e48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f4820385be42c4f78279631a96c0bd6d8604e4ceee241be2c85a06ecc6d3fa`  
		Last Modified: Fri, 13 Dec 2024 20:27:41 GMT  
		Size: 302.1 KB (302150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96030b2ed32cc56840069565227b3d7c2042ea8ae99d8a4f34ebafa238fd65de`  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292d455165da491976dfa5f422e03cf6e86124a8fab4909c0166226c9ef832e4`  
		Last Modified: Fri, 13 Dec 2024 20:28:24 GMT  
		Size: 10.6 MB (10639012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a163d20fad16ae11e35c5c91622ee28b7ef077ff0468e85fa3f6ff352bdcb9`  
		Last Modified: Fri, 13 Dec 2024 20:28:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:29c8c23854403557433d17bc6288580b495597c2ac7e5e8248371c4e9680c4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 KB (206501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281d595c9cb704531cd4cfb54f7f9ef9986bace52c8804473986e3d83fe8579d`

```dockerfile
```

-	Layers:
	-	`sha256:d971787f3c64e207b1abaa8c2f79f84d77f7bb59448f29d3dd3e01451038ec1f`  
		Last Modified: Fri, 13 Dec 2024 20:28:23 GMT  
		Size: 186.0 KB (185991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49f4a825ab96aa851677c0e5c52d4e60bcdb36db3c71d5d72d32976060203ef`  
		Last Modified: Fri, 13 Dec 2024 20:28:23 GMT  
		Size: 20.5 KB (20510 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine` - linux; riscv64

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
		Last Modified: Fri, 13 Dec 2024 22:36:21 GMT  
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

### `haproxy:alpine` - unknown; unknown

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

### `haproxy:alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:5e1ff3732aabedd4b2873ee917908200d366bf3d14c7b315133c16e63584f216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14146902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab7268500c24787ed3522091a62840ace49cbbcb9c569010c15d42cd4da10da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6bb41d73f39a586e7546bef3089a9f187cce6a791b0ced28e805eb51cd271`  
		Last Modified: Fri, 13 Dec 2024 20:28:54 GMT  
		Size: 300.4 KB (300434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3371042292b97385cd0692d6fa54b079ae46a89c8c47da15e9c8f6c33acf3c7`  
		Last Modified: Fri, 13 Dec 2024 20:28:54 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1755bc6d5ae63d1a3ed81ef3d26f0738fab6948cb1dfd936f60f794496f93a`  
		Last Modified: Fri, 13 Dec 2024 20:30:12 GMT  
		Size: 10.4 MB (10375495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe90027ace0bfd3130dd955254439ea5d14fb64404a568edb2035da295fecf2`  
		Last Modified: Fri, 13 Dec 2024 20:30:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:d30aa71572b8fe6216e52a704baab1d3caa2d348aee8e590bb7bb85386ab36e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 KB (206395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67be914bf9052eca8d1e59c05ca75f3bfd93c0d745d9211f75ee84d0d68089cb`

```dockerfile
```

-	Layers:
	-	`sha256:ff8c83eb059f6f0950b342356abd4b6447d87a4cae9e3c5cd72ef3b8e453930c`  
		Last Modified: Fri, 13 Dec 2024 20:30:12 GMT  
		Size: 185.9 KB (185945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f044111c3f09eb756331b197caec616db0ceb8436c005589688e4ebf29e271ca`  
		Last Modified: Fri, 13 Dec 2024 20:30:12 GMT  
		Size: 20.4 KB (20450 bytes)  
		MIME: application/vnd.in-toto+json
