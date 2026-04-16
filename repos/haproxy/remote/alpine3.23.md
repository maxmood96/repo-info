## `haproxy:alpine3.23`

```console
$ docker pull haproxy@sha256:4f97a2cb7f02fd08402259e74a65ef12fcfa3dff1ef78fddecb5228a17b7f4ad
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
$ docker pull haproxy@sha256:c9d86b3c7dd05bee030cf3caae27294be99a9e542e38a36a855855712f5eb3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19285103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa63c92e8cca19c75abe064644bac1d630f0033764838ff922107aa208980a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:16:46 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:17:27 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:17:27 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:17:27 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:17:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:17:27 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:17:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:27 GMT
USER haproxy
# Wed, 15 Apr 2026 20:17:27 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:17:27 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd8eea19270f3e99f06b82196407e22f2f20d7c2aea85e91c2c72840354ca16`  
		Last Modified: Wed, 15 Apr 2026 20:17:34 GMT  
		Size: 824.7 KB (824706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d78bdec2bec45c2a440394b1c93eb80d9e8df5bf149a3b7844502f9ccf7bc91`  
		Last Modified: Wed, 15 Apr 2026 20:17:33 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf526d94249029ef571ee11135fb5a8d61aa9618fc07dd7e406e174c65dfd65`  
		Last Modified: Wed, 15 Apr 2026 20:17:34 GMT  
		Size: 14.6 MB (14594778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c84bf08760d9f8dd20edf44511fa1ba3ece2a973b5fcd50d52bd8f4149653`  
		Last Modified: Wed, 15 Apr 2026 20:17:33 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:237bbcfd40ad9e7d21ecc3fabbea7ae74a578e7fe55bc99dbabb565417ab8626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 KB (246519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9dbea3582fe2af345202d285277c153eaafe3c6dca3ae85990474be341696`

```dockerfile
```

-	Layers:
	-	`sha256:dddfcf8c341e24d620d5917df24a7d0bae2a9828cc7976ecccbf02a92e394d2d`  
		Last Modified: Wed, 15 Apr 2026 20:17:33 GMT  
		Size: 225.4 KB (225351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7ca2dbe9cbc1d47f820a7460ac6166a53ecc01cdc5dd41dda06832074691a4`  
		Last Modified: Wed, 15 Apr 2026 20:17:33 GMT  
		Size: 21.2 KB (21168 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:0969a2765c3117d332749d2d5c49f96bd53edc752957051c132abdcc72470b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19214293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eacce0ee30e22739baf87c99b348411394a4b28dccd1011699c3c07ddeaf74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:17:06 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:17:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:17:06 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:17:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:17:06 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:17:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:06 GMT
USER haproxy
# Wed, 15 Apr 2026 20:17:06 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:17:06 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21daa6e8a453a33757ff2ae2543315987b72c28c1203f13d034c84f936a57890`  
		Last Modified: Wed, 15 Apr 2026 20:17:12 GMT  
		Size: 817.8 KB (817750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5261a61afb30cdb81d2d5b064752e1f2403bcb25da12332f9da3816b9be492e9`  
		Last Modified: Wed, 15 Apr 2026 20:17:12 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a819a82c3c3c85e7f027fc6543e2842e793ca000e416f8203eae53d1caa055`  
		Last Modified: Wed, 15 Apr 2026 20:17:12 GMT  
		Size: 14.8 MB (14823244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf86579b7f446fc12801ecbad4f3daa61709741d1a168684f3efd6809686743`  
		Last Modified: Wed, 15 Apr 2026 20:17:12 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:d65c79822e25562dd68f8a489abf524570e347ad5d0c079b8e8e52e682d16eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 KB (21075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040c0d42844e9c29c3429aad2ba78bc11b848c6a6720b2367feea011c380bd20`

```dockerfile
```

-	Layers:
	-	`sha256:d70d16d5045e221e18a3264b4a7a2ee15a63ec9044190ddda85a9ae3f2d586da`  
		Last Modified: Wed, 15 Apr 2026 20:17:12 GMT  
		Size: 21.1 KB (21075 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:1eca96f197719f616426d3babec3c4448d5823c5c3eff3203f6457ea0459d9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18722536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a513eb5e2331a080744692a84b82b0c460913bef02f910180b86ff5b250de7fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:16 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:16:16 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:17:03 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:17:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:17:03 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:17:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:17:03 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:17:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:17:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:03 GMT
USER haproxy
# Wed, 15 Apr 2026 20:17:03 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:17:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996edeba6639d46705f31e5fdafe3e9c8a849deceb9a1a45a24e0159359712a1`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 773.5 KB (773526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42987d749a66485e9d487d11f6236ea23975314046e6557ca0f853977ab5f4fa`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db4a17ea81e364ec51b4f0b2c1715aa0a1c3989ef958207497c1c5d77f8f14`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 14.7 MB (14664457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f610db9e83c66b570a9961960a9ef063a9bba54575faa024df998439a637ab`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:b5f1357155c3eb07a2a4b0ded2b38385828f38d8dc9ce423e68a01ce8dcb64af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (246044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83c1655852abb2cdf165a219b32072c10833de8b366d1ac1f9bdccbbdcb7633`

```dockerfile
```

-	Layers:
	-	`sha256:a9cc65b966266776379a5eff8d88e4f17ad90151fb01b075ff9ca49ec3bfa74b`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 224.8 KB (224753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:547429c2e4441ac95a3e8ce68c83f8c09fefe1223867612f9ab11227a5796912`  
		Last Modified: Wed, 15 Apr 2026 20:17:10 GMT  
		Size: 21.3 KB (21291 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2e7666d84715a0c83ee498fbdb08463c9d5274a4bfb56e437a5ddcd39e6f98c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19392038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c44cfe5c50a5199c0918b83af97a47d2fe36641bf342633268d88093c6209f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:15:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:15:22 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:16:05 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:16:05 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:16:05 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:16:05 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:16:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:05 GMT
USER haproxy
# Wed, 15 Apr 2026 20:16:05 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:16:05 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d191f8f918ff612d96b8d336132f320192343d2e33feedd3fd67ae20d658f95`  
		Last Modified: Wed, 15 Apr 2026 20:15:55 GMT  
		Size: 838.3 KB (838293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df345bf41c6e702f15627bc98ca1ce27eabbe100111f0de34be03497b9b795d0`  
		Last Modified: Wed, 15 Apr 2026 20:15:55 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34b0371a193ef9de796fc2ff063fcaf83179d9a45f4af648f8b5573959d1c78`  
		Last Modified: Wed, 15 Apr 2026 20:16:13 GMT  
		Size: 14.4 MB (14352441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b6fd11e1e8749767a5c81247f178b932e11b76874685d05d4939c7fd64002e`  
		Last Modified: Wed, 15 Apr 2026 20:16:12 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:a3ef921aa5ef55a0315edacdb490858339eb73fd187c3188eee8ef764c130b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 KB (246108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5b2c4d67b1ae050d73c3750b699fc89f222dc284911cb9b12b40bf2f3daed5`

```dockerfile
```

-	Layers:
	-	`sha256:3203b27a44b5c302614c7e56b889e0ff63e9d6e035db3b60f0415b5424d37be3`  
		Last Modified: Wed, 15 Apr 2026 20:16:12 GMT  
		Size: 224.8 KB (224781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a777255c0563ea1cb21c1337176d44a11b1fa3d4549bb5ba9f14aaa46a89a3`  
		Last Modified: Wed, 15 Apr 2026 20:16:12 GMT  
		Size: 21.3 KB (21327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; 386

```console
$ docker pull haproxy@sha256:1b7643c9caaa43198b4541ebf0b49150180e72be8587c5bc219cee5916ec8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18903344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500c1a1e5d2eda4a935d748d37be3519e7658a36772fc795f99fb1ed1fe8957`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:19:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 22:19:42 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 22:20:32 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 22:20:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 22:20:32 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 22:20:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 22:20:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 22:20:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:20:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:20:32 GMT
USER haproxy
# Wed, 15 Apr 2026 22:20:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 22:20:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5f7e1eaf68a69a18272aa63e935f689429aca2bb9613ba188ec9868f34699e`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 830.6 KB (830552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35e462513075680de979532e8a412e12ae0c73872e26d2e0c54bc99de0e056`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a838c51c7be4f66c639198ecaf5ecbf0ccbdb2069360adf6f09e7e4c7afc08d3`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 14.4 MB (14380911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226afe5611a3679a71721c7dee53af06fb103ba274940f2d7ddbf50c38aa2ea3`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:92a2ac681ec9a1d879ea2841c35d3a046012521dbdd271a1f2920014b43ba842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 KB (246439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb49a3165be9b9016b27c16ae6ec76ee999a4c8db2e46d65963a97a68b893d61`

```dockerfile
```

-	Layers:
	-	`sha256:10d9a5767e7c34c64bb437bd0c51c7d4a72eeb0f025a8e66fe41ffb7464523d9`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 225.3 KB (225316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce81c9970f6ec813cf88a8e98a69726ed6d88c628887104f1d2062163a1caac`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c43c0ab0daac273d8551dc359c425d15be873b4cef983cf1a2522dbb0baab5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20074044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f111778ba89304c086cbc3c68210eff2043b04b3f4daf7eb6ea9b7dc6ce151f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:12:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:12:14 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:13:37 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:13:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:13:37 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:13:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:13:37 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:13:37 GMT
USER haproxy
# Wed, 15 Apr 2026 20:13:38 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:13:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9792366a55b53496c1c2a0d88f4ec91d679cfd344eddee4e4794be643f587e45`  
		Last Modified: Wed, 15 Apr 2026 20:13:13 GMT  
		Size: 861.8 KB (861788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2feebeb884292ec39d7a9c5ca0da2df075e74ba2c13f2b280b0f002d5f0bfdf`  
		Last Modified: Wed, 15 Apr 2026 20:13:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e0a075181b03b8d40b38436db154d18bfdc54adbd2930f0808c04a558503e`  
		Last Modified: Wed, 15 Apr 2026 20:13:53 GMT  
		Size: 15.4 MB (15379889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e894e702fce9360368aa2d856a63995519227810fb27676ddcf097a350ea87dd`  
		Last Modified: Wed, 15 Apr 2026 20:13:52 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:120f16586b8611544b69a9e6372ddc33d70377fdcfc7f79ed419ff5f56035ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (245975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaba40a4f8e0504fe3358e0e2e4f986bcf4a94f5b0b13fe87dbce9a793c03b97`

```dockerfile
```

-	Layers:
	-	`sha256:f832fdb31f0532fa9a612d2585df6785f5f673ffa308e5afa5b97a83eb957928`  
		Last Modified: Wed, 15 Apr 2026 20:13:52 GMT  
		Size: 224.7 KB (224746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7efd29ddb7500ef41c6af7cade5222f639e5eff38dd413164b00b1eb62ee782`  
		Last Modified: Wed, 15 Apr 2026 20:13:52 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; riscv64

```console
$ docker pull haproxy@sha256:ce4ae3240481ed2989e97ff73e26cccaa145deb31709903e82d3a7f6f194417a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20182398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffc0210cd795bc64a1cc6219d64b97691bac8e532e3c94d259af617dc389af5`
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
# Wed, 15 Apr 2026 22:14:33 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 22:14:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 22:14:33 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 22:14:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 22:14:33 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 22:14:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:14:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:14:34 GMT
USER haproxy
# Wed, 15 Apr 2026 22:14:34 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 22:14:34 GMT
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
	-	`sha256:c6c50a6a201c39ce97c4f40df526a08aa64eaa47e75426f8a44db476e1fedf7b`  
		Last Modified: Wed, 15 Apr 2026 22:15:35 GMT  
		Size: 15.7 MB (15748054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d36020f50522ce95d4ff9eed7b7673f4bbde44e53e4d5beeb583c6b8965de61`  
		Last Modified: Wed, 15 Apr 2026 22:15:32 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:1a42d6d3c8e69eac6994d12b6dbf837b06a31388488c2419d2dadc45be0cac45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 KB (245971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246a9172864395ccf255f109778157ffcb242dbd408f5bb0d03f5c3de6a2700`

```dockerfile
```

-	Layers:
	-	`sha256:011a4d473d5d999da294436dc16337ffeae13a6f207e99a96169bf75173e0049`  
		Last Modified: Wed, 15 Apr 2026 22:15:32 GMT  
		Size: 224.7 KB (224742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532d387daf2793572ca430b24c62d2650dbdbbffb2e32012b7e96c0af9065cec`  
		Last Modified: Wed, 15 Apr 2026 22:15:32 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:alpine3.23` - linux; s390x

```console
$ docker pull haproxy@sha256:0e34e72e767106f89f7c81687819878fb754a72d483ff10566ef63ab2c3e84cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19613349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9816c098e52bc64e7b5026a53a037d33b463093ed5827f497cb18491c31be8ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:10:56 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		socat 	; # buildkit
# Wed, 15 Apr 2026 20:10:56 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 15 Apr 2026 20:12:35 GMT
ENV HAPROXY_VERSION=3.3.6
# Wed, 15 Apr 2026 20:12:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.3/src/haproxy-3.3.6.tar.gz
# Wed, 15 Apr 2026 20:12:35 GMT
ENV HAPROXY_SHA256=e69cb5dc59e4eb1ff72bcebf30d55f0919803c686e428c0c3a5903f2cf7c1fb6
# Wed, 15 Apr 2026 20:12:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Wed, 15 Apr 2026 20:12:35 GMT
STOPSIGNAL SIGUSR1
# Wed, 15 Apr 2026 20:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:12:35 GMT
USER haproxy
# Wed, 15 Apr 2026 20:12:35 GMT
WORKDIR /var/lib/haproxy
# Wed, 15 Apr 2026 20:12:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b742f1e347e2c20a8654ecc443a773f32c61ac5f8722273b695e3db677519168`  
		Last Modified: Wed, 15 Apr 2026 20:12:46 GMT  
		Size: 887.1 KB (887141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009faf31ad3bd6b7bb06b303ef52b5576ef17d5e4e592326b04dad4329ae5d`  
		Last Modified: Wed, 15 Apr 2026 20:12:46 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b08f9972300413d51392689719ed8b0a99c62a9c57ed73e51ce00969e3994f8`  
		Last Modified: Wed, 15 Apr 2026 20:12:48 GMT  
		Size: 15.0 MB (14998242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d974411950473b552cefb9ac78cc26241d8a63eae05c2b280c5356f8a5c590`  
		Last Modified: Wed, 15 Apr 2026 20:12:47 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:alpine3.23` - unknown; unknown

```console
$ docker pull haproxy@sha256:ff4ce5613135c096099eb75a3e0d564e314bf6261a9f2d48b08f158713d31f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 KB (245869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bbed5c5acae0f6acc247bae83b67d18143c629d349bb544092d2560d3f0f74`

```dockerfile
```

-	Layers:
	-	`sha256:f0d67eb54492eeaf34762be14f53ca74a15822e64d98bc2c928405782b81b658`  
		Last Modified: Wed, 15 Apr 2026 20:12:47 GMT  
		Size: 224.7 KB (224700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2150be25a69fff0389061c29c37259f4cae1f79d09a1d06be51c6480f32aa6c6`  
		Last Modified: Wed, 15 Apr 2026 20:12:47 GMT  
		Size: 21.2 KB (21169 bytes)  
		MIME: application/vnd.in-toto+json
