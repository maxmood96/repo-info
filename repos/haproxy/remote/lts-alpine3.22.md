## `haproxy:lts-alpine3.22`

```console
$ docker pull haproxy@sha256:bf416941ed8c352eeaa9966883c307bb1cbd12e0fc11417d470a6572fe1e7249
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
$ docker pull haproxy@sha256:a9b408a818f5d0d9a6a042ec2957921038399f7a515f8b7bfef2054ef7f4ce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15710077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4db2d244a92b77e077abfb2e6d791588c15f7d97a66db4b0e7ca96eede1f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 22:36:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 05 Nov 2025 22:36:53 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:37:27 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:37:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:37:27 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:37:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:37:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:37:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:37:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:37:27 GMT
USER haproxy
# Wed, 05 Nov 2025 22:37:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:37:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4deac1f35baff35fef9e5b3dcb02622ea3f7bd1658f1df5a1e2d59bc4803374c`  
		Last Modified: Wed, 05 Nov 2025 22:37:45 GMT  
		Size: 819.7 KB (819676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b192edcbb7418540dfbb5ce19e0383e454a2abd833db2651f3ad31eacba0cc`  
		Last Modified: Wed, 05 Nov 2025 22:37:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8945b45139d244a66d60a003ea3856f940f1621e5d20ea25853a0201e61ccb`  
		Last Modified: Wed, 05 Nov 2025 22:37:46 GMT  
		Size: 11.1 MB (11086505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4572df0781aac2d9040440b6679652c32fd149be1f3fec129e5b298a80b22f5d`  
		Last Modified: Wed, 05 Nov 2025 22:37:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:f67826da2b3110890d492ed961431f36b3f520994b01ca6844161bc0759b10fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 KB (248999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f00c0d536f2f594fdfbbf8188ab00456661da45cb6481f5f0e6c2e99c9c4a2`

```dockerfile
```

-	Layers:
	-	`sha256:686940171f1cd7ef629aea07d9d6a55f2060bb8264c3f973e9fc2232eb1bcc7d`  
		Last Modified: Wed, 05 Nov 2025 22:57:22 GMT  
		Size: 227.9 KB (227943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136f89ce65f3060081d9fc83ac2a5a27d3e93e3f47129e5f0c1d42c060466c8e`  
		Last Modified: Wed, 05 Nov 2025 22:57:23 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:2fba314e5f6d18378a28b5450bef1e02cd47908eb338472f29f3166dfc2d3fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af626c7514b944725876d8f8a41ffb054bab8c196e0ed9580b45014c4914aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:42:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:42:36 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:43:11 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:43:11 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:43:11 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:43:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:43:11 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:43:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:43:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:43:11 GMT
USER haproxy
# Mon, 10 Nov 2025 19:43:11 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:43:11 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8099f7d6e592d95165123b83144c6119fe318a36979d96586f7217067a07f8`  
		Last Modified: Mon, 10 Nov 2025 19:43:22 GMT  
		Size: 812.2 KB (812248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cccf7cf986f4ff055651aab54bf339c9ccf72034e8f473f2df6517114bc469`  
		Last Modified: Mon, 10 Nov 2025 19:43:21 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b0d5a9c22134c2ffb6e11877f36004b6247a439cef8296ab29ef7d1056f80`  
		Last Modified: Mon, 10 Nov 2025 19:43:23 GMT  
		Size: 11.2 MB (11176923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e908613659128c9bcc24edfa5b8769303ad6f9ca42ae1930c32216fc9e252032`  
		Last Modified: Mon, 10 Nov 2025 19:43:21 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:6b51b9ecfff1f59f1299416cce872bf3324fddce38e3401c7a68f10924d614ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (20979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123382df5484dfc6f1853b02b704d70c85097c66fb22478199854fb114f76bfa`

```dockerfile
```

-	Layers:
	-	`sha256:b4a018f68186e2c7d6b5e8ad5e8767c05768e6a4f1c267edc3e299591cca9ab7`  
		Last Modified: Mon, 10 Nov 2025 19:56:46 GMT  
		Size: 21.0 KB (20979 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:6569f1c85bc09d6a3d130de22bd7986b4b03e252ccf1d073eb9d7d432cd9db56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14998307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfe000376519c95bec900330aa94a8db0cb1bf07c74ddf4a5d8e8c01db91207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:43:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:43:38 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:44:13 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:44:13 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:44:13 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:44:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:44:13 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:44:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:44:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:44:13 GMT
USER haproxy
# Mon, 10 Nov 2025 19:44:13 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:44:13 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d56909b650f78462aa1c024b961a4ba77ec40291d2ac54f91d30bb1ee65e696`  
		Last Modified: Mon, 10 Nov 2025 19:44:26 GMT  
		Size: 768.4 KB (768363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a09a30036c7b65d5ac093b918e9f711779c68f7c093df08b71f7d23851faf93`  
		Last Modified: Mon, 10 Nov 2025 19:44:27 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca739abf85ce7501a10a8542b743c1f82cc57575011dc45d1ac082537189ca8`  
		Last Modified: Mon, 10 Nov 2025 19:44:28 GMT  
		Size: 11.0 MB (11006950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cbae26fb59cc3dce1cec9a18bf753ba9120efced7f04ecc679e8772b46e19e`  
		Last Modified: Mon, 10 Nov 2025 19:44:26 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:bc9b34d7262ced1b6c81747eb53e8face21bb233654247ff91dab76ccc66ecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 KB (249205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a23008856cf78b45bf13237ea3292343acc71219ece3dbd22c8dcc52f15078`

```dockerfile
```

-	Layers:
	-	`sha256:7a2d8fdef1037040a382f476c0e6303fdb285e7722f851f5849dc9a1bef4c7c8`  
		Last Modified: Mon, 10 Nov 2025 19:56:49 GMT  
		Size: 228.0 KB (228011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62758e29e4820f81cee2f77eaecb06ea4f21ca39a407e14f4606c60540a2a4bc`  
		Last Modified: Mon, 10 Nov 2025 19:56:50 GMT  
		Size: 21.2 KB (21194 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ea35e12454200894ed2a642172d675461d056e842bbdaddac8fe7db7f2e33c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15992103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b80d49664f9d2b075f982f26797cff99e0c3ce5367731d3190e81967f5a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 22:35:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 05 Nov 2025 22:35:15 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:37:06 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:37:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:37:06 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:37:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:37:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:37:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:37:06 GMT
USER haproxy
# Wed, 05 Nov 2025 22:37:06 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:37:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9e721394b161a74a5f0a2c57248c48ca5fe8c3b5bff4b881af63151abb24e`  
		Last Modified: Wed, 05 Nov 2025 22:36:05 GMT  
		Size: 831.9 KB (831905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47f348d92476fb08fbddce2cea45c711340d91b27b69ef9eedf68789d1f53f`  
		Last Modified: Wed, 05 Nov 2025 22:36:05 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d087b654bbba6335b765751d4585d9abc88ba7e0f4c8fd4d292357beffb13d`  
		Last Modified: Wed, 05 Nov 2025 22:37:19 GMT  
		Size: 11.0 MB (11020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2bae29aee7160b2e32e84eb0e22d8cad4a01fd235f7a958687ed00b93d9ae8`  
		Last Modified: Wed, 05 Nov 2025 22:37:18 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:d95ad246fb76a673b406669f7979cbf6c7bd15e051709ab8f01803801f74b125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 KB (249285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef73831852c2087cfcbcdfd5515b497a898197a565843222ff468fc6a654f33`

```dockerfile
```

-	Layers:
	-	`sha256:297f2afa1e544ad0539f6b6190a8ccfbbb6aba68d423eecae092d257139d4322`  
		Last Modified: Wed, 05 Nov 2025 22:57:26 GMT  
		Size: 228.0 KB (228047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b945af34922686eb8be1e5b7d645225c4bcda26e2b87baf9baf10c9ea83ade00`  
		Last Modified: Wed, 05 Nov 2025 22:57:27 GMT  
		Size: 21.2 KB (21238 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; 386

```console
$ docker pull haproxy@sha256:324862481e73b95a7b71dfd2daf017559254ae173e166fc5844105fea2dff087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15258264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7469d93d719468d6dc694df3bc24df307a24ed6c7682867e815a5544b929e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 22:37:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 05 Nov 2025 22:37:07 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:37:46 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:37:46 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:37:46 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:37:46 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:37:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:37:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:37:46 GMT
USER haproxy
# Wed, 05 Nov 2025 22:37:46 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:37:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e268eeb78168c2d7ac5e9c5e49ad25ff0ccb9e4405ab3184b98c254dee4ebe15`  
		Last Modified: Wed, 05 Nov 2025 22:37:57 GMT  
		Size: 823.0 KB (823025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a48b134fee69dc9ff6c19ba4c729882b0e96776f032705efca917698c8e1f21`  
		Last Modified: Wed, 05 Nov 2025 22:37:57 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0193a211c114ce12d9e7bf84a282a963fdaaf8c3d4ded73058f9f2a54b44b74e`  
		Last Modified: Wed, 05 Nov 2025 22:37:59 GMT  
		Size: 10.8 MB (10814871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f3b210e5e621fe67ec2478df24201372a5e802b52dfb00a4e2a32b22a31e80`  
		Last Modified: Wed, 05 Nov 2025 22:37:57 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:17c046601efe1f0a8be8ea32a93ed0ebbb3ad969a9cd8487d8644ac117ddf5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a0631a107f175ad24d5bba233f73af1c05d4105e3fb272760c15e3592e6545`

```dockerfile
```

-	Layers:
	-	`sha256:a964291195817de3dbf65ea6a06fba96471e26fe65d859e2a0b9beb0faebb0b3`  
		Last Modified: Wed, 05 Nov 2025 22:57:32 GMT  
		Size: 227.9 KB (227898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352824066bb61ba4a3a29c40767c1beb97c43378c8b5a0257c347fa49ba4f09b`  
		Last Modified: Wed, 05 Nov 2025 22:57:32 GMT  
		Size: 21.0 KB (21000 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; ppc64le

```console
$ docker pull haproxy@sha256:58c71ca280988f6c979ba18da5677ee0f67942e2a03b160ac3087ff479bebff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16292356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8737552fdec0548f97da33a6888136b865239d10baafd47f010d0a3fa0520ea8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 22:37:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 05 Nov 2025 22:37:22 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:38:01 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:38:01 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:38:01 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:38:01 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:38:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:38:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:38:01 GMT
USER haproxy
# Wed, 05 Nov 2025 22:38:02 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:38:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4cde4ced335fadf216750dbd0ab3b7bd6d887afd36392f4b0094bed3f100c5`  
		Last Modified: Wed, 05 Nov 2025 22:38:26 GMT  
		Size: 852.2 KB (852223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee701ed4f82b115e393c74a5e34010bd7865851419a065f2960358c44935dad`  
		Last Modified: Wed, 05 Nov 2025 22:38:26 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a17579465201dbd861bd9963f0ec75633cdc7402ade95793aaf84e604e261d4`  
		Last Modified: Wed, 05 Nov 2025 22:38:27 GMT  
		Size: 11.7 MB (11706452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c6113162dde98fa286ac320d6e88d766282c84ac21b2c239bcade9f9a59e0b`  
		Last Modified: Wed, 05 Nov 2025 22:38:26 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:0958a63ec3a687ddbf3e9d936144ee74aaad9d236ab345074e9c4dbab85c6586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bfe797917b150f351191230219b3bc8a694302c9b23021432550013727f8ff`

```dockerfile
```

-	Layers:
	-	`sha256:4bae1d7e538d39a51d40a2e11cadbf1d4a957b2f379346f16b336cadf7f1ebd9`  
		Last Modified: Wed, 05 Nov 2025 22:57:36 GMT  
		Size: 226.1 KB (226050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace8a5628842fcdcfa901787a6bf617d1e162230fc4d4de65b1eb2c47cb044d9`  
		Last Modified: Wed, 05 Nov 2025 22:57:37 GMT  
		Size: 21.1 KB (21128 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; riscv64

```console
$ docker pull haproxy@sha256:ce2e06ef3fcac393796a254e891f05576d8db43ba082fe5ef6328c408a35482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15126931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc7a06f4e3f798022eb9b8eb777ee949dc54684bcf184ca451f1b61ae07ec4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 23:02:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Sat, 08 Nov 2025 10:21:54 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Sat, 08 Nov 2025 10:33:44 GMT
ENV HAPROXY_VERSION=3.2.7
# Sat, 08 Nov 2025 10:33:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Sat, 08 Nov 2025 10:33:44 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Sat, 08 Nov 2025 10:33:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Sat, 08 Nov 2025 10:33:44 GMT
STOPSIGNAL SIGUSR1
# Sat, 08 Nov 2025 10:33:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 08 Nov 2025 10:33:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Nov 2025 10:33:44 GMT
USER haproxy
# Sat, 08 Nov 2025 10:33:44 GMT
WORKDIR /var/lib/haproxy
# Sat, 08 Nov 2025 10:33:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54ca2c451d09c1e8b05f4bf0794ee306188d6b5453eb34fec1d2bcfffc0366f`  
		Last Modified: Wed, 05 Nov 2025 23:16:13 GMT  
		Size: 837.7 KB (837712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943c25bcc5f553f96378a0a5eba68a6c4f52259fabd5ab8aac33fbf5a0a7692`  
		Last Modified: Sat, 08 Nov 2025 10:34:32 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaf3940d78bb91cd3347565e1b49677e4f486758a5f2aa78c505240c5ecd41f`  
		Last Modified: Sat, 08 Nov 2025 10:34:37 GMT  
		Size: 10.8 MB (10772532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4733ddd9358c43ad740a8cf5d337bf9c51f57a1446418e0e4a2cbd26cad4525`  
		Last Modified: Sat, 08 Nov 2025 10:34:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:eab05186e6bd2013aa84568ff49b9b17137cca7326e3db233c7cf72b836e7dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ad3820adad5b033c0f199e31f09b295c42edcc8d59a967c8034b0662d0b2c7`

```dockerfile
```

-	Layers:
	-	`sha256:73040696c6eae4e44da83d21de53d247cf7247952f13bd04ec53fd6992ddf047`  
		Last Modified: Sat, 08 Nov 2025 13:56:18 GMT  
		Size: 226.0 KB (226046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884530e24d7b4e21b6e1ee24cba198713dc278c4b20f3eca2de08a837c01b1ba`  
		Last Modified: Sat, 08 Nov 2025 13:56:19 GMT  
		Size: 21.1 KB (21128 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; s390x

```console
$ docker pull haproxy@sha256:4e2a18b29ac48b3ef33a91a16a9618025df46e8e35476ce597028647966e7879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15981568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca328a87116e289a0f3f407aa731abefd015f2625763a15569faf176b0cc1637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 22:35:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 05 Nov 2025 22:35:33 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 05 Nov 2025 22:46:36 GMT
ENV HAPROXY_VERSION=3.2.7
# Wed, 05 Nov 2025 22:46:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.7.tar.gz
# Wed, 05 Nov 2025 22:46:36 GMT
ENV HAPROXY_SHA256=1f0ae9dfb0b319e2d5cb6e4cdf931a0877ad88e0090c46cf16faf008fbf54278
# Wed, 05 Nov 2025 22:46:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 05 Nov 2025 22:46:36 GMT
STOPSIGNAL SIGUSR1
# Wed, 05 Nov 2025 22:46:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 22:46:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 22:46:36 GMT
USER haproxy
# Wed, 05 Nov 2025 22:46:36 GMT
WORKDIR /var/lib/haproxy
# Wed, 05 Nov 2025 22:46:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf2a1cae342a60114c4c0f4af3acf94d5dce269d58e2bd38c3b4a76af39bb39`  
		Last Modified: Wed, 05 Nov 2025 22:37:05 GMT  
		Size: 879.2 KB (879237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ab283bf3ef70abb0663efc1215510d8d4f834793f4a09118aa8765ff68dd6b`  
		Last Modified: Wed, 05 Nov 2025 22:37:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5414e73dec635186cbc0456bba51eb5ddf60b60affe94bda3e3fdaa332e9635b`  
		Last Modified: Wed, 05 Nov 2025 22:46:53 GMT  
		Size: 11.5 MB (11451646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afeed9574a83ac7adf3293969b2cc750f0a485ab4dad10591f842004a9a61fc`  
		Last Modified: Wed, 05 Nov 2025 22:46:52 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:4199b92701b8586e8ab5601caabd388fb452be311e8532ca2d7249e9a1e05273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b01490f316846d8c0e9fbac1196e1a4c2ced6b47f3d7c27747b126d4b5761f9`

```dockerfile
```

-	Layers:
	-	`sha256:efb049acc58a4015d4c7ce3036977bd0736ec58c6991c74a2f093bbabb355658`  
		Last Modified: Wed, 05 Nov 2025 22:57:44 GMT  
		Size: 226.0 KB (225992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b1bd09512cfd6c829e3b676017b14bf92cdd662db99cae92fcd8cadf7c9928`  
		Last Modified: Wed, 05 Nov 2025 22:57:45 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
