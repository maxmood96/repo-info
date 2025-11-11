## `haproxy:lts-alpine3.22`

```console
$ docker pull haproxy@sha256:8c6b55d891584afded3ab1b91063a703ecc8ff2481302b691773648ffa806226
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
$ docker pull haproxy@sha256:93cf807de7dbcf6318ccc7e6a7b9501a183ce8f8a9325a48fe26930832fea191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15711110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860ce603929fcbba86b21480d0c0087936d92bb86e67b3c97f9597724c28e030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:43:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:43:39 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:46:05 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:46:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:46:05 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:46:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:46:05 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:46:05 GMT
USER haproxy
# Mon, 10 Nov 2025 19:46:05 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:46:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065fd24111a02cce418b566150f1963ea9d079c4803d650c246a4bbff88cc51f`  
		Last Modified: Mon, 10 Nov 2025 19:44:30 GMT  
		Size: 819.7 KB (819671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3ace485c62ad2a5a6e199cb426883e73830a8c59eda28291d9126c7a4271e`  
		Last Modified: Mon, 10 Nov 2025 19:44:30 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7663d62a53c26609f0461a22eef2b5050b853b9f37a5b379c99fff66483f2eb`  
		Last Modified: Mon, 10 Nov 2025 19:46:16 GMT  
		Size: 11.1 MB (11087549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f9c5cd9e9d48c8a818b6498bb1405f6ddb7affcdf3154a1435e4d8754145f7`  
		Last Modified: Mon, 10 Nov 2025 19:46:16 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:2b15daea2145bc8adcc0d141c8d43da687b859fac5084efde1760dd4de383bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 KB (248999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f804f8940e2baffa19df6febee3484c915b3b7d0ad68053a62b42fbd48ec234`

```dockerfile
```

-	Layers:
	-	`sha256:30472895f08ee6bc45416857f9248a6ff4a8d3f41b465f8c57318fcd570f477e`  
		Last Modified: Mon, 10 Nov 2025 22:57:30 GMT  
		Size: 227.9 KB (227943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13b1196a6d00e3606d311c6d09d53467d2bbf5b88957a3c12574e23ed3a1139a`  
		Last Modified: Mon, 10 Nov 2025 22:57:31 GMT  
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
$ docker pull haproxy@sha256:8e7008c0b1cf0dd76427b1f1c27e0ca1e17303900754fade8a099befaae55200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15995711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d54ec7e57e08d7f9805a2b9bef77e5b57e7d9cfec28b5496efe27d9bdb0a662`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:46:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:46:31 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:48:47 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:48:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:48:47 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:48:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:48:47 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:48:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:48:47 GMT
USER haproxy
# Mon, 10 Nov 2025 19:48:47 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:48:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfff24c04f9863befb4d30a65355eef3e0b96ffc4567383dc718fea50ce5c8d`  
		Last Modified: Mon, 10 Nov 2025 19:47:18 GMT  
		Size: 831.9 KB (831894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6798db7261c43142a64b4aa8195a4022e976c9ff468bbc8a12990ac319a137`  
		Last Modified: Mon, 10 Nov 2025 19:47:18 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f34b3ddc034734245d5b56fb1802a24123f3e9ff5b27bbb37d92c64c9b78e19`  
		Last Modified: Mon, 10 Nov 2025 19:48:58 GMT  
		Size: 11.0 MB (11024310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4994ded3670e14d7a060792cd1d4ce656fed81a99b66f18a1e38029fda03dde6`  
		Last Modified: Mon, 10 Nov 2025 19:48:58 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:e68bdef4e00e6c9440480b0dcf86d2099bdfccd78da13d1739f446a8f3fab3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 KB (249285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481ab1d3b966cb58e97e7bd3af67b266dbe96b95fb0529c073acaa758148d74`

```dockerfile
```

-	Layers:
	-	`sha256:3a5ce647acb257ac723d54785e8637ce252be727805f89e5f5a281d528b10797`  
		Last Modified: Mon, 10 Nov 2025 22:57:41 GMT  
		Size: 228.0 KB (228047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e07997e3abccbc80a898a6de9ed2f8eafbc062b0bbf1b540752f680f0d8d486`  
		Last Modified: Mon, 10 Nov 2025 22:57:41 GMT  
		Size: 21.2 KB (21238 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; 386

```console
$ docker pull haproxy@sha256:1126d10fac7ba23bab33a5b48b38406c0c3de94d1b6ddf42cafd191b73733a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15259289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d07bb4a47c5af41e2498daf2b84f78324f5f6cff06910dfc6e7bdaa786d81f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:48:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:48:18 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:48:51 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:48:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:48:51 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:48:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:48:51 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:48:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:48:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:48:51 GMT
USER haproxy
# Mon, 10 Nov 2025 19:48:51 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:48:51 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68585da5141f2041b70a1ecd97d051311adfc58e780e8cbf1e010b0d5e621811`  
		Last Modified: Mon, 10 Nov 2025 19:49:04 GMT  
		Size: 823.0 KB (823033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb15cc3d6c84efbd386629dbc525148318adc443dab193a9a050e5074aff8b1`  
		Last Modified: Mon, 10 Nov 2025 19:49:04 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fce3cc1b1e648475a4a8339ac1c2192d6e485ff28e43246951de00352df3ca`  
		Last Modified: Mon, 10 Nov 2025 19:49:05 GMT  
		Size: 10.8 MB (10815878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470262dc30cde74d1978df7df7f72b9a64be5898787e550069c80dfa0a57a3c`  
		Last Modified: Mon, 10 Nov 2025 19:49:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:3ded44cf16aafddf2bc08c6638adb6c059cd93e8182429afdb1f882b8ea04892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 KB (248897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c949e75a464dfaf85908affffec5c2bf6b8492d2699b92ce942d34f8df14d8eb`

```dockerfile
```

-	Layers:
	-	`sha256:22b44adeb92e4baeb9b0f1288ad1a8392aab45340615b825aba34b0afd65fee9`  
		Last Modified: Mon, 10 Nov 2025 22:57:45 GMT  
		Size: 227.9 KB (227898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfbb173afdc520a7894c83d9092e68aed214d3d854470b8675a2f0b2383bd772`  
		Last Modified: Mon, 10 Nov 2025 22:57:45 GMT  
		Size: 21.0 KB (20999 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; ppc64le

```console
$ docker pull haproxy@sha256:9c7d5bb709c5264f1e3151b3f4d34e178237b2eeb59ad604c4457647916cfa91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16293803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df0b835aae0e29a991ef271ce8befff350e278fee4a20a72ac9c0b6c0b90c4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 19:53:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 19:53:44 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 19:56:58 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 19:56:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 19:56:58 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 19:56:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 19:56:58 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 19:56:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 19:56:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:56:58 GMT
USER haproxy
# Mon, 10 Nov 2025 19:56:58 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 19:56:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eb1591b5b07d594c31f3570b8f93fdf0b949769b57c334d6c6cb52f58188b4`  
		Last Modified: Mon, 10 Nov 2025 19:54:39 GMT  
		Size: 852.2 KB (852230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71523ceb06006e7b49285afb0942c15d6fb51b86d548ccabdcc03741c2c62b`  
		Last Modified: Mon, 10 Nov 2025 19:54:38 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96b6ab07ade951f34faaa2c2b25c4a10dfd5faec94e58e666e18df67e4e7fa`  
		Last Modified: Mon, 10 Nov 2025 19:57:23 GMT  
		Size: 11.7 MB (11707888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39a44ffc463fa002634ec1a81a479b4502bc3bf553fa3f05bff67390a94f28`  
		Last Modified: Mon, 10 Nov 2025 19:57:22 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:459be37b7954176d8e545441aa0c68499b524515ae46ab1c46a793cc6971f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862790ea1b42a82908cf84167e711205773f0a0186bec25e50c62b72159a040a`

```dockerfile
```

-	Layers:
	-	`sha256:cd94d5124d355c17924c0d0be32b910712f33f4f84f5017bab3a34aac94902b2`  
		Last Modified: Mon, 10 Nov 2025 22:57:48 GMT  
		Size: 226.1 KB (226050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3202b3a28b284d77d4dbbea2780d20497b7dff0d572069458eb86f6c154bbc`  
		Last Modified: Mon, 10 Nov 2025 22:57:49 GMT  
		Size: 21.1 KB (21128 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; riscv64

```console
$ docker pull haproxy@sha256:63fab446e7f7bc480eda92829395894632f35e9ca28eb002ab79b2a46a1cd872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15129819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3931a2d84b2fdb82f37365f789ad26a3bdc2d4cf6fdf8f9c1fc5b0cf060eba35`
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
# Mon, 10 Nov 2025 20:53:23 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 20:53:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 20:53:23 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 20:53:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 20:53:23 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 20:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 20:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 20:53:23 GMT
USER haproxy
# Mon, 10 Nov 2025 20:53:23 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 20:53:23 GMT
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
	-	`sha256:fe3066857c274e9a4170d41a5680a7506805677654091033f5fa0247f5ee8739`  
		Last Modified: Mon, 10 Nov 2025 20:54:14 GMT  
		Size: 10.8 MB (10775418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce93b1a306ffca112ac20270ab75b2a58991200c3465f92d90b0dc17bd0ee116`  
		Last Modified: Mon, 10 Nov 2025 20:54:08 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:11ffdf1260683a630cfb8bbfea24f30c6363713f724e28ac3c393e1fcd71a34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac675022436189cbc64db4696f4497ecf8625f7493f544af1bb71b44da0ef31`

```dockerfile
```

-	Layers:
	-	`sha256:ed66d160bb15cc7dff43df6894602b0a57a23a7bc3496206f92de8d9e889335f`  
		Last Modified: Mon, 10 Nov 2025 22:57:52 GMT  
		Size: 226.0 KB (226046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc712d3dfe0e1014a08ec0b3846f6028ac8eaa8c731e0d013dc179d9bd858f18`  
		Last Modified: Mon, 10 Nov 2025 22:57:53 GMT  
		Size: 21.1 KB (21128 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine3.22` - linux; s390x

```console
$ docker pull haproxy@sha256:8bb86a2a94844db197bf077d3b746f5eeab4fb26feaad0af3c72248348e84506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a91a66ff9b30d5fe6e8ff9e664e649ca8507cd771430b15bc6acab213c70835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 10 Nov 2025 20:33:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Mon, 10 Nov 2025 20:33:14 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Nov 2025 20:37:04 GMT
ENV HAPROXY_VERSION=3.2.8
# Mon, 10 Nov 2025 20:37:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.8.tar.gz
# Mon, 10 Nov 2025 20:37:04 GMT
ENV HAPROXY_SHA256=46703fb94720f92cce2b08049a40d9176962037ba676885c55a56bd9d625e7c2
# Mon, 10 Nov 2025 20:37:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Mon, 10 Nov 2025 20:37:04 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Nov 2025 20:37:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 20:37:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 20:37:04 GMT
USER haproxy
# Mon, 10 Nov 2025 20:37:05 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Nov 2025 20:37:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666625c23ec7445ba90e79de6286ae630484af87bcf4b596f01e291f1bedf935`  
		Last Modified: Mon, 10 Nov 2025 20:34:24 GMT  
		Size: 879.2 KB (879217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcd488b162c16e9e61742fb5bcabf57af17b4799e45b6b2482ecc31f40bbcd9`  
		Last Modified: Mon, 10 Nov 2025 20:34:24 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ff334585fbc434a63579067497086f5f06ecc55ff8c6d52a67bcb4e77c7c97`  
		Last Modified: Mon, 10 Nov 2025 20:37:23 GMT  
		Size: 11.5 MB (11452485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f492e5f1b9ab106b12057a1d3f6941e05f20fb01b7494c732bde7606ee616c0`  
		Last Modified: Mon, 10 Nov 2025 20:37:22 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine3.22` - unknown; unknown

```console
$ docker pull haproxy@sha256:35a61339adb059245c5035afd374287eb26e5db83790f6d9068ae63482679acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 KB (247047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a861347c45231bf3765b16c6632a3c12ccf6f69a00149802bef8027cca2d9663`

```dockerfile
```

-	Layers:
	-	`sha256:09e2f3a2026ab837e083855e121816dc8990a5bdc69cfc13a884718f5f62211a`  
		Last Modified: Mon, 10 Nov 2025 22:57:56 GMT  
		Size: 226.0 KB (225992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cfe17d959a74811ede0dfdebddcf00e0405b57c7e7b5cedfc0c035e5beb79f8`  
		Last Modified: Mon, 10 Nov 2025 22:57:57 GMT  
		Size: 21.1 KB (21055 bytes)  
		MIME: application/vnd.in-toto+json
